# Lessons from national biobank projects utilizing whole-genome sequencing for population-scale genomics
> 전장유전체 시퀀싱(WGS)을 활용한 국가 바이오뱅크 프로젝트가 인구집단 규모 유전체학에 주는 교훈

## 서지 정보
- **저자**: Hyeji Lee¹·², Wooheon Kim³, Nahyeon Kwon¹·², Chanhee Kim¹·², Sungmin Kim¹·⁴, **Joon-Yong An(안준용)¹·²·³ (교신저자, joonan30@korea.ac.kr)**
  - 제1저자: Hyeji Lee, Wooheon Kim, Nahyeon Kwon 3인 공동 제1저자(equal contribution)
  - 소속: 고려대학교 통합바이오·생명과학과, L-HOPE 프로그램, 보건과학대학 바이오시스템·생의학과 / 국립보건연구원 정밀의료 유전체과학과(Sungmin Kim)
- **저널 / 연도**: Genomics & Informatics (2025) 23:8 — Open Access, BMC/Springer Nature
- **PMID / DOI**: PMID 40050991 / https://doi.org/10.1186/s44342-025-00040-9
  - 접수 2024-12-15, 게재승인 2025-01-27, 온라인 출판 2025-03-06
- **논문 유형**: 리뷰(Review) — 국가 유전체 자원(national genome resource) 종설

## 한 줄 요약
전 세계 주요 국가 바이오뱅크(UK Biobank, All of Us, PRECISE, Biobank Japan, 한국 국가 바이오빅데이터 NPBBD-Korea)의 WGS 기반 접근법·기술 인프라·과학적 발견을 종합 비교하고, 한국인·동아시아 인구집단 특이적 유전변이와 희귀질환 연구에 대한 NPBBD-Korea의 최신 기여를 조망한 종설이다.

## 연구 요약
대규모 국가 유전체 프로젝트는 유전체 연구의 판도를 바꾸며, 시퀀싱 비용 하락과 인구 수준 유전정보의 가치에 대한 인식 확대에 힘입어 수십만~수백만 명 규모의 전장유전체 시퀀싱(WGS) 데이터를 생산하고 있다. 이러한 프로젝트의 차별적 강점은 고해상도 WGS 데이터를 풍부한 표현형·환경·임상 정보와 통합한다는 데 있으며, 특정 질환에 국한된 전통적 유전연구와 달리 인간 유전변이의 전체 스펙트럼(희귀변이, 구조변이, 조절요소 포함)을 체계적으로 탐구할 수 있게 한다. 그러나 기존 유전체 자원은 유럽계 인구에 편중되어 있어 발견의 일반화 가능성을 제한하고 건강 격차를 심화시킬 위험이 있으며, 다양한 지리적 배경의 국가 프로젝트가 이 불균형을 해소하려 하고 있다.

이 리뷰는 (1) 세계 주요 국가 바이오뱅크의 방법론과 특성 개관, (2) 시퀀싱·데이터 분석·저장을 가능케 한 기술적 진보, (3) 이들 자원이 창출한 주요 과학적 발견, (4) NPBBD-Korea의 최신 성과, (5) 정밀의료와 글로벌 보건 형평성을 위한 향후 방향의 순서로 구성된다. 개관 대상은 미국 All of Us(24.5만 WGS, 목표 100만), 영국 UK Biobank(약 50만, WGS 49만여), 싱가포르 PRECISE(SG10K→SG100K→50만), 일본 Biobank Japan(WGS 1.4만, SNP 27만), 그리고 한국 NPBBD-Korea(9년간 100만 명, WGS 55만 목표) 등이다.

