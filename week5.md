[WEEK5] 1회차 : Flutter 앱 개발 맛보기 & Dart 문법 익히기

- flutter 이해하기 -> flutter는 모든 것이 위젯으로 만들어져 있다.
Scaffold(
	appBar: 다른 위젯, // 상단 바
	body: 다른 위젯, //화면 중앙에 가장 큰 면적
	bottomNavigationBar: 다른 위젯, //하단 바
	floatingActionButton: 다른 위젯, //우측 하단
),

- 자동완성 단축기: ctrl + space

- 버튼
// 위로 올라와 있는 듯한 버튼
ElevatedButton(
  onPressed: () {},
  child: Text('Elevated Button'),
),

// 텍스트 버튼
TextButton(
  onPressed: () {},
  child: Text('Text Button'),
),

// 아이콘 버튼
IconButton(
  onPressed: () {},
  icon: Icon(Icons.add),
),

- TextField()
- 텍스트 입력란 생성
- labelText: 입력란 안에 텍스트 입력
- obscureText: true 비밀번호가 안보이게 됨

- AppBar 위젯의 title은 Android에서는 왼쪽 정렬, iOS에서는 중앙 정렬로 보이므로
- centerTitle: true
- 라고 넣어 두 플랫폼에서 모두 중앙 정렬이 되도록 만들어줌

[Dart 문법]

-변수의 이름을 부르면 변수에 담긴 값이 나옴
var name = "철수";
print(name); // 철수

- 함수 입력 값을 이름과 함께 전달하는 방법
- say(from: 영희);

- String getName(){ return "철수" }
- String getName() => "철수"
- 두 함수는 동일하다

- 클래스의 구성 요소
속성(Property) : 클래스 내의 변수
메소드(Method) : 클래스 내의 함수
생성자(Constructor) : 클래스 명과 동일한 함수

- 상속
- class 클래스A extends 클래스B
