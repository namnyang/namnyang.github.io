---
title: 쉽고 간단하게 Github Page 만들기 [1]
author: namnyang
date: 2020-12-04 01:33
categories: [Github Page]
tags: [github]
---

#### 간단하게 GitHub 블로그를 만들어보자
이 글을 따라하면 누구나 쉽게 `https://username.github.io` 이라는 URL을 가진 블로그를 만들 수 있습니다



>   **시작하기에 앞서, 이 블로그는 기록하는 용도로 만든 블로그 입니다
>   맞춤법이나, 여러가지 불편한 점이 있을 수 있습니다**



### 1. Repository 만들기

이름이 **github username.github.io** 인 Repository를 만듭니다

예를 들어 깃허브 닉네임이 abc라면 Repository이름을 **adb.github.io**로 지어주면 됩니다

공개 유형은 **Public**으로 해야 Github Page기능이 활성화 됩니다

<img src="https://media.discordapp.net/attachments/757834543473623121/780631957246705696/unknown.png" alt="Repository 생성" style="zoom: 67%;" />

### 2. Repository Clone 해오기

Repository를 자신의 컴퓨터로 다운로드 합시다

**`Code ▼`**를 눌러 사진에 표시한 링크를 복사합시다 

맥/리눅스 사용자 라면 **Terminal,** 윈도우 사용자라면 **WSL**이나 **Git Bash**를 열고

```terminal
$ git clone 복사한 링크
```

를 입력해 Repository를 Clone합니다

<img src="https://cdn.discordapp.com/attachments/783321855774687273/784260364153913344/unknown.png" style="zoom: 67%;" />

### 3. Jekyll 테마 찾기

지금 이 상태에서도 **html**파일이나 **md**파일을 만들고 자신의 블로그 주소로 접속하면 파일 안의 내용이 출력 되기는 하지만,

더 예쁘게(?) 꾸미기 위해서 공개되어 있는 Jekyll 테마를 적용합시다

Github에는 수백 개의 [테마](https://github.com/topics/jekyll-theme)가 공개되어 있습니다

> -   [jekyllthemes.org](http://jekyllthemes.org/)
-   [github.com/topics/jekyll-theme](https://github.com/topics/jekyll-theme)
-   [jamstackthemes.dev/ssg/jekyll](https://jamstackthemes.dev/ssg/jekyll/)
-   [jekyllthemes.io](https://jekyllthemes.io/)

여기 있는 링크들은 모두 Jekyll테마를 다운받을 수 있는 사이트들 입니다

 이 글에서는 [첫 번째 사이트](http://jekyllthemes.org/)에 있는 **Chirpy **테마를 기준으로 설명하겠습니다

<img src="https://cdn.discordapp.com/attachments/783321855774687273/784256132659150858/unknown.png" alt="https://jekyllthemes.io 사이트" style="zoom: 67%;" />

### 4. 테마 적용하기

마음에 드는 테마를 찾았다면

**Download**를 눌러 선택한 테마를 다운로드 하고, 압축을 풀어 주세요

<img src="https://cdn.discordapp.com/attachments/783321855774687273/784257750581772328/unknown.png" style="zoom: 67%;" />

[여기에서](###2.-repository-clone-해오기) Clone한 폴더를 열고, 테마 폴더에 있는 파일을 모두 이동합니다

<img src="https://media.discordapp.net/attachments/783321855774687273/784268732460433438/unknown.png?width=1070&height=581" style="zoom: 67%;" />

### 5. `_config.yml ` 파일 수정

이동한 파일중에 `_config.yml `파일을 열어줍니다

>   **다시한번 말하지만, 이 글에서는 [이 사이트](http://jekyllthemes.org/)에 있는 Chirpy 테마를 기준으로 설명합니다**

```yaml
title: 블로그 제목                          # the main title

tagline: 블로그 부제목  # it will display as the sub-title

description: >-                        # used by seo meta and the atom feed
  블로그 설명글

 # fill in the base hostname & protocol for your site, e.g., 'https://username.github.io'
url: '깃허브 블로그 주소'

author: your_full_name                  # change to your full name

avatar: /assets/img/sample/avatar.jpg   # support internet resources
```

20번째 줄에 있는 url부분에 자신의 깃허브 블로그 주소 `(https://username.github.io)`를 입력합니다

다른 테마들도 조금씩 다를수는 있지만 파일의 구조는 비슷합니다

이렇게 옆에 적혀있는 주석을 보며 설정 파일을 수정해 주세요

### 6. 깃허브에 Push하기

`_config.yml ` 파일을 다 수정했다면 깃허브에 Push해 블로그에 적용해 봅시다

맥/리눅스 사용자 라면 **Terminal,** 윈도우 사용자라면 **WSL**이나 **Git Bash**를 열고

>   Github Desktop으로 GUI환경에서도 가능합니다

```terminal
$ git add .
$ git commit -m "커밋 내용"
$ git push
```

를 입력해 깃허브에 Push 해줍니다



`https://username.github.io`로 접속해서 Github Page가 정상적으로 만들어 졌는지 확인할 수 있습니다

>   **변경사항이 블로그에 반영되기까지 시간이 조금 걸릴 수 있습니다**
>   **만약 20분 정도 기다렸는데도 변경 사항이 반영되지 않으면 브라우저 캐시를 삭제해 보세요**



다음 포스트 에서는 Github Page에 포스트를 작성해 봅시다