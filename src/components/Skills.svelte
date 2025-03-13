<script lang="ts">
import Skill from "./Skill.svelte";

import java from "../assets/java.png";
import javascript from "../assets/javascript.png";
import typescript from "../assets/typescript.png";
import csharp from "../assets/c-sharp.png";
import sql from "../assets/sql.png";
import html from "../assets/html.png";
import bash from "../assets/bash.png";

import react from "../assets/react.png";
import jquery from "../assets/jquery.webp";
import svelte from "../assets/svelte.png";
import wordpress from "../assets/wordpress.png";
import jsp from "../assets/jsp.png";

import spring from "../assets/spring.png";
import nodejs from "../assets/nodejs.png";
import express from "../assets/express.png";
import mybatis from "../assets/mybatis.png";

import oracle from "../assets/oracle.webp";
import mongodb from "../assets/mongodb.svg";

import git from "../assets/git.png";
import vite from "../assets/vite.png";
import jwt from "../assets/jwt.svg";
import docker from "../assets/docker.png";
import ubuntu from "../assets/ubuntu.png";
import intellij from "../assets/intellij.png";
import nginx from "../assets/nginx.svg";

import lang from "../assets/lang.jpg";
import programming from "../assets/programming.jpg";
import server from "../assets/server.jpg";
import database from "../assets/database.jpg";
import tools from "../assets/tools.jpg";
</script>

