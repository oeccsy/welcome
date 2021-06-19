# [.gitignore 사용법]

에디터를 사용할때 필요한 파일(.vs)이나 실행파일(.exe) 까지 push 하게 되면
원격 저장소가 지저분해진다.

또한 push해서는 안되는 파일을 실수로 push 하는 일이 생길 수 도 있는데,  
  
.gitignore 을 잘 사용하면 위의 내용이 모두 해결된다.

## [.gitignore 작성 규칙]

* #로 시작하는 라인은 주석처리 된다.
* 제외하고 싶은 파일이나 유형을 입력한다. ex) *.class
* /로 시작하면 하위 디렉터리에 적용되지 않는다. 
* 디렉터리는 끝에 /를 사용하여 표현한다.
* !로 시작하는 패턴의 파일은 무시하지 않는다.

## [작성 예시]
```
#ignore all .exe files
*.exe

#ignore vscode
.vscode/*
```
Study-Baekjoon 레포에서는 실행파일과 vscode 관련 파일을 제외하기 위해  
위와 같이 작성하였다.

## [.gitignore 가 잘 적용되지 않을 때]

간혹 .gitignore가 잘 적용되지 않는 경우가 있다.  
이럴 때 다음과 같이 git의 캐시 내용을 전부 삭제 후 다시 add All 하여 커밋한다.

`git rm -r --cached .`  
`git add .`  
`git commit -m "fixed untracked files"`  


#### [참고링크]
* https://velog.io/@psk84/.gitignore-%EC%A0%81%EC%9A%A9%ED%95%98%EA%B8%B0
* https://jojoldu.tistory.com/307 