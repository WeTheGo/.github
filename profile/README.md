<!--

**Here are some ideas to get you started:**

🙋‍♀️ A short introduction - what is your organization all about?
🌈 Contribution guidelines - how can the community get involved?
👩‍💻 Useful resources - where can the community find your docs? Is there anything else the community should know?
🍿 Fun facts - what does your team eat for breakfast?
🧙 Remember, you can do mighty things with the power of [Markdown](https://docs.github.com/github/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)
-->
![header](https://capsule-render.vercel.app/api?type=cylinder&color=auto&height=300&section=header&text=WeTheGo%20Github&fontSize=90&animation=twinkling )
<div>
<h5>Notion 바로가기</h5>
<a href="https://reliable-bunny-1f8.notion.site/80b1b15e82e446b0b796865e4244ebab">
  <img src="https://img.shields.io/badge/notion-black?style=flat-square&logo=notion&logoColor=white"/>
  </a>
</div>



<div align=left><h2>📚 STACKS</h2></div>
<div align=center> 
  <img src="https://img.shields.io/badge/java-007396?style=for-the-badge&logo=java&logoColor=white">
  <img src="https://img.shields.io/badge/html5-E34F26?style=for-the-badge&logo=html5&logoColor=white"> 
  <img src="https://img.shields.io/badge/css-1572B6?style=for-the-badge&logo=css3&logoColor=white"> 
  <img src="https://img.shields.io/badge/javascript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"> 
  <img src="https://img.shields.io/badge/jquery-0769AD?style=for-the-badge&logo=jquery&logoColor=white">
  <img src="https://img.shields.io/badge/mysql-4479A1?style=for-the-badge&logo=mysql&logoColor=white"> 
  <img src="https://img.shields.io/badge/mariaDB-003545?style=for-the-badge&logo=mariaDB&logoColor=white">
  <br>
  <img src="https://img.shields.io/badge/react-61DAFB?style=for-the-badge&logo=react&logoColor=black">
  <img src="https://img.shields.io/badge/spring-6DB33F?style=for-the-badge&logo=spring&logoColor=white">
  <img src="https://img.shields.io/badge/linux-FCC624?style=for-the-badge&logo=linux&logoColor=black"> 
  <img src="https://img.shields.io/badge/apache tomcat-F8DC75?style=for-the-badge&logo=apachetomcat&logoColor=white">
   <img src="https://img.shields.io/badge/github-181717?style=for-the-badge&logo=github&logoColor=white">
  <img src="https://img.shields.io/badge/git-F05032?style=for-the-badge&logo=git&logoColor=white">
  
  </div>
 
# git branch

* 브랜치 확인
    - 현재 로컬에 존재하는 브랜치 확인
~~~
git branch

ex)
* main
  test

*는 현재 선택 된 (checkout된 브랜치를 의미)
~~~

* 브랜치 생성
~~~
git branch BRANCH_NAME
~~~

* 브랜치 선택
~~~
git checkout BRANCH_NAME

참고)
git checkout -b BRANCH_NAME
새로운 브랜치 생성과 동시에 해당 브랜치를 선택할 수 있습니다.
~~~

* 브랜치 이력 및 차이점 확인
~~~
git log
- 현재 브랜치 수정 내역 출력
~~~
![1](https://user-images.githubusercontent.com/104331314/182086983-6aa6657c-b914-4ffa-a602-db8f24d368ac.JPG)

~~~
git log --branches
- 모든 브랜치의 수정 내용
~~~
![2](https://user-images.githubusercontent.com/104331314/182087258-09cf47bd-c56c-4c7d-962f-60c72fb502f4.JPG)

~~~
--graph 옵션을 사용하면, 조금 더 이해하기 쉽게 출력됩니다.
~~~
![3](https://user-images.githubusercontent.com/104331314/182087447-0d6db30a-00b6-4028-a0b6-bf5eee7c0d6e.JPG)

~~~
git log --branches --graph --oneline

 --oneline 옵션을 사용하면, 간단하게 브랜치와 메시지만을 확인할 수 있습니다.
 ~~~
 ![4](https://user-images.githubusercontent.com/104331314/182087618-d37c6acc-5eaf-4a8d-be12-2c30b66dbed1.JPG)

* git log 브랜치 비교
~~~
git log main..BRANCH_NAME

-  현재 브랜치와 main 브랜치의 커밋 차이를 확인할 수 있습니다.
~~~
![5](https://user-images.githubusercontent.com/104331314/182087889-45a32884-640a-4be1-a0ee-9d21a0a8ed4f.JPG)

~~~
git log -p main..BRANCH_NAME

-p 옵션을 사용하면, 수정된 내용도 함께 확인할 수 있습니다.
~~~
![6](https://user-images.githubusercontent.com/104331314/182088064-7a192b2d-a8be-436d-9500-85f7ad053749.JPG)

* git diff 브랜치 비교
~~~
git diff main..BRANCH_NAME

파일명과 수정 내용을 확인할 수 있습니다.
~~~
![7](https://user-images.githubusercontent.com/104331314/182088290-78de0d6c-8c13-4142-ab5c-866d72673ce4.JPG)

* git merge
1. git checkout main 으로 이동
2. git merge 명령어를 사용하여 main 브랜치에 병합하고자 하는 브랜치를 병합합니다.
    ex)git merge BRANCH_NAME
3. 병합 성공 예시
  
![8](https://user-images.githubusercontent.com/104331314/182088542-cd0636e4-87d4-41e4-b620-0922aab81e50.JPG)

4. 병합 된 브랜치 제거
~~~
git branch -d BRANCH_NAME

-d : 병합 된 브랜치를 지울 때
-D : 병합되지 않은 브랜치를 지울 때
~~~

* 충돌
1. git merge 명령어를 사용하여, 브랜치를 병합할 때, 동일한 파일을 수정한 경우 다음과 같이 충돌(Conflict)로 인해 병합에 실패하는 것을 확인할 수 있다.

![9](https://user-images.githubusercontent.com/104331314/182088841-245398e7-2d9e-4b91-8848-89dce3f66dcc.JPG)

2. git status 명령어를 실행하여, 현재 상태를 확인하면 다음과 같이 병합을 하지 못한 파일을 확인할 수 있다.

![22](https://user-images.githubusercontent.com/104331314/182088973-baa33ceb-68b8-4086-9faf-6f9a42a470a5.JPG)


