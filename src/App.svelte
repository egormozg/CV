<script>
  import { onMount } from 'svelte';
  import meImage from './I.jpg';
  
  // --- Internationalization (i18n) Content Object ---
  const content = {
    en: {
      name: "Egor Spinu",
      title: "JavaScript Full-Stack Engineer",
      location: "Gornoe, Moldova",
      phone: "+37369445470",
      email: "egor.i.spinu@gmail.com",
      linkedin: "linkedin.com/in/egorspinu",
      linkedinUrl: "https://www.linkedin.com/in/egorspinu/",
      website: "gifokamp.com",
      websiteUrl: "https://gifokamp.com",
      summary: "A self-taught, proactive, and results-driven Full-Stack JavaScript Engineer with a proven track record of architecting and deploying complex web applications from concept to completion. Thrives in high-pressure, ambiguous environments, leveraging exceptional problem-solving skills and a holistic, strategic mindset to see the \"whole picture\" and deliver robust solutions. Combines deep technical expertise in the Svelte/Node.js ecosystem with a practical, hands-on understanding of cybersecurity and proficiency in leveraging cutting-edge AI tools to accelerate development.",
      sections: {
          summary: "Summary",
          skills: "Technical Skills",
          experience: "Professional Experience",
          competencies: "Core Competencies",
          awards: "Awards & Recognition",
          volunteering: "Community & Volunteering"
      },
      skills: [
        { category: 'Frontend', details: 'SvelteKit, Svelte 5 (Runes), JavaScript (ES6+), HTML5, CSS3, Tailwind CSS v4' },
        { category: 'Backend', details: 'Node.js, Firebase Cloud Functions, Serverless Architecture, REST API Design' },
        { category: 'Databases & Cloud', details: 'Firestore (NoSQL), Google Cloud Platform (GCP), Firebase Suite (Auth, Storage)' },
        { category: 'Development & DevOps', details: 'Git, GitHub, Vite, Bun, CI/CD Principles, AI-Assisted Development' },
        { category: 'Cybersecurity', details: 'Network Security, Web Application Vulnerabilities (OWASP Top 10), Penetration Testing Methodologies' },
        {
          category: 'Languages',
          items: [
            { name: 'Russian', proficiency: 'Native' },
            { name: 'Romanian', proficiency: 'Native' },
            { name: 'English', proficiency: 'C1 Professional Proficiency (Strong comprehension and learning; conversational fluency limited by practice)' }
          ]
        }
      ],
      experiences: [
        {
          title: 'Founder & Lead Full-Stack Engineer',
          company: 'Gifokamp',
          company_url: 'gifokamp.com',
          period: '2023 – Present',
          subtitle: 'Personal Startup',
          details: [
            'Architected and developed a full-stack, serverless language acquisition platform from the ground up, now supporting ~85 languages through a unique multisensory learning approach. Handled the entire product lifecycle from ideation to deployment and maintenance.',
            'Engineered a modular, microservices-style backend on <strong>Firebase Cloud Functions</strong>, creating distinct, scalable services for authentication, media processing, and data management.',
            'Led the frontend development using <strong>SvelteKit</strong>, delivering a highly reactive, intuitive, and performant user interface. Drove the strategic migration of the codebase to <strong>Svelte 5 (Runes)</strong> for improved state management and future-proofing.',
            'Designed and implemented a real-time NoSQL database schema in <strong>Firestore</strong>, optimized for complex queries and user-generated content including media-rich "playlists" and learning pairs.',
            'Developed and integrated a companion <strong>Chrome Extension</strong> to act as a "web clipper," enabling users to seamlessly capture and import content, demonstrating an understanding of a cohesive, multi-platform user experience.',
            'Integrated a comprehensive suite of advanced third-party services: leveraging <strong>TTS (Text-to-Speech), STT (Speech-to-Text), and Translation APIs</strong> for core multi-sensory language acquisition features; utilizing <strong>Gemini AI</strong> for intelligent content processing; and incorporating tools like <strong>Nanobanana and Google Analytics</strong> for optimized performance and data-driven insights.',
            'Engineered a multi-layered caching strategy using <strong>IndexedDB</strong> for client-side persistence and <strong>Redis</strong> for server-side caching, creating a highly performant, optimistic UI obsessed with speed.'
          ]
        }
      ],
      awards: [
        {
          title: 'Google for Startups Cloud Program',
          issuer: 'Pre-Seed Funding',
          year: '2024',
          detail: 'Awarded funding and cloud credits in recognition of the project\'s innovative concept, strong technical foundation, and potential for market impact.'
        }
      ],
      competencies: [
        {
            title: "Rapid & On-the-Go Learning",
            detail: "Proven ability to quickly master new technologies and complex domains. The intensive 240-hour cybersecurity program on TryHackMe is a recent example of this self-directed, practical approach to skill acquisition."
        },
        {
            title: "AI-Powered Development",
            detail: "Professionally leverage the power of cutting-edge AI tools in both development and research to accelerate workflows, solve complex problems, and deliver robust solutions efficiently."
        },
        {
            title: "Entrepreneurial Resilience",
            detail: "Proven initiative from childhood, having bootstrapped ventures and consistently adapted to overcome significant challenges, including adverse life events and professional setbacks. Drives projects forward with unwavering determination and a results-oriented mindset."
        }
      ],
      volunteering: [
          {
              title: "IT Specialist Volunteer",
              organization: "Jewish Community of Moldova (JCM)",
              period: "2022",
              detail: "Developed and implemented IT solutions to streamline logistics and coordinate aid for Jewish refugees from Ukraine during the 2022 crisis. <a href='https://jcm.md/news/v3/' target='_blank' rel='noopener noreferrer'>Learn more</a>."
          }
      ]
    },
    ru: {
      name: "Егор Спыну",
      title: "JavaScript Full-Stack Инженер",
      location: "Горное, Молдова",
      phone: "+37369445470",
      email: "egor.i.spinu@gmail.com",
      linkedin: "linkedin.com/in/egorspinu",
      linkedinUrl: "https://www.linkedin.com/in/egorspinu/",
      website: "gifokamp.com",
      websiteUrl: "https://gifokamp.com",
      summary: "Инициативный и ориентированный на результат Full-Stack JavaScript инженер-самоучка с подтвержденным опытом проектирования и развертывания сложных веб-приложений от концепции до завершения. Преуспевает в условиях высокого давления и неопределенности, используя исключительные навыки решения проблем и целостное стратегическое мышление, чтобы видеть \"полную картину\" и предоставлять надежные решения. Сочетает глубокие технические знания в экосистеме Svelte/Node.js с практическим пониманием кибербезопасности и умением использовать передовые инструменты ИИ для ускорения разработки.",
      sections: {
          summary: "Обо мне",
          skills: "Технические навыки",
          experience: "Профессиональный опыт",
          competencies: "Ключевые компетенции",
          awards: "Награды и признание",
          volunteering: "Общественная деятельность и волонтерство"
      },
      skills: [
        { category: 'Фронтенд', details: 'SvelteKit, Svelte 5 (Runes), JavaScript (ES6+), HTML5, CSS3, Tailwind CSS v4' },
        { category: 'Бэкенд', details: 'Node.js, Firebase Cloud Functions, Serverless Architecture, REST API Design' },
        { category: 'Базы данных и облако', details: 'Firestore (NoSQL), Google Cloud Platform (GCP), Firebase Suite (Auth, Storage)' },
        { category: 'Разработка и DevOps', details: 'Git, GitHub, Vite, Bun, CI/CD Principles, AI-Assisted Development' },
        { category: 'Кибербезопасность', details: 'Сетевая безопасность, уязвимости веб-приложений (OWASP Top 10), методологии пентестинга' },
        {
          category: 'Языки',
          items: [
            { name: 'Русский', proficiency: 'Родной' },
            { name: 'Румынский', proficiency: 'Родной' },
            { name: 'Английский', proficiency: 'C1 Professional (сильное понимание и обучаемость; разговорная речь ограничена практикой)' }
          ]
        }
      ],
      experiences: [
        {
          title: 'Основатель и Ведущий Full-Stack Инженер',
          company: 'Gifokamp',
          company_url: 'gifokamp.com',
          period: '2023 – настоящее время',
          subtitle: 'Собственный стартап',
          details: [
            'Спроектировал и разработал с нуля полностековую, бессерверную платформу для изучения языков, поддерживающую ~85 языков через уникальный мультисенсорный подход. Управлял всем жизненным циклом продукта от идеи до развертывания и поддержки.',
            'Разработал модульный бэкенд в стиле микросервисов на <strong>Firebase Cloud Functions</strong>, создав отдельные, масштабируемые сервисы для аутентификации, обработки медиа и управления данными.',
            'Руководил фронтенд-разработкой с использованием <strong>SvelteKit</strong>, обеспечив высокореактивный, интуитивно понятный и производительный пользовательский интерфейс. Осуществил стратегический переход кодовой базы на <strong>Svelte 5 (Runes)</strong> для улучшения управления состоянием и обеспечения будущего развития.',
            'Разработал и внедрил схему NoSQL базы данных в реальном времени в <strong>Firestore</strong>, оптимизированную для сложных запросов и пользовательского контента, включая медиа-насыщенные «плейлисты» и учебные пары.',
            'Разработал и интегрировал сопутствующее <strong>Chrome-расширение</strong> для «веб-клиппинга», позволяющее пользователям беспрепятственно захватывать и импортировать контент, демонстрируя понимание целостного многоплатформенного пользовательского опыта.',
            'Интегрировал комплекс передовых сторонних сервисов: используя <strong>TTS (Text-to-Speech), STT (Speech-to-Text), и API для перевода</strong> для создания ключевых мультисенсорных функций изучения языков; применяя <strong>Gemini AI</strong> для интеллектуальной обработки контента; и внедряя инструменты, такие как <strong>Nanobanana и Google Analytics</strong>, для оптимизации производительности и анализа данных.',
            'Разработал многоуровневую стратегию кэширования с использованием <strong>IndexedDB</strong> для персистентности на стороне клиента и <strong>Redis</strong> для кэширования на стороне сервера, создав высокопроизводительный, оптимистичный UI, одержимый скоростью.'
          ]
        }
      ],
      awards: [
        {
          title: 'Программа Google for Startups Cloud',
          issuer: 'Pre-Seed финансирование',
          year: '2024',
          detail: 'Получил финансирование и облачные кредиты в знак признания инновационной концепции проекта, прочной технической базы и потенциала для рыночного влияния.'
        }
      ],
      competencies: [
        {
            title: "Быстрое обучение «на лету»",
            detail: "Подтвержденная способность быстро осваивать новые технологии и сложные области. Интенсивная 240-часовая программа по кибербезопасности на TryHackMe является свежим примером такого самостоятельного, практического подхода к приобретению навыков."
        },
        {
            title: "Разработка с помощью ИИ",
            detail: "Профессионально использую возможности передовых инструментов ИИ как в разработке, так и в исследованиях для ускорения рабочих процессов, решения сложных задач и эффективного создания надежных решений."
        },
        {
            title: "Предпринимательская устойчивость",
            detail: "Подтвержденная инициатива с детства, включая запуск собственных проектов с нуля и последовательную адаптацию для преодоления значительных трудностей, в том числе неблагоприятных жизненных обстоятельств и профессиональных неудач. Двигаю проекты вперед с непоколебимой решимостью и нацеленностью на результат."
        }
      ],
      volunteering: [
          {
              title: "Волонтер-ИТ-специалист",
              organization: "Еврейская Община Молдовы (JCM)",
              period: "2022",
              detail: "Разработал и внедрил ИТ-решения для оптимизации логистики и координации помощи еврейским беженцам из Украины во время кризиса 2022 года. <a href='https://jcm.md/news/v3/' target='_blank' rel='noopener noreferrer'>Подробнее</a>."
          }
      ]
    }
  };

  // --- Language State ---
  let lang = 'en';
  $: t = content[lang]; // Derived store for current language's content

  // Set document language attribute for accessibility
  onMount(() => {
      document.documentElement.lang = lang;
  });

  $: if (typeof document !== 'undefined') {
      document.documentElement.lang = lang;
  }
