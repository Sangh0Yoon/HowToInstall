# ๐ sql_project ์คํ์ ์ํ ์ค์น ๋ฐ ๋ฐฉ๋ฒ
----------------------------
- ### [MySQL ์ค์น](https://dev.mysql.com/downloads/mysql/)
![image](https://user-images.githubusercontent.com/100823955/209512586-7cf69671-b30f-432d-b741-a629154a1546.png)
![image](https://user-images.githubusercontent.com/100823955/209512608-34e65218-38bf-4d02-8103-bd7be3703db7.png)
![image](https://user-images.githubusercontent.com/100823955/209512662-0062ffec-df83-4042-a98b-e52eeaa9d1f7.png)
![image](https://user-images.githubusercontent.com/100823955/209512681-44668c15-009e-4481-9bb9-9334043de0c0.png)
- ### [PyCharm ์ค์น](https://www.jetbrains.com/ko-kr/pycharm/)
![image](https://user-images.githubusercontent.com/100823955/209512770-1e1ac253-430c-4d1b-b5fa-c408d01548ab.png)
![image](https://user-images.githubusercontent.com/100823955/209512798-16849c21-d6a9-480d-b35d-ed9a1dfbc45f.png)
- django, mysqlclient ์ค์น
1. PyCharm์ Working Directory๋ฅผ ๋ง๋ค๊ณ , PyCharm์์ ๋ง๋  ์์ํด๋๋ฅผ Openํ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209513375-323d74aa-45dd-4b72-8409-b943e738aab6.png)
2. PyCharm ํ๋จ์ Terminal์ ํด๋ฆญํ๊ณ , ํฐ๋ฏธ๋์ Command Prompt๋ฅผ ์ ํํ๋ค.(๋ณธ์ธ์ Local๋ก ์งํํ์์ ๋ ์๋์ Command Prompt๋ก ์งํํ์์.)
3. python3 -m venv .projectEnv ์ ์๋ ฅํ์ฌ ๊ฐ์ํ๊ฒฝํด๋๋ฅผ ์์ฑํ๋ค.(์์ฑ๋ ํด๋ ํ์ธ)
4. .projectEnv\Scripts\activate.bat ๋ฅผ ์๋ ฅํ์ฌ .projectEnv ๊ฐ์ํ๊ฒฝ์ ํ์ฑํ ํ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209513428-70ad4ce8-f5e1-4b54-84b3-f62c71eb22f4.png)
5. ํ์ฑ๋ ๊ฐ์ํ๊ฒฝ์์ pip install django๊ณผ pip install mysqlclient ๋ฅผ ํฐ๋ฏธ๋์ ์๋ ฅํ์ฌ django ํจํค์ง์ mysqlclient๋ฅผ ์ค์นํ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209513473-4d87300e-20d6-4b81-a2ff-cb8411abc24f.png)
- ์๋ก์ด Django Project ์์ฑ
1. django-admin startproject category ๋ฅผ ์๋ ฅํ์ฌ Django Project๋ฅผ ์์ฑํ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209513700-d89b9ddc-5689-42a4-b85b-1b4840e83eff.png)
2. category ๋ผ๋ ํ๋ก์ ํธ ํด๋๊ฐ ์์ฑ๋์๋์ง ํ์ธํ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209513771-6a22695c-c2e3-4beb-901e-58919e9d070d.png)
3. ์ด์ ๋ถํฐ Category ํด๋์์ ์์ํ  ๊ฒ์ด๋ฏ๋ก Root Directory๋ก ์ค์ ํด์ค๋ค.
![image](https://user-images.githubusercontent.com/100823955/209513862-ed52aefc-d70b-4a61-9990-8c3f7d319cd3.png)
- ์๋ก์ด Django application ์์ฑ
1. python manage.py startapp myApp์ ์๋ ฅํ์ฌ myApp์ด๋ผ๋ ์์ผ๋ก ์์ํ  ๊ณต๊ฐ์ ์์ฑํด์ค๋ค.<br>
![image](https://user-images.githubusercontent.com/100823955/209514073-17b129a7-630d-4ef2-8590-5cd42ec2bb75.png)
2. ์์ฑ๋ ์์ ๊ณต๊ฐ์ ํ์ธํ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209514102-734477af-1933-4478-a7a4-e01bb75e8053.png)
- myApp ๋ฑ๋ก
1. category์ setting.py๋ฅผ ์ด๊ณ , INSTALLED_APPS์ myApp์ ์ถ๊ฐํด์ค๋ค.
![image](https://user-images.githubusercontent.com/100823955/209514319-7a685d1a-a8a3-4016-bce0-a1df3ea77b73.png)
- ์น์ฌ์ดํธ ํ๋ ์์ํฌ ํ์คํธ
1. python manage.py makemigrations ์๋ ฅ
2. python manage.py migrate ์๋ ฅ
![image](https://user-images.githubusercontent.com/100823955/209514438-2d57d818-b8b8-4ab5-9011-5cfbb60ddf6a.png)
3. python manage.py runserver ๋ฅผ ์๋ ฅํ์ฌ ์น์ฌ์ดํธ๊ฐ ์ ๋ฃจํ๋๊ณ  ์ผ์ง๋์ง ํ์ธํ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209514579-2b5d5567-7e8c-4730-a404-5cc06bad3375.png)
- MySQL ๋ฐ์ดํฐ๋ฒ ์ด์ค ์์ฑ
1. MySQL Workbench๋ฅผ ์คํํ์ฌ โ์ ๋๋ฌ์ ์ด๋ฆ์ ์ค์ ํ๊ณ  OK๋ฅผ ๋๋ฅธ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209514849-66f70529-a254-42cf-a8c1-7667cc4c2e18.png)
2. ์์ฑ๋ ์ด๋ฆ์ ๋ฐ์ดํฐ๋ฒ ์ด์ค๋ฅผ ๋๋ธํด๋ฆญํ ํ root์ password๋ฅผ ์๋ ฅํ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209514935-391227ba-3b2d-48f8-bdc9-b762b9c96dec.png)
3. ํ์ด๋ธ ์์ฑ ๋ฌธ์ฅ์ ์์ฑํ ํ ๋ฒ๊ฐ๋ชจ์(?) ๋ฒํผ์ ๋๋ฅด๋ฉด ํ์ด๋ธ์ ์์ฑํ  ์ ์๋ค.
![image](https://user-images.githubusercontent.com/100823955/209515039-f5e9b626-65ce-4f27-8750-f960889a143f.png)
4. ์ผ์ชฝ Navigator์ SCHEMAS์ ๊ฐฑ์ ๋ฒํผ์ ๋๋ฌ์ ๋ฐ์ดํฐ๋ฒ ์ด์ค๋ฅผ ๊ฐฑ์ ํ  ์ ์๋ค.
![image](https://user-images.githubusercontent.com/100823955/209515133-f1c4fa3a-5371-4446-b6c5-b019931f87e9.png)
- MySQL๊ณผ Django Project ์ฐ๋
1. category์ settings.py๋ฅผ ์คํํ์ฌ DATABASE ๋ถ๋ถ์ ๋ฐ์ดํฐ๋ฒ ์ด์ค ์ด๋ฆ๊ณผ, ์ ์  ์ด๋ฆ, ํจ์ค์๋๋ฅผ ์๋ ฅํ ํ
python manage.py migrate๋ฅผ ํ๋ฉด ๋์ Djaango Project์ MySQL์ ์ฐ๋ํ  ์ ์๋ค.
![image](https://user-images.githubusercontent.com/100823955/209515392-a6800cdf-f806-42b7-a1e6-7c54d333ce51.png)
- templates ํด๋ ์์ฑ
1. setting.py๋ฅผ ์คํํ์ฌ import os๋ฅผ ํ ํ TEMPLATES ๋ถ๋ถ์ 'DIRS': [os.path.join(BASE_DIR, 'templates)],
๋ฅผ ์์ฑํ์ฌ templates์ base ์ฃผ์๋ฅผ ์ค์ ํด์ค๋ค.
![image](https://user-images.githubusercontent.com/100823955/209515877-d83cfaa9-5827-4375-aea2-1e5a4fc6de43.png)
2. myApp ํด๋์ templates ํด๋๋ฅผ ์์ฑํ๋ค.
3. templates ํด๋ ์์ myApp ํด๋๋ฅผ ์์ฑํ๊ณ  myApp ํด๋์๋ ์์ผ๋ก ์น์ฌ์ดํธ ์ถ๋ ฅ์ ๋ด๋นํ  html\
ํ์ผ์ ์์ฑํ๋ค.
![image](https://user-images.githubusercontent.com/100823955/209515896-275be4e2-0dc4-4862-8cfd-b3168f362d06.png)

------------------------------------
## ๐๋ผ์ด์ผ์ค
๋ถ์ฐ๋ํ๊ต 2022 ๋ฐ์ดํฐ๋ฒ ์ด์ค[์ด๊ธฐ์ค ๊ต์๋] ์์ ppt ์๋ฃ.
