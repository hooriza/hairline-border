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
* android 의 경우 position:static 인 엘리먼트에는 hairline 클래스명을 사용 할 수 없습니다.
* android 에서 hairline 클래스명을 사용 한 경우, border-radius 의 크기가 절반으로 보여집니다.
* android 에서 hairline 클래스명을 사용 한 경우, 해당 엘리먼트에서 ::before 를 사용 할 수 없습니다.
