<script>

import Link from "./Link.svelte";

import homepage from "/src/assets/homepage-capture.jpg";
import portfolio from "/src/assets/portfolio-capture.jpg";
import ellixspace from "/src/assets/ellixspace-capture.jpg";
import human_health from "/src/assets/human-health-capture.jpg";
import ojakgyo from "/src/assets/ojakgyo-capture.jpg";
import hanmat from "/src/assets/hanmat-capture.jpg";
import ccfolia_log_beautifier from "/src/assets/ccfolia-log-beautifier-capture.jpg";
import mrkb_ui from "/src/assets/mrkb-ui-capture.jpg";
</script>

<section id="portfolio">
    <h2>Projects</h2>
    <div class="container">
        <h3>WebPage</h3>
        <Link
                title="Homepage"
                image={homepage}
                address="mrkb.kr"
                link="https://mrkb.kr"
                source="https://github.com/MaronKB/react-site"
                tags={["Javascript", "React", "Node.js", "Express", "OAuth2", "REST API", "MongoDB", "Mongoose", "Webpack"]}
                summary="개인 홈페이지입니다."
        >
            <ul slot="tech-stack">
                <li>Language: JavaScript</li>
                <li>Frontend: React</li>
                <li>Backend: Node.js, Express</li>
                <li>Build: Webpack</li>
                <li>Database: MongoDB, Mongoose</li>
                <li>Build: Webpack</li>
                <li>Auth: OAuth2</li>
                <li>Version Control: Git</li>
                <li>Source Code Management: Github</li>
                <li>Web Server: Express</li>
                <li>Reverse Proxy: NGINX</li>
            </ul>
            <ul slot="key-features">
                <li>OAuth2를 사용한 구글 소셜 로그인 및 회원가입 기능</li>
                <li>REST API를 사용한 로그 아카이브 기능 및 타 서비스와의 연동</li>
                <li>Webpack을 사용한 번들링 및 최적화</li>
            </ul>
            <ul slot="role">
                <li>프로젝트 인원 : 1인</li>
                <li>기획 및 설계 (전 분야)</li>
                <li>프론트엔드 및 백엔드 개발 (모든 기능)</li>
                <li>디자인 및 퍼블리싱</li>
            </ul>
            <ul slot="development-period">
                <li>2024.01 ~ 2024.06 (6개월)</li>
            </ul>
            <ul slot="outcome">
                <li>개인 홈페이지 구축</li>
            </ul>
            <ul class="challenges" slot="challenges">
                <li>컴포넌트 위주 개발에 낯섬과 어려움을 느낌</li>
                <li>다양한 라이브러리에 따라 사고방식을 전환할 수 있는 하이브리드 개발자적 관념 정착</li>
                <li>브라우저와 OS의 차이에 따른 최적화 및 기능 작동 오류 문제</li>
                <li>브라우저 호환성에 대한 심도 깊은 조사와 단위별 테스트를 통한 기능 확인·최적화</li>
                <li>React 버전과 모듈 종속성의 차이로 인한 지속적 오류 발생</li>
                <li>프로젝트 재생성 단계에서 필요 모듈을 체크하고 테스트해보는 과정을 거침 + 호환성 이슈가 있는 모듈의 기능은 스니펫으로 직접 작성해서 보완</li>
                <li>다른 서비스와의 연동 과정에서 CORS 정책 오류</li>
                <li>서버와 클라이언트 간의 통신을 위한 CORS 정책 설정 + 백엔드 통신으로 처리해서 우회 + SSL 인증서 발급을 통한 HTTPS 통신 활성화</li>
            </ul>
        </Link>
        <Link
                title="Portfolio"
                image={portfolio}
                address="portfolio.mrkb.kr"
                link="https://portfolio.mrkb.kr"
                source="https://github.com/MaronKB/portfolio-index"
                tags={["Javascript", "TypeScript", "Svelte"]}
                summary="포트폴리오 정리 페이지입니다."
        >
            <ul slot="tech-stack">
                <li>Language: JavaScript, TypeScript</li>
                <li>Frontend: Svelte</li>
                <li>Build: Vite</li>
                <li>Version Control: Git</li>
                <li>Source Code Management: Github</li>
                <li>Web Server & Reverse Proxy: NGINX</li>
            </ul>
            <ul slot="key-features">
                <li>Svelte를 사용한 Single Page Application 구성</li>
            </ul>
            <ul slot="role">
                <li>프로젝트 인원 : 1인</li>
                <li>기획 및 설계 (전 분야)</li>
                <li>프론트엔드 개발 (모든 기능)</li>
                <li>디자인 및 퍼블리싱</li>
            </ul>
            <ul slot="development-period">
                <li>2025.02 ~ 2025.02 (2주)</li>
            </ul>
            <ul slot="outcome">
                <li>지속 및 유지 가능한 포트폴리오 정리 페이지 구축</li>
            </ul>
            <ul class="challenges" slot="challenges">
                <li>프레임워크의 특성에 대한 이해 부족으로 인한 개발 속도 저하</li>
                <li>공식 문서와 예제 코드를 통한 학습 및 실습을 통한 이해</li>
                <li>취업 준비를 위해 요구되는 짧은 개발 기간과 성능 간의 조절 문제</li>
                <li>프로젝트 초기에 미리 구상한 디자인과 기능 구현을 통한 개발 속도 향상</li>
            </ul>
        </Link>
        <Link
                title="Ellixspace"
                image={ellixspace}
                address="ellixspace.com"
                link="https://ellixspace.com"
                source="#"
                tags={["Javascript", "React", "Apache"]}
                summary="외주로 진행한 개인 웹사이트입니다."
        >
            <ul slot="tech-stack">
                <li>Language: JavaScript</li>
                <li>Frontend: React</li>
                <li>Backend: None</li>
                <li>Version Control: Git</li>
                <li>Source Code Management: Github</li>
                <li>Web Server & Reverse Proxy: Apache</li>
            </ul>
            <ul slot="key-features">
                <li>React를 사용한 페이지 구성</li>
                <li>JSON을 사용한 간단 포트폴리오 업로드 기능</li>
                <li>메일서버 연동을 통한 연락 폼 전송</li>
            </ul>
            <ul slot="role">
                <li>프로젝트 인원 : 1인</li>
                <li>기획 및 설계 (전 분야)</li>
                <li>프론트엔드 개발 (모든 기능)</li>
                <li>퍼블리싱</li>
            </ul>
            <ul slot="development-period">
                <li>2023.08 ~ 2023.09 (3주)</li>
            </ul>
            <ul slot="outcome">
                <li>외주 프로젝트 완료</li>
            </ul>
            <ul class="challenges" slot="challenges">
                <li>개발 도중에 발견된 문제점으로 일부 기획의 수정 필요사항 발생</li>
                <li>발주자와의 재논의를 통한 수정사항 반영, 수정요구와 일정 재조정 경험</li>
            </ul>
        </Link>
        <Link
                title="Human Health"
                image={human_health}
                address="portfolio.mrkb.kr/human-health"
                link="https://portfolio.mrkb.kr/human-health"
                source="https://github.com/MaronKB/human_health"
                tags={["HTML", "CSS", "Javascript", "JQuery"]}
                summary="건강 관리 서비스입니다."
        >
            <ul slot="tech-stack">
                <li>Language: Vanilla JavaScript</li>
                <li>Frontend: HTML, CSS, Jquery</li>
                <li>Backend: None</li>
                <li>Version Control: Git</li>
                <li>Collaboration: Notion</li>
                <li>Communication: Discord</li>
                <li>Design: Figma</li>
                <li>Documentation: Markdown</li>
                <li>Source Code Management: Github</li>
                <li>Code Review: Github</li>
                <li>Web Server & Reverse Proxy: NGINX</li>
            </ul>
            <ul slot="key-features">
                <li>HTML, CSS, Javascript, JQuery를 사용한 페이지 구성</li>
                <li>LocalStorage를 이용한 임시 데이터베이스 및 로그인, 유저 정보 저장·수정 기능</li>
                <li>최적 식단 및 운동량 계산 기능</li>
                <li>임시 데이터베이스를 이용한 게시판&이미지 업로드</li>
            </ul>
            <ul slot="role">
                <li>프로젝트 인원: 5인</li>
                <li>적정 운동/식사 칼로리 계산 API(100%)</li>
                <li>프론트엔드(50%) 개발</li>
                <li><ul class="sub-role">
                    <li>랜딩 페이지(100%)</li>
                    <li>유저 페이지 + 기능(100%)</li>
                    <li>로그인 및 회원가입 페이지 + 기능(80%)</li>
                    <li>활동 및 식단 페이지 모달 + 기능(70%)</li>
                    <li>사이트 테마 및 디자인(70%)</li>
                </ul></li>
                <li>퍼블리싱</li>
            </ul>
            <ul slot="development-period">
                <li>2024.07 ~ 2024.08 (4주)</li>
            </ul>
            <ul slot="outcome">
                <li>휴먼교육센터 개발자 양성 과정 조별 성취도 평가 1위</li>
            </ul>
            <ul class="challenges" slot="challenges">
                <li>팀원 개개인의 제반지식 부족으로 인한 프로젝트 진행성 저하</li>
                <li>프로젝트 진행 과정에서 직접 기술 자문 역할 수행, 모든 개발 과정에 개입하면서 WBS 관리</li>
                <li>소규모 프로젝트에서 5인이라는 과한 수의 프론트엔드 개발자의 존재로 인한 개발 일관성 부족 및 방향성 충돌</li>
                <li>공용 가이드라인 및 스니펫 코드 작성, CSS 클래스 통일에 의한 통일성 유지</li>
            </ul>
        </Link>
        <Link
                title="Ojakgyo"
                image={ojakgyo}
                address="github.com/MaronKB/ojakgyo"
                link="https://github.com/MaronKB/ojakgyo"
                source="https://github.com/MaronKB/ojakgyo"
                tags={["Javascript", "Java", "Spring Boot", "JSP", "Gradle", "Oracle", "Mybatis"]}
                summary="장거리 연애 커플을 위한 데이트 코스 추천 서비스입니다."
        >
            <ul slot="tech-stack">
                <li>Language: JavaScript, Java</li>
                <li>Frontend: JSP</li>
                <li>Backend: Spring Boot</li>
                <li>Database: Oracle</li>
                <li>ORM: Mybatis</li>
                <li>Build: Gradle</li>
                <li>Version Control: Git</li>
                <li>Collaboration: Notion</li>
                <li>Communication: Discord</li>
                <li>Design: Figma</li>
                <li>Documentation: Markdown</li>
                <li>Source Code Management: Github</li>
                <li>Code Review: Github</li>
            </ul>
            <ul slot="key-features">
                <li>Spring Boot를 사용한 페이지 구성</li>
                <li>TMap Reverse Geocoding, 주소기반산업서비스 API 등을 이용한 지도상 최적 만남 지점 산출 기능</li>
                <li>TMap API를 사용한 지역 기반 주변 관광지, 식당, 숙소 선정 기능</li>
                <li>Oracle Database를 사용한 데이터 저장 및 검색 기능</li>
                <li>Mybatis를 사용한 데이터베이스 연동</li>
                <li>Gradle을 사용한 빌드 및 배포</li>
            </ul>
            <ul slot="role">
                <li>프로젝트 인원: 5인</li>
                <li>프론드엔드(70%) 개발</li>
                <li><ul class="sub-role">
                    <li>랜딩 페이지(100%)</li>
                    <li>장소 찾기 페이지 + 기능(100%)</li>
                    <li>지도 API(100%)</li>
                    <li>길찾기 기능 및 API(100%)</li>
                    <li>커뮤니티 디자인 및 기능(60%)</li>
                    <li>마이페이지 + 기능(80%)</li>
                    <li>백엔드 연결(90%)</li>
                </ul></li>
                <li>백엔드(70%) 개발</li>
                <li><ul class="sub-role">
                    <li>클래스 설계(100%)</li>
                    <li>외부 API 연동(100%)</li>
                    <li>로그인 및 회원가입 API(100%)</li>
                    <li>DB 구조 설계 및 구현(100%)</li>
                    <li>보안 및 인증(100%)</li>
                </ul></li>
            </ul>
            <ul slot="development-period">
                <li>2024.09 ~ 2024.10 (4주)</li>
            </ul>
            <ul slot="outcome">
                <li>휴먼교육센터 개발자 양성 과정 조별 성취도 평가 1위</li>
            </ul>
            <ul class="challenges" slot="challenges">
                <li>요구 스펙 제한으로 인한 기능 구현 불가</li>
                <li>대대적인 코드 리팩토링에 의한 우회 구현, 일부 기술 스택 타협</li>
                <li>만남 지점이 도심지나 관광지가 아닌 지역을 가리키는 문제</li>
                <li>시청/군청/역/터미널 등의 시내 랜드마크를 중심으로 만남 지점을 검색하도록 개선</li>
            </ul>
        </Link>
        <Link
                title="HanMat"
                image={hanmat}
                address="portfolio.mrkb.kr/hanmat"
                link="https://portfolio.mrkb.kr/hanmat"
                source="https://github.com/MaronKB/hanmat"
                tags={["Javascript", "TypeScript", "React", "Java", "Spring Boot", "Gradle", "Oracle", "MongoDB", "JPA", "Nginx", "Express"]}
                summary="외국인을 대상으로 한 한식 맛집 추천 서비스입니다."
        >
            <ul slot="tech-stack">
                <li>Language: JS, TS, Java</li>
                <li>Frontend: React</li>
                <li>Backend: Java, Spring Boot</li>
                <li>Database: Oracle, MongoDB, H2</li>
                <li>ORM: JPA</li>
                <li>Build: Gradle</li>
                <li>Version Control: Git</li>
                <li>Collaboration: Notion</li>
                <li>Communication: Discord</li>
                <li>Design: Figma</li>
                <li>Documentation: Markdown</li>
                <li>Source Code Management: Github</li>
                <li>Code Review: Github</li>
                <li>Security: JWT</li>
                <li>API Gateway: Nginx</li>
                <li>Load Balancer: Nginx</li>
                <li>Web Server: Express</li>
            </ul>
            <ul slot="key-features">
                <li>React와 Spring Boot를 사용한 페이지 구성</li>
                <li>JWT Token을 이용한 회원가입 및 로그인 기능</li>
                <li>위치 정보 기반 한식 맛집 리스팅</li>
                <li>사용자 리뷰 작성 및 게시팡 열람 기능</li>
                <li>JPA Database 검색 알고리즘을 통한 맛집 검색 최적화</li>
                <li>Websocket을 통한 사용자간 채팅 기능</li>
                <li>북마크, 리뷰 평가 등을 통한 데이터 사용자화</li>
                <li>i18n을 통한 한국어, 영어, 일본어 로컬라이징</li>
                <li>네이버 지도, TMap Reverse Geocoding, 주소기반산업서비스 API 등을 이용한 지도상 맛집 표시 서비스</li>
            </ul>
            <ul slot="role">
                <li>프로젝트 인원 : 5인</li>
                <li>프론트엔드(60%)개발</li>
                <li><ul class="sub-role">
                    <li>헤더 + 푸터 + 기능(100%)</li>
                    <li>다크모드(100%)</li>
                    <li>로컬라이징 기능 및 번역(100%)</li>
                    <li>랜딩 페이지(100%)</li>
                    <li>맛집 찾기 페이지 + 기능(100%)</li>
                    <li>네이버 지도 + 지오코딩 API(100%)</li>
                    <li>소셜 로그인 기능(100%)</li>
                    <li>맛집 상세 모달(100%)</li>
                    <li>마이페이지 + 기능(100%)</li>
                    <li>리뷰 작성 및 열람 페이지 + 기능(50%)</li>
                    <li>친구 페이지 + 채팅 기능(100%)</li>
                    <li>백엔드 연결(80%)</li>
                </ul></li>
                <li>백엔드(80%) 개발</li>
                <li><ul class="sub-role">
                    <li>클래스 설계(100%)</li>
                    <li>유저, 맛집, 리뷰 API 설계 및 구현(80%)</li>
                    <li>DB 구조 설계 및 구현(100%)</li>
                    <li>보안 및 인증(100%)</li>
                    <li>채팅 API(100%)</li>
                </ul></li>
                <li>디자인 및 퍼블리싱</li>
            </ul>
            <ul slot="development-period">
                <li>2024.12 ~ 2025.01 (4주)</li>
            </ul>
            <ul slot="outcome">
                <li>휴먼교육센터 개발자 양성 과정 조별 성취도 최종 평가 1위</li>
            </ul>
            <ul class="challenges" slot="challenges">
                <li>팀원 개개인의 숙련도 문제로 인한 개발 기한 준수 위기</li>
                <li>프로젝트 진행 과정에서 직접 기술 자문 역할 수행, 모든 개발 과정에 개입하면서 WBS 관리</li>
                <li>데이터베이스에 저장된 음식점 좌표계와 네이버 지도 API의 좌표계 불일치 문제</li>
                <li>좌표계 변환 알고리즘 개발, 실사용을 통한 데이터베이스 Bulk edit으로 데이터 일치화</li>
            </ul>
        </Link>
    </div>
    <div class="container">
        <h3>WebApp</h3>
        <Link
                title="CCFOLIA Log Beautifier"
                image={ccfolia_log_beautifier}
                address="mrkb.kr/ccfolia-log-beautifier"
                link="https://mrkb.kr/ccfolia-log-beautifier"
                source="https://github.com/MaronKB/ccfolia-log-beautifier"
                tags={["Javascript", "TypeScript", "React", "Nginx"]}
                summary="TRPG VTT인 COCOFOLIA에서 출력한 로그를 보기 좋게 꾸며주는 서비스입니다."
        >
            <ul slot="tech-stack">
                <li>Language: JavaScript, TypeScript</li>
                <li>Frontend: React</li>
                <li>Build: Vite</li>
                <li>Version Control: Git</li>
                <li>Documentation: Markdown</li>
                <li>Source Code Management: Github</li>
                <li>Web Server & Reverse Proxy: NGINX</li>
            </ul>
            <ul slot="key-features">
                <li>React를 사용한 페이지 구성</li>
            </ul>
            <ul slot="role">
                <li>프로젝트 인원 : 1인</li>
                <li>기획 및 설계 (전 분야)</li>
                <li>프론트엔드 개발 (모든 기능)</li>
                <li>디자인 및 퍼블리싱</li>
            </ul>
            <ul slot="development-period">
                <li>2025.03 ~ 2025.03 (2주)</li>
            </ul>
            <ul slot="outcome">
                <li>일일 평균 이용자 수 10명 이상</li>
            </ul>
            <ul class="challenges" slot="challenges">
                <li>React 생명주기와 백엔드 부재에 의한 잦은 상태 휘발</li>
                <li>React Hook을 사용한 상태 관리 및 컴포넌트 재사용성을 통한 해결</li>
            </ul>
        </Link>
        <Link
                title="MRKB UI"
                image={mrkb_ui}
                address="foundryvtt.com/packages/mrkb-ui"
                link="https://foundryvtt.com/packages/mrkb-ui"
                source="https://github.com/MaronKB/mrkb-ui"
                tags={["Javascript", "Node.js", "Handlebars.js"]}
                summary="TRPG VTT인 FoundryVTT에서 사용할 수 있는 UI 모듈입니다."
        >
            <ul slot="tech-stack">
                <li>Language: JavaScript</li>
                <li>Frontend: Handlebars.js</li>
                <li>Backend: Node.js</li>
                <li>Version Control: Git</li>
                <li>Documentation: Markdown</li>
                <li>Source Code Management: Github</li>
            </ul>
            <ul slot="key-features">
                <li>FVTT API를 이용한 채팅 전처리 및 후처리 기능</li>
                <li>Webhook을 사용한 클라이언트-서버 간 동기화</li>
                <li>로컬 데이터 조작 편의성 개선</li>
                <li>미형 디자인</li>
            </ul>
            <ul slot="role">
                <li>프로젝트 인원 : 1인</li>
                <li>기획 및 설계 (전 분야)</li>
                <li>프론트엔드 및 백엔드 개발 (모든 기능)</li>
                <li>디자인</li>
            </ul>
            <ul slot="development-period">
                <li>2024.03 ~ (유지보수 중)</li>
            </ul>
            <ul slot="outcome">
                <li>Foundry VTT 공식 홈페이지 등재</li>
            </ul>
            <ul class="challenges" slot="challenges">
                <li>의존하는 프레임워크 도큐멘테이션의 열악함</li>
                <li>반복적인 테스트와 코드 분석으로 원하는 기능 추출을 통해 해결</li>
                <li>잦은 업데이트로 인한 지속적인 호환성 문제</li>
                <li>업데이트 시퀸스 설계와 자동화로 부담 완화</li>
            </ul>
        </Link>
    </div>
