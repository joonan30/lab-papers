# AnnQ: reference-based quantification of cellular abnormality at single-cell resolution
> AnnQ: 단일세포 해상도에서 세포 비정상성의 레퍼런스 기반 정량화

## 서지 정보
- **저자**: Davin Lee(제1저자, 공동)·Gaeun Byeon(제1저자, 공동), Seojin Chung, Dongmin Shin, Jongseo Park, Ingyeon Koh, **Joon-Yong An(교신저자)**. (Davin Lee와 Gaeun Byeon이 공동 제1저자; 소속: 고려대학교 통합의생명과학과 등, 일부 저자 Hospital for Sick Children/Toronto)
- **저널 / 연도**: Briefings in Bioinformatics, 2026, Vol. 27, Issue 3, article bbag278 (Published 31 May 2026; Received 12 Mar 2026, Revised 27 Apr 2026, Accepted 11 May 2026)
- **PMID / DOI**: PMID 논문에 명시되지 않음 / DOI 10.1093/bib/bbag278
- **논문 유형**: 방법론 / 소프트웨어 도구 (Oxford의 "Problem Solving Protocol" 카테고리, Open Access CC-BY 4.0)

## 한 줄 요약
레퍼런스 기반 세포유형 주석 도구가 만들어 내지만 관행적으로 버려지던 "주석 불확실성(annotation uncertainty)"을 기술적 잡음이 아니라 세포 정체성 불안정성의 생물학적 신호로 재해석하여, 각 세포의 비정상성을 연속적으로 정량화하는 파이썬 프레임워크 AnnQ를 제안한 논문.

## 연구 요약
단일세포 RNA 시퀀싱(scRNA-seq)에서 대규모 아틀라스를 활용해 라벨을 이식하는 레퍼런스 기반 주석 도구(CellTypist, scArches, Azimuth 등)가 표준이 되었다. 이들 도구는 중간 계산 단계에서 각 세포에 대해 후보 세포유형들에 대한 **확률 분포**를 생성하지만, 현행 워크플로는 최상위 라벨만 추출하고 나머지 분포 정보를 버린다. 낮은 confidence, 경합하는 라벨 확률, 높은 엔트로피를 보이는 세포들은 대개 기술적 아티팩트로 간주되어 필터링·제거되지만, 저자들은 섭동(perturbation) 실험에서 이런 세포들이야말로 연구자가 찾으려는 생물학적으로 의미 있는 정체성 이탈(deviation)을 대표할 수 있다고 문제를 제기한다.

이에 저자들은 주석 불확실성을 세포 비정상성의 **정량 지표**로 재활용하는 AnnQ(Annotation Quantification of cellular identity uncertainty)를 제안한다. AnnQ는 확률적 세포유형 할당에서 불확실성 인지 특징(assurance/confidence, confidence gap, admixture ratio, normalized entropy)을 추출하여 다차원 불확실성 공간을 구성하고, 이 공간에서 각 세포가 레퍼런스 집단(정상·야생형·대조군)으로부터 얼마나 벗어났는지를 측정하는 **out-of-reference(OOR) score**를 계산한다. 동시에 임계값 기반 논리로 세포를 G0(단일 정체성/confident), G1(모호/저confidence), G2(같은 계통 내 다중 정체성/전이), G3(서로 다른 계통 간 다중 정체성/비정상)의 이산 그룹으로 분류한다.

저자들은 이 프레임워크를 유전적 섭동 및 약물 저항성 데이터셋에 적용해, OOR score가 기존의 군집화(clustering)나 차등 존재량(differential abundance) 분석으로는 잘 해상되지 않는 비정상·전이 세포 상태를 검출함을 보였다. 대규모 사례로 Mouse Brain Perturbation Atlas(약 194만 세포)에 적용해 섭동 집단이 전반적으로 정체성 불안정 쪽으로 계통적 이동(G1·G3 분획 확장)을 보임을 확인했고, RNA 처리/스플라이싱(Hnrnpu, Eftud2)이나 크로마틴 리모델링(Smarcb1) 섭동이 가장 심한 정체성 불안정을 유발함을 발견했다.

