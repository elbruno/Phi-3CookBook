# VS Code 확장 프로그램에 오신 것을 환영합니다

## 폴더 안에 있는 것들

* 이 폴더에는 확장 프로그램에 필요한 모든 파일이 포함되어 있습니다.
* `package.json` - 확장 프로그램과 명령어를 선언하는 매니페스트 파일입니다.
  * 샘플 플러그인은 명령어를 등록하고 제목과 명령어 이름을 정의합니다. 이 정보로 VS Code는 명령어 팔레트에 명령어를 표시할 수 있습니다. 플러그인을 아직 로드할 필요는 없습니다.
* `src/extension.ts` - 명령어의 구현을 제공할 메인 파일입니다.
  * 이 파일은 하나의 함수 `activate`를 내보내며, 이는 확장 프로그램이 처음 활성화될 때 호출됩니다 (이 경우 명령어를 실행하여). `activate` 함수 내부에서 `registerCommand`를 호출합니다.
  * 명령어의 구현을 포함하는 함수를 두 번째 매개변수로 `registerCommand`에 전달합니다.

## 설정

* 추천 확장 프로그램을 설치하세요 (amodio.tsl-problem-matcher, ms-vscode.extension-test-runner, dbaeumer.vscode-eslint)

## 바로 시작하기

* `F5`를 눌러 확장 프로그램이 로드된 새 창을 엽니다.
* (`Ctrl+Shift+P` 또는 Mac의 경우 `Cmd+Shift+P`)을 눌러 명령어 팔레트에서 명령어를 실행하고 `Hello World`를 입력합니다.
* `src/extension.ts` 내부에 코드를 설정하여 확장 프로그램을 디버그합니다.
* 디버그 콘솔에서 확장 프로그램의 출력을 찾습니다.

## 변경 사항 적용하기

* `src/extension.ts`에서 코드를 변경한 후 디버그 도구 모음에서 확장 프로그램을 다시 시작할 수 있습니다.
* 또한 (`Ctrl+R` 또는 Mac의 경우 `Cmd+R`)을 눌러 확장 프로그램이 있는 VS Code 창을 다시 로드하여 변경 사항을 적용할 수 있습니다.

## API 탐색하기

* 파일 `node_modules/@types/vscode/index.d.ts`을 열면 전체 API 세트를 확인할 수 있습니다.

## 테스트 실행하기

* [Extension Test Runner](https://marketplace.visualstudio.com/items?itemName=ms-vscode.extension-test-runner)를 설치하세요.
* **Tasks: Run Task** 명령어를 통해 "watch" 작업을 실행하세요. 이것이 실행 중인지 확인하세요, 그렇지 않으면 테스트가 발견되지 않을 수 있습니다.
* 활동 표시줄에서 테스트 보기를 열고 "Run Test" 버튼을 클릭하거나 단축키 `Ctrl/Cmd + ; A`을 사용하세요.
* 테스트 결과 보기에서 테스트 결과 출력을 확인하세요.
* `src/test/extension.test.ts`을 변경하거나 `test` 폴더 내에 새로운 테스트 파일을 만드세요.
  * 제공된 테스트 러너는 이름 패턴 `**.test.ts`과 일치하는 파일만 고려합니다.
  * 테스트를 원하는 방식으로 구조화하려면 `test` 폴더 내에 폴더를 생성할 수 있습니다.

## 더 나아가기

* [확장 프로그램 번들링](https://code.visualstudio.com/api/working-with-extensions/bundling-extension)을 통해 확장 프로그램의 크기를 줄이고 시작 시간을 개선하세요.
* VS Code 확장 프로그램 마켓플레이스에 [확장 프로그램을 게시](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)하세요.
* [지속적 통합](https://code.visualstudio.com/api/working-with-extensions/continuous-integration)을 설정하여 빌드를 자동화하세요.

**면책 조항**:
이 문서는 기계 기반 AI 번역 서비스를 사용하여 번역되었습니다. 정확성을 위해 노력하지만 자동 번역에는 오류나 부정확성이 있을 수 있습니다. 원본 문서의 원어를 권위 있는 자료로 간주해야 합니다. 중요한 정보의 경우, 전문 인간 번역을 권장합니다. 이 번역 사용으로 인해 발생하는 오해나 잘못된 해석에 대해 당사는 책임을 지지 않습니다.