# [week7] Flutter 앱 개발 완성 - 3회차

## 1. 패키지(pakage)

+  __패키지__ : 다른 사람들이 만들어 둔 위젯 또는 기능들

   링크: <https://pub.dev/>
  
   위 링크에서 다양한 패키지들을 사용 가능하다


## 2. 온보딩 화면 만들기

+ __온보딩__ : 앱에 대한 소개 및 사용법을 알려주는 과정

   - introduction_screen -> 소개 페이지가 만들어져 있는 패키지 파일
   
      > Navigator.pushReplacement : 화면 교체 코드

   - google_fonts -> 폰트를 사용가능하게 해주는 패키지 파일

   - shared_preferences -> 데이터를 메모리가 아닌 다른 곳에 저장해 앱을 재시작해도 이전 데이터를 유지하는 방법을 사용하는 패키지 파일


## 3. 버킷 리스트 앱 만들기

+ __버킷리스트 앱의 기능__


   1 . 버킷 리스트 작성(Create)
   
   2 . 버킷 리스트 조회(Read)

   3 . 버킷 리스트 수정(Update)

   4 . 버킷 리스트 삭제(Delete)
   
+ 코드

   ```
    body: bucketList.isEmpty
         ? Center(child: Text("버킷 리스트를 작성해 주세요."))
         : Center(child: Text('버킷 리스트가 존재합니다!')),
   ```
   > 조건문으로, ? 다음에는 TRUE 인 경우, : 다음에는 FALSE 인 경우가 온다
   

   ```
   TextEditingController textController = TextEditingController();
   ```
   > TextField의 값을 가져올 때 사용

         
         


## 4. 상태 관리 패키지 Provider 준비하기

+ __Provider__ (링크: <https://pub.dev/packages/provider/install>)

   - Provider를 이용하여 BucketService를 위젯 트리(Widget tree)의 꼭대기에 배치
   
   - 어디서든 쉽게 접근할 수 있도록 만들어줌

+ __ChangeNotifier 클래스__

   notifylisteners();를 호출하여 위젯들을 갱신하는 기능을 사용 가능


## 5. 버킷 리스트 앱에 Provider 적용하기

+ __Consumer 위젯__

   provider에서 제공해주는 위젯으로, 꼭대기에 있는 것들을 홈페이지에서 접근할 수 있게 함
   
+ __Provider 사용법 정리__

   - 전역적으로 사용되는 데이터를 담당할 서비스로 만듦

   - 해당 데이터에 대한 CRUD를 모두 해당 서비스에서 구현함

   - ChangeNotifier를 상속받아야 notifyListeners();를 호출하여 데이터를 사용하는 화면을 갱신할 수 있음

   - ChangeNotifier를 상속받아야 notifyListeners();를 호출하여 데이터를 사용하는 화면을 갱신할 수 있음
