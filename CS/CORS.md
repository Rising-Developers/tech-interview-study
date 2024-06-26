## CORS란 무엇인가요?

- CORS는 다른 도메인에서 리소스를 요청할 때 발생하는 보안 문제를 해결하기 위한 메커니즘입니다.
- 웹 페이지가 자신의 도메인 외부의 도메인에서 자원을 요청할 때, 브라우저가 요청을 허용할지 여부를 결정하는 방법입니다.

## 꼬리질문

### 왜 CORS가 필요한가요?

- 웹 보안 정책 중 하나인 동일 출처 정책(Same-Origin Policy)은 웹 페이지가 다른 도메인의 리소스에 접근하는 것을 제한합니다.
- 동일 출처 정책은 악의적인 사이트가 다른 도메인에서 민감한 데이터를 가져오는 것을 방지합니다.
- 그러나 실제 웹 개발에서는 다른 도메인의 API를 호출하거나, 리소스를 가져와야 할 때가 많습니다. 이때 CORS가 필요합니다.

### CORS 작동 방식

- Preflight Request: 단순한 요청이 아닌 경우, 브라우저는 실제 요청을 보내기 전에 OPTIONS 메서드를 사용하여 사전 요청을 보냅니다.
- Access-Control-Allow-Origin 헤더: 서버는 응답 헤더에 이 헤더를 추가하여 어떤 도메인이 요청을 허용할지 지정합니다.
- Access-Control-Allow-Methods: 서버는 이 헤더를 통해 어떤 HTTP 메서드가 허용되는지 명시합니다.
- CORS는 이렇게 브라우저와 서버 간의 상호작용을 통해 보안을 유지하면서 다른 도메인에 대한 요청을 가능하게 합니다.
