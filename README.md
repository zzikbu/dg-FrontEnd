## 음주미식회
<img alt="header" width="1024" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/header.png?raw=true">
<div align="center">
    <a target="_blank" href="https://apps.apple.com/kr/app/%EC%9D%8C%EC%A3%BC%EB%AF%B8%EC%8B%9D%ED%9A%8C/id6737059933">
        <img alt="appstore" width="180" src="https://github.com/zzikbu/dg-FrontEnd/blob/develop/readme_assets/appstore.png?raw=true">
    </a>
</div>
<br/>

## 목차
- [프로젝트 소개](#프로젝트-소개)
- [팀 구성 및 역할](#팀-구성-및-역할)
- [담당 기능](#%EB%8B%B4%EB%8B%B9-%EA%B8%B0%EB%8A%A5)
- [기술 스택](#%EA%B8%B0%EC%88%A0-%EC%8A%A4%ED%83%9D)
- [담당 기능 실행 화면](#%EB%8B%B4%EB%8B%B9-%EA%B8%B0%EB%8A%A5-%EC%8B%A4%ED%96%89-%ED%99%94%EB%A9%B4)
<br/><br/>

## 프로젝트 소개
AI 기반 주류 추천 및 커뮤니티 서비스

오늘의 기분, 날씨, 먹고싶은 음식에 따라 어울리는 주류를 추천받고, 커뮤니티를 통해 사용자들과 소통할 수 있는 모바일 애플리케이션입니다.
<br/>

### 개발 기간
- 2024.01.22 ~ 2024.10.31 (약 9개월)
<br/><br/>

## 팀 구성 및 역할
iOS 3명, BE 5명, PM 1명, Design 1명
<br/><br/>

## 담당 기능
1. **주류 추천:** 사용자의 기분, 날씨, 먹고싶은 음식을 입력받아 AI를 기반으로 주류 추천

2. **오늘의 조합(주간 베스트조합):** 추천받은 주류를 바탕으로 실제 경험을 공유하고, 댓글을 통해 소통하는 커뮤니티

3. **레시피북:** 안주와 술 관련 레시피를 공유하고, 댓글을 통해 소통하는 커뮤니티

4. **좋아요한 게시물:** 사용자가 관심 있는 게시물을 저장하고 모아볼 수 있는 스크랩 기능

5. **신고/차단:** 스토어 정책에 대응한 부적절한 콘텐츠와 사용자를 필터링하여 건전한 커뮤니티 유지

6. **마이페이지:** 추천받은 주류와 작성한 게시물을 모아보고, 프로필 이미지를 변경할 수 있는 프로필 공간
<br/><br/>

## 기술 스택
- **언어:** `Swift`
- **프레임워크:** `UIkit`
- **아키텍쳐**: `MVC`
- **사용한 패키지:**
  - Auth: `Kakao SDK`
  - HTTP Client: `Alamofire`
  - Util: `Then`, `SnapKit`, `IQKeyboard`
  - UI: `Pageboy`, `Tabman`, `TagListView`, `Toast`
  - Image: `Kingfisher`, `Lottie`
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
