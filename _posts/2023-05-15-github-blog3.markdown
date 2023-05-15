---
layout: post
title: '[GithubPages] 3. Jekyll Theme 적용 (Hydejack)'
# date: "{{ 'now' | date: '%Y-%m-%d %H:%M:%S' }}"
categories: git
permalink: '/:categories/:year/:month/:day/:title/'
# published: false
comments: true
---

{% include hits.md %}

저는 테마중에 Hydejack이 한글에서 제일 가독성이 괜찮다고해서 해당 테마를 설치하였습니다.

**설치 환경 : Mac**

# Hydejack Theme 설치

저는 [zeddios](https://zeddios.tistory.com/1223) 포스팅과 [SuperMemi's Study](https://supermemi.tistory.com/entry/%EB%82%98%EB%A7%8C%EC%9D%98-github-%EB%B8%94%EB%A1%9C%EA%B7%B8-Jekyll-%EC%9C%BC%EB%A1%9C-%EA%BE%B8%EB%A9%B0-%EB%B3%B4%EC%9E%90-gitHubio)님의 포스팅을 보고 설치 진행하였습니다.<br>

### 1. Theme download 하기 <br>

[Download](https://hydejack.com/download/)<br>
저는 9.1.6 버전을 다운받았습니다.

### 2. 다운로드한 파일 복사 및 내 github.io 폴더에 붙혀넣기

- 다운로드한 파일 복사 후 내 github.io 폴더에 복사 붙혀넣기
- 대치 되는 항목은 모두 대치해줍니다.

![다운로드파일복사](/assets/img/git/blog/blog_3_1.png '다운로드파일복사')
<br><br>

![내원격저장소에붙혀넣기](/assets/img/git/blog/blog_3_2.png '내원격저장소에붙혀넣기')

### 3. bundle install 후 serve 실행

```
   bundle install
   bundle exec jekyll serve
```

### 4. http://127.0.0.1:4000/ 실행시 화면이 노출되면 완료

1. conflict error 발생 시 **404.html, about.markdown, index.markdown 세개의 파일을 삭제**
   ![conflict error](/assets/img/git/blog/blog_3_3.png 'conflict error')

### 5. 원격저장소에 push하기

```
    git add .
    git commit -m "Hydejack Theme install"
    git push
```

1. push 후 충돌이 있는경우 \_config.yml 파일을 수정해주시면됩니다.

   ![push 후 충돌](/assets/img/git/blog/blog_3_4.png 'push 후 충돌')
   <br><br>

2. remote_theme앞 #지우고 theme앞에 #넣기<br>
   **변경전**

   ```
       theme: jekyll-theme-hydejack
       #remote_theme: hydecorp/hydejack@v9
   ```

   **변경 후**

   ```
       #theme: jekyll-theme-hydejack
       remote_theme: hydecorp/hydejack@v9
   ```

3. 다시 커밋 후 push하면 끝입니다.

### 6. https://${username}.github.io/ 실행시 화면이 노출되면 완료입니다.

### 7. 다시 로컬 작업시 수정사항

- push 해줄때는 remote_theme가 주석이면 안되지만 local에서는 주석처리가 되어야합니다.<br>
  그러므로 로컬작업시에는 remote_theme앞에 #를 넣어주고 theme앞에 #는 지워주세요.<br>
  또한 push할때는 다시 반대로 해주셔야합니다.

```
    theme: jekyll-theme-hydejack
    #remote_theme: hydecorp/hydejack@v9
```

---

#### 다음글은 콘텐츠 꾸미기입니다.
