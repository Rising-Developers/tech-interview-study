## TypeScript에서 undefined가 뭘까요?

변수가 초기화 없이 선언되면 undefined가 할당됩니다. undefined 자체로는 별로 유용하지 않습니다. undefined와 다르게 null은 변수에 할당되었지만 값이 없음을 나타냅니다.

```ts
console.log(null == null); // true
console.log(undefined == undefined); // true
console.log(null == undefined); // true, with type-conversion
console.log(null === undefined); // false, without type-conversion
console.log(0 == undefined); // false
console.log('' == undefined); // false
console.log(false == undefined); // false
```