# eslint-config-spoqa

스포카 내에서 사용되는 자바스크립트 스타일 가이드입니다.

지금은 TypeScript 프로젝트에만 사용할 수 있습니다.

## 사용 방법

### Install

```bash
$ yarn add -D @spoqa/eslint-config-spoqa
```

### Config

`.eslintrc.yaml` 등의 파일을 추가하고 다음 예제처럼 설정을 extends에 추가합니다.

다음 예시는 prettier를 함께 사용하는 next.js 프로젝트의 설정입니다.

```yaml
parserOptions:
  project: tsconfig.json
extends:
  - '@spoqa/eslint-config-spoqa/react'
  - '@spoqa/eslint-config-spoqa/recommended'
  - '@spoqa/eslint-config-spoqa/next'
  - prettier
  - 'prettier/@typescript-eslint'
  - prettier/react
```

## 예시

### Custom import groupingg

```yaml

---
rules:
  import/order:
    - error
    - groups:
        - builtin
        - external
        - internal
        - parent
        - sibling
        - index
      pathGroups:
        - pattern: 'dumb/**'
          group: internal
          position: before
        - pattern: 'components/**'
          group: internal
          position: before
        - pattern: 'public/**'
          group: index
          position: after
      alphabetize:
        order: asc
```

### 절대경로 import 지원

```yaml

---
settings:
  import/resolver:
    node:
      paths:
        - .
```

## 기능 추가 및 릴리즈

[CONTRIBUTING.md](./CONTRIBUTING.md)를 확인해주세요.
