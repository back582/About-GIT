# About-GIT
2019/01/01 기준

(처음)
development에서 클론(1단계)
manager branch만들어(gitlab, git branch manager)

git checkout manager >> branch변경됨

----------------------------------------------------------------------------
(갱신)
git pull origin develop

코딩하고
git add .
그날 바로
git commit -m " 규칙정해서 작성하고"
git push origin manager(branch이름)

다음날도 git 
그다음날도

---------------------------------------------------------------------
(기능이 완료될때마다)
그러다 해당 기능이 완료됐다.
gitlab에서 manager -> development merge요청을 때려git 
git merge origin develop

그럼 내가 merge request 허락 하면

그떄! development branch는 너가 manager에서 작성한 기능이 merge되서 update됌
>> 누군가 1단계를 통해 clone을 하면 너가 작성한 기능가지 포함되서 clone받아지는거야

금요일마다 development에서 master로 merge할게요
이말은 master (live 사이트 운용되고있는 소스코드들생각합니다.)



그러면... master branch는 최신화되는거. 

----------------------------------------------------------------------------------------
git remote -v : 저장소 확인
	origin  https://lab.ssafy.com/webmobile3-sub3/s02p13c103.git (fetch)
	origin  https://lab.ssafy.com/webmobile3-sub3/s02p13c103.git (push)
	(컴퓨터가 알아먹는 저장소 이름-로컬이름) (저장소 주소-URL)
