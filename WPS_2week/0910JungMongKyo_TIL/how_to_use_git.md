#git

###__공부 자료__ [git-scm](https://git-scm.com/book/ko)

history - 파일이 처음 생성되고 나서부터 변경사항을 전부 모아놓은것 

리모트 저장소 : 

거의 모든 명령을 로컬에서 실행 

1. 히스토리를 조회할 때 서버 없이 조회한다 
	* 속도가 빠름
2. git의 무결성
	* 우리가 원하는 데이터가 그대로 보존된다
	* 해시 충돌이 발생하지 않아야 무결성이 보장된다고 한다. 
	* 체크섬 : 
	* SHA-1 체크섬 : 
3. git에는 데이터를 추가한다
	* 어떤 작업을 했다는 사항이 추가되는 것
	* programming과 관련없는 코드가 들어가면 안된다

	
* 세 가지 상태
	* committed : 데이터가 로컬 데이터베이스에 안전하게 저장된 상태
	* Modified : 아직 git에는 올라가지 않았았는데 수정이 된 상태
	* Staged : 수정된 파일을 곧 커밋할 것이라고 표시한 상태
	* 순서(한가지 상태가 더 있다 : Modified -> Staged -> committed

	* staged는 unmodified상태와 같다 
	* untracked 

* CLI 와 GUI
	* CLI : command line interface 
		* 명령어 인터페이스
	
	* GUI : Graphic user interface

	
[__zsh설치 및 개발 환경 참고 블로그__] (https://subicura.com)


git diff --staged : add로 추가된 staged 영역을 보여준다 
git diff : add 로 추가되기 전에 modifed된 영역을 보여준다 


* 무시하고 싶은 파일은 gitignore속에 적는다:
	
		$ vim gitignore 
		
	> 모든 abc 파일 
	
	 	abc.txt
	 		
	> 현재 해당 폴더 안의 파일 
		
		/abc.txt
		
	###[__gitignore 참고 사이트__](https://gitignore.io)
	
	
### 파일 삭제하는 방법

rm 명령어를 이용한다. 

ex) abc.txt 파일 삭제 방법

	$ rm abc.txt
	$ git add abc.txt
	$ git commit -m 'abc.txt파일 삭제'
	
staged 영역에서 지우는 방법

	$ git rm --cached abc.txt
	
	
### 파일 복사하는 방법	

	$ cp <원본> <대상 (파일이름 생략가능)>
	
* branch 는 commit 을 가리키는 pointer 

* 기본적으로 Head 는 branch를 가르킨다
	* 현재 작업 내용이 Head를 통해 설정된다 


* checkout은 commit의 이동에도 쓰지만 Head 포인터를 움직일 때도 쓰인다 

		$ git checkout 'branch name'
		

3-1 까지 따라해보기