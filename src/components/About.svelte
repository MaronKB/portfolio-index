<script>
    import {FontAwesomeIcon} from "@fortawesome/svelte-fontawesome";
    import {faCode, faHashtag, faNewspaper, faPaintbrush, faPenNib, faSnowflake} from "@fortawesome/free-solid-svg-icons";
    import Logo from '/src/assets/logo.svg?raw';
    import Title from '/src/assets/title.svg?raw';

    let active = false;
</script>

<section id="about">
    <div class="container">
        <div class="profiles">
            <div id="profile">
                <span>{@html Logo}</span>
            </div>
            <div id="name">
                <span>{@html Title}</span>
                <h4>SHIN HEE-CHEOL [신희철]</h4>
                <h5>1999. 06. 12</h5>
            </div>
            <div class="tags">
                <span><FontAwesomeIcon icon={faCode}/>FRONTEND DEVELOPER</span>
                <span><FontAwesomeIcon icon={faCode}/>BACKEND DEVELOPER</span>
                <span><FontAwesomeIcon icon={faCode}/>FULLSTACK DEVELOPER</span>
                <span><FontAwesomeIcon icon={faNewspaper}/>WEB PUBLISHER</span>
                <span><FontAwesomeIcon icon={faNewspaper}/>WEB DESIGNER</span>
                <span><FontAwesomeIcon icon={faPaintbrush}/>ILLUSTRATOR</span>
                <span><FontAwesomeIcon icon={faPenNib}/>WRITER</span>
            </div>
        </div>
        <hr class="profile-horizon"/>
        <div class="description">
            <p>저는 사용자 경험을 중심적인 디자인과 상호작용을 중시하는 엔지니어링을 결합하여 사용자 인터페이스를 디자인하고 구현하는 데에 높은 열정을 가진 <span>프론트엔드 개발자</span>이자, 고안정성과 고효율성을 기조로 하여 RESTful한 API를 설계하고 개발하는 <span>백엔드 개발자</span>이고, 시스템의 전체적인 구조를 기획하고 조정할 수 있는 <span>풀스택 개발자</span>이기도 합니다.</p>
            <p><span>효율주의자</span> : 저는 <span>사용성, 직관성, 상호 반응성</span>을 중시하고, 특히 <span>반응형 디자인과 최적화</span>에 지대한 관심이 있습니다. <span>코드 재사용성</span>을 높이고 <span>클래스 기조의 코딩</span>을 활용하여 코드 반복성을 최대한 줄이려 노력합니다.</p>
            <p><span>문학적 코더</span> : 웹 페이지 디자인 뿐 아니라 코드 작성에 있어서도 <span>직관성과 통일감, 그리고 유지보수성</span>을 크게 중시하여 <span>읽고 다시 쓰기 편한 코드 작성</span>에 지대한 노력을 기울이고 있습니다.</p>
        </div>
        <div class="tags skills" class:active={active}>
            <span><FontAwesomeIcon icon={faHashtag}/>Java</span>
            <span><FontAwesomeIcon icon={faHashtag}/>JavaScript</span>
            <span><FontAwesomeIcon icon={faHashtag}/>TypeScript</span>
            <span><FontAwesomeIcon icon={faHashtag}/>C#</span>
            <span><FontAwesomeIcon icon={faHashtag}/>SQL</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Bash</span>
            <span><FontAwesomeIcon icon={faHashtag}/>PowerShell</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Linux</span>
            <span><FontAwesomeIcon icon={faHashtag}/>HTML5</span>
            <span><FontAwesomeIcon icon={faHashtag}/>CSS3</span>
            <span><FontAwesomeIcon icon={faHashtag}/>React</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Jquery</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Next</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Svelte</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Wordpress</span>
            <span><FontAwesomeIcon icon={faHashtag}/>JSP</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Thymeleaf</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Spring</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Node.js</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Express</span>
            <span><FontAwesomeIcon icon={faHashtag}/>JPA</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Mybatis</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Oracle RDBMS</span>
            <span><FontAwesomeIcon icon={faHashtag}/>MySQL</span>
            <span><FontAwesomeIcon icon={faHashtag}/>MariaDB</span>
            <span><FontAwesomeIcon icon={faHashtag}/>MongoDB</span>
            <span><FontAwesomeIcon icon={faHashtag}/>AWS</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Oracle Cloud</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Git</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Github</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Ubuntu</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Docker</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Intellij IDEA</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Webpack</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Nginx</span>
            <span><FontAwesomeIcon icon={faHashtag}/>Markdown</span>
            <span><FontAwesomeIcon icon={faHashtag}/>JLPT</span>
        </div>
        <button class="toggle" on:click={() => active = !active}>
            <span>{active ? 'Hide' : 'Show'} Skills</span>
        </button>
    </div>
