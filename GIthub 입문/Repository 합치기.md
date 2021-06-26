# [Repository 합치기]

현재 유니티의 연습용 Repository로 Unity3D와 Unity2D로 구분하여 저장하고 있다.

그런데 종종 연습용 Repository를 합칠 필요가 있는지 고민할 때 가 있다.

결국 고민 끝에 합치지 않았지만 나중에 혹시 합치는 일이 필요할 수 있으니

Repository를 합치는 방법을 간단하게 알아보았다.

## [git 명령어]

`git subtree add --prefix=(해당 Repository 하위의 디렉터리 구조) (옮겨올 Repository 주소) (옮겨올 Repository의 branch)`
`git subtree add --prefix=temp http://github.com/oeccsy/test3.git main`
* subtree를 이용하여 Repository를 합친다. 이때 commit log 까지 합쳐진다.

### [참고 링크]
* http://yeoseon.kr/git-repository-habcigi-commit-log-yuji-subtree-iyong/ 
* https://velog.io/@rssungjae/GitHub-GitHub-%EC%A0%95%EB%A6%AC%ED%95%98%EA%B8%B0