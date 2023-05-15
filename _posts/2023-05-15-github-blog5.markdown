---
layout: post
title: '[GithubPages] 5. Jekyll Hits 사용하여 조회수 표기법'
categories: git
permalink: '/:categories/:year/:month/:day/:title/'
# published: false
# comments: true
---

{% include hits.md %}

**설치 환경 : Mac**

# 기본 설정

저는 [khw11044](https://khw11044.github.io/blog/githubpages/2020-12-26-making-blog-08/)님의 포스팅과 chatGPT와 진행하였습니다.<br>
또한 저는 html이 아닌 markdown파일로 진행하였습니다.

### 1. Hits 사용법

[Hits](http://hits.dwyl.io/)의 사용방법

```
  ![HitCount](http://hits.dwyl.com/${username}/${project}.svg)
```

사용 예

```
  ![HitCount](http://hits.dwyl.com/maryk22/maryk22.github.io.svg)
```

### 2. Post내에 넣기

post 파일내에 해당 hits를 작성하면,

```
  ![HitCount](http://hits.dwyl.com/maryk22/maryk22.github.io.svg)
```

![Post내 Hits넣기](/assets/img/git/blog/blog_5_1.png 'Post내 Hits넣기')

![Hits 표기](/assets/img/git/blog/blog_5_2.png 'Hits 표기')<br><br>
이렇게 노출이 됩니다. 너무 예쁘지 않으니 꾸며보는 시간을 가져보아요.

### 3. Hits 꾸미기

[Hits 꾸미기](https://hits.seeyoufarm.com/) 사이트로 이동하여 원하는 아이콘과 색상 등을 수정해봅니다.<br><br>
![Hits 꾸미기](/assets/img/git/blog/blog_5_3.png 'Hits 꾸미기')
<br><br>

- 원하는 아이콘과 색상 등을 수정하고, markdown 코드를 복사하여 post내에 넣어줍니다.

![변경된 코드 넣기](/assets/img/git/blog/blog_5_4.png '변경된 코드 넣기')
![변경된 코드 확인](/assets/img/git/blog/blog_5_5.png '변경된 코드 확인')

<br><br>

- 저는 **링크**가 생기는게 싫어서 코드를 수정하였습니다.<br><br>
  **수정 전**

```
  [![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fmaryk22.github.io&count_bg=%2371B4E7&title_bg=%23555555&icon=bitrise.svg&icon_color=%23E7E7E7&title=%EC%A1%B0%ED%9A%8C%EC%88%98&edge_flat=false)](https://hits.seeyoufarm.com)
```

**수정 후**

```
  ![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fmaryk22.github.io&count_bg=%2371B4E7&title_bg=%23555555&icon=bitrise.svg&icon_color=%23E7E7E7&title=%EC%A1%B0%ED%9A%8C%EC%88%98&edge_flat=false)
```

![추가수정된 코드 확인](/assets/img/git/blog/blog_5_6.png '추가수정된 코드 확인')

### 4. 개별 조회수로 노출되게 변경하기

위에 단계까지는 개별 포스트의 조회수가 아닌 종합의 조회수가 노출됩니다.<br>
제가 원하는 것으로 **개별 포스트의 조회수**로 코드를 수정하였습니다.

```
  ![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fmaryk22%2Fmaryk22.github.io{page.url 넣는곳}&count_bg=%237FB7F1&title_bg=%23555555&icon=bitrise.svg&icon_color=%23E7E7E7&title=%EC%A1%B0%ED%9A%8C%EC%88%98&edge_flat=false)
```

<br><br>
url=https%3A%2F%2Fgithub.com%2Fmaryk22%2Fmaryk22.github.io 뒤 **&#123;&#123; page.url &#125;&#125;** 이부분을 추가하여 넣었습니다.<br><br>
이부분은 해당 페이지 url에 들어왔을경우에 조회수를 체크해주는 것 입니다.
<br><br>
![개별조회수 코드 넣기](/assets/img/git/blog/blog_5_7.png '개별조회수 코드 넣기')

### 5. Include 하기

매번 저 긴 코드를 넣기가 그래서 Include하는 방법을 찾아보았습니다.<br>
다만 저는 \_layer폴더 자체가 없어서 html로 한번에 하는 방법을 모르겠어서 다른방법으로 하였습니다.<br>
만약 다른 좋은 방법을 알고 계신다면 메일이나, 댓글로 부탁드립니다!

1. \_includes 폴더 내 hits.md 파일 생성
2. 해당 코드를 넣어주기
   ![hits.md내 코드 넣기](/assets/img/git/blog/blog_5_8.png 'hits.md내 코드 넣기')
3. 원하는 포스트.md파일에 include 시켜주기
   ![포스트.md include 하기](/assets/img/git/blog/blog_5_9.png '포스트.md include 하기')

<code>
  &#123;% include hits.md %&#125;
</code>
<br>

이렇게 github blog 내 조회수 넣기 완료하였습니다.

---

#### 다음글은 댓글기능 넣기입니다.
