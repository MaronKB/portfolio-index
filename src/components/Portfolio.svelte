<script>

import Link from "./Link.svelte";

import Logo from "/src/assets/logo-title-row.png";
import homepage from "/src/assets/homepage-capture.jpg";
import portfolio from "/src/assets/portfolio-capture.jpg";
import human_health from "/src/assets/human-health-capture.jpg";
import hanmat from "/src/assets/hanmat-capture.jpg";
import ccfolia_log_beautifier from "/src/assets/ccfolia-log-beautifier-capture.jpg";
</script>

<section id="portfolio">
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
            <li>Language: JavaScript, TypeScript</li>
            <li>Frontend: React</li>
            <li>Backend: Node.js, Express</li>
            <li>Database: MongoDB, Mongoose</li>
            <li>Build: Webpack</li>
            <li>Auth: OAuth2</li>
            <li>Web Server: Express</li>
            <li>Reverse Proxy: NGINX</li>
        </ul>
        <ul slot="key-features">
            <li>OAuth2를 사용한 구글 소셜 로그인 및 회원가입 기능</li>
            <li>REST API를 사용한 로그 아카이브 기능 및 타 서비스와의 연동</li>
            <li>Webpack을 사용한 번들링 및 최적화</li>
        </ul>
        <ul slot="role">
            <li>프론트엔드 및 백엔드 개발</li>
            <li>디자인 및 퍼블리싱</li>
        </ul>
        <ul slot="development-period">
            <li>2024.01 ~ 2024.06</li>
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
            <li>Backend: Node.js</li>
            <li>Build: Vite</li>
            <li>Web Server & Reverse Proxy: NGINX</li>
        </ul>
        <ul slot="key-features">
            <li>Svelte를 사용한 Single Page Application 구성</li>
        </ul>
        <ul slot="role">
            <li>프론트엔드 및 백엔드 개발</li>
            <li>디자인 및 퍼블리싱</li>
        </ul>
        <ul slot="development-period">
            <li>2025.02 ~ 2025.02</li>
        </ul>
        <ul slot="outcome">
            <li>포트폴리오 정리 페이지 구축</li>
        </ul>
        <ul class="challenges" slot="challenges">

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
            <li>Web Server & Reverse Proxy: NGINX</li>
        </ul>
        <ul slot="key-features">
            <li>HTML, CSS, Javascript, JQuery를 사용한 페이지 구성</li>
            <li>LocalStorage를 이용한 임시 데이터베이스 및 로그인, 유저 정보 저장·수정 기능</li>
            <li>최적 식단 및 운동량 계산 기능</li>
            <li>임시 데이터베이스를 이용한 게시판&이미지 업로드</li>
        </ul>
        <ul slot="role">
            <li>프론트엔드 개발(5인 협력)</li>
            <li>디자인 및 퍼블리싱</li>
        </ul>
        <ul slot="development-period">
            <li>2024.07 ~ 2024.08</li>
        </ul>
        <ul slot="outcome">
            <li>휴먼교육센터 개발자 양성 과정 조별 성취도 평가 1위</li>
        </ul>
        <ul class="challenges" slot="challenges">
            <li>-</li>
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
            <li>React</li>
            <li>Java</li>
            <li>Spring Boot</li>
            <li>Gradle</li>
            <li>Oracle</li>
            <li>MongoDB</li>
            <li>JPA</li>
            <li>Nginx</li>
            <li>Express</li>
        </ul>
        <ul slot="key-features">
            <li>React와 Spring Boot를 사용한 페이지 구성</li>
        </ul>
        <ul slot="role">
            <li>프론트엔드 및 백엔드 개발</li>
            <li>디자인 및 퍼블리싱</li>
        </ul>
        <ul slot="development-period">
            <li>2023.08 ~ 2023.09</li>
        </ul>
        <ul slot="outcome">
            <li>외국인을 대상으로 한 한식 맛집 추천 서비스 구축</li>
        </ul>
        <ul class="challenges" slot="challenges">
            <li>React와 Spring Boot를 사용한 페이지 구성</li>
        </ul>
    </Link>
    <Link
            title="CCFOLIA Log Beautifier"
            image={ccfolia_log_beautifier}
            address="mrkb.kr/ccfolia-log-beautifier"
            link="https://mrkb.kr/ccfolia-log-beautifier"
            source=""
            tags={["Javascript", "TypeScript", "React", "Nginx"]}
            summary="TRPG VTT인 COCOFOLIA에서 출력한 로그를 보기 좋게 꾸며주는 서비스입니다."
    >
        <ul slot="tech-stack">
            <li>React</li>
            <li>Nginx</li>
        </ul>
        <ul slot="key-features">
            <li>React를 사용한 페이지 구성</li>
        </ul>
        <ul slot="role">
            <li>프론트엔드 개발</li>
            <li>디자인 및 퍼블리싱</li>
        </ul>
        <ul slot="development-period">
            <li>2023.07 ~ 2023.07</li>
        </ul>
        <ul slot="outcome">
            <li>TRPG VTT인 COCOFOLIA에서 출력한 로그를 보기 좋게 꾸며주는 서비스 구축</li>
        </ul>
        <ul class="challenges" slot="challenges">
            <li>React를 사용한 페이지 구성</li>
        </ul>
    </Link>

</section>

<style>
    #portfolio {
        max-width: 900px;
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(240px, 1fr));
        grid-template-rows: repeat(auto-fill, minmax(320px, 1fr));
        gap: 20px;
        padding: 20px;
        margin: 0 auto;
    }
    ul {
        display: flex;
        flex-direction: column;
        gap: 5px;
        list-style: none;
        padding: 0;
        margin: 0;
    }
    ul li {
        font-size: 14px;
    }
    ul li::before {
        content: "•";
        margin-right: 5px;
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
</style>