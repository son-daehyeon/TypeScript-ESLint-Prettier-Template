# TypeScript-ESLint-Prettier-Template

> TypeScript + ESLint + Prettier 프로젝트 템플릿

Node.js용 TypeScript 프로젝트를 시작할 때 컴파일·린트·포맷 설정을 매번 새로 잡지 않으려고 만든 템플릿이다. ESLint flat config에 typescript-eslint와 Prettier를 묶어 두었다. 2022년에 만들어 2024년에 의존성과 설정을 갱신했다.

## 주요 기능
- `ts-node`로 바로 실행하고 `tsc`로 `dist/`에 빌드
- ESLint 9 flat config: `@eslint/js`·typescript-eslint 권장 규칙, `no-console` 경고, Prettier 규칙 연동
- Prettier 설정: 작은따옴표, 세미콜론, 들여쓰기 2칸, 줄 길이 100, 후행 쉼표 `all`
- `strict`, `noImplicitReturns`, 데코레이터 메타데이터를 켠 `tsconfig.json`(target ES6, CommonJS)

## 기술 스택
| 영역 | 기술 |
|---|---|
| 언어 | TypeScript 5.5 |
| 도구 | ESLint 9, typescript-eslint 7, Prettier 3, ts-node 10, Yarn |

## 구조
```
src/app.ts             진입점
tsconfig.json          컴파일 설정 (src → dist)
eslint.config.mjs      ESLint flat config
prettier.config.mjs    Prettier 설정
```

## 실행
```bash
yarn install
yarn start          # ts-node src/app.ts
yarn lint           # eslint --fix
yarn format         # prettier --write
yarn build          # tsc
yarn start:prod     # node dist/app.js
```

---
2022 · 개인 프로젝트 · 보관됨
