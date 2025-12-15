<script>
  // Hardcoded values from CV.md for simplicity
  const name = "Egor Spinu";
  const title = "JavaScript Full-Stack Engineer"; // UPDATED
  const location = "Gornoe, Moldova";
  const phone = "+37369445470";
  const email = "egor.i.spinu@gmail.com";
  const linkedin = "linkedin.com/in/egorspinu";
  const linkedinUrl = "https://www.linkedin.com/in/egorspinu/";
  const website = "gifokamp.com";
  const websiteUrl = "https://gifokamp.com";
  const photo = "/I.jpg";

  const summary = "A self-taught, proactive, and results-driven Full-Stack JavaScript Engineer with a proven track record of architecting and deploying complex web applications from concept to completion. Thrives in high-pressure, ambiguous environments, leveraging exceptional problem-solving skills and a holistic, strategic mindset to see the \"whole picture\" and deliver robust solutions. Combines deep technical expertise in the Svelte/Node.js ecosystem with a practical, hands-on understanding of cybersecurity and proficiency in leveraging cutting-edge AI tools to accelerate development.";

  const skills = [
    { category: 'Frontend', details: 'SvelteKit, Svelte 5 (Runes), JavaScript (ES6+), HTML5, CSS3, Tailwind CSS v4' },
    { category: 'Backend', details: 'Node.js, Firebase Cloud Functions, Serverless Architecture, REST API Design' },
    { category: 'Databases & Cloud', details: 'Firestore (NoSQL), Google Cloud Platform (GCP), Firebase Suite (Auth, Storage)' },
    { category: 'Development & DevOps', details: 'Git, GitHub, Vite, Bun, CI/CD Principles, AI-Assisted Development' },
    { category: 'Cybersecurity', details: 'Network Security, Web Application Vulnerabilities (OWASP Top 10), Penetration Testing Methodologies' },
    {
      category: 'Languages',
      items: [ // UPDATED: Changed from 'details' to 'items' array for better rendering
        { name: 'Russian', proficiency: 'Native' },
        { name: 'Romanian', proficiency: 'Native' },
        { name: 'English', proficiency: 'C1 Professional Proficiency (Strong comprehension and learning; conversational fluency limited by practice)' } // UPDATED
      ]
    }
  ];

  const experiences = [
    {
      title: 'Founder & Lead Full-Stack Engineer',
      company: 'Gifokamp',
      period: '2023 – Present',
      subtitle: 'Personal Startup',
      details: [
        'Architected and developed a full-stack, serverless language acquisition platform from the ground up, now supporting ~85 languages through a unique multisensory learning approach. Handled the entire product lifecycle from ideation to deployment and maintenance.',
        'Engineered a modular, microservices-style backend on <strong>Firebase Cloud Functions</strong>, creating distinct, scalable services for authentication, media processing, and data management.',
        'Led the frontend development using <strong>SvelteKit</strong>, delivering a highly reactive, intuitive, and performant user interface. Drove the strategic migration of the codebase to <strong>Svelte 5 (Runes)</strong> for improved state management and future-proofing.',
        'Designed and implemented a real-time NoSQL database schema in <strong>Firestore</strong>, optimized for complex queries and user-generated content including media-rich "playlists" and learning pairs.',
        'Developed and integrated a companion <strong>Chrome Extension</strong> to act as a "web clipper," enabling users to seamlessly capture and import content, demonstrating an understanding of a cohesive, multi-platform user experience.',
        // UPDATED
        'Integrated a comprehensive suite of advanced third-party services: leveraging <strong>TTS (Text-to-Speech), STT (Speech-to-Text), and Translation APIs</strong> for core multi-sensory language acquisition features; utilizing <strong>Gemini AI</strong> for intelligent content processing; and incorporating tools like <strong>Nanobanana and Google Analytics</strong> for optimized performance and data-driven insights.',
        'Engineered a multi-layered caching strategy using <strong>IndexedDB</strong> for client-side persistence and <strong>Redis</strong> for server-side caching, creating a highly performant, optimistic UI obsessed with speed.'
      ]
    }
  ];

  const awards = [
    {
      title: 'Google for Startups Cloud Program',
      issuer: 'Pre-Seed Funding',
      year: '2024',
      detail: 'Awarded funding and cloud credits in recognition of the project\'s innovative concept, strong technical foundation, and potential for market impact.'
    }
  ];
  
  // NEW SECTION DATA
  const competencies = [
    {
        title: "Rapid & On-the-Go Learning",
        detail: "Proven ability to quickly master new technologies and complex domains. The intensive 240-hour cybersecurity program on TryHackMe is a recent example of this self-directed, practical approach to skill acquisition."
    },
    {
        title: "AI-Powered Development",
        detail: "Professionally leverage the power of cutting-edge AI tools in both development and research to accelerate workflows, solve complex problems, and deliver robust solutions efficiently."
    }
  ];

</script>

<div class="container">
  <header class="card">
    <div class="card-left">
      <img src={photo} alt="Photo of {name}" class="profile-photo"/>
    </div>
    <div class="card-right">
      <h1>{name}</h1>
      <h2>{title}</h2>
      <div class="contact-info">
        <p><i class="fas fa-map-marker-alt"></i> <span>{location}</span></p>
        <p><i class="fas fa-phone"></i> <a href="tel:{phone}">{phone}</a></p>
        <p><i class="fas fa-envelope"></i> <a href="mailto:{email}">{email}</a></p>
        <p><i class="fab fa-linkedin"></i> <a href={linkedinUrl} target="_blank" rel="noopener noreferrer">{linkedin}</a></p>
        <p><i class="fas fa-globe"></i> <a href={websiteUrl} target="_blank" rel="noopener noreferrer">{website}</a></p>
      </div>
    </div>
  </header>

  <main class="cv-content">
    <section id="summary">
        <h3>Summary</h3>
        <p>{@html summary}</p>
    </section>

    <section id="skills">
      <h3>Technical Skills</h3>
      <div class="skills-grid">
        {#each skills as skill}
          <div class="skill-item">
            <strong>{skill.category}</strong>
            {#if skill.category === 'Languages'}
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
      <h3>Professional Experience</h3>
      {#each experiences as exp}
        <div class="job">
          <h4>{exp.title}</h4>
          <h5>{exp.company} | {exp.period}</h5>
          {#if exp.subtitle}<i>{exp.subtitle}</i>{/if}
          <ul>
            {#each exp.details as detail}
              <li>{@html detail}</li>
            {/each}
          </ul>
        </div>
      {/each}
    </section>

    <!-- NEW SECTION -->
    <section id="competencies">
      <h3>Core Competencies</h3>
      <div class="competency-grid">
         {#each competencies as competency}
            <div class="competency-item">
                <h4>{competency.title}</h4>
                <p>{competency.detail}</p>
            </div>
          {/each}
      </div>
    </section>

    <section id="awards">
        <h3>Awards & Recognition</h3>
        {#each awards as award}
            <div class="award-item">
                <h4>{award.title}</h4>
                <h5>{award.issuer} | {award.year}</h5>
                <p>{award.detail}</p>
            </div>
        {/each}
    </section>
  </main>
</div>