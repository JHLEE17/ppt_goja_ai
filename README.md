---
typora-root-url: ../human
---

# **딥러닝** 기반의 PPT 자동제작 서비스: **발펴고자**

## SW마에스트로 11기 연수생  **발표합니까 휴먼?** 팀 - **이종호**(팀장)**, 남지훈, 이제인**



### 프로젝트 요약

* 사용자가 입력한 텍스트와 이미지에 적합하게 AI가 완성된 PPT를 생성한 후 제공하는 서비스

* Flask 기반 웹사이트에서 사용자가 텍스트와 이미지를 입력하면, 딥러닝 기술 (자연어처리와 컴퓨터비전)을 통해 내용을 분석하여 맥락과 어울리도록 PPT 자료를 구성, 사용자가 완성된 파일을 다운로드 받을 수 있도록 한다.

### 기획 의도

* 고품질 PPT의 빠른 작성을 위해 **단순 반복 작업을 대신 해줄 인공지능 기술**이 필요함.

* 텍스트와 이미지 입력만으로 완성된 PPT를 생성하는 서비스 기획
  * 딥러닝과 python 라이브러리를 통해 맥락을 이해하고 단순, 반복 작업을 컴퓨터가 수행하도록 함.
  * 자연어처리, 영상처리, 이미지 크롤링 등의 기술을 접목한 품질 높은 PPT 문서 생성

- 기존 PPT 관련 서비스들은 PPT 템플릿, 이미지, 다이어그램 등의 디자인적 요소들을 제공하여 사용자를 보조해주는 기능으로 그쳤으나, 본 서비스는 **보조를 넘어 편집의 자동화를 목적으로** 하여, 사용자가 만들고자 하는 자료를 입력만 하면 **딥러닝 기**술을 통해 이 내용을 분석하여 맥락과 어울리도록 **완성된 PPT 자료를 제공**함.
- 결정적으로, 기존 서비스는 각 슬라이드에서 사용자가 선택하는 한계로 결국 문서를 사용자가 직접 작성해야 하나, 본 서비스는 **사용자의 에디터 입력만으로 완성된 PPT 문서를 생성**하여 제공하므로 PPT의 작성과 제공에 있어 차별이 뚜렷하게 존재함.

### 사용자 시나리오

1. 사용자가 웹에서 PPT로 만들고자 하는 **콘텐츠 입력**한다.
   - 제시된 규칙에 따라 마크다운 형식으로 텍스트를 입력한다.
   - 편리한 GUI의 에디터를 제공하여 누구나 쉽게 입력할 수 있게 한다.
   - 사용자가 필요하다면 선택적으로 이미지를 입력한다.

2. 사용자가 변환하기 버튼을 누르면 서버에서 **PPT를 생성**한다.
   1. 콘텐츠의 내용에 대해 **딥러닝** 분석을 거친다.
   2. **주제와 어울리는** 테마를 적용하고, 섹션 별로 **내용에 맞는** 레이아웃을 결정하여 슬라이드를 구성한다.
   3. 필요하다면 각 섹션의 **키워드를 추출**하여 사진이나 아이콘을 추가한다.

3. 사용자가 선호하는 **PPT를 다운로드**한다.
   1.  제공된 다양한 결과물들 중 사용자는 원하는 슬라이드를 선택한다.
   2. 선택한 슬라이드들을 병합하여 완성된 PPT 파일을 다운로드 받을 수 있는 버튼을 제공한다.

### 시스템 구성도 및 적용 기술

<img src="/sysArchImage.png" style="zoom:67%;" />

* **Web Front**:  HTML, CSS, JavaScript, Bootstrap
* **Server**:  python Flask, AWS, HTTP, ajax
* **NLP**:  keyword extraction, named entity recognizing, text classification / KoBERT, CRF
* **CV**:  background removal, super resolution, image to pictogram / MaskRCNN, PointRend, Iconify
* **PPT**:  python-pptx



## 주요기능 및 수행 방법

### 1. 마크다운 에디팅 기능

* (설명글 + 그림)

### 2. 이미지 후처리 기능

* (설명글 + 그림)

### 3. PPT 파일 생성 기능

<img src="/image/3_기능설명.png" style="zoom:67%;" />
* 추출한 텍스트와 후처리된 이미지를
python-pptx 라이브러리를 이용하여 삽입


### 4. 키워드 및 주제 추출 기능

* (설명글 + 그림)

### 5. PPT 미리보기 및 파일 다운로드 기능

* (설명글 + 그림)



## 현재까지의 개발 성과 및 코드 설명

### 1. 웹사이트에서의 마크다운 에디팅

* (설명글 + 캡쳐사진 + 코드설명)

### 2. 컴퓨터비전을 통한 이미지 후처리

* (설명글 + 캡쳐사진 + 코드설명)

### 3. PPT 파일 생성

<img src="/image/객체구조도.PNG" style="zoom:67%;" />
* Python 코드로 파워포인트를 생성하기 위한 기능들의 모듈화.

* PPT 파일, 슬라이드, 텍스트 프레임, 단락 등이 객체화.

* 크기나 모양 등을 조절할 수 있기 때문에 간단히 파워포인트를 구성할 수 있음.
<img src="/image/3_코드2.png" style="zoom:67%;" />

### 4. 자연어처리를 통한 주제 추출

* (설명글 + 캡쳐사진 + 코드설명)

### 5. PPT 파일 다운로드

* (설명글 + 캡쳐사진 + 코드설명)



## 앞으로의 개발 계획 및 목표

### 1. 마크다운 에디팅 기능

* (남은거에대한설명 + 그걸위해서지금해놓은게뭔지)

### 2. 이미지 후처리 기능

* (남은거에대한설명 + 그걸위해서지금해놓은게뭔지)

### 3. PPT 파일 생성 기능
* PPT 생성을 위한 대부분의 기능들
→ 자체 API의 형태로 이미 모듈화 완료

* 앞으로 추가 이슈는 API 응용으로 충분
→ 추후 개발속도 증진

* 서비스 품질을 위한 이슈
1. 폰트 종류 추가
2. 개행 규칙 개선
3. 템플릿 다양화
<img src="/image/3_계획.png" style="zoom:67%;" />
### 4. 키워드 및 주제 추출 기능

* (남은거에대한설명 + 그걸위해서지금해놓은게뭔지)

### 5. PPT 미리보기 및 파일 다운로드 기능

* (남은거에대한설명 + 그걸위해서지금해놓은게뭔지)



### * 후속 활용 방안

* 지원 파일 포맷 확장
  * 문서 파일 포맷(.docx, .hwp 등) 생성 기능을 추가하여 보고서 자동 생성 서비스 추가 제공
  * 스프레드시트 파일 포맷(.xlsx, .cell 등) 추가 지원
* 사용자 입력 다양화
  * 보고서, 논문 등의 다양한 정형화된 데이터를 추가 지원하여 서비스의 적용범위를 확장
  * 회의록, 대본 등의 비정형화 텍스트를 후처리 후 데이터로 활용하여 범용성 및 사용자 편의성을 증대
  * 실시간 화상회의 녹화본을 비롯한 비정형화 음성 파일을 입력데이터로 지원

→ 포스트 코로나 시대의 비대면 화상 모임 수요 증가에 맞춰 화상 모임의 대화 내용을 다양하게 가공하여 문서로 제공하는 통합 서비스 제공