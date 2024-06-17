## null의 개념과 TypeScript에서의 사용예시를 설명해주세요.

프로그래밍에서 null 값은 값이 없음을 나타냅니다. null 변수는 어떤 객체도 가리키지(참조하지) 않습니다. 그렇기 때문에 변수의 속성에 액세스하거나 해당 메서드를 호출할 수 없습니다.

TypeScript에서 null 값은 'null' 키워드로 표시됩니다.

```ts
function greet(name: string | null) {
  // 두가지 경우 모두 내부에서 처리해준다.
  if (name === null) {
    console.log("Name is not provided");
  } else {
    console.log("Good morning, " + name.toUpperCase());
  }
}

var foo = null;
greet(foo); // "Name is not provided"

foo = "Anders";
greet(foo);  // "Good morning, ANDERS"
```