### 산업보안학과 20220331 윤채원 


### 1. 문제점 : php 로딩 오류

#### 1) php-웹사이트 로딩 오류

![image](https://github.com/ychxnn/information_security/assets/112887768/bf7d1d02-f54c-440f-9d7f-ecd2bc00ef47)

localhost:(port number) / (php파일 이름)을 실행해보았는데, httpd.conf 파일에서 포트 이름을 바꿔봐도 잘 해결이 되지 않습니다. 

#### 2) php 설치 후, xampp로 mysql과 apache24를 시작하려 했으나 이 과정에서 실행 불가 오류를 해결하지 못했습니다. 

![image](https://github.com/ychxnn/information_security/assets/112887768/042d7775-e2aa-41e0-8964-57b4b7839ded)

> 이를 해결하기 위해 apache는 3306->3307로 변경하고, mysql의 포트 번호는 80 -> 8088등으로 변경하여 진행했습니다. 

> apache24폴더와 mysql 폴더 외에도 xampp 폴더 내 apache24의 httpd.conf 텍스트 파일과 mysql의 my.ini 텍스트 파일에서도 변경하여 진행했으나, 사진과 같은 오류가 며칠간 계속되었습니다. 

이를 위해 사용한 실행 방법입니다.

> apache24의 경우 작업 관리자를 켜서 직접 stop한 후 진행했으며, Apache Monitor를 삭제했다가 다시 깔아서 진행해보기도 했습니다. 하지만 해당 오류가 계속되어 이를 해결하기 어려웠습니다. 

> mysql의 경우, 작업 관리자에 들어가서 stop한 후 진행했으며 cmd 창을 관리자 권한으로 열어서 삭제했다 재설치한 후 텍스트 파일을 변경하는 등의 작업을 거쳤습니다. 하지만 마찬가지로 이 경우에도 사진과 같은 내용의 오류가 떴습니다. 

=> 해결을 위해 찾아본 레퍼런스들입니다.

https://glennbouchard.com/ko/101-cara-mengatasi-apache-xampp-yang-tidak-bisa-start.html

https://velog.io/@so_sa/XMAPP-Control-Panel-Apache-%ED%8F%AC%ED%8A%B8-%EC%98%A4%EB%A5%98-%ED%95%B4%EA%B2%B0

https://patiencelee.tistory.com/1108

https://old-moon.tistory.com/102

https://sweepty.medium.com/xampp%EC%97%90%EC%84%9C-apache%EA%B0%80-start%EB%90%98%EC%A7%80-%EC%95%8A%EB%8A%94-%EB%AC%B8%EC%A0%9C-1e836f756a4f

https://youtu.be/I6fQrT25ek0

https://youtu.be/oXOHIdMDvzs

https://youtu.be/tcoIVp1eNgM

https://youtu.be/EPNWxjriRuI

### <해결방안>
3주간의 간격을 두고, mysql, php, 데이터베이스에 대한 추가 공부를 하며 php를 실행해보려 했으나 어떠한 방법을 써봐도 제 컴퓨터로는 php 파일을 실행하기 어렵다는 결론을 얻었습니다. 
실제로 제가 작성한 코드들을 동기들의 컴퓨터로 실행해보았을 때에는 웹사이트가 로딩되는 것을 확인할 수 있었습니다.  

.php 파일이 로딩되지 않아, 과제 진행에 있어서 그 이상의 진척이 어려웠습니다. 
이 문제점은 제가 예상하지 못한 변수였으며, 과제 제출일 하루 전까지도 해결이 어려울 것이라고 생각하지 못했습니다. 
이러한 상황 속에서 작성한 코드들이기 때문에 완성도가 떨어질 수 있을 것이라 예상하여, 교수님께 미리 양해를 구하고 싶습니다. 완성도는 떨어질 수 있어도, 강의 내용과 구글, 강의자료를 최대한 활용하여 구성한 사이트입니다!!

따라서 

1. 처음에 구상했던 사이트의 구성
2. 메인 사이트 html 코드
  (db에 추가 / 수정 / 삭제가 이루어지는 상황을 확인 가능한 각 기능 코드)

제 문제만 해결된다면 바로 사용해 사이트를 만들 수 있도록 하는 코드들을 첨부하겠습니다.  

### 2. 사이트의 구성

##### 제가 구상한 사이트는 학사 관리 사이트입니다.

해당 사이트에서는 회원가입 또는 로그인을 통해 본인 인증 시, 

1. 본인이 입력한 일정에 따른 그날의 일정 확인 가능
2. 본인이 입력한 일주일 시간표에 따른 그날의 시간표 확인 가능 
3. 본인이 수강한 과목에 따라 학점 계산 기능 제공 
4. 원하는 날짜의 일기 작성 가능 

의 기능을 제공합니다. 

### 3. 사이트 html 코드

1) 로그인/회원가입 페이지

[loginphpfile_2.zip](https://github.com/ychxnn/information_security/files/11692470/loginphpfile_2.zip)

=> 해당 파일에는 assignment를 위한 회원가입 과정, 회원가입, 로그인 과정, 로그인, 로그아웃 과정을 담은 php 파일이 있습니다.

=> php 파일의 실행 여부는 확인해보지 못했으나, 강의 시간에 들은 내용과 생활코딩을 통해 독학한 내용을 바탕으로 작성해보았습니다. 

2) 메인 페이지

[main.zip](https://github.com/ychxnn/information_security/files/11693047/main.zip)

![image](https://github.com/ychxnn/information_security/assets/112887768/d27fae74-95ce-4398-81e5-209cd62349f1)
=> html 형식은 파일 자체 업로드가 불가능하여 이미지로 대체합니다!

3) 일정 확인 페이지

=> zip 파일에서 확인 가능

4) 시간표 확인 페이지

=> zip 파일에서 확인 가능

5) 학점 입력 & 확인 페이지

=> zip 파일에서 확인 가능 

6) 일기 작성 페이지

=> zip 파일에서 확인 가능 
