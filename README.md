# CheatSheet

# FFMPEG

- 고프로 회전할때 명령어 ( 링크 : https://blog.naver.com/PostView.nhn?blogId=chandong83&logNo=221298545679&categoryNo=0&parentCategoryNo=0&viewDate=&currentPage=1&postListTopCurrentPage=1&from=postView )
$ ffmpeg -i [입력 영상 파일명] -vf "transpose=[회전 모드]" [저장할 영상 파일명]

회전 모드는 다음과 같다.
0 = 90도를 시계 반대 방향으로 돌리고 상하 반전 시킨다.(기본값)
1 = 90도를 시계 방향으로 돌린다.
2 = 90도를 시계 반대 방향으로 돌린다.
3 = 90도를 시계 방향으로 돌리고 상하 반전 시킨다.

실제로 아래와 같이 사용한다.
$ ffmpeg -i in.mp4 -vf "transpose=3" out.mp4

- 동영상 합치기 ( 링크 : http://blog.daum.net/_blog/BlogTypeView.do?blogid=0BDqd&articleno=87&_bloghome_menu=recenttext )
a.mp4 랑 b.mp4 를 합칠때 
$ cat files.txt
file 'a.mp4'
file 'b.mp4'

$ ffmpeg -f concat -i files.txt -c copy c.mp4

- 이미지로 영상 만들기
$ ffmgeg -loop true -i input.jpg -ss 00:00:00 -to 01:15:00 output.mp4

Git Command

git cached
git log --pretty=oneline -2
git log --pretty=oneline -p diff 까지 보여주는거
git checkout -b
git diff --cached
git merge "현재로 합치고 싶은 branch"

git remote add upstream https://github.com/blah/원격 저장소
git remote -v  => 연결된 저장소

git commit --amend 현재 커밋에 합쳐서 커밋

git tag "tag-name"
git push --tags    => 태그 푸쉬할때

git stash
git stash list
git stash apply --index {number}
git stash drop {number}
git stash pop ???

git branch

체크아웃에다가 브랜드 생성
git checkout -b <branch>
