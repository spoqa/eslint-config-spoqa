git-flow를 사용합니다.

## 새 기능 추가하기

- PR은 `develop` 브랜치로 머지해주세요.

## 릴리즈하기

1. `develop` 브랜치에서 `release/0.0.0` 브랜치를 따주세요.
2. 버전 범프 커밋을 추가합니다.
3. `master` 브랜치로 머지해주세요.
4. GitHub에서 릴리즈를 생성해주세요.

   - `yarn publish --access public` 명령으로 npm에 배포해주세요.
   - GitHub에서 "Draft a new release" 버튼을 누르고 Tag version을 입력한 뒤 타겟을 (방금 머지한) master 브랜치로 설정합니다.
     - 태그 버전은 반드시 0.0.0 형식이어야 합니다.