기술 파트에서는 변이 검출(GATK, DRAGEN, Sentieon, DeepVariant), 다중 샘플 VCF 생성(joint calling vs aggregation, N+1 문제), 데이터 표현·저장(CRAM, sparse VCF, Hail VDS), 클라우드/HPC 컴퓨팅 환경, Hail·Glow 등 다운스트림 분석, 계층적(tiered) 데이터 접근·보안 체계를 프로젝트별로 비교한다(Table 1). 발견 파트에서는 eQTL 로커스 발견, 희귀변이 발견과 질병 위험층화(risk stratification), 그리고 NPBBD-Korea의 최신 발견을 다룬다.

결론적으로 저자들은 WGS 기반 국가 유전체 프로젝트가 코딩·비코딩 영역, 구조변이, 초희귀 인구특이 대립유전자를 포괄적으로 포착함으로써 질병의 예방·진단·치료를 근본적으로 진전시키고 있음을 강조한다. 특히 유럽 편중을 극복하는 다인종 포용성은 폴리제닉 위험점수(PRS)의 정확도를 높이고 인구특이 질병변이를 규명하는 과학적·윤리적 당위이며, NPBBD-Korea가 한국인·동아시아 인구의 유전적 다양성과 희귀질환 이해를 진전시켜 글로벌 유전체학과 정밀의료·보건 형평성에 기여할 것으로 전망한다. 다만 방대한 규모에 따른 계산·물류·윤리적 과제(데이터 공유, 프라이버시, 동의, 다양성 확보)는 지속적으로 해결해야 한다고 짚는다.

## 사용된 기술 및 방법
- **연구 유형**: 문헌 리뷰(종설). 새로 생성·분석한 데이터셋 없음(Data availability: "No datasets were generated or analysed").
- **시퀀싱**: short-read WGS 중심(대부분 30× 커버리지, 암 조직은 60×), long-read 시퀀싱 언급(복합변이·후성유전 수식·NOTCH2NLC 같은 반복 확장 분석).
- **변이 검출(variant calling) 도구**:
  - GATK(BWA-MEM 정렬 + GATK 변이 검출) — UK Biobank, NPBBD-Korea, PRECISE, BBJ의 표준
  - DRAGEN(FPGA 하드웨어 가속) — All of Us, UK Biobank의 초대규모 처리
  - Sentieon(GATK 호환 고속화), DeepVariant(딥러닝 기반 변이 정밀도 향상) — All of Us
- **다중 샘플 VCF 생성**: joint calling(GATK GenotypeGVCFs, Graphtyper 그래프 기반) vs aggregation(DRAGEN Iterative gVCF Genotyper/IGG, All of Us의 Genomic Variant Store/GVS, GLnexus). aggregation은 재분석 없이 새 샘플 병합이 가능해 N+1 문제 해결.
- **데이터 표현·저장 포맷**: BAM→CRAM(참조 대비 압축, 약 50% 저장공간 절감), dense VCF→sparse VCF(Hail Variant Dataset/VDS[All of Us], DRAGEN IGG multi-sample VCF[UK Biobank], Savvy, Sparse Project VCF).
- **컴퓨팅 환경**: 클라우드 기반 — UK Biobank RAP(DNAnexus+AWS), All of Us Workbench(Google Cloud Platform), PRECISE RAPTOR; 로컬 HPC 기반 — NPBBD-Korea(KISTI 국가슈퍼컴퓨팅센터), BBJ. 컨테이너(Docker, Singularity)·워크플로우(Nextflow, WDL)·Terra 플랫폼.
- **다운스트림 분석**: Hail·Glow(Apache Spark 기반 분산처리), region-based association testing 및 유전체 사전 서브셋팅(pre-subsetting)으로 대규모 연관분석 가속.
- **데이터 관리 시스템**: UK Biobank "category-field" 구조, All of Us DRC(Raw Data Repository/RDR + Curated Data Repository/CDR), NPBBD-Korea GIMS(Genomic Information Management System, 한국생명공학연구원 개발).
- **데이터 접근·보안**: 계층형(tiered) 접근 체계(UK Biobank 3단계 유료, NPBBD-Korea 4단계 무료, BBJ 3단계, All of Us "data passport", SG10K_Health RAPTOR), 재식별(reidentification) 위험 대응(익명화·암호화·다중인증·접근통제·실시간 모니터링).
- **통계·분석 응용**: GWAS·메타분석, eQTL·TWAS 매핑, 폴리제닉 위험점수(PRS), 머신러닝(DeepGAMI 등 유전형-표현형 예측 모델), CNV·구조변이·짧은반복(STR) 확장 분석, trio 기반 de novo 변이 분석, 프로테오믹스·프로테오지노믹스 통합.

