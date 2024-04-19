# egameProject

## 목차

- [프로젝트소개](#프로젝트소개)
- [개발내용](#개발내용)
- [주요기능](#주요기능)
- [시연영상](#시연영상)

## 프로젝트소개

### 1. 기획의도
기존 펀딩사이트에서 전문화 시켜 게임만을 위한 펀딩사이트를 만들어보고자 했습니다.

### 2. 개발기간
2024.02.20에 시작하여 2024.03.21에 마무리하였습니다.</br></br>


## 개발내용

### 1. 적용기술
Java Spring Oracle DB  Oracle Cloud
HTML CSS5 Java script Jquery 
ChatGPT 3.5 git gitHUB gitDesktop </br>

### 2. DB설계
![DB](https://i.esdrop.com/d/f/D6JOYU5GMF/PRnvynQtDN.png)</br></br>
총 8개의 테이블로 구성하였습니다.</br></br>

## 주요기능

### 1. 썸머노트 api
![썸머노트](https://i.esdrop.com/d/f/D6JOYU5GMF/8HReurLHGY.png)</br></br>
글쓰기 기능으로 썸머노트 api를 사용하였습니다.</br>
기본적인 글작성기능들과 이미지삽입, 동영상첨부가 가능하게 구현하였습니다.

### 2. 파일처리관련 기능
![파일처리1](https://i.esdrop.com/d/f/D6JOYU5GMF/ipvI9TxOhF.png)</br></br>
server.xml파일에서 docBase 절대경롤르 지정하여 이미지저장경로를 설정했습니다.</br>

![파일처리2](https://i.esdrop.com/d/f/D6JOYU5GMF/xOEfaCv8Ua.png)</br></br>
글 작성도중에는 화면에 이미지를 보여주기 위해 임시폴더에 파일을 저장해놓습니다.</br>

![파일처리3](https://i.esdrop.com/d/f/D6JOYU5GMF/DnhOI5qjMq.png)</br></br>
글 작성완료 시 글작성자의 이메일값이 파일이름에 포함되어 있고 작성한 내용안에 포함되어 있다면 </br>
글 번호폴더 생성 후 글번호폴더에 파일을 복사합니다. 복사가 정상적으로 처리되었으면 임시폴더안 작성자이메일이 포함된 파일을 삭제합니다.</br>

![파일처리4](https://i.esdrop.com/d/f/D6JOYU5GMF/U912ki6x4x.png)</br></br>
글작성,수정도중 페이지를 벗어나게되면 $(window).on('beforeunload',function(){});함수를 사용하여 </br>
더미파일을 삭제하는 방식으로 불필요한 파일이 남지않게 관리를 하였습니다.


### 3. 동영상 삽입
![리뷰기능](https://i.esdrop.com/d/f/D6JOYU5GMF/rmhrfp5ynk.png)</br></br>
상품을 클릭하면 상품상세페이지로 이동합니다.</br>
리뷰는 상품을 구매해야지만 작성할 수 있으며 평점도 필수로 선택해야만 합니다.</br>
한사람당 1개의 리뷰만 작성할 수 있으며 이미 작성한 리뷰가 있다면 찾기 쉽게하기위해 리뷰작성란이 사라지고 내가작성한 리뷰가 보이게끔 구성하였습니다.</br>
내가작성한 리뷰를 클릭하면 수정, 삭제가 가능합니다.

### 4. 할인기능
관리자기능중 하나인 할인관리입니다.</br>
![할인등록](https://i.esdrop.com/d/f/D6JOYU5GMF/L1pnLBqXS8.png)</br></br>
관리자메뉴의 상품관리를 통해 상품상세페이지에 들어가면 할인등록을 할 수 있습니다.</br>
할인등록에는 할인율, 시작날짜, 종료날짜를 입력해야만 합니다. 등록 후 ,실질적인 할인등록은 관리자메뉴> 할인관리 탭에서 가능합니다.</br>

![할인관리](https://i.esdrop.com/d/f/D6JOYU5GMF/djJV346v12.png)</br></br>

할인관리에서는 우측상단의 버튼을통해 할인일괄적용, 일괄해제가 가능합니다.
일괄적용의 경우 현재날짜가 설정된할인의 시작,종료날짜 사이에 있으면서 적용이안된 할인이 있다면 적용시켜줍니다.

![상품할인적용](https://i.esdrop.com/d/f/D6JOYU5GMF/ZeW0rhaI3N.png)</br></br>

상품에 할인이 적용된 모습입니다.</br></br>

<h4>더 많은기능들이 있지만 자세한 설명은 시연영상 시청을 부탁드립니다.</h4>

## 시연영상
https://youtu.be/J-3O4g2vs1s
---
