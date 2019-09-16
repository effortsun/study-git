> #git commit

git commit은 디렉토리에 있는 파일들의 변경사항을 기록하는 것을 말한다.  
git은 최대한 가볍게 유지하는 특성을 갖고 있어 이전버전과 다음 버전의 변경내역인 스냅샷만을 저장하고 있다.

![git commit](./images/git%20commit.png)

그래서 보통 커밋을 할 때 디렉토리 전체를 복사하지 않고 commit을 하게 되면  
이전의 부모 commit 가르키게 됩니다.  
아래 그림의 *C1*이 *C0*을 가르키는 것과 같이..

![git commit2](./images/git%20commit2.png)  

여기서 git commit을 하게 되면 새로운 C2가 생성되며 C1을 가르키게 됩니다.  
**C2에서는 C1과 다른**, C1 이후의 변동사항이 기록되는 것 입니다.

![git commit3](./images/git%20commit3.png)

> #git branch

우선 branch는 _하나의 커밋과 그 부모 커밋들을 포함하는 작업 내역_ 이라고 알아 두고, 예제를 봅니다.

![git branch](./images/git%20branch.png)

**git branch newImage** 를 통해 새로운 **newImage**라는 브랜치 생성,  
현재 **master**라는 브랜치가 C1을 가르키고 있어 같은 위치에 생성됩니다.

![git branch2](./images/newImageBranch.png)

이 상태에서 **git commit**을 하게 되면 C2라는 새로운 commit이 생기고 master가 이를 가르키게 됩니다.  
그러나 새로 생성한 newImage 브랜치는 그대로 C1에 있는데,  
_이는 (*)가 master를 가르키고 있어, 현재 브랜치가 master에 있기 때문입니다._

![git branch3](./images/git%20branch2.png)

만약 새로 생성한 _newImage라는 브랜치에서_ commit을 하고 싶다면  
*git checkout* 명령어를 통해 브랜치를 변경하면 됩니다.  
*git checkout newImage; git commit;*
 
![git branch3](./images/git%20checkout.png)
