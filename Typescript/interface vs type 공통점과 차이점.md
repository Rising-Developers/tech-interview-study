## interface vs type 공통점과 차이점

### 공통점
- 객체의 형태를 정의할 수 있습니다.
```ts
interface PersonInterface {
  name: string;
  age: number;
}

type PersonType = {
  name: string;
  age: number;
};

```
- 제너릭 사용이 가능합니다.
- 인덱스 시그니처(Index Signature)의 사용이 가능합니다. 
- 함수타입을 정의할 수 있습니다. 
```ts
interface AddInterface {
  (a: number, b: number): number;
}

type AddType = (a: number, b: number) => number;

```
- 클래스 구현(implements)시 사용이 가능합니다.

### 차이점
- 유니온 타입은 타입만 가능합니다.
```ts
type StringOrNumber = string | number;
// interface StringOrNumberInterface {} // 유니온 타입을 정의할 수 없음
```
- 튜플과 배열타입도 타입에서만 가능합니다.
```ts
type Pair = [number, number]
type StringList = string[]
type NamedNums = [string, ...number[]]
```
- 확장 방식: interface는 extends 키워드를 사용하여 확장할 수 있고, type은 교차 타입(&)을 사용하여 결합할 수 있습니다.
```ts
interface Animal {
  name: string;
}

interface Dog extends Animal {
  breed: string;
}

type AnimalType = {
  name: string;
};

type DogType = AnimalType & {
  breed: string;
};

```
- 중복 선언 허용: interface는 중복 선언이 가능하여 자동으로 병합되지만, type은 동일한 이름으로 중복 선언할 수 없습니다.
```ts
interface Mergeable {
  name: string;
}

interface Mergeable {
  age: number;
}

const person: Mergeable = { name: "Alice", age: 30 };

// type MergeableType = { name: string; }  // 오류 발생
// type MergeableType = { age: number; }

```

## 꼬리질문

### 함수에서 타입을 어떻게 지정해줄까요?
함수는 특정 코드를 수행하기 위한 코드 블록입니다. 함수는 선택적으로 하나 이상의 인수를 취하여 처리하고 선택적으로 값을 반환할 수 있습니다.
```ts
function greet(name: string): string {
  return `Hello, ${name}`;
}

let greeting = greet("Anders");
console.log(greeting);  // "Hello, Anders"
```

