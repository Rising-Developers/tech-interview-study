## 선택적 속성( optional properties)을 지정하려면 어떻게 해야할까요?

객체 유형은 속성 이름 뒤에 '?'를 추가하여 선택적 속성(optional properties)을 가질 수 있습니다.

```ts
let pt: { x: number; y: number; z?: number } = {
  x: 10,
  y: 20
};
console.log(pt);
```

위의 코드에서 'z' 속성은 선택적 속성(optional properties)으로 표시되어 있으므로 초기화 중에 제공하지 않아도 컴파일 과정에서 문제가 없습니다.