# 잘못된 Commit / Push를 취소

commit과 push를 반복하다 보면, 어쩌다 한번씩 잘못된 commit을 push 하는 경우가 발생한다.  이때 push를 어떻게 취소할 수 있는지 알아보았다.

## commit 목록 확인

`$ git log`  
`$ git log --oneline`  
지금까지 commit되어 있던 목록들을 확인할 수 있다.  
`--oneline` 옵션을 추가하면 한줄로 깔끔하게 확인할 수 있다.  

## $ git reset

`$ git reset --hard HEAD^`  
가장 최근의 commit을 지운다.  
  
`$ git reset --hard 1a2b3c`  
예시로 `1a2b3c` 라는 commit을 만들었지만, 실제로는 commit목록을 확인 후 사용한다.  
`1a2b3c`를 commit했을 당시의 상태로 reset된다.

## 강제 push

`$ git push origin -f`  
강제로 push 하는 방법이다.  
원격 저장소까지 reset한 상태로 바뀌게 된다.  
reset한 상태에서 push를 하게 되면 기존의 내용이 삭제되는 위험이 있기 때문에  
일반적인 push는 막히고 강제 push만 가능하다.  
  
개인적으로 사용하고 있는 repository는 강제 push를 사용해도 상관 없지만,  
팀프로젝트나 다른사람과 같이 사용하는 repository라면 반드시 상의 후에 진행해야 한다.