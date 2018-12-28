
# 해피머니 클론 사이트

## 개발환경 소개
```
서비스 개발: Vue Cli3
스타일: HTML, CSS (직접 작성)
배포: AWS S3, Cloudfront
```

## 개발 기간
`2018-12-1 ~ 2018-12-21`

## 환경 세팅
```bash
# 배포 환경
@/assets/js/variable.js 를 API 서버로 수정

# 서버 실행
npm run serve

# 배포 (dist 파일이 생성)
npm run build

# 에러시
node_modules 를 삭제 후
npm install

```

## 이용가능한 서비스
```
1. 회원가입
2. 로그인
3. 마이페이지
4. 해피캐시 충전 (카카오페이, 상품권으로 충전)
5. 상품권 충전 (EMAIL 상품권, SMS 상품권, 카카오페이, 해피캐시 결제)
6. 해피 쇼핑몰 (이용안내, 좋아요)
7. 온라인 사용처 (카테고리, 사용처명 조회, Ordering)
8. 오프라인 사용처 (위와 같음)
9. 이벤트 (카테고리, 페이지네이션, 지난 이벤트, 지난 이벤트 검색)
10. 고객센터 (FAQ, 1:1 문의, 공지사항)
11. 로그아웃
```

## 수정해야할 사항
```
- giftCardBuyInfo
  [x]INPUT 창 재사용
  [x]SMS 상품권 구매 사람 추가할 시 계산되지 않음
  
- joinStore
  [x] 좋아요가 동작이 이상함
  [x] 카테고리, 사용처명, Ordering이 같이 동작하게
  
- FAQ
  [] 카테고리 서치 모든 카테고리 선택시 검색이 되지 않음
  [] 페이지네이션
  
- 1:1 문의
  [] 1:1 문의 내역 보기, 1:1 문의하기 수정
  
- 공지사항
  [] 공지사항 조회순 등록순 CSS
  
- 사이트맵 연결
```
