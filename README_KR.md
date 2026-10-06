# 할인 표시 방식 A/B 테스트 웹사이트 사용 방법

## 1 GitHub Pages에 올리기

1. GitHub에서 `username.github.io` 저장소를 만듭니다.
2. 이 폴더의 `index.html` 파일을 저장소에 업로드합니다.
3. 2~3분 후 `https://username.github.io`에서 페이지를 확인합니다.

## 2 Version 화면 확인

- Version A 통제 조건: `https://username.github.io`
- Version B 디자인 미리보기: `https://username.github.io/?preview=B`

`preview=B`는 디자인 확인용입니다. 실제 실험 링크에는 사용하지 않습니다.

## 3 VWO 추적 코드 설치

1. VWO에서 실험 사이트 도메인을 입력하고 SmartCode를 생성합니다.
2. `index.html`의 `<head>` 안에 표시된 `VWO SmartCode 시작`과 `VWO SmartCode 끝` 사이에 코드를 붙여넣습니다.
3. GitHub에서 변경 사항을 Commit합니다.
4. VWO의 SmartCode 확인 기능으로 설치 상태를 확인합니다.

## 4 VWO 실험 설정

- 실험 유형: A/B Test
- 실험 URL: `https://username.github.io`
- 트래픽 배분: Version A 50%, Version B 50%
- Version A 문구: `2,000원 할인`
- Version B 문구: `10% 할인`
- 변경 대상 CSS 선택자: `#discount-label`
- 목표: 요소 클릭
- 목표 CSS 선택자: `#purchase-button`
- 주요 지표: 고유 방문자 기준 구매 버튼 클릭률

## 5 실험 전 확인

- 시크릿 창에서 페이지가 정상적으로 열리는지 확인합니다.
- 모바일과 PC에서 가격, 할인 문구, 구매 버튼이 잘 보이는지 확인합니다.
- Version B에서는 할인 문구만 바뀌었는지 확인합니다.
- 구매 버튼 클릭 후 감사 안내창이 나타나는지 확인합니다.
- 실제 결제와 개인정보 수집이 없다는 문구가 보이는지 확인합니다.

