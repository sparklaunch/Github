# Github (백업 툴로서의 Git)

PC 간의 동기화를 위해 클라우드 시스템의 필요성이 대두됨. 버전 관리, 백업 매체, 협업 툴로서 Github이 각광을 받고 있음.



> 지역 저장소 (Local Repository) : 자신의 컴퓨터에 설치되어 있는 저장소.
>
> 원격 저장소 (Remote Repository) : 호스팅 서버에 설치되어 있는 저장소.



* Push : 로컬 저장소의 커밋들을 원격 저장소에 옮김.
* Pull : 원격 저장소의 커밋들을 로컬 저장소로 가져옴.
* Clone : 원격 저장소의 모든 커밋들을 로컬 저장소로 복제.



## 1. 백업 프로세스

1. Local Repository와 Remote Repository의 연결.
2. Local Repository를 Remote Repository로 Push.
3. Remote Repository로부터 Clone.
4. 반복...



## 2. 원격 저장소와 연결

* `git remote` : 현재 등록되어 있는 모든 원격 저장소를 보여줌.
* `git remote -v` : 현재 등록되어 있는 모든 원격 저장소를 더 자세하게 보여줌.
* `git remote add [name] [.git url]` : 원격 저장소와 현재 로컬 저장소를 연결함.



## 3. 원격 저장소로 Push

* `git push origin master` : master 브랜치를 원격 저장소로 푸시함.



> 참고 : 처음 푸시할 때에는, Github 계정 등록 과정이 필요.
>
> 참고 : `git push -u origin master` 와 동일.



## 4. 원격 저장소로부터의 Clone

* `git clone [.git url]` : 해당 원격 저장소 자체를 통째로 복제함.



> 참고 : `git pull` : 해당 원격 저장소로부터 전체 커밋을 가져옴(Pull). 엄밀히 말하면, 가져옴과 동시에 Merge 수행.
>
> 참고 : `git fetch` : git pull과 동일하나, 단지 Merge가 자동으로 수행되지 않는다는 차이점이 있음.
>
> 후에 `git merge [branch name]` 으로 Merge.