## 주요 유전자 / 단백질
(종설로서 여러 인용 연구에서 언급된 대표 유전자·단백질)
- **APOE** — 알츠하이머병 병인 관련 핵심 eQTL/위험 로커스(뇌척수액 바이오마커 통합 연구)
- **TMEM106B** — 알츠하이머병 관련 로커스
- **PCSK9** — 지질 대사·심혈관 위험 관련(대사체 eQTL 연구)
- **CELSR2** — 지질 대사·심혈관질환 발생 관련
- **LRRK2** — 염증성 장질환(IBD)·파킨슨병(PD) 공통 경로의 고영향 희귀변이
- **IL10RA** — IBD·PD 동반이환 관련 희귀변이
- **PANK1** — 동아시아 대장암 조직 조절변이 관련(크로마틴 상호작용 분석)
- **MYH7** — 심근병증(cardiomyopathy) 변이 분류·병원성 평가(한국인 대상 in silico)
- **FBN1** — 마르판증후군의 심부 인트론 변이(WGS로 규명)
- **NOTCH2NLC** — 신경세포 핵내 봉입체 질환 관련 GGC 반복 확장(한국인, long-read)
- **RP1** — 유전성 망막질환의 Alu 삽입 변이
- **GRIN2D** — 알츠하이머병 뇌척수액 다변량 GWAS에서 시냅스 기능 관련으로 시사

