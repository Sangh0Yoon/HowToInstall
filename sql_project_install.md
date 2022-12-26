# 🔑 sql_project 실행을 위한 설치 및 방법
----------------------------
- ### [MySQL 설치](https://dev.mysql.com/downloads/mysql/)
![image](https://user-images.githubusercontent.com/100823955/209512586-7cf69671-b30f-432d-b741-a629154a1546.png)
![image](https://user-images.githubusercontent.com/100823955/209512608-34e65218-38bf-4d02-8103-bd7be3703db7.png)
![image](https://user-images.githubusercontent.com/100823955/209512662-0062ffec-df83-4042-a98b-e52eeaa9d1f7.png)
![image](https://user-images.githubusercontent.com/100823955/209512681-44668c15-009e-4481-9bb9-9334043de0c0.png)
- ### [PyCharm 설치](https://www.jetbrains.com/ko-kr/pycharm/)
![image](https://user-images.githubusercontent.com/100823955/209512770-1e1ac253-430c-4d1b-b5fa-c408d01548ab.png)
![image](https://user-images.githubusercontent.com/100823955/209512798-16849c21-d6a9-480d-b35d-ed9a1dfbc45f.png)
- django, mysqlclient 설치
1. PyCharm의 Working Directory를 만들고, PyCharm에서 만든 작업폴더를 Open한다.
![image](https://user-images.githubusercontent.com/100823955/209513375-323d74aa-45dd-4b72-8409-b943e738aab6.png)
2. PyCharm 하단에 Terminal을 클릭하고, 터미널을 Command Prompt를 선택한다.(본인은 Local로 진행하였을 때 안되서 Command Prompt로 진행하였음.)
3. python3 -m venv .projectEnv 을 입력하여 가상환경폴더를 생성한다.(생성된 폴더 확인)
4. .projectEnv\Scripts\activate.bat 를 입력하여 .projectEnv 가상환경을 활성화 한다.
![image](https://user-images.githubusercontent.com/100823955/209513428-70ad4ce8-f5e1-4b54-84b3-f62c71eb22f4.png)
5. 활성된 가상환경에서 pip install django과 pip install mysqlclient 를 터미널에 입력하여 django 패키지와 mysqlclient를 설치한다.
![image](https://user-images.githubusercontent.com/100823955/209513473-4d87300e-20d6-4b81-a2ff-cb8411abc24f.png)
- 새로운 Django Project 생성
1. django-admin startproject category 를 입력하여 Django Project를 생성한다.
![image](https://user-images.githubusercontent.com/100823955/209513700-d89b9ddc-5689-42a4-b85b-1b4840e83eff.png)
2. category 라는 프로젝트 폴더가 생성되었는지 확인한다.
![image](https://user-images.githubusercontent.com/100823955/209513771-6a22695c-c2e3-4beb-901e-58919e9d070d.png)
3. 이제부터 Category 폴더에서 작업할 것이므로 Root Directory로 설정해준다.
![image](https://user-images.githubusercontent.com/100823955/209513862-ed52aefc-d70b-4a61-9990-8c3f7d319cd3.png)
- 새로운 Django application 생성
1. python manage.py startapp myApp을 입력하여 myApp이라는 앞으로 작업할 공간을 생성해준다.<br>
![image](https://user-images.githubusercontent.com/100823955/209514073-17b129a7-630d-4ef2-8590-5cd42ec2bb75.png)
2. 생성된 작업 공간을 확인한다.
![image](https://user-images.githubusercontent.com/100823955/209514102-734477af-1933-4478-a7a4-e01bb75e8053.png)
- myApp 등록
1. category의 setting.py를 열고, INSTALLED_APPS에 myApp을 추가해준다.
![image](https://user-images.githubusercontent.com/100823955/209514319-7a685d1a-a8a3-4016-bce0-a1df3ea77b73.png)
- 웹사이트 프레임워크 테스트
1. python manage.py makemigrations 입력
2. python manage.py migrate 입력
![image](https://user-images.githubusercontent.com/100823955/209514438-2d57d818-b8b8-4ab5-9011-5cfbb60ddf6a.png)
3. python manage.py runserver 를 입력하여 웹사이트가 잘 루팅되고 켜지는지 확인한다.
![image](https://user-images.githubusercontent.com/100823955/209514579-2b5d5567-7e8c-4730-a404-5cc06bad3375.png)
- MySQL 데이터베이스 생성
1. MySQL Workbench를 실행하여 ⊕을 눌러서 이름을 설정하고 OK를 누른다.
![image](https://user-images.githubusercontent.com/100823955/209514849-66f70529-a254-42cf-a8c1-7667cc4c2e18.png)
2. 생성된 이름의 데이터베이스를 더블클릭한 후 root의 password를 입력한다.
![image](https://user-images.githubusercontent.com/100823955/209514935-391227ba-3b2d-48f8-bdc9-b762b9c96dec.png)
3. 테이블 생성 문장을 작성한 후 번개모양(?) 버튼을 누르면 테이블을 생성할 수 있다.
![image](https://user-images.githubusercontent.com/100823955/209515039-f5e9b626-65ce-4f27-8750-f960889a143f.png)
4. 왼쪽 Navigator의 SCHEMAS의 갱신버튼을 눌러서 데이터베이스를 갱신할 수 있다.
![image](https://user-images.githubusercontent.com/100823955/209515133-f1c4fa3a-5371-4446-b6c5-b019931f87e9.png)
- MySQL과 Django Project 연동
1. category의 settings.py를 오픈하여 DATABASE 부분에 데이터베이스 이름과, 유저 이름, 패스워드를 입력한 후
python manage.py migrate를 하면 나의 Djaango Project와 MySQL을 연동할 수 있다.
![image](https://user-images.githubusercontent.com/100823955/209515392-a6800cdf-f806-42b7-a1e6-7c54d333ce51.png)
- templates 폴더 생성
1. setting.py를 오픈하여 import os를 한 후 TEMPLATES 부분에 'DIRS': [os.path.join(BASE_DIR, 'templates)],
를 작성하여 templates의 base 주소를 설정해준다.
![image](https://user-images.githubusercontent.com/100823955/209515877-d83cfaa9-5827-4375-aea2-1e5a4fc6de43.png)
2. myApp 폴더에 templates 폴더를 생성한다.
3. templates 폴더 안에 myApp 폴더를 생성하고 myApp 폴더에는 앞으로 웹사이트 출력을 담당할 html\
파일을 작성한다.
![image](https://user-images.githubusercontent.com/100823955/209515896-275be4e2-0dc4-4862-8cfd-b3168f362d06.png)
