# eslint_parserOption_project

Eslint 설정파일에서, parserOptions의 project의 역할에 대해서 테스트합니다.

## 기본사항

- eslint의 일부 규칙은 type information을 요구합니다.
- type information은 type checker을 사용함으로써 획득된다.
- type checker는 program에 있는데, program은 tsconfig.json을 필요로 함.
- eslint는 program을 따로 생성함.
- 따라서 eslint에 tsconfig.json의 위치를 알려줘야한다.

## 실험 진행

| consistent-type-exports 룰이 type information을 필요로한다.

비교함으로써 진행한다.  
[A: type information을 사용하는 rule을 쓰지만, project를 알려주지 않은 경우]

1. .eslintrc.cjs에 project를 주석처리한다.
2. `yarn eslint .`를 실행한다.
3. 에러를 확인한다.

[B: type information을 사용하는 rule을 쓰며, project를 알려주는 경우]

1. .eslintrc.cjs에 project를 주석을 해제한다.
2. `yarn eslint .`를 실행한다.
3. eslint rule 에러를 확인한다.