두 편의 심층 사례 연구에서 (1) Fezf2 섭동 모델에서 별개의 군집을 형성하지 않는 비정상 신경세포 상태를 정량화하고, (2) 4기 유방암 환자의 종단(longitudinal) 데이터에서 약물 내성(persister)–전이 전구체(precursor) 상태 전이를 주석 동역학만으로 추적했다. 다섯 개 독립 암 코호트에 대한 교차 아틀라스 검증으로 알려진 불안정성 패턴의 재현성과 다축(multi-axis) 이탈 구조의 신규 발견을 입증했다.

결론적으로 AnnQ는 발현 공간이 아니라 주석 확률 공간에서 세포 정체성 이탈을 측정하는, 기존 접근에 **상보적인(orthogonal)** 관점을 제공한다. 이산 라벨이 포착하지 못하는 전이적·비정상 세포 상태를 단일세포 해상도에서 특성화하며, 파이썬으로 구현되어 소스코드와 문서가 공개되어 있다.

## 사용된 기술 및 방법
- **입력 데이터**: 외부 주석 도구(예: CellTypist)가 생성한 확률 행렬 P (세포 i가 세포유형 j에 속할 확률 P_ij, Σ_j P_ij = 1). 세포 수준 메타데이터(sample, genotype, cluster)를 층화 분석·시각화에 활용.
- **불확실성 인지 특징(uncertainty-aware features)** 4종:
  - Assurance(P1): 최대 예측 확률, P1_i = max_j P_ij
  - Confidence gap(Delta): 상위 두 확률 차, Δ_i = P1_i − P2_i (P2는 두 번째 최대 확률)
  - Admixture ratio: A_i = P2_i / P1_i (두 번째 정체성의 상대 강도)
  - Normalized entropy: H_i = −(1/log K) Σ_j P_ij log P_ij (K = 후보 세포유형 수)
- **세포 상태 분류(임계값 기반)**: 하드 임계값 T_h(confident 할당), 선택적 소프트 임계값 T_s(약하지만 생물학적으로 의미 있는 신호). 임계값을 초과하는 세포유형 "hits" 수와 계층 구조(tissue/cell class) 소속을 평가해 G0~G3 및 소프트 그룹 G2s·G3s로 분류. 적응 모드(adaptive)에서 상위 확률 P1 분포의 IQR 기반으로 임계값 자동 제안.
- **레퍼런스 분포 구성**: 야생형/대조군 세포로 다변량 평균 벡터 μ_c와 공분산 행렬 Σ_c를 클러스터 조건부(cluster-conditional)로 추정. 클러스터별 레퍼런스 세포가 부족하면(n < 50) 전역(global) 레퍼런스로 폴백.
- **OOR score 계산**: 제곱 마할라노비스 거리, OOR_i = (x_i − μ_c)^T Σ_k^{−1} (x_i − μ_c). 불확실성 특징 간 상관을 반영하고 스케일 불변 이탈 척도를 제공. 수치 안정성을 위해 대각 공분산 구조로의 shrinkage 정규화(coefficient λ = 0.1) 적용.
- **군집 수준 요약 통계**: median OOR shift(조건 간 중앙 OOR 차이), tail enrichment(레퍼런스 OOR의 특정 분위수, 예: 90th percentile을 초과하는 비레퍼런스 세포 분획). 레퍼런스(야생형) OOR 분포를 경험적 귀무모델(empirical null)로 취급, 이항 검정 또는 순열 재표집(permutation resampling)으로 유의성 평가, Benjamini–Hochberg FDR로 다중검정 보정.
- **구현/파이프라인**: Python 3.9+, CLI + Python API 모두 제공. CellTypist 등의 확률 행렬을 입력받아 분류 결과·OOR score·요약 통계를 CSV로 출력. YAML 설정 파일. 시각화(QC·결과 해석용 publication-ready plots). MIT 라이선스.
- **검증 실험**: (a) 반(半)시뮬레이션 — Di Bella 2021 E15.5 대뇌피질 레퍼런스를 체계적으로 변형(레퍼런스-계통 dropout, 레퍼런스 커버리지 30~100% 스윕, 14개 세부유형→6개 광역 클래스로 점진적 조대화)해 G1 신호가 레퍼런스 희소성의 아티팩트가 아님을 확인. (b) 5개 독립 대뇌피질 아틀라스를 대체 레퍼런스로 사용한 교차-레퍼런스 재현성. (c) 유전자 수준 log-linear regression으로 OOR score를 발현량에 회귀시켜 분자적 driver 식별. Fisher's exact test로 OOR tail 유의성 검정.
- **적용 데이터셋**: Mouse Brain Perturbation Atlas(약 1,944,500 세포; 31개 섭동, 25개 timepoint, 22개 뇌 영역, 28개 데이터셋; CellTypist Developing Mouse Brain / Whole Mouse Brain 모델), Fezf2 섭동 scRNA-seq, 4기 유방암 환자 종단 scRNA-seq(Pre/Post1/Post2/Meta), Lambrechts 4개 암 코호트(lung, colorectal, ovarian, breast), PanCAF 범암종 섬유아세포 아틀라스.

