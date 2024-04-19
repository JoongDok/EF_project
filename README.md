# egameProject

## 목차

- [프로젝트소개](#프로젝트소개)
- [개발내용](#개발내용)
- [주요기능](#주요기능)

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

<b>VIEW</b></br>
![파일처리4](https://i.esdrop.com/d/f/D6JOYU5GMF/k3Y5RUtXe9.png)</br>

<b>CONTROLLER</b></br>
![파일처리5](https://i.esdrop.com/d/f/D6JOYU5GMF/zWyo0D9vB3.png)</br>
글작성,수정도중 페이지를 벗어나게되면 $(window).on('beforeunload',function(){});함수를 사용하여 </br>
더미파일을 삭제하는 방식으로 불필요한 파일이 남지않게 관리를 하였습니다.


### 3. 동영상 삽입
![동영상삽입](https://i.esdrop.com/d/f/D6JOYU5GMF/2ck8bdT9U1.png)</br></br>
정규식을 활용하여 youtube링크의 id값을 추출한 뒤 youtube에서 지원하는 iframe용 링크형식으로 변환 후 썸머노트 내용에 추가해주는식으로 구현하였습니다.</br>

### 4. AOP활용 로그인 체크
AOP(Aspect)기능을 사용하여 특정 메서드가 실행되기 전에 로그인체크기능을 실행하게끔 구현하였습니다.</br>
![AOP1](https://i.esdrop.com/d/f/D6JOYU5GMF/aB7BwxdJFO.png)</br></br>
@Pointcut어노테이션으로 로그인체크기능을 걸어놓을 메서드를 지정합니다.</br>
지정된 메서드 실행전 @Before어노테이션 메서드가 실행되고 로그인처리기능을 실행합니다.</br>
로그인이 안되어있을 시 고의로 예외를 발생시켜 controller로 예외를 던져줍니다.</br>

![AOP2](https://i.esdrop.com/d/f/D6JOYU5GMF/oEBRYr3arC.png)</br></br>
던져인 예외를 @ExceptionHandler 어노테이션을 활용해 로그인페이지로 이동하게끔 구현해놓았습니다.