## 주요 발견
- **국가 바이오뱅크 규모 비교(Fig 1)**: 목표 코호트 기준 All of Us 100만*, NPBBD-Korea 100만*, UK Biobank 50만, BBJ 27만, PRECISE-SG100K 10만* 등. 가용 WGS 기준(Fig 1b): All of Us 24.5만(다인종), UK Biobank 50만(유럽계), PRECISE-SG100K 5만(중국·말레이·인도계), NPBBD-Korea 2.5만(인구기반+질환), Biobank Japan 1.4만(일본계).
- **UK Biobank**: 약 50만 명(40–69세), 이 중 유럽계 452,264명(93.5%), WGS 490,640명, SNP 11억+ 개·삽입결실 약 11억 개. 여성 54%·남성 46%.
- **All of Us**: 2024년 2월 기준 WGS 245,388명 공개(목표 100만). WGS 참여자의 77%가 생의학연구에서 과소대표 집단(아프리카계 22%, 히스패닉/라티노 18%, 아시아계 2%, 유럽계 51.1%). EHR 28.7만+, 1/4은 최대 10년 종단 EHR.
- **PRECISE(싱가포르)**: 3단계(2017–2027). Phase 1 SG10K_Health 9,770명(중국 58.4%·인도 21.8%·말레이 19.5%), Phase 2 PRECISE-SG100K 10만+, Phase 3 목표 50만.
- **Biobank Japan**: 1기 약 20만 명(2003–2008), 2기 7만 명(2012–2017). WGS 1.4만, SNP 어레이 27만(2개 코호트). 대사체 4,000명(추가 6만 계획), 프로테옴 3,000명(+3,000 진행).
- **NPBBD-Korea(국가 바이오빅데이터)**: 2024–2032년 9년간 100만 명 대상 국가 R&D. Phase 1(2024–2028) 772,000명 모집(희귀질환 47,000, 중증/암 140,000, 일반 585,000), 이 중 240,000명 30× WGS. 암 환자 60× WGS 41,000샘플(13개 암종), 5개 암종 3,000샘플 멀티오믹스. Phase 2(2029–2032) 추가. 전체적으로 100만 명 임상·공공데이터 + 550,000명 WGS 확보 목표, 데이터는 2026년부터 제공. **파일럿에서 25,000명 시퀀싱 완료**(희귀질환 약 15,000, 기타 질환 약 3,000, 건강인 약 7,000).
- **기술 트렌드**: GATK가 신뢰성으로 표준을 유지하나 초대규모에서는 계산집약성 한계 → DRAGEN(FPGA), Sentieon, DeepVariant로 속도·정확도 개선. CRAM은 BAM 대비 약 50% 저장 절감. NPBBD-Korea·BBJ는 로컬 HPC, UKB·All of Us·PRECISE는 클라우드 채택.
- **eQTL 발견**: Gamazon 등 44개 조직 eQTL 통합; UK Biobank로 정신질환 eQTL 점수(Barbu)와 기분 불안정성 GWAS 46개 로커스(Ward); 골관절염 치료표적(Tachmazidou); 석회성 대동맥판막협착 TWAS; FinnGen+UK Biobank 대장암 위험 관련 13개 단백질·인과변이; DeepGAMI로 조현병·AD 유전형-표현형 관계 규명; 아프리카계 SIREN 뇌졸중 코호트; 카타르 바이오뱅크의 멘델질환 eQTL; 호주 원주민 Tiwi 공동체의 만성신장질환 인구특이 변이.
- **희귀변이·위험층화**: FinnGen에서 핀란드 집단 농축 유해 대립유전자(Kurki); 일본 심부 WGS 희귀변이(Nagasaki); UK Biobank 단백질코딩 로커스(Sun); 혈액·소변 바이오마커 35종 유전학; National Bio-Big Data+UK Biobank+Estonian Biobank 통합으로 **질병연관 CNV 73개**(간질·고혈압·만성신장질환 등); IBD·PD 동반이환의 LRRK2·IL10RA; 아프리카계 크론병 대립유전자 빈도 차이; 베타지중해빈혈·선천성 제XI인자결핍·면역혈소판감소증 희귀변이; 약 50만 UK Biobank WES로 교육수준·반응시간 영향 단백질절단·손상 미스센스 변이 규명.
- **NPBBD-Korea 최신 발견(4.3)**: KoGES 76개 표현형 GWAS로 **122개 신규 연관** 발견; KoGES+BBJ 32개 표현형 메타분석으로 **379개 추가 신규 연관** 및 PRS 예측력 향상; **한국인 참조유전체(Korean Reference Genome, 1,490명)**로 희귀·한국인특이 변이 임퓨테이션 정확도 대폭 개선(기존 패널 대비 우수); ASD에서 크로마틴 상호작용 교란 de novo 변이·짧은반복 확장 규명; 신경발달장애 아동 trio 기반 WGS로 **진단수율 33%** 달성; 샤르코-마리-투스병·유전성 망막질환·마르판증후군·RP1 Alu 삽입 진단; 혈액형 유전형·수혈 표현형 예측; MYH7 심근병증 변이 평가; **동아시아 최대 ASD WGS 데이터로 여성에서 de novo 단백질절단변이 부담이 더 높음(성차)** 규명; NOTCH2NLC GGC 반복 확장·long-read 응용.

## 연구의 응용
- 인구특이 참조유전체·임퓨테이션 패널 구축을 통한 정밀의료·질병 위험예측 향상(특히 한국인·동아시아 인구).
- WGS 기반 희귀질환·신경발달장애(ASD 등) 진단수율 개선 및 미진단 질환 해결(구조·인트론·비코딩 변이 포착).
- 폴리제닉 위험점수(PRS)의 다인종 정확도 개선 → 관상동맥질환·제2형 당뇨·COVID-19 중증도 등 복합질환 예측.
- 약물유전체(pharmacogenomics)·치료표적 발굴(프로테오지노믹스 통합, phospho-kinase 표적 등).
- 국가 바이오뱅크 데이터 인프라(변이검출·저장·클라우드·계층접근) 설계에 대한 실무적 비교 참조.

