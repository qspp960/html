HTML
1. 기본형식: <태그>콘텐츠</태그>

2. 속성 추가: <태그 속성1="값" 속성2="값">콘텐츠</태그>

3. 태그 안에 태그 추가: <div> <p>Hello</p> </div>

4. 콘텐츠가 없다면: <태그 속성1="값" />

html에서 주석은 코드에 영향을 끼치지 않아야 한다.
 <!--주석--> 
 
html로 웹 기본 구성 짜기

<html>
	<head>
	
	</head>
	<body>
	
	</body>
</html>

html 주요 태그

-h1,h2,h3,h4,h5,h6
 헤드라인의 약자로 일반적으로 제목을 표시할 때 사용
 (크기에 따라 나뉘어 진다)

-p
 문단을 나눌 때 사용, 일반 텍스트를 사용할 때 주로 사용

-br
 줄바꿈을 시켜 줌

-a
 href 속성이 필요, a태그를 클릭했을 때 쓰여진 주소로 넘어가게 된다
 
-img
 img를 말 그대로 보여주는 태그, 필수 속성으로 이미지 주소 필요, 외부에 있는 이미지나 내부 이미지 사용가능
 
-form
 input 태그들을 넣어 사용자들이 입력한 데이터를 관리해준다.
 ex) <form> <label> </label> <input type="text"/></form>
 
-div
 영역을 나눌 때 사용, 하나의 박스로 생각
 
 CSS

선택자, 속성 존재

선택자는 스타일을 적용할 대상, 태그 id class 등을 선택할 수 있음

<html>
	<head>
		<style type="text/css">
			p {
				color: orange;
			}
			
			#id-test {
				color: blue;
			}
			
			.class-test{
				color: red;
			}
			
		</style>
	</head>
	<body>
		<p>hello</p>
		<div id="id-test">id 적용</div>
		<div class="class-test">클래스 적용</div>
	</body>
</html>

복합선택자
- 하위선택자, 자식선택자
<html>
	<head>
		<style type="text/css">
		
			/*하위 선택자*/
			#item-list p{
				color: red;
			}
			
			/*자식 선택자*/
			#item-list > p {
				color: blue;
			}
		</style>
	</head>
	<body>
		<div id="item-list">
			<p>첫번째 자식1</p>
			<p>첫번째 자식2</p>
			<div>
				<p>두번째 자식1</p>
				<p>두번째 자식2</p>
			</div>
		</div>
	</body>
</html>


<html>
	<head>
		<style type="text/css">
			#item1 {
				width: 100px;
				heigth: 100px;
				background-color: red;
				color: white;
			}
			#item2 {
				width: 300px;
				heigth: 100px;
				color: blue;
				font-size: 32px;
				font-weigth: bold;
			}
			#item-list {
				heigth: 200px;
				background-color: gray;
				padding: 16px;
			}
			#item-list > #item3{
				margin-bottom: 16px;
				background-color: yellow;
			}
			#item-list > #item4{
				margin-left: 16px;
				background-color: green;
				border: 5px solid blue;
			}
			
			
		</style>
	</head>
	<body>
		<div id="item1">1번 아이템</div>
		<div id="item2">2번 아이템</div>
		<div id="item-list">
			<div id="item3>3번 아이템</div>
			<div id="item4>4번 아이템</div>
		</div>
	</body>
</html>

flex layout
 보통은 html요소들이 수직적으로 배치되지만 원하는대로 배치할 때 사용
 flex의 핵심은 container와 item

<html>
    <head>
        <style>
            .parent {
				display: flex;
                background-color: aqua;
            }

            .child {
                width: 100px;
                height: 100px;
                background-color: blue;
								margin-right: 8px;
            }
        </style>
    </head>

    <body>
        <div class="parent">
            <div class="child">
                자식
            </div>
            <div class="child">
                자식
            </div>
            <div class="child">
                자식
            </div>
				</div>
    </body>

</html>

justify-contents
 아이템들의 여백을 관리 할 때 사용한다.
 flex-start, flex-end, center, space-around, space-between

align-items
 아이템 정렬방향과 수직방향으로 아이템의 여백을 관리한다.
 stretch, flex-start, flex-end, center, baseline
 


 


 


 


