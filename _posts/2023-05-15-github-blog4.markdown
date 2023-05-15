---
layout: post
title: '[GithubPages] 4. Jekyll Theme Hydejack 콘텐츠 꾸미기 및 작성 법'
categories: git
permalink: '/:categories/:year/:month/:day/:title/'
# published: false
---

{% include hits.md %}

**설치 환경 : Mac**

# 기본 설정

저는 [khw11044](https://khw11044.github.io/blog/githubpages/2020-12-26-making-blog-03/)님의 포스팅과 chatGPT와 진행하였습니다.<br>

### 1. \_config.yml 설정

![_config.yml](/assets/img/git/blog/blog_4_3.png '_config.yml')
![_config.yml](/assets/img/git/blog/blog_4_4.png '_config.yml')
![_config.yml](/assets/img/git/blog/blog_4_5.png '_config.yml')
![_config.yml](/assets/img/git/blog/blog_4_1.png '_config.yml')

- url : 나의 github주소를 넣어 baseURL를 설정
- lang : 언어 선택
- title : 블로그의 타이틀 설정
- description : 설명글
- tagline : 사이드바에 넣을 설명글
- logo : logo 이미지 넣어줌
- author : 저자 설정
- menu : 사이드바에 넣을 카테고리 (저는 현재 git만 있어서 git만 넣음 추후 추가예정)
- accent_image : 사이드바 이미지 변경
- accent_color : defalut 컬러값 설정
- author1 : About에 대한 설정

### 2. \_data 설정 <br>

- \_data/authors.yml 파일에서 블로그의 저자와 설명글 등을 적을 수 있는 곳입니다.

![authors.yml](/assets/img/git/blog/blog_4_1.png 'authors.yml')
<br><br>

- name : 자기 이름<br>
- email : 자기 이메일<br>
- about : About 보여줄 자기 또는 블로그 설명 글<br>
- picture: picture은 About에 보일 자기 얼굴이다.<br>
  - 1x는 웹에서 보일사진
  - 2x는 모바일용이다.
- 이미지의 경로는 assets/img내에 넣어주면 된다.
- social은 여러개가 있는데 저는 github만 넣었다. (미사용은 주석처리)

### 3. \_featured_categories 설정

- 사이드바의 카테고리로 설정을 진행하는 곳입니다.
- 원하는 카테고리의 이름으로 변경 or 추가를 진행하면 됩니다.
- 저는 현재 git만 생성해 놓았으며, 다른것을 포스팅할경우 추가할 예정입니다.

![categories 설정](/assets/img/git/blog/blog_4_2.png 'categories 설정')
<br><br>

### 4. \_posts 작성방법

- 게시물은 **연-월-일-카테고리이름-내용제목.md**를 기준으로 작성해야함
  ![_posts 작성방법](/assets/img/git/blog/blog_4_6.png '_posts 작성방법')

- layout : post이기 때문에 post 다른 레이아웃도 많음
- title : 포스트의 제목
- categories : 사이드바에 맞춰서 넣음
- permalink : 설정을 하지않을시 (git/2023-05-15-github-blog4/) URL이 통으로 나오는데 필자는 카테고리/년/월/일/제목(git/- 2023/05/15/github-blog4/)으로 바꾸고 싶어서 변경했음
- published : 아직 포스트를 올리고싶지않다면 false로 해당 포스트가 노출이 되지 않습니다.

### 5. logo 제작

Logo는 [Canva](https://www.canva.com/ko_kr/create/logos/)라는 무료제작 사이트에서 제작하게 되었습니다.<br>
다양한 소스들이 있어 디알못인 필자에게 딱이였습니다.
![logo](/assets/img/img_logo_m.png 'logo')

### 6. favicon 설정

favicon는 만들어 놓은 Logo이미지를 활용하였습니다.

1. [favicon 사이트](https://www.favicon-generator.org/)에 들어가 favicon을 생성 및 다운로드
2. assets 폴더 내 icons 폴더 생성(있는 경우 생성X)
3. favicon.ico, icon-192x192.png 파일 넣기
   ![favicon](/assets/img/git/blog/blog_4_7.png 'conflict favicon')
4. docs/config.md 내 apple_touch_icon URL변경(동일하게 있다면 변경X)
   ![config](/assets/img/git/blog/blog_4_8.png 'conflict config')
   <br>

이렇게 기본 설정은 끝입니다.

---

#### 다음글은 포스트 내 조회수 넣기입니다.
