## 타입 annotaion(지정)을 꼭 해줘야 하는경우

### 1. any 타입을 리턴하는 경우
cordinates에 hover해보면 cordinates:any 라고 뜨는 것을 볼 수 있다. JSON.parse는 json을 파싱해준다. 인풋으로 들어가는 json을 확인하면 대충 어떤 타입이 리턴될지 개발자는 예상할 수 있지만, 타입스크립트는 여기까지 지원하지 않는다. 리턴 타입이 일정하지 않으므로 any를 리턴한다고 추론해버린다. 그러므로 이 경우에는 타입 어노테이션(지정)을 해주어야 한다. 

```ts
const json = '{"x": 4", "y": 7}'
const cordinates = JSON.parse(json);
console.log(cordinates)
```

### 2. 변수 선언을 먼저하고 나중에 초기화하는 경우
변수 선언과 동시에 초기화하면 타입을 추론하지만, 선언을 먼저하고 나중에 값을 초기화할 때는 추론하지 못한다.

```ts
let greeting
greeting = 'hello'
```

### 3. 변수에 대입될 값이 일정하지 않은 경우
여러 타입이 지정되어야 할때는 ‘ | ’ 로 여러 타입을 어노테이션 해준다.

```ts
let num = [-7, -2, 10]
let numAboveZero: boolean | number = false

for(let i=0; i < num.length; i++) {
  if(num[i] > 0) {
    numAboveZero = num[i]
  }
}
```