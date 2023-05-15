---
layout: post
title: '[GithubPages] 2. Jekyll로 github blog 꾸미기'
# date: "{{ 'now' | date: '%Y-%m-%d %H:%M:%S' }}"
categories: git
permalink: '/:categories/:year/:month/:day/:title/'
# published: false
---

Jekyll 설치부터 실행까지 해보겠습니다.

**설치 환경 : Mac**

# 1. Jekyll 설치

저는 [Jekyll](https://jekyllrb-ko.github.io/) 공식사이트에서 알려주는 방법과 [SuperMemi's Study](https://supermemi.tistory.com/entry/%EB%82%98%EB%A7%8C%EC%9D%98-github-%EB%B8%94%EB%A1%9C%EA%B7%B8-Jekyll-%EC%9C%BC%EB%A1%9C-%EA%BE%B8%EB%A9%B0-%EB%B3%B4%EC%9E%90-gitHubio)님의 포스팅을 보고 설치 진행하였습니다.<br>

### 1. gem으로 jekyll과 bundler를 설치해줍니다 <br>

```
    gem install jekyll bundler
```

1-1. 만약 설치가 안된다면, [설치방법](https://jekyllrb.com/docs/installation/) 사이트를 보고 자기의 설치환경에 맞는 걸로 찾아 설치해주시면 됩니다.<br>
1-2. 저는 jekyll bundler를 전역으로 설치해주었습니다.

### 2. 설치가 완료되면 기존의 만들어 둔 index.html를 삭제합니다.

```
    rm -f index.html
```

### 3. jekyll를 원하는 곳에 설치 해줍니다.

**여기서 주의사항 만약 나의 github.io의 위치가 ~/blog/${username}.github.io/라면 해당 터미널의 명렁어는 blog에서 진행해주셔야 합니다.<br>즉, 상위폴더에서 진행주셔야합니니다.**

```
    jekyll new ./
```

### 4. jekyll new ./ 사용시 Error 해결

**SuperMemi's Study**님의 포스팅처럼 "jekyll new ./" 해당 명령어를 실행했더니 Error메세지가 나왔습니다.

```
    Conflict: /blog/maryk22.github.io exists and is not empty.
            Ensure /blog/maryk22.github.io is empty or else try again with `--force` to proceed and overwrite any files.
```

해당 error메세지는 해당폴더가 비어있지않다는 내용입니다.

```
    jekyll new ${username}.github.io -f
```

이때는 해당 명령어를 실행하여 주시면 됩니다. [JunYoung's Blog](https://cjy-tech.github.io/make-blog-with-jekyll-and-github_pages/) 참고<br>

### 5. 설치가 완료 되면 bundle 설치 후 실행하여주시면 됩니다.

```
    bundle install
    boundle exec jekyll serve
```

![로컬서버](/assets/img/git/blog/blog_2_1.png '로컬서버')

### 6. http://127.0.0.1:4000/ 실행시 화면이 노출되면 완료입니다.

<br>

---

# 2. Github Push

로컬에서 잘나오는걸 확인을 했다면, 이제 원격 저장소에 push를 해봅시다.

```
    git add .
    git commit -m "jekyll start"
    git push
```

완료 후 시간이 조금 지나면 https://${username}.github.io/에 로컬에서 확인한 내용들이 보일거예요!

---

#### 다음글은 Jekyll의 테마적용입니다.
