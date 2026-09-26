## Key Learning
1. HTML Form의 다양한 입력 요소와 속성을 사용하여 사용자로부터 데이터를 입력받는 방법
2. Bootstrap의 Form 관련 클래스를 활용하여 Input, Select, Checkbox, Radio 등 활용
3. JavaScript의 addEventListener(), checkValidity(), preventDefault(), focus() 등을 활용하여 Form의 입력값을 검사하고 제출 

## Form Elements
- input type="text": 이름, 사용자 이름, 주소, 카드번호 등의 문자열 입력
- input type="email": 이메일 입력 및 이메일 형식 확인
- input type="date": 카드 유효기간 입력
- input type="checkbox": 배송지 동일 여부 및 정보 저장 여부 선택
- input type="radio": 결제 방법 선택
- select: Country와 State 선택
- textarea: 배송 관련 요청사항 입력
- button type="submit": Form 제출
- label: 각 입력 요소의 이름을 표시하고 해당 Input과 연결

## HTML vs CSS
form1.html에서는 Form의 기본적인 구조와 입력 요소를 구성하였다. form1_css.html에서는 기존 HTML 구조를 유지하면서 Bootstrap과 Internal CSS를 적용하여 Form의 디자인과 배치를 변경하였다.
즉, HTML은 Form의 구조와 입력 요소를 구성하고, CSS와 Bootstrap은 Form의 디자인과 배치를 담당한다.

## Validation & JS
HTML Validation에서는 required, type="email", minlength, maxlength 등을 사용하여 입력값의 조건을 설정
JavaScript에서는 Form의 submit 이벤트를 addEventListener()로 처리 
event.preventDefault()를 사용하여 Form의 기본 제출 동작을 막고, checkValidity()를 이용하여 입력값이 조건을 만족하는지 확인
유효하지 않은 입력이 발견되면 alert()로 안내하고 focus()를 이용하여 해당 입력 요소로 이동
모든 조건을 만족하면 등록 완료 메시지를 출력
또한 Country의 선택값에 따라 State의 선택 항목이 변경되도록 change 이벤트와 innerHTML을 활용하였다.

## Problem & Solution
Country와 State를 각각 별도의 select로 만들었을 때 Country에 따라 State의 선택 항목을 변경하는 방법을 알기 어려웠다. 처음에는 optgroup을 사용하면 될 것이라고 생각했지만, optgroup은 선택 항목을 그룹으로 묶는 기능이고 다른 Select의 내용을 변경하는 기능은 아니었다.
따라서 JavaScript의 change 이벤트를 사용하여 Country의 선택값을 확인하고, innerHTML을 이용하여 State의 <option> 내용을 동적으로 변경하였다.

## Reflection
이번 실습을 통해 HTML Form은 단순히 입력창을 만드는 것이 아니라 사용자의 데이터를 입력받고 검증하여 처리할 수 있는 구조라는 것을 이해하게 되었다. 특히 HTML의 Validation 기능과 JavaScript를 함께 사용하면 사용자가 잘못된 값을 입력했을 때 직접 안내하고 입력 위치까지 이동시킬 수 있다는 점을 알게 되었다. 또한 Bootstrap을 사용하면 CSS를 직접 작성하지 않아도 Form의 기본적인 디자인을 쉽게 적용할 수 있다는 것을 알게 되었다.