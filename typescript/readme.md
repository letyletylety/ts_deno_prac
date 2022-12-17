# 2. 타입스크립트: 3000미터 상공에서 내려다보기

## 2-1 컴파일러

프로그램.

AST = (추상 문법 트리 abstract syntax tree)

- 일반적인 컴파일러의 역할 : 소스코드 → AST → 바이트코드

- 런타임(runtime) 이 하는 일 : 바이트코드를 평가한다.

- Typescript의 경우? 바이트코드 대신 자바스크립트로 변환 ts 소스코드 → AST →
  typechecker → js → js AST → bytecode → runtime 에서 바이트코드 평가

- 엔진 = (컴파일러 + 런타임 + …) V8(nodeJS, chrome, opera),
  spidermonkey(firefox), JSCore(Safari)

## Type System

= typechecker가 프로그램에 타입을 할당할 때 사용하는 규칙 집합

타입은 결국 타입 확인에서만 쓰인다.

- 타입 시스템 기능
  - 정적, 컴파일 타임, 컴파일 타임 에러 검출

## Code Editor Setting

타입 스크립트 시작

```bash
npm init
npm install --save-dev typescript tslint @types/node

tsc --init
tslint --init
```

- tsconfig.json
  - tsc —init
- tslint.json
  - tslint —init

tsc로 컴파일을 하고

nodejs 같은 런타임으로 코드 실행
