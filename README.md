# 📣 올라 데이터엔지니어링팀 과제 안내

안녕하세요! 여러분의 관심과 지원에 감사드립니다.🤗

아래 내용을 꼼꼼히 읽고 조건에 맞춰 과제를 완성해주세요.  

<br>

# 🏅 과제 제출 방법

Private Repository를 생성한 뒤 과제를 진행해주세요.  
Repository명은 **allra-crawling-assignment**로 부탁드립니다.

과제가 완성되면 README.md 상단에 **지원자분의 성함**을 적어주세요.  
그리고 **dev@allra.co.kr** 계정을 멤버로 초대하여 과제를 제출해주세요.

1. GitHub 과제 Repository 접속
2. Settings 탭 클릭
3. 좌측 Collaborators and teams 메뉴 클릭
4. add people 클릭하여 'dev@allra.co.kr' 초대

<br>

# ✏️ 과제 개요

책 데이터를 수집하는 크롤러를 개발하여 카테고리별 책 정보를 MongoDB에 저장합니다.

<br>

# 📝 요구 사항

## 1️⃣ 기술적 요구사항

1. Poetry를 이용하여 패키지관리를 해주세요.
2. Scrapy를 이용하여 크롤러를 개발해주세요.
3. Git을 사용해 작업 내용을 관리해주세요.
4. README.md를 작성해주세요.

<br>

## 2️⃣ 데이터 수집 요구사항

1. URL: [Books to Scrape](https://books.toscrape.com/)
2. 카테고리별 책 데이터 수집
3. 수집항목: 제목, 별점, 가격, 재고상태, 이미지, 카테고리
4. 항목별 데이터 타입
    - 가격: `float` 
    - 별점: `int` 
    - 제목: `str`
    - 이미지: `str`
    - 재고상태: `str`
    - 카테고리: `str`
5. 데이터 예시: 
    ```python
    {
        "제목": "Soumission",
        "가격": 50.10,
        "별점": 1,
        "재고상태": "Y",
        "카테고리": "poetry"
    }

    # key는 변경이 가능합니다.
    # 파싱된 데이터를 전처리해서 value를 만들어주세요.
    ```
6. Scrapy pipeline 이용하여 몽고DB에 저장
7. 검증을 위해 수집된 데이터를 데이터프레임으로 만들어 `books_data.xlsx`로 저장 

<br>

## 3️⃣ 프로젝트 디렉토리 구조

```
books_scraper/
├── books_scraper/          # Scrapy 프로젝트 디렉토리
│   ├── spiders/            # Scrapy 크롤러 스파이더 파일
│   │   └── books_spider.py # 크롤러 구현 파일
│   ├── pipelines.py        # Scrapy Pipeline (MongoDB 저장 로직 포함)
│   └── settings.py         # Scrapy 설정
├── data/                   # 수집된 데이터를 저장하는 디렉토리
│   └── books_data.xlsx     # 최종 결과물
├── README.md               # 프로젝트 설명
├── poetry.lock             # Poetry 종속성 잠금 파일
└── pyproject.toml          # Poetry 설정 파일
```
<br>

# 🙏 공지 사항

✔️  스스로 문제를 정의하고 해결하는 과정을 통해 과제를 완성해주세요.  
✔️  문제 해결 과정에서 고민이 있었던 부분은 Issue로 남겨주시면 더욱 좋아요.  