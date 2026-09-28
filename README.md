# AI 소상공인 홍보 스튜디오

제품 정보와 제품 사진을 입력받아 AI 홍보문구, 포스터, 광고영상 생성 단계로 전달하기 위한 React 입력 화면입니다.

## 실행 방법

프로젝트 폴더에서 다음 명령을 순서대로 실행합니다.

```bash
npm install
npm run dev
```

터미널에 표시되는 주소(기본값 `http://localhost:5173`)를 브라우저에서 열면 됩니다.

## 포함 기능

- 제품명과 제품 설명 입력
- 고객층, 핵심 특징, 홍보 분위기 입력
- 제품 사진 드래그앤드롭 업로드
- JPG, PNG, WebP 및 최대 10MB 검증
- 사진 미리보기 및 삭제
- 모바일 반응형 화면
- 입력 완료 결과 확인
- 백엔드 전송용 `FormData` 변환 함수

## 다음 팀원과 연결하기

현재 `src/App.jsx`는 입력 결과를 화면에 표시하는 데모 동작입니다. 백엔드가 준비되면 `handleProductSubmit` 안에서 아래 함수를 호출합니다.

```jsx
import { submitProductInput } from "./components/productInputPayload";

const result = await submitProductInput(product, "/api/products");
```

서버는 업로드된 이미지를 저장하고 `photoUrl`을 포함한 공통 데이터를 반환하도록 구성합니다.
