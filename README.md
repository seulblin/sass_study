# JSX기본규칙 : 리액트에서 컴포넌트의 생김새를 정의할 때 사용하는 문법.
1. 태그는 꼭 닫아야한다. <div> </div>
<input>이나 <br>처럼 닫는 코드가 없는 경우 셀프클로징태그를 사용한다.
셀프클로징태크는 본인 스스로 열고 닫는 태그로 <input />처럼 슬래쉬를 붙여준다!

2. 2개 이상의 태그는 꼭 하나의 태그로 감싸져 있어야 한다!!
function App() {
  retrun(
    <div> --->Q. 감싸기가 애매한 상황! 꼭 해야만 할까? : NO! 프래그먼트 사용한다.(비어있는 태그) <></>
     <input />                            
     <div>안녕하세요!</div>                 
    </div>
  )--->프로그램의 가독성을 주기위함. 없어도 작동! but있는게 더 깔끔해보임. 1줄로 작성된 것은 없어도 무방.
}

# props(properties) 컴포넌트를 사용하게 될 때 특정 값을 전달 시 사용. --Wrapper.js 참조

# 조건부 렌더링 : 특정 조건이 참(true)인지 거짓(false)인지에 따라 다른 결과를 보여준다. --Counter.js 참조

# 리액트에서 객체를 업데이트 하려면, 기존 것을 복사를 한다. ...(spread 문법)을 사용한다

# useRef 로 컴포넌트 안의 변수 만들기

useRef로 관리 된 것은 바뀌어도 리랜더링 되지 않는다.
1. setTimeout, setInterval의 ID
2. 외부 라이브러리를 사용하여 생성된 인스턴트 Scroll 위치 등 다양하게~

# 배열에 새로운 항목을 추가하는 법
1. 스프레드 연산자를 통해 복사 + 원하는 함수
2. concat함수 사용하기
*** push, splice 등 사용 금지!

# 배열에 있는 항목 삭제하는 법
1. filter 함수 : 배열에서 특정 조건을 만족하는 값들만 따로 추출해 새로운 배열 만듦.

# 배열안에 있는 특정 항목 수정하기
1. 계정 명을 클릭 했을 때 색이 바뀌게 하기!
2. map함수를 통해 구현 가능


# useMemo Hook 사용하기 : 성능 최적화
1. 특정 값이 바뀌었을 때만 특정함수를 통해 실행.
2. 원하는 값이 바뀌지 않으면 리랜더링 할 때 이 전의 값을 재사용한다.