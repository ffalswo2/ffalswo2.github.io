# 프로젝트 Build 과정

## 레포지토리 생성

1. 새로운 Repository를 만든다
- Repository name : username.github.io의 형식으로 만든다
2. 로컬에 HTTPS를 통해 git clone을 해준다.
3. Clone받은 파일에 index.html에 간단한 텍스트를 입력한 후에 `htts://<username>.github.io`의 URL로 접속했을 때 입력한 텍스트가 뜬다면 올바르게 된 것이다.

## 테마 적용
1. 터미널을 통해 아래 명령을 실행한다.
<pre><code>
gem install bundler
gem install jekyll
</pre></code>

2. 원격저장소에 연결된 디렉토리에서
<pre><code>
jekyll new ./
</pre></code>

3. 번들 설치
<pre><code>
bundle install
</pre></code>

4. 변경사항 add, commit, push
- Github Action이 끝난 후 URL로 접근해보면 테마가 적용된 모습을 확인할 수 있다.

## 댓글 기능 적용하기
1. Disqus 가입 & 세팅
2. 해당 디렉토리의 _config.yml에 알맞은 key-value 추가
<pre><code>
comment:
  provider: "disqus"
  disqus:
    shortname:  "<사용자가 정한 이름>"
</pre></code>
3. disqus에서 universal code를 복사해서 _layouts/post.html에 적용
4. 댓글을 허용하고 싶은 곳에 아래와 같이 comments: true 코드 추가
<pre><code>
layout: page
title: About
comments: true
</pre></code>
5. 해당 게시물 아래에 댓글 기능이 추가된 것을 확인할 수 있다.