</section>

<style>
    .container {
        position: relative;
        max-width: 900px;
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
        grid-template-rows: repeat(auto-fill, minmax(320px, 1fr));
        gap: 10px;
        margin: 0 auto;
    }
    @media (max-width: 900px) {
        .container {
            grid-template-columns: 1fr;
        }
    }
    .container h3 {
        position: absolute;
        top: 0;
        left: 0;
        transform: translate(-20px, -30px) rotate(-4deg);
        flex: none;
        width: 200px;
        height: 40px;
        display: flex;
        justify-content: center;
        align-items: center;
        font-family: var(--font-handwrite), sans-serif;
        font-size: 24px;
        font-weight: var(--font-weight-regular);
        color: var(--background-color);
        background: var(--text-color);
        margin: 0 auto 0 0;
        pointer-events: none;
    }
    ul {
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 5px;
        list-style: none;
        padding: 0;
        margin: 0;
    }
    ul li {
        width: 100%;
        font-size: 14px;
    }
    ul li::before {
        content: "•";
        margin-right: 5px;
    }
    ul li:has(ul)::before {
        display: none;
    }
    ul.sub-role {
        color: var(--text-color-3);
        margin: 0 0 5px 15px;
    }
    ul.challenges li:nth-child(2n-1) {
        color: var(--text-color-3);
    }
    ul.challenges li:nth-child(2n) {
        font-weight: bold;
        color: var(--text-color-1);
        margin: 0 0 5px 0;
    }
    ul.challenges li:nth-child(2n-1)::before {
        content: "•";
    }
    ul.challenges li:nth-child(2n)::before {
        content: "→";
    }
    @media print {
        .container {
            max-width: unset;
            display: flex;
            flex-direction: column;
            gap: 0;
        }
        .container h3 {
            display: none;
        }
        ul[slot="tech-stack"]:has(li:nth-of-type(5)),
        ul.sub-role  {
            width: 100%;
            display: grid;
            grid-template-columns: repeat(3, 1fr);
        }
        ul[slot="key-features"]:has(li:nth-of-type(5)) {
            width: 100%;
            display: grid;
            grid-template-columns: repeat(2, 1fr);
        }
    }
</style>