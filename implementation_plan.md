# Implementation Plan — Site Sections

## Navigation

- [Home / Hero](#home-hero)
- [About](#about)
- [Experience](#experience)
- [Projects / Portfolio](#projects-portfolio)
- [Blog / Writings](#blog-writings)
- [Talks & Media](#talks-media)
- [Skills & Endorsements](#skills-endorsements)
- [Education & Certifications](#education-certifications)
- [Open Source & Contributions](#open-source-contributions)
- [Resume / CV](#resume-cv)
- [Contact](#contact)
- [Footer & Utility Pages](#footer-utility-pages)

Using the LinkedIn profile (www.linkedin.com/in/jose-m-cordoba) as the source of truth, below are recommended site sections, their purpose, and quick implementation notes (routes, components, data sources).

<a id="home-hero"></a>

## Home / Hero

- Purpose: Immediate introduction (name, title, elevator pitch) and primary CTAs (View resume, Contact, Latest post).
- Route: `/`
- Components: `Hero`, `FeaturedProjects`, `LatestPost`, `CTAButtons`.

<a id="about"></a>

## About

- Purpose: Longer professional summary, biography, high-level timeline, headshot.
- Route: `/about`
- Components: `AboutHero`, `Timeline`, `Values`.
- Data: Static markdown or JSON (for easy editing).

<a id="experience"></a>

## Experience (Career timeline)

- Purpose: Roles, companies, short descriptions and links (reflect LinkedIn chronology).
- Route: `/experience`
- Components: `ExperienceList`, `ExperienceItem` (expandable details), filters by type (startup, leadership).
- Data: JSON or frontmatter-driven markdown per role.

<a id="projects-portfolio"></a>

## Projects / Portfolio

- Purpose: Showcase notable projects, startups, open-source work with images, tech stack, links, and short case studies.
- Route: `/projects`
- Components: `ProjectGrid`, `ProjectCard`, `ProjectDetail` (lazy-loaded).
- Data: `content/projects/*.md` or a JSON index for metadata.

<a id="blog-writings"></a>

## Blog / Writings

- Purpose: Articles, essays, technical posts, and talks. Supports discoverability and SEO.
- Route: `/blog` and `/blog/:slug`
- Components: `PostList`, `PostItem`, `PostPage` (markdown rendering with syntax highlighting).
- Data: `content/blog/*.md` (frontmatter: title, date, tags, summary).

<a id="talks-media"></a>

## Talks & Media

- Purpose: Presentations, podcasts, videos, slides, and event history.
- Route: `/talks`
- Components: `TalkList`, `TalkItem`.

<a id="skills-endorsements"></a>

## Skills & Endorsements

- Purpose: Summary of technical and leadership skills, proficiency levels, and badges/certifications.
- Route: `/skills`
- Components: `SkillsGrid`, `CertificationList`.

<a id="education-certifications"></a>

## Education & Certifications

- Purpose: Degrees, courses, and notable certifications (brief entries linking back to evidence if available).
- Route: `/education`

<a id="open-source-contributions"></a>

## Open Source & Contributions

- Purpose: Highlight repositories, notable PRs, and community work (link to GitHub).
- Route: `/opensource`
- Components: `RepoList` (could be dynamic via GitHub API or static curated list).

<a id="resume-cv"></a>

## Resume / CV (Downloadable)

- Purpose: Provide a printable, up-to-date resume PDF and an HTML page variant for quick scanning.
- Route: `/resume` + `GET /resume.pdf`

<a id="contact"></a>

## Contact

- Purpose: Contact form, email link, social links (LinkedIn, GitHub, Twitter), newsletter signup (optional).
- Route: `/contact`
- Components: `ContactForm` (use mailto or third-party form provider), `SocialLinks`.

<a id="footer-utility-pages"></a>

## Footer & Utility Pages

- Purpose: Privacy, terms, sitemap, small bio, and social links.
- Route: `/privacy`, `/sitemap.xml` (generate at build), etc.

Implementation notes and conventions

- Routing: add pages to `src/router/index.ts` using lazy-loading for large pages. Example:

  { path: '/projects', component: () => import('@/views/Projects.vue') }

- Content: prefer markdown files for `blog` and `projects` to keep content editable and versioned. Place under `content/`.
- Styling: use Tailwind utilities consistently; create small presentational components in `src/components/`.
- Data sources: keep canonical data in `content/` (markdown/json). Use GitHub API only for optional live repo lists.
- Tests: add unit tests for key components under `src/__tests__/` following the existing `App.spec.ts` pattern.

Next steps

- Wire up the `routes` and create skeleton views for each section.
- Add content files for `about.md`, a few `projects/*.md`, and a sample `blog/hello-world.md`.
- I can scaffold the routes and basic page components now — tell me if you want that scaffolded automatically.
