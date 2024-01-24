# hyundaiCard
 

목차
 =====
 
1.소개

2.사용 기술

3.주요 기능

4.폴더 및 파일 구조

5.외부 라이브러리 및 프레임워크


 소개
  =====
이 웹페이지는 현대카드의 다양한 신용카드 상품, 혜택, 그리고 협력사와의 프로모션을 소개하는 페이지입니다. 직관적인 디자인과 함께 사용자들에게 흥미로운 콘텐츠를 제공하여 현대카드의 브랜드 가치를 전달합니다.

사용 기술

HTML5

CSS3

JavaScript

jQuery

Slick Carousel

ScrollReveal


주요 기능
  =====
1.모달 표시 및 닫기:

showModal ID를 가진 요소를 클릭하면 모달이 나타납니다.
closeModal ID를 가진 요소를 클릭하면 모달이 닫힙니다.
예시:
$('#showModal').click(function () {
    $('.dimm').show();
});

$('#closeModal').click(function () {
    $('.dimm').hide();
});

2.동적 콘텐츠 로딩:

jQuery의 load 함수를 사용하여 다양한 요소의 콘텐츠를 동적으로 로드합니다.
예시:
헤더 로딩: $('.main_header').load('../inc/header.html')
카테고리 로딩: $('.category').load('../inc/category.html')
푸터 로딩: $('.footer').load('../inc/footer.html')

3.스크롤 이벤트 처리:

스크롤 위치에 따라 특정 요소의 가시성이나 동작을 제어하기 위한 스크롤 이벤트 리스너가 있습니다.
예시:
html
Copy code
$(window).scroll(function () {
    // '.card_book' 요소에 대한 스크롤 처리
    // 스크롤 위치에 따라 투명도 변경
});

4.Swiper (슬라이더) 초기화:

카드 선택 슬라이더에 대한 Swiper 초기화가 이루어집니다.
슬라이더에는 네비게이션 화살표가 있으며 현재 항목의 세부 정보가 동적으로 표시됩니다.
예시:
html
Copy code
var swiper = new Swiper(".slider", {
    // Swiper 설정
    on: {
        slideChange: (index) => {
            // 현재 슬라이드를 기반으로 콘텐츠 동적으로 업데이트
        }
    }
});

5.동적 링크 수정:

특정 링크의 href 속성이 동적으로 수정됩니다.
예시:
$('#click').attr('href', './event.html')
$('.card_design a').attr('href', './event.html')
$('.main .button a').attr('href', './event_2.html')  