## 확장 가능성 / 향후 방향
- **long-read 시퀀싱** 확대로 복합·구조·후성유전 변이 및 반복 확장 해상도 향상.
- **멀티오믹스 통합**(전사체·단백체·대사체·후성유전체)과 **프로테오지노믹스**로 pQTL·단백체 바이오마커 발굴.
- **AI/머신러닝** 고도화를 통한 유전형-표현형 상관·질병 예후 예측·신규 치료표적 규명.
- **실시간 유전체학(real-time genomics)**과 EHR 통합으로 임상 의사결정 직접 지원.
- **다양성·포용성 확대**: 유럽 편중 극복, 과소대표 집단 모집으로 글로벌 정밀의료 형평성 실현.
- NPBBD-Korea 데이터(2026년 개방)와 글로벌 유전체 DB 연계를 통한 국제 협력 및 한국인특이 신약 개발 가속.
- 지속과제: 계산·물류·윤리 인프라, 데이터 공유·프라이버시·동의 거버넌스, 표준화된 방법론.

## 질환에서의 의미
알츠하이머병·조현병 등 뇌질환(APOE, TMEM106B, GRIN2D), 심혈관·지질질환(PCSK9, CELSR2), 염증성 장질환·파킨슨병 동반이환(LRRK2, IL10RA), 대장암(PANK1)·유방암 등 암, 심근병증(MYH7), 마르판증후군(FBN1), 유전성 망막질환(RP1), 신경세포 핵내 봉입체 질환(NOTCH2NLC), 자폐스펙트럼장애(ASD)·신경발달장애, 만성신장질환, 간질·고혈압, 혈액질환(지중해빈혈·제XI인자결핍·면역혈소판감소증) 등 광범위한 희귀·복합질환에서 유전적 구조와 인구특이 위험변이를 규명하는 의미를 가진다. 특히 ASD의 성차(여성 de novo 단백질절단변이 부담 증가)와 동아시아 인구 특이 변이 발견이 강조된다.

## 기존 연구와의 차이 / 신규성
- 개별 바이오뱅크가 아니라 **UK Biobank·All of Us·PRECISE·BBJ·NPBBD-Korea를 방법론·기술 인프라·발견 측면에서 횡단 비교**한 통합 종설이라는 점.
- 변이검출→다중샘플 VCF→저장포맷→컴퓨팅→다운스트림→관리·접근·보안에 이르는 **파이프라인 전주기를 프로젝트별 표(Table 1)로 정리**.
- **한국 NPBBD-Korea의 최신 성과**(122+379개 신규 연관, 1,490명 한국인 참조유전체, ASD 성차, 33% 진단수율 등)를 동아시아·한국인 인구집단 관점에서 별도 섹션으로 심층 조명.
- 유럽 편중 극복과 글로벌 보건 형평성이라는 관점에서 다인종·인구특이 자원의 과학적·윤리적 당위를 강조.

## 데이터 / 코드 가용성
- 본 연구는 신규 데이터셋을 생성·분석하지 않음("No datasets were generated or analysed during the current study").
- 인용된 각 바이오뱅크의 접근 포털: NPBBD-Korea(한국 바이오데이터스테이션, https://www.kobic.re.kr/kobic/res/ngp), UK Biobank(https://biobank.ndph.ox.ac.uk), All of Us Research Program, PRECISE(SG10K_Health), BioBank Japan(https://biobankjp.org). 각 자원은 계층형 접근(무료/유료, IRB·심의 승인 필요)으로 제공.

## 핵심 키워드
Whole-genome sequencing(WGS), National biobank(국가 바이오뱅크), NPBBD-Korea(국가 바이오빅데이터), Precision medicine(정밀의료), Multi-omics integration, Population genetics, eQTL, Rare variant, Korean Reference Genome, Tiered data access
