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



