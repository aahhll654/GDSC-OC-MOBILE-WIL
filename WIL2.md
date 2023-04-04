# 기본 위젯 4개

위젯은 모바일 앱에 디자인을 하기 위해 필요한 기본 요소라고 볼 수 있다. 이번주에는 Text, Image, Icon, Container 등 기본적인 4개의 위젯에 대해 배웠다.

## Text

Text 위젯은 모바일 앱에 글자를 넣고 싶을때 사용한다.  
`Text('글자')` 와 같은 형식으로 사용할 수 있다.

## Image

앱에 이미지를 넣고 싶을때는 Image 위젯을 사용하면 되는데, 그 전에 프로젝트 내에 'assets' 라는 이름의 폴더를 만들고 이미지 파일을 이 폴더에 넣어두어야 한다.  
그 후, pubspec.yaml 파일 중간부분의 'flutter:' 의 하위항목에 폴더의 이름을 등록해주어야 한다.

```yaml
flutter:
  assets:
    - assets/
```

위와 같은 형식으로 작성해주면 된다.  
그리고, `Image.asset('이미지경로')` 와 같은 형식으로 사용하면 된다.

## Icon

앱에 아이콘을 넣고 싶을때는 Icon 위젯을 사용하면 된다.
`Icon(Icons.아이콘이름)` 과 같은 형식으로 사용할 수 있다.
아이콘 이름은 아래의 주소에서 찾을 수 있다.  
<https://api.flutter.dev/flutter/material/Icons-class.html>

## Container

앱 안에 네모 박스를 넣고 싶을 때는 Container 또는 SizedBox 위젯을 사용하면 된다. 파라미터를 통해 넓이, 높이, 색상등을 지정해 줄 수 있다.  
예를 들어, `Container(width : 50, height : 50, color: Colors.blue)` 과 같이 사용할 수 있다.  
이때 사용하는 숫자의 단위는 LP이다. flutter 에서의 모든 단위는 LP라는 단위인데 이것은 cm나 inch 처럼 우리가 눈으로 보는 절대적인 수치이다. 1cm가 38LP이다.  
그런데 위와 같이 넓이와 높이를 지정해주어도 박스의 위치를 어디를 기준으로 잡아야 될지 작성해주지 않았기 때문에 width와 height 속성이 화면에 적용이 안된다.  
그래서 Center와 같은 위젯으로 position을 잡아주어야 한다.
Center 위젯은 자식 child 위젯의 position을 정가운데로 잡아주는 위젯이다.  
다음과 같이 사용할 수 있다.

```dart
MaterialApp(
  home: Center(
    child: Container(width : 50, height : 50, color: Colors.blue)
  )
)
```

# 질문

flutter에서 <https://api.flutter.dev/flutter/material/Icons-class.html> 이곳에서 제공하는 아이콘외에 다른 아이콘이나 직접 제작한 아이콘을 사용할 수 있는 방법이 있을까요?