</script>

<div class="container">  
  <div class="lang-switcher">
    <button class:active={lang === 'en'} on:click={() => lang = 'en'}>EN</button>
    <button class:active={lang === 'ru'} on:click={() => lang = 'ru'}>RU</button>
  </div>

  <header class="card">
    <div class="card-left">
      <img src={meImage} alt="Photo of {t.name}" class="profile-photo"/>
    </div>
    <div class="card-right">
      <h1>{t.name}</h1>
      <h2>{t.title}</h2>
      <div class="contact-info">
        <p><i class="fas fa-map-marker-alt"></i> <span>{t.location}</span></p>
        <p><i class="fas fa-phone"></i> <a href="tel:{t.phone}">{t.phone}</a></p>
        <p><i class="fas fa-envelope"></i> <a href="mailto:{t.email}">{t.email}</a></p>
        <p><i class="fab fa-linkedin"></i> <a href={t.linkedinUrl} target="_blank" rel="noopener noreferrer">{t.linkedin}</a></p>
        <p><i class="fas fa-globe"></i> <a href={t.websiteUrl} target="_blank" rel="noopener noreferrer">{t.website}</a></p>
      </div>
    </div>
  </header>

  <main class="cv-content">
    <section id="summary">
        <h3>{t.sections.summary}</h3>
        <p>{@html t.summary}</p>
    </section>

    <section id="skills">
      <h3>{t.sections.skills}</h3>
      <div class="skills-grid">
        {#each t.skills as skill}
          <div class="skill-item">
            <strong>{skill.category}</strong>
            {#if skill.category === 'Languages' || skill.category === 'Языки'}
              <div class="language-tags">
                {#each skill.items as language}
                  <span class="language-tag"><strong>{language.name}</strong> ({language.proficiency})</span>
                {/each}
              </div>
            {:else}
              <span>{@html skill.details}</span>
            {/if}
          </div>
        {/each}
      </div>
    </section>

    <section id="experience">
      <h3>{t.sections.experience}</h3>
      {#each t.experiences as exp}
        <div class="job">
          <h4>{exp.title}</h4>
          <h5>{exp.company} (<a href="https://{exp.company_url}" target="_blank" rel="noopener noreferrer">{exp.company_url}</a>) | {exp.period}</h5>
          {#if exp.subtitle}<i>{exp.subtitle}</i>{/if}
          <ul>
            {#each exp.details as detail}
              <li>{@html detail}</li>
            {/each}
          </ul>
        </div>
      {/each}
    </section>

    <section id="competencies">
      <h3>{t.sections.competencies}</h3>
      <div class="competency-grid">
         {#each t.competencies as competency}
            <div class="competency-item">
                <h4>{competency.title}</h4>
                <p>{competency.detail}</p>
            </div>
          {/each}
      </div>
    </section>

    <section id="awards">
        <h3>{t.sections.awards}</h3>
        {#each t.awards as award}
            <div class="award-item">
                <h4>{award.title}</h4>
                <h5>{award.issuer} | {award.year}</h5>
                <p>{award.detail}</p>
            </div>
        {/each}
    </section>

    <!-- NEW VOLUNTEERING SECTION -->
    <section id="volunteering">
        <h3>{t.sections.volunteering}</h3>
        {#each t.volunteering as vol}
            <div class="volunteering-item">
                <h4>{vol.title}</h4>
                <h5>{vol.organization} | {vol.period}</h5>
                <p>{@html vol.detail}</p>
            </div>
        {/each}
    </section>
  </main>
</div>
