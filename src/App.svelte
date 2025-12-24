<script>
  // Svelte 5 Runes syntax
  import meImage from './assets/I.jpg';

  let lang = $state('en');

  // --- Internationalization (i18n) Content Object ---
  const content = {
    en: {
      name: "Egor Spinu",
      title: "Full-Stack Engineer | Ben Noah",
      location: "Gornoe, Moldova",
      phone: "+37369445470",
      email: "egor.i.spinu@gmail.com",
      linkedin: "linkedin.com/in/egorspinu",
      linkedinUrl: "https://www.linkedin.com/in/egorspinu/",
      website: "gifokamp.com",
      websiteUrl: "https://gifokamp.com",
      objective: "<strong>Academic Goal:</strong> To enroll in the <strong>B.Sc. in Mathematics and Computer Science</strong> program at <strong>Ariel University</strong>.  As a founder developing a startup in the AI era, I recognize that simply using existing tools is not enough. I seek the rigorous mathematical foundation provided by the Faculty to deeply understand the logic, algorithms, and fundamental principles necessary to innovate and build resilient systems for the future.",
      summary: "A Senior Full-Stack Engineer and entrepreneur currently developing an AI language learning ecosystem. My path has been unconventional: I entered the workforce at 14 to support myself, was married and divorced 12 years ago (no children), and built businesses from scratch. I am applying to Ariel University to bridge my practical experience with deep theoretical mathematics and Computer Science.",
      sections: {
          summary: "Professional Summary",
          objective: "Objective",
          skills: "Technical Skills",
          experience: "Professional Experience & Entrepreneurship",
          education: "Education & Certifications",
          competencies: "Core Competencies",
          awards: "Awards & Recognition",
          volunteering: "Community & Volunteering"
      },
      skills: [
        { category: 'Frontend', details: 'JavaScript, Flutter, SvelteKit, Svelte 5 (Runes), Tailwind CSS v4' },
        { category: 'Backend', details: 'Node.js, Firebase Cloud Functions, Serverless Architecture, REST API Design' },
        { category: 'Databases & Cloud', details: 'Firestore (NoSQL), Google Cloud Platform (GCP), Firebase Suite' },
        { category: 'AI & Security', details: 'Gemini AI Integration, OWASP Top 10, Cybersecurity (TryHackMe)' },
        {
          category: 'Languages',
          items: [
            { name: 'Russian', proficiency: 'Native' },
            { name: 'Romanian', proficiency: 'Native' },
            { name: 'Hebrew', proficiency: 'Beginner (Learning)' },
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
          subtitle: 'AI Language Learning Ecosystem',
          details: [
            'Developing a complete ecosystem for language acquisition.',
            '<strong>Web App:</strong> Built with <strong>Svelte 5</strong> and Firebase. Features custom visual playlists, AI pronunciation coaching, and a Spaced Repetition System (SRS).',
            '<strong>AI Language Clipper (Chrome Extension):</strong> An intelligent agent using <strong>Gemini AI</strong> for context-aware translation and seamless integration with the user account.',
            '<strong>Mobile:</strong> Cross-platform <strong>Flutter</strong> application. (in development).'
          ]
        },
        {
          title: 'Co-Founder & Director',
          company: 'Logoritm Corp',
          period: '2015 – 2018',
          subtitle: 'Construction & Heating Engineering',
          details: [
            'Co-founded a firm providing construction and heating engineering services. Responsible for technical oversight and client management.',
            '<strong>Project Management:</strong> Single-handedly organized a sold-out Magician Concert at the <strong>National Philharmonic</strong> on April 1st, 2017. Handled venue negotiation, promotion, ticket sales, and logistics.',
            '(Company is currently passive as partner relocated to Russia).'
          ]
        },
        {
          title: 'HVAC Technical Specialist',
          company: 'Self-Employed',
          period: '2010 – 2015',
          details: [
            'Worked full-time installing heating systems to gain financial independence.',
            'Learned real-world systems and problem-solving through practical application.'
          ]
        }
      ],
      education: [
        {
            title: "Ericksonian Hypnotherapy Certification",
            institution: "IGiSP",
            year: "2012 – 2014",
            note: "Completed an intensive 200-hour course under the program of Mikhail Ginzburg. Focused on cognitive structures and linguistics. Pursued this path as self-study proved more effective than the formal university curriculum."
        },
        {
            title: "Psychopedagogy (2 Years Completed)",
            institution: "Free International University of Moldova (ULIM)",
            year: "2012 – 2014",
            note: "Completed 4 semesters. Left to focus on specialized certification in hypnotherapy and business ventures."
        },
        {
            title: "Innovation Engineering",
            institution: "Technical University of Moldova (TUM)",
            year: "Sep 2010 – Nov 2010",
            note: "Completed 1st semester coursework. Withdrew to work full-time in heating system installations due to financial necessity."
        },
        {
            title: "Baccalaureate Diploma",
            institution: "Liceul Teoretic Romanesti",
            year: "2010",
            note: "Studied at Romanesti; Exams taken at Center 'Ion Vatamanu'.<br><strong>Mathematics: 8.34</strong> | Physics: 8.96 | Informatics: 8.55"
        }
      ],
      awards: [
        {
          title: 'International Memory Championships',
          issuer: 'Memory Sports',
          year: '2018 - 2019',
          detail: '<strong>Asia Open (Bali, 2019):</strong> Ranked 90th out of ~170 competitors. <strong>Korea OPEN (2018):</strong> Ranked 122nd out of ~150 competitors.'
        },
        {
          title: 'Google for Startups Program',
          issuer: 'Ideation Funding',
          year: '2024',
          detail: 'Awarded funding and cloud credits in recognition of the project\'s innovative concept, strong technical foundation, and potential for market impact.'
        }
      ],
      competencies: [
        {
            title: "Autodidactic Mastery",
            detail: "Proven ability to master complex domains independently, from Full-Stack coding and English (C1) to Cognitive Science."
        },
        {
            title: "System Architecture",
            detail: "Experience designing and executing complex systems, whether in software (Gifokamp), engineering (Logoritm), or event logistics."
        },
        {
            title: "Entrepreneurial Resilience",
            detail: "Proven initiative since childhood, bootstrapping ventures and adapting to significant challenges. I drive projects forward with determination and a results-oriented mindset."
        }
      ],
      volunteering: [
          {
              title: "IT Specialist Volunteer",
              organization: "Jewish Community of Moldova (JCM)",
              period: "2022",
              detail: "Developed and implemented IT solutions to streamline logistics and coordinate aid for Jewish refugees from Ukraine during the onset of the 2022 war. <a href='https://jcm.md/news/v3/' target='_blank'>Learn more</a>."
          }
      ]
    },
    ru: {
      name: "Егор Спыну",
      title: "Full-Stack Инженер | Бен Ноах",
      location: "Горное, Молдова",
      phone: "+37369445470",
      email: "egor.i.spinu@gmail.com",
      linkedin: "linkedin.com/in/egorspinu",
      linkedinUrl: "https://www.linkedin.com/in/egorspinu/",
      website: "gifokamp.com",
      websiteUrl: "https://gifokamp.com",
      objective: "<strong>Цель:</strong> Поступление на программу <strong>B.Sc. Математика и Компьютерные Науки</strong> в <strong>Ариэльский Университет</strong>. Развивая стартап в эпоху ИИ, понимаю, что простого использования инструментов недостаточно. Мне необходим строгий математический фундамент, предоставляемый факультетом, чтобы глубоко понимать логику, алгоритмы и принципы, необходимые для создания инновационных систем.",
      summary: "Senior Full-Stack инженер и предприниматель, разрабатывающий экосистему для изучения языков на базе ИИ. C 14 лет начал работать, рано женился и развелся (детей нет), строил бизнес с нуля. Хочу поступить в Ариэльский университет, чтобы объединить практический опыт с глубокой теоретической подготовкой в области математики и компьютерных наук.",
      sections: {
          summary: "Обо мне",
          objective: "Цель",
          skills: "Технические навыки",
          experience: "Профессиональный опыт и Бизнес",
          education: "Образование и Сертификаты",
          competencies: "Ключевые компетенции",
          awards: "Награды и Достижения",
          volunteering: "Волонтерство"
      },
      skills: [
        { category: 'Фронтенд', details: 'JavaScript, Flutter, SvelteKit, Svelte 5 (Runes), Tailwind CSS v4' },
        { category: 'Бэкенд', details: 'Node.js, Firebase Cloud Functions, Serverless Architecture, REST API Design' },
        { category: 'Базы данных', details: 'Firestore (NoSQL), Google Cloud Platform (GCP), Firebase Suite' },
        { category: 'ИИ и Безопасность', details: 'Gemini AI Integration, OWASP Top 10, Кибербезопасность (TryHackMe)' },
        {
          category: 'Языки',
          items: [
            { name: 'Русский', proficiency: 'Родной' },
            { name: 'Румынский', proficiency: 'Родной' },
            { name: 'Иврит', proficiency: 'Начальный уровень' },
            { name: 'Английский', proficiency: 'C1 Professional (сильное понимание и обучаемость; разговорная речь ограничена практикой)' }
          ]
        }
      ],
      experiences: [
        {
          title: 'Основатель и Full-Stack Инженер',
          company: 'Gifokamp',
          company_url: 'gifokamp.com',
          period: '2023 – Наст. время',
          subtitle: 'Экосистема изучения языков с ИИ',
          details: [
            'Разработка полной экосистемы для изучения языков.',
            '<strong>Web App:</strong> Создано на <strong>Svelte 5</strong> и Firebase. Включает визуальные плейлисты, ИИ-коучинг произношения и систему интервальных повторений (SRS).',
            '<strong>AI Language Clipper (Chrome Extension):</strong> Интеллектуальный агент на базе <strong>Gemini AI</strong> для контекстного перевода и интеграции с аккаунтом пользователя.',
            '<strong>Mobile:</strong> Кроссплатформенное приложение на <strong>Flutter</strong>. (в разработке).'
          ]
        },
        {
          title: 'Соучредитель и Директор',
          company: 'Logoritm Corp',
          period: '2015 – 2018',
          subtitle: 'Строительство и Инженерия',
          details: [
            'Соучредитель фирмы по оказанию строительных и инженерных услуг. Ответственный за технический надзор и работу с клиентами.',
            '<strong>Управление проектами:</strong> В одиночку организовал концерт иллюзионистов в <strong>Национальной Филармонии</strong> 1 апреля 2017 года (аншлаг). Управлял переговорами с площадкой, рекламой, продажей билетов и логистикой.',
            '(Компания пассивна в связи с переездом партнера в Россию).'
          ]
        },
        {
          title: 'Технический специалист HVAC',
          company: 'Частная практика',
          period: '2010 – 2015',
          details: [
            'Работал полный день на установке систем отопления для достижения финансовой независимости.',
            'Изучал реальные системы и решение проблем через практику.'
          ]
        }
      ],
      education: [
        {
            title: "Сертификация по Эриксоновскому гипнозу",
            institution: "ИГиСП",
            year: "2012 – 2014",
            note: "Завершил интенсивный 200-часовой курс по программе Михаила Гинзбурга. Фокус на когнитивных структурах и лингвистике. Выбрал этот путь, так как самообразование оказалось эффективнее университетской программы."
        },
        {
            title: "Психопедагогика (2 курса)",
            institution: "Международный Независимый Университет Молдовы (ULIM)",
            year: "2012 – 2014",
            note: "Закончил 4 семестра. Оставил учебу, чтобы сосредоточиться на сертификации по гипнотерапии и бизнесе."
        },
        {
            title: "Инженерия и инновации",
            institution: "Технический Университет Молдовы (TUM)",
            year: "Сен 2010 – Ноя 2010",
            note: "Прошел обучение в 1-м семестре. Вынужден был оставить учебу и работать полный день на монтаже систем отопления из-за финансовой необходимости."
        },
        {
            title: "Диплом Бакалавра",
            institution: "Теоретический Лицей Романешты",
            year: "2010",
            note: "Обучение в Романештах; Экзамены в центре 'Ион Ватаману'.<br><strong>Математика: 8.34</strong> | Физика: 8.96 | Информатика: 8.55"
        }
      ],
      awards: [
        {
          title: 'Международные соревнования по памяти',
          issuer: 'Memory Sports',
          year: '2018 - 2019',
          detail: '<strong>Asia Open (Бали, 2019):</strong> 90-е место из ~170. <strong>Korea OPEN (2018):</strong> 122-е место из ~150.'
        },
        {
          title: 'Google for Startups Program',
          issuer: 'Ideation Funding',
          year: '2024',
          detail: 'Получил финансирование для развития облачной инфраструктуры в знак признания инновационной концепции проекта, сильной технической базы и потенциала положительного влияния.'
        }
      ],
      competencies: [
        {
            title: "Мастерство самообучения",
            detail: "Способность самостоятельно осваивать сложные области: от Full-Stack разработки и английского (C1) до когнитивистики."
        },
        {
            title: "Архитектура систем",
            detail: "Опыт проектирования и реализации сложных систем, будь то программное обеспечение (Gifokamp), инженерия (Logoritm) или логистика мероприятий."
        },
        {
            title: "Предпринимательская стойкость",
            detail: "Проявленная с детства инициатива: запуск собственных проектов и адаптация к сложным вызовам. Я продвигаю проекты с решимостью и ориентацией на результат."
        }
      ],
      volunteering: [
          {
              title: "Волонтер-ИТ-специалист",
              organization: "Еврейская Община Молдовы (JCM)",
              period: "2022",
              detail: "Разработал и внедрил ИТ-решения для оптимизации логистики и координации помощи еврейским беженцам из Украины в начале войны 2022 года. <a href='https://jcm.md/news/v3/' target='_blank'>Подробнее</a>."
          }
      ]
    }
  };

  let t = $derived(content[lang]);
  $effect(() => {
    if (typeof document !== 'undefined') {
      document.documentElement.lang = lang;
    }
  });
</script>

<div class="container">  
  <div class="lang-switcher">
    <button class:active={lang === 'en'} onclick={() => lang = 'en'}>EN</button>
    <button class:active={lang === 'ru'} onclick={() => lang = 'ru'}>RU</button>
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
    
    <section id="objective" class="objective-section">
        <h3>{t.sections.objective}</h3>
        <p>{@html t.objective}</p>
    </section>

    <section id="summary">
        <h3>{t.sections.summary}</h3>
        <p>{@html t.summary}</p>
    </section>

    <section id="skills">
      <h3>{t.sections.skills}</h3>
      <div class="skills-grid">
        {#each t.skills as skill}
          <div class="skill-item" class:full-width={skill.category === 'Languages' || skill.category === 'Языки'}>
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
          <h5>{exp.company} {#if exp.company_url}(<a href="https://{exp.company_url}" target="_blank" rel="noopener noreferrer">{exp.company_url}</a>){/if} | {exp.period}</h5>
          {#if exp.subtitle}<i>{exp.subtitle}</i>{/if}
          <ul>
            {#each exp.details as detail}
              <li>{@html detail}</li>
            {/each}
          </ul>
        </div>
      {/each}
    </section>

    <section id="education">
        <h3>{t.sections.education}</h3>
        {#each t.education as edu}
            <div class="education-item">
                <h4>{edu.title}</h4>
                <h5>{edu.institution} | {edu.year}</h5>
                {#if edu.note}
                    <p class="edu-note">{@html edu.note}</p>
                {/if}
            </div>
        {/each}
    </section>

    <section id="competencies">
      <h3>{t.sections.competencies}</h3>
      <div class="competency-grid">
         {#each t.competencies as competency}
            <div class="competency-item">
                <h4>{competency.title}</h4>
                <p>{@html competency.detail}</p>
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
                <p>{@html award.detail}</p> 
            </div>
        {/each}
    </section>

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

<style>
    .objective-section {
        background-color: #f0f9ff;
        border-left: 4px solid #0077b6;
        padding: 1rem;
        margin-bottom: 2rem;
    }
    
    .education-item {
        margin-bottom: 1.5rem;
    }
    
    .edu-note {
        font-size: 0.95rem;
        color: #555;
        margin-top: 0.3rem;
        font-style: italic;
    }

    .skills-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 1rem;
    }
    
    /* MODIFIED: Forced 3 columns for competencies */
    .competency-grid {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 1.5rem;
    }

    .competency-item {
        background: #f9f9f9;
        padding: 1rem;
        border-radius: 8px;
        border: 1px solid #eee;
    }
    
    .competency-item h4 {
        color: #0077b6;
        margin-top: 0;
        margin-bottom: 0.5rem;
    }

    /* Logic to span full width */
    .skill-item.full-width {
        grid-column: 1 / -1;
    }
    
    .language-tags {
        display: flex;
        gap: 1.5rem;
        flex-wrap: wrap;
        margin-top: 0.5rem;
    }
    
    @media (max-width: 768px) {
        /* On small mobile screens, revert to 1 column so text is readable */
        .competency-grid {
            grid-template-columns: 1fr;
        }
    }
</style>