<section id="skills">
    <div class="container">
        <h3>Languages</h3>
        <Skill
                name="Java"
                image={java}
                percentage="70"
                list={["SE JDK 11, 17, 21, 23 사용 경험 있음", "객체 지향 프로그래밍과 절차 지향 프로그래밍 간 차이점과 그 장단점을 인식하고, 언어의 목적에 부합하는 구조로 패키지를 작성할 수 있음", "버전 11 - 23 간 차이점을 이해하고, 버전별 기능 및 문법에 맞게 코드를 작성할 수 있음"]}
        />
        <Skill
                name="Javascript"
                image={javascript}
                percentage="80"
                list={["ES6 이상 문법을 사용하여 코드를 작성할 수 있음", "CommonJS와 ES6 문법 양 쪽에 충분한 이해도를 가지고, 성능, 코드 작성 간의 효율성, 배포 환경 등을 고려하여 다양한 문법을 취사선택할 수 있음", "클래스 단위 프로그래밍에 익숙하고, 함수 지향적 프로그래밍과 스니펫 코드 작성 및 활용에 효율적"]}
        />
        <Skill
                name="Typescript"
                image={typescript}
                percentage="90"
                list={["동적 타입과 정적 타입의 장단점을 파악하고 타입스크립트를 사용해야 하는 이유를 충분히 이해하고 있음", "인터페이스, 타입 지정, 상속 등을 효율적으로 이용하여 코드 길이를 줄이는 데에 특화됨"]}
        />
        <Skill
                name="C#"
                image={csharp}
                percentage="60"
                list={["인스턴스 개념을 이해하고 싱글톤 패턴을 사용하여 최적의 메모리를 사용하도록 코드를 작성할 수 있음", "Unity 엔진을 이용한 애플리케이션 개발 가능"]}
        />
        <Skill
                name="SQL"
                image={sql}
                percentage="70"
                list={["Oracle, MySQL 간 문법 차이를 이해하고 쿼리문을 작성할 수 있음", "동적 쿼리문을 사용한 데이터베이스 입출력 자동화 프로세스에 특화"]}
        />
        <Skill
                name="HTML5, CSS3"
                image={html}
                percentage="80"
                list={["웹 디자인 및 퍼블리싱 가능", "미디어 쿼리를 사용한 반응형 페이지 작성에 능통함"]}
        />
        <Skill
                name="Bash, PowerShell, Linux Shell"
                image={bash}
                percentage="70"
                list={["GUI가 없는 서버 전용 OS를 능숙하게 사용할 수 있음", "클라우드 서버를 사용한 애플리케이션 배포 환경 구성이 자유로움", "쉘 스크립트를 사용한 자동화 프로세스 구축 가능"]}
        />
    </div>
    <div class="container">
        <h3>Frontend Frameworks</h3>
        <Skill
                name="React"
                image={react}
                percentage="80"
                list={["React Hooks, Context API, Redux 등을 사용한 상태 관리에 능통함", "React Router를 사용한 SPA(Single Page Application) 구축 가능", "함수형, 클래스형 컴포넌트 양쪽을 자유롭게 사용할 수 있고, 모듈형 개발과 관련 패키지에 대한 지식이 높음", "상태 관리와 React Hook을 통한 동적 페이지 렌더링에 특화", "Webpack과 ESLint를 사용한 코드 관리 및 최적화 중요시"]}
        />
        <Skill
                name="JQuery"
                image={jquery}
                percentage="70"
                list={["ES6 이후의 VanillaJS에 탑재된 기능과 비교하여 적재적소에 올바르게 사용할 수 있음", "기본 Javascript 문법과 혼용하여 필요한 기능을 취사선택 가능", "Ajax를 사용한 비동기 통신에 능통함"]}
        />
        <Skill
                name="Svelte"
                image={svelte}
                percentage="60"
                list={["Svelte의 장점과 단점을 이해하고, React, Vue와의 차이점을 파악하여 적재적소에 사용할 수 있음", "Svelte의 컴포넌트 기반 개발 방식을 이해하고, Svelte의 라이프사이클을 활용하여 코드를 작성할 수 있음", "Svelte의 Store를 사용한 상태 관리에 능통함"]}
        />
        <Skill
                name="Wordpress"
                image={wordpress}
                percentage="70"
                list={["Wordpress의 테마 및 플러그인 개발 가능", "Wordpress의 기본 기능을 활용하여 웹사이트 구축 가능", "운영 측면에서 개발 관련 지식 없이 유지 보수가 가능한 관리 프로세스를 설계하고 구현할 수 있음"]}
        />
        <Skill
                name="JSP"
                image={jsp}
                percentage="60"
                list={["JSP의 기본 문법을 이해하고, JSP를 사용한 웹 애플리케이션 개발 가능", "JSTL을 사용한 JSP 페이지 구성 가능", "EL(Expression Language)을 사용한 데이터 바인딩 가능"]}
        />
    </div>
    <div class="container">
        <h3>Backend Frameworks</h3>
        <Skill
                name="Spring"
                image={spring}
                percentage="80"
                list={["Spring MVC 모델을 포함한 여러 디자인 패턴 간의 차이점을 인식하고 서비스에 적합한 종류를 선택할 수 있음", "Spring Boot를 사용한 REST API 구축 가능", "Spring Security를 사용한 인증 및 권한 관리 가능", "Spring Data JPA를 사용한 데이터베이스 입출력 자동화 가능"]}
        />
        <Skill
                name="Node.js"
                image={nodejs}
                percentage="80"
                list={["NPM을 사용한 패키지 관리 가능", "이미지 처리, 웹 애플리케이션 등을 개발하고 바이너리화하여 배포할 수 있음"]}
        />
        <Skill
                name="Express"
                image={express}
                percentage="70"
                list={["Express Generator를 사용한 프로젝트 구성 및 관리 가능", "WebSocket과 데이터베이스 입출력, REST API 등 백엔드 서버에 필요한 기능과, 프록싱, 정적 파일 호스팅, 파일 업로드/다운로드 등 웹서버에 필요한 기능 모두 운용 가능", "Middleware를 사용한 요청 처리 가능"]}
        />
        <Skill
                name="MyBatis"
                image={mybatis}
                percentage="60"
                list={["MyBatis의 Mapper와 SQL, 동적 쿼리문을 사용한 데이터베이스 입출력 자동화 가능"]}
        />
    </div>
    <div class="container">
        <h3>Databases</h3>
        <Skill
                name="Oracle"
                image={oracle}
                percentage="70"
                list={["DBMS와 버전에 따른 SQL 문법의 차이점을 이해하고, 이용하고자 하는 DBMS에 맞게 쿼리문을 작성할 수 있음", "Oracle SQL Developer를 사용한 데이터베이스 관리 가능", "PL/SQL을 사용한 프로시저 및 트리거 작성에 능통함"]}
        />
        <Skill
                name="MongoDB"
                image={mongodb}
                percentage="60"
                list={["NoSQL DBMS의 장단점을 인식하고, 개발 목적에 맞는 DBMS를 취사 선택할 수 있음", "Mongoose를 사용한 데이터베이스 입출력 자동화 가능", "보안, 백업, 권한 및 데이터베이스 / 테이블 관리 등 비 서비스 관련 이슈를 관리할 수 있음"]}
        />
    </div>
    <div class="container">
        <h3>Tools</h3>
        <Skill
                name="Git"
                image={git}
                percentage="80"
                list={["Git Bash를 사용한 버전 관리 가능", "GitHub, GitLab 등을 사용한 원격 저장소 관리 가능", "Git Flow를 사용한 팀 프로젝트 관리 가능"]}
        />
        <Skill
                name="Vite"
                image={vite}
                percentage="70"
                list={["Vite를 사용하여 프로젝트를 구성하여 관리하고, 이를 빌드 하고 배포할 수 있음", "테스트 및 디버깅 절차를 이해하고, 이를 통해 프로젝트를 효율적으로 관리할 수 있음"]}
        />
        <Skill
                name="JWT"
                image={jwt}
                percentage="60"
                list={["JWT를 사용한 인증 및 권한 관리 가능", "JWT 사용을 전제한 로그인, 회원가입 등 REST API 구축", "JWT를 활용한 데이터 암호화 및 복호화 가능"]}
        />
        <Skill
                name="Docker"
                image={docker}
                percentage="70"
                list={["Docker를 사용한 컨테이너, 이미지 관리 가능", "Docker 사용 환경에서의 네트워크 구성에 익숙함"]}
        />
        <Skill
                name="Ubuntu"
                image={ubuntu}
                percentage="60"
                list={["Ubuntu를 사용한 서버 구축 및 관리 가능", "리눅스 환경에서의 네트워크 구성 및 보안 설정 가능", "Ubuntu를 사용한 서버 모니터링 및 로그 분석 가능"]}
        />
        <Skill
                name="IntelliJ IDEA"
                image={intellij}
                percentage="80"
                list={["IntelliJ IDEA를 사용한 프로젝트 구성, 관리, 디버깅 및 테스트 가능", "코드 리팩토링 및 최적화 중시"]}
        />
        <Skill
                name="Nginx"
                image={nginx}
                percentage="70"
                list={["Nginx를 사용한 웹 서버 구축 및 관리 가능", "로드 밸런싱, 리버스 프록싱과 보안 설정 절차 숙지"]}
        />
    </div>
</section>

<style>
    #skills {
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 40px;
        padding: 40px;
        perspective: 3000px;
    }
    @media (max-width: 900px) {
        #skills {
            padding: 20px;
        }
    }
    .container {
        position: relative;
        flex: 1;
        width: 100%;
        max-width: 900px;
        height: 100%;
        display: grid;
        grid-template-columns: repeat(2, 1fr);
        gap: 20px;
        background: var(--background-color-2);
        padding: 15px;
        border-radius: 5px;
        box-shadow: 0 0 5px #0003;
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
</style>