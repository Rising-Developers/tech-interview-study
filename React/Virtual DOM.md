## Virtual DOM이란?

Virtual DOM은 실제 DOM의 가상 표현입니다. Virtual DOM은 React와 같은 라이브러리가 DOM 조작을 효율적으로 하기 위해 사용하는 개념입니다. 컴포넌트의 상태가 변경되면 새로운 Virtual DOM이 생성되고, 이전 Virtual DOM과 비교하여 실제 DOM에서 변경이 필요한 부분만 업데이트합니다. 이를 통해 불필요한 DOM 조작을 줄이고 성능을 최적화할 수 있습니다

## 꼬리질문

### Virtual DOM의 동작 방식에 대해 조금 더 구체적으로 설명해주세요.

Virtual DOM의 동작 방식은 다음과 같습니다:

    1.	상태가 변경되면 새로운 Virtual DOM이 생성됩니다.
    2.	React는 이 새로운 Virtual DOM과 이전 Virtual DOM을 비교합니다.
    3.	두 Virtual DOM의 차이를 계산하여 실제 DOM에서 변경이 필요한 부분만 업데이트합니다.

이 과정에서 효율적인 업데이트를 위해 React는 ’재조정’이라는 과정을 사용합니다. 이로 인해 실제 DOM 조작에 비해 성능이 크게 향상됩니다.
