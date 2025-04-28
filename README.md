## 음주미식회
<img alt="header" width="1024" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/header.png?raw=true">

## 목차
- [프로젝트 소개](#프로젝트-소개)
- [개발 기간](#개발-기간)
- [팀 구성 및 역할](#팀-구성-및-역할)
- [담당 기능](#담당-기능)
- [기술 스택](#기술-스택)
- [담당 기능 실행 화면](#담당-기능-실행-화면)
<br/><br/>

## 프로젝트 소개
AI 기반 주류 추천 및 커뮤니티 서비스

오늘의 기분 / 날씨 / 먹고 싶은 음식을 기반으로 AI가 주류를 추천해주고, 커뮤니티를 통해 다른 사용자들과 소통할 수 있는 모바일 애플리케이션입니다.
<br/><br/>

## 개발 기간
2024.01.22 ~ 2024.10.31 (약 9개월)
<br/><br/>

## 팀 구성 및 역할
iOS 3명, BE 5명, PM 1명, Design 1명
<br/><br/>

## 담당 기능
1. **주류 추천:** 오늘의 기분 / 날씨 / 먹고 싶은 음식을 기반으로 AI가 주류를 추천

2. **오늘의 조합:** 추천받은 주류를 바탕으로 실제 경험을 공유하는 커뮤니티

3. **레시피북:** 안주와 술 관련 레시피를 공유하는 커뮤니티

4. **좋아요한 게시물:** 관심 있는 게시물을 저장하고 모아보는 스크랩 기능

5. **신고/차단:** 부적절한 게시물이나 사용자를 필터링해 건전한 커뮤니티를 유지하는 기능

6. **마이페이지:** 추천받은 주류와 작성한 게시물을 모아보고, 프로필을 수정할 수 있는 공간
<br/><br/>

## 기술 스택
- **언어:** `Swift`
- **프레임워크:** `UIkit`
- **아키텍쳐**: `MVC`
- **Package:**
  - Auth: `Kakao SDK`
  - HTTP Client: `Alamofire`
  - Media: `Kingfisher`, `Lottie`
  - Util: `Then`, `SnapKit`, `IQKeyboard`
  - UI: `Pageboy`, `Tabman`, `TagListView`, `Toast`
<br/><br/>

## 담당 기능 실행 화면

| 주류추천 입력                                                      | 주류추천 결과                                                      | 오늘의 조합                                                       | 레시피북                                                         |
|:------------------------------------------------------------:|:------------------------------------------------------------:|:------------------------------------------------------------:|:------------------------------------------------------------:|
| <img alt="recommend_input" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/recommend_input.gif?raw=true"> | <img alt="recommend_result" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/recommend_result.gif?raw=true"> | <img alt="combination" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/combination.gif?raw=true"> | <img alt="recipebook" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/recipebook.gif?raw=true"> |
| 게시물 신고/차단                                                    | 댓글 작성/삭제                                                     | 댓글 신고/차단                                                     | 좋아요한 게시물                                                     |
| <img alt="content_report_block" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/content_report_block.gif?raw=true"> | <img alt="comment" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/comment.gif?raw=true"> | <img alt="comment_report_block" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/comment_report_block.gif?raw=true"> | <img alt="like" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/like.gif?raw=true"> |
| 마이페이지                                                        | 프로필 이미지 변경 / 삭제                                              |                                                              |                                                              |
| <img alt="mypage" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/mypage.gif?raw=true"> | <img alt="profile_image" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/gif/profile_image.gif?raw=true"> |                                                              |                                                              |
<br/>

## 트러블슈팅

### ✅ 메모리 효율성 향상을 위한 댓글 UI 구조 개선
**문제상황**
- 댓글 목록이 있는 커뮤니티 상세 페이지에서 UIStackView 기반으로 UI 구현 시 여러 성능 문제 발생
- 모든 댓글 View를 한 번에 메모리에 로드하는 방식으로 인해 댓글이 많아질수록 메모리 사용량 급증
- 페이징 처리 구현이 복잡하고, 스크롤 성능 저하 및 사용자 경험 악화
- 새로운 댓글 추가나 삭제 시 전체 스택뷰 재구성 필요

**해결방안**
- UITableView의 셀 재사용 메커니즘을 활용하여 메모리 사용량을 크게 줄이고 성능을 개선
- UITableViewDataSourcePrefetching 프로토콜을 구현하여 효율적인 무한 스크롤 페이징을 적용
- 게시글 정보를 테이블뷰의 헤더뷰로 분리하여 댓글 목록과 게시글 정보의 관리를 분리
- [PR #100 - Feat: 오늘의 조합 상세보기 테이블뷰로 구현](https://github.com/UMC5th-DrinkingGourmet/dg-FrontEnd/pull/100)
- [PR #102 - Feat: 오늘의 조합 댓글 구현](https://github.com/UMC5th-DrinkingGourmet/dg-FrontEnd/pull/100)
