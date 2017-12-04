[https://xho95.github.io/blog/github/pages/jekyll/minima/theme/2017/03/04/Jekyll-Blog-with-Minima.html](https://xho95.github.io/blog/github/pages/jekyll/minima/theme/2017/03/04/Jekyll-Blog-with-Minima.html)를 주로 참고 하였다. 

# 시작

저 링크에 써진대로 깃허브가 뭔지, 지킬이 뭔지 하나도 모른다. 그냥 만들어 봤다. 환경은 macOS.

## Github에 올릴 준비 하기 : Github에 repository 만들기

1. github.com 로그인
2. [Start a project] 버튼 클릭
3. 'Repository name'에 'haekwan.github.io' 입력 후, [Create repository] 버튼 클릭


## jekyll을 github에 올리기

> 여러 포스팅에서는 [지킬용 테마가 많이 올라와 있는곳](http://jekyllthemes.org/)에 가서 Fork하라고 하였으나, 실제로 해본 결과 CSS가 깨진다. 
>
> _config.yml 파일에서 경로를 수정하면 되던데, 이왕 할바에야 새로 해보는게 좋겠다 싶어서 새로 시작

### Clone ! 

1. 터미널 실행

2. ```$ git clone https://github.com/username/username.github.io```입력  (username 부분은 자기꺼 사용)

3. 이러면 /Documents/Github/username.github.io로 뭐가 다운로드 되더라. 이게 클론하는거 인가보다.

### 로컬에 jekyll 설치하기

>시행 착오
>
>1. 터미널 실행
>2. ``` $ sudo gem install jekyll```
>3. 이러니까 안되더라… 루비 버전이 낮다고 하는것 같다.
>4. 루비를 높은 버전으로 설치
>5. [http://www.ruby-lang.org/en/documentation/installation/](http://www.ruby-lang.org/en/documentation/installation/)에 가니까 brew로 된다고 하던데, 그것도 설치되어 있지 않았다.
>6. [https://brew.sh/index_ko.html](https://brew.sh/index_ko.html) 여기서 brew 설치


1. 블로그 글 참조하여 다시 해봄. ```$ sudo gem install jekyll bundler```
2. 오!

### jekyll로 블로그 만들기

1. 아무 폴더로 이동하여 블로그를 만들어본다. 난 도큐먼트 폴더에다 만들고 싶었기 때문에 도큐먼트 폴더로 이동. ```cd documents```
2. ```$ jekyll new my-awesome-site``` 
3. my-awesome-site라는 폴더가 생기고 그안에 여러가지 것들이 생긴다.

### 잘 되는지 테스트 해본다

1. ```bundle exec jekyll serve``` 
2. 브라우저에 http://localhost:4000 입력
3. 오! 잘 나온다.

> 이것이 로컬에서 해보고 확인하기 좋은 방법이라고 한다. 

### 이제 블로그를 올린다

1. 깃허브에서 클론받은 저장소로 저걸 옮겨야한단다. 

2. 터미널  ```cd users/documents/github/username.github.io```로 이동

3. ```cp -r users/documents/my-awesome-site/ ./```
   1. 근데 그냥 마우스로 드래그해서 옮겨도 될것 같다. 

4. ```$ git add .```
   ```$ git commit -m "my first blog"```
   아무일도 안일어나더라...


5. ```$ git push origin master```

6. http://username.github.io 접속

7. 잘 나온다!

소요 시간은 잘 몰라서 이것 저것 살펴보다가 한시간 정도 걸린것 같다.

## 간단한 세팅

1. github.com/username/username.github.io 접속
2. _config.yml 클릭
3. 연필 모양 클릭 (edit)
4. Title, email, description, url, GitHub_username 등 간단히 수정
5. 하단으로 내려 [Commit changes] 클릭
6. http://username.github.io 에서 변경사항 확인

추가적으로 [GitHub desktop](https://desktop.github.com/) 을 받아 연결 해보니, 수정사항도 잘 볼수 있더라.