</section>

<style>
    section {
        padding: 80px 40px;
        perspective: 1000px;
    }
    @media (max-width: 600px) {
        section {
            padding: 80px 0;
        }
    }
    .container {
        position: relative;
        width: 100%;
        max-width: 600px;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background: var(--background-color);
        padding: 80px 40px;
        border-radius: 10px;
        box-shadow: 0 0 10px #0003;
        margin: auto;
        overflow: hidden;
    }
    @media (max-width: 600px) {
        .container {
            padding: 40px 20px;
            border-radius: 0;
        }
    }
    .profiles {
        flex: none;
        width: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        gap: 10px;
    }
    #profile {
        width: 160px;
        height: 160px;
        background: white;
        border: 5px solid white;
        overflow: hidden;
        transform: rotate(45deg);
        margin: 50px 0 -20px 0;
    }
    #profile > span {
        display: flex;
        width: 100%;
        height: 100%;
        justify-content: center;
        align-items: center;
        padding: 20px;
        object-fit: contain;
        transform: rotate(-45deg);
    }
    #name {
        width: 100%;
        display: flex;
        flex-direction: column;
        gap: 5px;
        margin: 50px 0 0 0;
    }
    #name > * {
        text-align: center;
    }
    #name > span {
        width: 100%;
        max-width: 200px;
        fill: var(--text-color);
        margin: 20px auto 5px auto;
    }
    #name > h4 {
        padding: 5px;
        border-bottom: 1px solid;
        border-image: linear-gradient(to right, transparent 30%, var(--text-color-3), transparent 70%) 1;
    }
    .profile-horizon {
        width: calc(100% - 40px);
        height: 5px;
        background: linear-gradient(to right, var(--background-color), transparent 30% 70%, var(--background-color)), repeating-linear-gradient(135deg, var(--text-color) 0 10px, transparent 10px 20px);
        border: 0;
        margin: 15px 0 5px 0;
    }
    .description {
        width: 100%;
        margin: 5px 0;
    }
    .description > p {
        width: 100%;
        font-size: 14px;
        line-height: 1.5;
        text-indent: 5px;
        color: var(--text-color-3);
        margin: 4px 0;
    }
    .description > p > span {
        font-weight: var(--font-weight-bold);
        color: var(--text-highlight);
    }
    .tags {
        width: calc(100vw - 20px);
        max-width: 100%;
        display: flex;
        flex-wrap: wrap;
        gap: 3px;
        justify-content: flex-start;
        align-content: flex-start;
        align-items: flex-start;
    }
    .tags span {
        flex: auto;
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 5px;
        font-size: 12px;
        font-weight: var(--font-weight-bold);
        text-align: center;
        text-transform: uppercase;
        color: var(--text-color);
        padding: 6px 8px;
        border: 2px solid var(--text-color-3);
        border-radius: 4px;
    }
    .tags.skills {
        position: absolute;
        bottom: 40px;
        left: 0;
        width: 100%;
        height: 100%;
        align-content: flex-end;
        background: linear-gradient(to bottom, transparent, var(--background-color));
        padding: 20px;
        opacity: 0;
        pointer-events: none;
        transition: opacity 0.5s;
        z-index: 1;
    }
    .tags.skills.active {
        opacity: 1;
        pointer-events: all;
    }
    .toggle {
        position: absolute;
        bottom: 0;
        right: 0;
        width: 100%;
        height: 40px;
        font-size: 12px;
        font-weight: var(--font-weight-bold);
        text-transform: uppercase;
        color: var(--text-color);
        background: var(--background-color);
        border: 0;
        border-top: 1px solid var(--background-color-3);
        border-radius: 0 0 10px 10px;
        cursor: pointer;
        transition: background 0.5s;
        z-index: 2;
    }
    .toggle:hover {
        background: var(--background-color-2);
    }
    @media print {
        .toggle {
            display: none;
        }
    }
</style>