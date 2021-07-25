
* 컴포넌트 랜더링 결과물을 사용하기 위해선 React.memo 사용
React.Memo

컴포넌트의 리랜더링 되는 함수를 최적화함.
프롭스가 바뀌었을 때만 리랜더링.

1.export default React.memo(UserList);
2. export default React.memo(CreatUser);

이런식으로 마지막에 적어줌. 

export default React.memo(UserList, (prevProps, nextProps) => nextProps.users === prevProps.users);
이런식으로 쓸 수도 있지만 나머지 프롭스가 고정적이라 비교할 필요가 없는지 확인이 필요!
 함수형 업데이트 (예: users => users.map((user) =>) 하지 않았더라면, 
최신 상태의 users 를 가르키고 있지 않음.


정리! 컴포넌트를 최적화하는 방법