## 주요 유전자 / 단백질
- **Fezf2**: 피질 상하행(subcerebral) 투사 신경세포(SCPN) 정체성을 결정하는 전사인자; 소실 시 corticothalamic 유사 비정상 신경 상태 유발(사례 연구 1의 핵심).
- **Hnrnpu**: 전역 RNA 처리·스플라이싱에 필수적인 핵 리보뉴클레오단백질; 섭동 시 가장 높은 G1 분획(72.4%) — 최대 정체성 불안정.
- **Eftud2**: 스플라이세오솜 구성요소; 높은 불확실성 섭동(G1 60.6%).
- **Smarcb1 / Smarca4**: SWI/SNF 크로마틴 리모델링 복합체 구성요소(Smarcb1 G1 55.7%; Smarca4는 낮은 G1이나 높은 G2, 계통 내 다중 정체성).
- **Ctnnb1(β-catenin)**: 중심 Wnt 경로 이펙터; 헤테로 결손 시 낮은 G1(7.6%)·높은 G2 — 밀접하게 연관된 하위유형 간 다중 정체성 유지.
- **Hesx1**: 전사인자; 높은 G1 분획(72.4%).
- **Satb2 / Slit2 / Sema3a**: 축삭 유도·신경 정체성 관련 유전자; Fezf2 CThPN 집단에서 상승한 OOR의 유의한 분자적 driver.
- **SNAI2(Slug)**: 상피–중간엽 전이(EMT) driver; 유방암 G1 세포에서 상향조절.
- **PDCD1, CXCL13, GZMB**: T세포 소진(exhaustion) 마커; HighExh 코호트에서 양의 log2 fold change.
- **HLA-A/B/C/D, CCL5, CXCR4**: 항원제시·면역상호작용 유전자; 병변 연관 축(E19 클러스터)에서 상향조절.
- **PRSS1, CPA1, CLPS, AMY2A**: 외분비(exocrine)-유사 프로그램; 종양에서 더 강한 이동.

