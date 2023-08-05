# eslint_cascade\_\_extends

eslint에서 cascade가 어떻게 일어나는지 실험합니다.

## 실험

[A: src안에 있는 것을 root로 삼아, 상위 폴더의 설정을 가져오지 않게 합니다.]

1. src/.eslintrc.cjs의 root설정을 주석해제합니다.
2. src/foo.ts에서 eslint에러가 나지 않는 것을 확인합니다.

[B: src안의 .eslintrc.cjs에서 상위 디렉토리의 설정을 포함하도록 합니다.]

1. src/.eslintrc.cjs의 root설정을 주석처리합니다.
2. src/foo.ts에서 eslint에러가 나는 것을 확인합니다.
