# 박준형 포트폴리오

GitHub Pages로 서비스되는 개인 포트폴리오입니다.

## 배포 방법

1. `ACORN0415.github.io` 이름으로 새 레포지토리 생성
   (다른 이름으로 만들면 `github.com/ACORN0415/<레포명>` 경로로 열립니다)
2. `index.html`을 레포 루트에 올리기
3. Settings → Pages → Source를 `Deploy from a branch`, 브랜치는 `main` / `/(root)`로 지정
4. 1~2분 뒤 `https://ACORN0415.github.io` 에서 확인

## 구조

`index.html` 한 파일입니다. CSS와 JS가 모두 안에 들어 있어 빌드 과정이 없습니다.
수정할 내용은 대부분 HTML 본문에 있고, 색과 여백은 파일 상단 `:root` 변수에서 바꿉니다.

## 128코어 그리드

히어로 오른쪽 격자는 Fibonacci를 컴파일했을 때 실제로 나온 코어 배치입니다.
데이터는 `<script>` 안의 `MAP` 객체에 있습니다. 코어 번호를 키로, 값은
`[레지스터명, C 수준 연산, 하드웨어 명령]` 순서입니다.

FIR 필터 배치로 바꾸려면 `MAP`을 교체하고, 상단 `core-head`의
`fibonacci.c → GPC 1` 표기도 함께 고치면 됩니다.

## 폰트

Pretendard(본문)와 IBM Plex Mono(수치·코드)를 CDN에서 불러옵니다.
오프라인에서 열면 시스템 기본 폰트로 대체됩니다.
