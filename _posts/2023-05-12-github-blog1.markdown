---
layout: post
title: '[GithubPages] 1. 깃허브블로그 만들기!'
# date: "{{ 'now' | date: '%Y-%m-%d %H:%M:%S' }}"
categories: git
permalink: '/:categories/:year/:month/:day/:title/'
comments: true
---

{% include hits.md %}

기술적인 부분을 기록으로 남기기 위해서 테그 블로그를 생성하려고 알아보는중 Github 블로그를 만들어보면 좋겠다고 생각하여 시작하게 되었습니다.
이 글이 도움이 되길 바라면서 그럼 설치부터 시작합니다.

**설치 환경 : Mac**

# 1. Github Repository 만들기

---

## 1. github로그인 후 New 버튼 클릭

## 2. Repository name은 **${username}.github.io**로 만들기

<small>(저는 이미 생성되어있는 Repository 라서 에러 메세지가 나오는데 처음만드시는 분들은 안나옵니다!)</small>
<br>
![Repository 생성](/assets/img/git/blog/blog_1_1.png 'Repository 생성')
<br>

## 3. Repository로 들어온후 Code 클릭후 Clone 진행

![clone](/assets/img/git/blog/blog_1_2.png 'clone')<br>
<br>

1.  주소를 복사<br>
2.  clone하고 싶은 폴더 생성 후 터미널로 clone 진행<br>

    ```
    git clone ${복사한 주소}
    ```

3.  clone완료 후 해당 폴더로 들어간후 index.html파일 만들기<br>

    ```
    cd ${username}.github.io
    echo "hello gitblog" > index.html
    ```

4.  생성된 html파일 원격저장소에 Push<br>

    ```
    git add *
    git commit -m "원하는 커밋메세지"
    git push -u origin main
    ```

5.  주소창에 ${username}.github.io 검색 후 페이지 나오면 완성

---

#### 다음글은 Jekyll로 Blog를 꾸미기입니다.
