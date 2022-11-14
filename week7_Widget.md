# 1. __TabBarView__

- 일반적으로 TabBar와 함께 사용됨

  ```
  TabBar(
        tabs: [
               Tab(text: "Cat"),
               Tab(text: "Dog"),
      ],
  ),
  ```
- 선택한 Tab에 따라 화면이 바뀌기 때문에 ```StatefulWidget```을 상속하도록 만들어줌

- TabBar 안에 Tab을 이용해서 문자, 아이콘 또는 하위 위젯을 명시할 수 있음



   + ```indicator```: 선택된 Tab에 스타일 적용시 사용

   + ```labelColor: Colors.white```: 선택된 Tab의 label 색상 지정

   + ```unselectedLabelColor: Colors.black```: 선택되지 않은 Tab의 label 색상 지정

- TabBar 안에서 TabBarView 위젯을 통해 탭별 화면을 보여줌

  ```
  TabBarView(
       children: [
            탭1 화면,
            탭2 화면,          
      ],
  ),
  ```
  
- TabView 하위 항목과 탭은 일치해야 함

### -   __TabController__: TabBar와 TabBarView 간의 탭 선택을 조정함

- TabBar 및 TabBarView에 편리한 상태 저장 조상이 없는 경우 ```DefaultTabController``` 상속 위젯을 제공하여 TabController를 공유할 수 있음

# 2. FloatingActionButton

- FloatingActionButton: 디자인 액션 버튼

- Scaffold 안에 넣어서 사용 

```
floatingActionButton: FloatingActionButton(
        child: Icon(Icons.add),
        onPressed: () {
          // Add onPressed code
        },
```

- 하단 탭이 있는 경우에도 FAB를 끼워넣을 수 있음