## 주요 발견
- **핵심 착상**: 레퍼런스 기반 주석의 전체 확률 분포(엔트로피·형태·다변량 구조)를 최상위 라벨 대신 정체성 불안정성과 세포 이탈의 연속적 정량 지표로 사용 — 기존에 이를 직접 활용한 프레임워크는 없었다.
- **두 가지 상보적 산출물**: (i) G0/G1/G2/G3 4그룹 이산 분류(각각 confident 단일 정체성, 모호/저confidence, 계통 내 다중 정체성, 계통 간 다중 정체성) + 소프트 그룹 G2s/G3s, (ii) 마할라노비스 거리 기반 연속 OOR score.
- **Mouse Brain Perturbation Atlas(약 194만 세포)**: 전체 54.9% G0, 28.1% G1, 13.2% G2/G2s, 3.8% G3/G3s. 섭동 집단은 정상 대조군 대비 G1·G3/G3s 분획 확장 등 정체성 불안정 쪽으로 체계적 이동.
- RNA 처리(Hnrnpu, Eftud2)·크로마틴 리모델링(Smarcb1) 섭동이 가장 심한 세포 정체성 불안정을 유발. Ctnnb1(Het)·Smarca4는 계통 내 다중 정체성(G2) 유지(Smarca4 G2 81.5%로 아틀라스 최고).
- **발생 시기 취약성**: 초기 출생 후(P0–P7) 세포에서 극단적 주석 불확실성 — G1 분획 P0 62.8%, P1 76.1%, P4 90.4%(성숙 P28 9.4%와 대조). 발생 가소성의 생물학적 신호로 해석.
- **반시뮬레이션 검증**: 레퍼런스에서 세포유형을 제거하면 잘 정의된 정체성 세포도 G1으로 포착(CThPN 99.9%, Interneurons 99.6%, SCPN 94.9%). 레퍼런스 커버리지 30~100% 전 구간에서 ΔG1(Hom−Het)이 +12.2~+18.2 pp로 일관되게 상승 → 레퍼런스 희소성 아티팩트 배제. 5개 대체 피질 아틀라스에서 ΔG1 +1.8~+12.8 pp로 재현.
- **사례 1(Fezf2)**: 표준 군집화·차등 존재량 분석으로는 별개 집단이 없어 검출 불가였으나, AnnQ는 모호(G1) 집단의 약 2.1배 확장(Hom 41.8% vs Het 20.4%) 검출. 세포유형별 G1 증가 SCPN +55.8 pp, CThPN +39.3 pp, DL CPN +20.0 pp, Migrating neurons +16.6 pp. Hom CThPN 세포의 높은 OOR tail 유의(Fisher's exact, OOR>1: Het 11.1% vs Hom 46.9%, OR=7.05, P=1.14×10⁻¹⁰¹). Satb2·Slit2·Sema3a가 OOR driver.
- **사례 2(유방암)**: 레퍼런스에 "악성" 라벨이 없어 암세포가 "Luminal" 계통으로 강제 분류(forced classification)되며 OOR 과소추정 문제 발생. AnnQ 불확실성 지표로 숨은 이질성 발굴 — 치료 전 G1의 63.2%가 약한 DTP 시그니처 발현, 치료 후 G1 분획 78.5% 확장(EMT 상승·DTP 프로그램 하향 → 증식성 MPC로 전이). 전이(Meta)에서 CSC 마커 재활성·EMT 감소(MET). "전이 역설": OOR 최고치인데 G0 분획도 증가 — 전이세포가 중간적 luminal-basal 특징의 "LumSec-basal" 레퍼런스 상태로 수렴하기 때문.
- **교차 아틀라스(5개 데이터셋)**: HighExh vs LowExh median OOR shift CRC 1.17, Breast 1.09, Ovarian 0.45, Lung 0.39. PanCAF에서 전역 G1 분획 Normal 0.7237 → Adjacent 0.7594 → Tumor 0.7814로 증가. 이동 크기는 클러스터 간 비단조(non-monotonic) — 이산 라벨이 놓치는 병렬 field-effect·종양 코어 리모델링 축 발견.

## 연구의 응용
- 섭동/질환 진행 맥락의 scRNA-seq 분석에서 이산 라벨이 놓치는 전이적·비정상 세포 상태의 검출·정량.
- 유전적 섭동(예: CRISPR, knockout) 스크린에서 별개 군집을 형성하지 않는 협응적(coordinated) 정체성 불안정의 등급화된(graded) 검출.
- 암 종단 연구에서 약물 내성 persister → 전이 전구체 상태 전이를 주석 동역학만으로 추적.
- 다중 코호트/다중 아틀라스에 걸친 알려진 불안정성 패턴의 재현성 검증 및 신규 다축 이탈 구조의 체계적 발견 도구(discovery tool).
- QC 필터로 버려지던 저confidence 세포에서 생물학적 신호 회수 — 발현 거리·조성 존재량 분석과 통합해 섭동 유발 세포 변화를 더 완전하게 파악.

## 확장 가능성 / 향후 방향
- 사용자 편집 가능한 계층 JSON(커스텀 라벨 관계 정의·레퍼런스 추가)과 입력 확률 행렬 CSV(알려진 주석 열 병합)의 두 개입 지점으로 연구별 맥락 반영 가능.
- 확장된 다중모달(multimodal) 레퍼런스와 생성 모델(generative modeling) 접근으로 정상 불확실성의 경계를 더 정교화 가능.
- OOR의 절대 크기가 레퍼런스 조성·계통별 분산 구조에 영향을 받으므로, cluster-normalized OOR shift나 within-lineage delta score 같은 상대적 이탈 지표를 상보 지표로 활용해 더 맥락 인지적 해석.
- 잘 큐레이션된 레퍼런스 아틀라스에 적용할 때 가장 신뢰도가 높음 — 레퍼런스 품질 개선이 성능을 좌우.

## 질환에서의 의미
- **암 생물학**: 약물 내성 persister(DTP), 전이 전구체(MPC), 암줄기세포(CSC)·EMT/MET 전이 상태 등 정형 라벨을 유지하지 않는 병리적 세포 상태를 정량화. 레퍼런스에 악성 라벨이 없어 정상 유사 카테고리로 강제 분류되는 문제를 불확실성 지표로 보완. T세포 소진, 종양-인접부 field effect, 항원제시 활성화 축을 여러 암종에서 검출.
- **신경발생/신경질환**: Fezf2 소실에 따른 SCPN 정체성 붕괴 등 전사인자 소실이 만드는 비정상 신경 정체성 상태를 별개 군집 없이도 포착. 대장암의 줄기세포–분화 연속체, 유방암의 전이 이질성 등 질환 진행의 특징인 연속적·중간 세포 상태 해석에 활용.

## 기존 연구와의 차이 / 신규성
- 기존 주석 신뢰도/불확실성 지표는 거의 전적으로 **저confidence 세포를 필터링하거나 미할당 집단을 검출하는 품질관리(QC) 필터**로만 사용됨. AnnQ는 이를 뒤집어 불확실성을 **생물학적 정량 신호**로 재해석하는 최초의 체계적 프레임워크.
- 기존 섭동 정량 프레임워크는 (i) 분류기 기반 세포유형 분리성(예: Augur), (ii) 이웃 수준 조성 이동(예: Milo), (iii) CRISPR 시그니처의 혼합 모델링, (iv) 엔트로피 기반 잠재력(예: SCENT) 등 발현 공간에서 작동. AnnQ는 **발현 공간이 아니라 주석 확률 공간에서 이탈을 측정**하는 직교(orthogonal) 정보 축을 도입 — 기존 방법과 통합해 상보적으로 사용 가능.
- 집단 수준이 아닌 **단일세포 수준**에서, 별개 군집을 형성하지 않는 협응적 정체성 불안정을 검출. 마할라노비스 거리 기반 공분산 인지 OOR score로 불확실성 특징 간 상관을 반영하고 스케일 불변 이탈을 제공.

## 데이터 / 코드 가용성
- **코드**: GitHub 저장소 https://github.com/joonan-lab/AnnQ.git 에 공개, MIT 라이선스. 튜토리얼·예제 데이터셋 포함.
- **데이터**: 검증에 사용한 Mouse Brain Perturbation Atlas 데이터셋은 Zenodo(DOI 10.5281/zenodo.17112344)에서 이용 가능. 그림 재현에 필요한 모든 처리 데이터·분석 스크립트는 GitHub 저장소에 있음. 사례 연구에 사용한 그 밖의 모든 데이터셋은 원 출판물·저장소에서 공개적으로 이용 가능.

## 핵심 키워드
single-cell RNA sequencing, cell type annotation, annotation uncertainty, out-of-reference (OOR) score, Mahalanobis distance, reference-based analysis, perturbation analysis, cellular identity instability, CellTypist, drug-tolerant persister / metastatic precursor
