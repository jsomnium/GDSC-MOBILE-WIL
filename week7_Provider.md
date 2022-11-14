# Provider 학습 파일

##### 학습 링크: <<https://youtu.be/te5rAq9F_hU>>

## __provider를 적용하지 않고 state를 사용해서 화면 전환을 하는 경우__

  * 각각 ```setState```를 해서 화면 전환을 해줌

  * example에서, 아래를 눌렀을 때 위가 바뀌게 하는 것
  
  * 보통 화면 전체가 ```setState```되어서 낭비가 있음

  * 화면의 반만 ```setState``` 해주기




## __provider를 적용해서 하는 경우__

  * ```class _ extends ChangeNotifier``` 이용
  
  * 화면 전환을 하기 위해서 ```notifyListners()``` 사용
  
  * ```StatelessWidget```을 더 선호함
  
  * ```notifyListners()```가 있는 위젯을 사용하여 화면의 반만 전환
  
### Provider의 장점: 화면의 필요한 부분만 효율적으로 다시 그리게 하는 것
