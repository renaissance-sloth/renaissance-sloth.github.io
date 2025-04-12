---
title: "깃허브 블로그 시작하기"
excerpt: "깃허브 블로그를 시작하는 법"

tags: github blog jekyll
header:
  teaser: https://github.githubassets.com/assets/GitHub-Mark-ea2971cee799.png
---

# Github Blog 시작하기
## 기본 환경 설정
### Ruby 세팅
<a href="https://rubyinstaller.org/downloads/" target="_blank">Ruby download 링크</a>에 접속하여, **Ruby+Devkit (버전) (x86)** 을 설치한다. Jekyll이 32bit이기 때문에 꼭 **(x86)** 인지 확인하길 바란다.

### Jekyll 세팅
명령 프롬프트(CMD) 창에 아래의 명령어를 입력한다.
```
gem install jekyll
```

`ruby -v`와 `jekyll -v`로 잘 설치되었는지 확인할 수 있다.

## 테마
테마는 <a href="http://jekyllthemes.org/" target="_blank">링크</a>에 접속해 마음에 드는 것을 골라 사용할 수 있다. 

나는 `minimal mistakes`를 선택할 것이다. 

<a href="https://github.com/mmistakes/minimal-mistakes" target="_blank">mmistakes github</a>에 접속해서 코드를 clone 받아오자. 

![img](https://drive.google.com/thumbnail?id=1lqgKEqof_gYDoD4A9gcpEja9Qj2_cV4W&sz=w1000)

위의 그림에서 선택된 파일들은 사용하지 않는 파일들로 삭제해도 좋다.

더욱 상세히, 많은 정보를 원한다면, <a href="https://mmistakes.github.io/minimal-mistakes/" target="_blank">mmistakes homepage</a>를 참고해보자.

## 레포지토리 만들기

`(본인의 깃허브 아이디).github.io`로 레포지토리를 생성하고 진행사항을 push하면 된다.

## 로컬 서버 실행
레포지토리 폴더에서
명령 프롬프트(CMD) 창에 아래의 명령어를 입력한다.
```
gem install bundler
bundle exec jekyll serve
```
계속 서버를 보고싶다면 CMD 창을 종료하면 안된다.

`Server running... press ctrl-c to stop.`가 나온다면 정상적으로 작동하는 것이다.

<a href="http://localhost:4000" target="_blank">http://localhost:4000</a>에서 확인할 수 있다. 지금 상태는 **로컬**에서 열린 것으로 다른 컴퓨터에서는 볼 수 없다.
아직 자랑하지는 말자.

## _config.yml 편집

기본적인 데이터들을 넣어주자.

<a href="https://mmistakes.github.io/minimal-mistakes/docs/configuration/" target="_blank">링크</a>에서 한줄 한줄 친절히 설명해준다.

