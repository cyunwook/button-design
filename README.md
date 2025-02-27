# button-design
버튼디자인

버튼에 커서를 올리기 전에는 buy, 커서를 올리면 색이 바뀌고 sold out으로 글자가 바뀌는 버튼이다

index.html파일에서는 btn,btn-swap이라는 클래스에, 버튼의 기본텍스트는 buy, 내부에 span태그로 감싸진 sold out을 적는다.
<body>
    <button class="btn btn-swap">
        Buy<span>Sold out</span>
    </button>
</body>

style.css파일이다.
body{
    background-color:#204063;
    display:flex;
    justify-content: center;
    align-items: center;
    height:100vh;
}
이 부분은 버튼을 중앙에 위치시키기 위한 부분이다.

cursor: pointer; → 마우스를 올리면 커서가 포인터(손가락 모양)로 변경하는 부분이다. 지난번 계산기 만들기에서도 사용했던거다.

.btn-swap span 부분은 버튼안에 감싸진 부분이다.
position: absolute; → 부모 요소(button)을 기준으로 절대 위치 설정한다.
opacity: 0; → 기본적으로 span을 보이지 않게 설정한다.
transition: opacity 0.5s; → opacity가 변경될 때 0.5초 동안 부드럽게 변화하게 해준다.

.btn-swap:hover span {
    opacity: 1;
}
이부분은 마우스를 버튼위에 올리면 span이 보이게되는것에대한 부분이다.

