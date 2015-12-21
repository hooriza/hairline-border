# hairline-border
hairline border 를 쉽게 그릴 수 있도록 도와주는 CSS

## 사용방법
hairline.css 를 추가하고, 그냥 원하는 엘리먼트에 hairline 클래스명만 지정 해 주면 된다.

````html
<link rel="stylesheet" src="/path/to/hairline.css">
<style>
   .box { position:relative; border:1px solid #f0f; margin:10px; }
</style>
<div class="box">1px border</div>
<div class="box hairline">hairline border</div>
````

## 데모
http://bit.ly/1ZfiH0o

## 주의사항
* android 의 경우 position:static 인 엘리먼트에는 hairline 클래스명을 사용 할 수 없다.
* android 에서 hairline 클래스명을 사용 한 경우, 해당 엘리먼트에서 ::before 를 사용 할 수 없다.
* android 에서 border-radius 와 함께 hairline 클래스명을 사용 한 경우 원하지 않는 모습으로 보여진다.

	````html
	<!-- 만약 이 문제를 해결 하기 위해서는 다음과 같이 ::before 엘리먼트의 border-radius 를 2배 크게 지정하는 방법을 써야 한다. -->
	<style>
		#foo::before { border-radius:20px; }
	</style>
	<div id="foo" class="hairline" style="border-radius:10px;">content</style>
	````

----

# hairline-border
You can draw the hairline border easily with this CSS.

## Usage
Add hairline.css to your HTML, and just add the 'hairline' className onto what element you want.

````html
<link rel="stylesheet" src="/path/to/hairline.css">
<style>
   .box { position:relative; border:1px solid #f0f; margin:10px; }
</style>
<div class="box">1px border</div>
<div class="box hairline">hairline border</div>
````

## Demo
http://bit.ly/1ZfiH0o

## Attention (In case of Android)
* You can't use the 'hairline' className onto what element be set 'position:absolute'.
* You can't use '::before' with the 'hairline' className.
* If you use 'border-radius' with the 'hairline' classNane, it will show a undesirable layout.

	````html
	<!-- If you want to solve this problem, The 'border-radius' have to be set 2 times in '::before' pseudo-element. -->
	<style>
		#foo::before { border-radius:20px; }
	</style>
	<div id="foo" class="hairline" style="border-radius:10px;">content</style>
	````
