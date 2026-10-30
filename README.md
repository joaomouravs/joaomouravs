## João Vitor Moura dos Santos

**Full-stack developer and UI/UX designer** in Rio de Janeiro, Brazil.
Software Engineering student at Universidade Veiga de Almeida (UVA), with a technical
degree in IT from CEFET/RJ.

I design the interface and build the system behind it: the data model, the API, the
tests and the deploy. Most of my work is freelance for small businesses and institutions,
and that code stays private. The repositories below are the ones I can share, and each
README explains the decisions behind the code, not only how to run it.

[Portfolio](https://joaovux.com.br) ·
[LinkedIn](https://www.linkedin.com/in/jo%C3%A3o-vitor-aa9a6724b/) ·
[Behance](https://www.behance.net/joovmourad) ·
[joaoviux@gmail.com](mailto:joaoviux@gmail.com)

<sub>Versão em português no fim da página.</sub>

### Selected work

**[Carteiro](https://github.com/joaomouravs/carteiro)** · Go, PostgreSQL, Next.js, Docker<br>
A self-hostable webhook delivery service. PostgreSQL is the queue: workers claim
deliveries with `FOR UPDATE SKIP LOCKED` and a lease, and a fencing token stops a worker
that lost its lease from overwriting a newer result. Deliveries are signed per the
Standard Webhooks spec, and the SSRF guard runs in the dialer, so DNS rebinding cannot get
around it. Seven ADRs, tests against a real database, and load tests in GitHub Actions:
1,549 deliveries/s with 4 workers after I found and fixed a lock convoy.

**[Biblioteca NEABI-NI](https://github.com/joaomouravs/neabi)** · Next.js 16, Prisma, PostgreSQL, Auth.js · [live](https://neabi-alpha.vercel.app)<br>
The catalog and reservation system I built for NEABI, the Afro-Brazilian and Indigenous
Studies Center at CEFET/RJ. Permissions are checked on the server for every action,
approvals claim a physical copy with a conditional update (a test races six approvals for
two copies, and exactly two win), uploads are validated by their binary signature, and the
Playwright suite fails if any page scrolls sideways at any of seven screen widths.

**[LUME Watches](https://github.com/joaomouravs/lume-watches)** · Next.js, GSAP, Tailwind CSS · [live](https://lume-psi-three.vercel.app)<br>
A product page for a fictional watch brand, built around a scroll-driven exploded view of
a 17-layer movement. A `sharp` script derives each layer's transparency and rotation pivot
from the source renders. The pinned gallery works with the keyboard, and
`prefers-reduced-motion` turns the page into a complete static version.

**[LUME Restaurant](https://github.com/joaomouravs/lume-restaurante)** · Astro, TypeScript, GSAP · [live](https://lume-restaurante-bice.vercel.app)<br>
A restaurant site rendered as static HTML, loading JavaScript only where there is
interaction. Opening hours live in one data file that drives the "open now" badge, the
structured data and the time slots of a three-step reservation flow.

**[Portfolio](https://github.com/joaomouravs/Portfolio)** · Next.js, TypeScript, GSAP · [live](https://joaovux.com.br)<br>
The source of my portfolio: a port of the original HTML/CSS/JS site that kept the design
value for value, cut images from 21 MB to 2.27 MB and validates every case study with Zod
at build time.

Client projects with private code, like **TuringBox** (equipment lending for CEFET/RJ) and
**Refúgio** (a membership club with recurring payments activated by webhook), are written
up as case studies on [my portfolio](https://joaovux.com.br).

### What I work with

- **Front end:** TypeScript, React, Next.js (App Router, Server Actions), Astro, Tailwind CSS, GSAP
- **Back end:** Go, Node.js, PostgreSQL, Prisma, sqlc, Supabase with RLS, Auth.js, Zod, PHP
- **Testing and delivery:** Vitest, Playwright, k6, GitHub Actions, Docker, Vercel, Prometheus, Grafana
- **Design:** Figma, design systems and tokens, prototyping, accessibility with WCAG 2.1 AA as the target

### Experience

- **IT Intern**, Procuradoria Geral do Estado do Rio de Janeiro (2025–2026)
- **IT Intern**, Prefeitura de Nova Iguaçu, Environment Department (2023–2024)
- **Freelance** full-stack development and UI/UX design

### Education

- Bachelor's in Software Engineering, UVA (in progress)
- Technical High School in IT, CEFET/RJ (2021–2025)

---

<details>
<summary><b>Versão em português</b></summary>

<br>

**Desenvolvedor full-stack e designer UI/UX** no Rio de Janeiro. Estudante de Engenharia
de Software na Universidade Veiga de Almeida (UVA) e técnico em Informática pelo CEFET/RJ.

Desenho a interface e construo o sistema por trás dela: o modelo de dados, a API, os
testes e o deploy. A maior parte do meu trabalho é freelance, para pequenos negócios e
instituições, e esse código é privado. Os repositórios abaixo são os que posso mostrar, e
cada README explica as decisões por trás do código, não só como rodar.

#### Projetos

**[Carteiro](https://github.com/joaomouravs/carteiro)** · Go, PostgreSQL, Next.js, Docker<br>
Serviço de entrega de webhooks auto-hospedável. O PostgreSQL é a própria fila: os workers
reservam entregas com `FOR UPDATE SKIP LOCKED` e um lease, e um fencing token impede que um
worker que perdeu o lease sobrescreva um resultado mais novo. As entregas são assinadas no
padrão Standard Webhooks, e a proteção contra SSRF roda no dialer, então DNS rebinding não
a contorna. Sete ADRs, testes contra banco real e testes de carga no GitHub Actions: 1.549
entregas/s com 4 workers depois que encontrei e corrigi um lock convoy.

**[Biblioteca NEABI-NI](https://github.com/joaomouravs/neabi)** · Next.js 16, Prisma, PostgreSQL, Auth.js · [no ar](https://neabi-alpha.vercel.app)<br>
Sistema de acervo e reservas que construí para o NEABI, o Núcleo de Estudos
Afro-Brasileiros e Indígenas do CEFET/RJ. As permissões são conferidas no servidor em toda
ação, a aprovação reivindica o exemplar com uma atualização condicional (um teste dispara
seis aprovações simultâneas para dois exemplares, e exatamente duas vencem), os uploads são
validados pela assinatura binária e os testes do Playwright falham se alguma página rolar
para o lado em qualquer uma de sete larguras de tela.

**[LUME Watches](https://github.com/joaomouravs/lume-watches)** · Next.js, GSAP, Tailwind CSS · [no ar](https://lume-psi-three.vercel.app)<br>
Página de produto de uma marca fictícia de relógios, construída em torno de uma vista
explodida de um calibre de 17 camadas controlada pelo scroll. Um script com `sharp` deriva
a transparência e o eixo de rotação de cada camada a partir dos renders originais. A
galeria fixada funciona pelo teclado, e com `prefers-reduced-motion` a página vira uma
versão estática completa.

**[LUME Restaurante](https://github.com/joaomouravs/lume-restaurante)** · Astro, TypeScript, GSAP · [no ar](https://lume-restaurante-bice.vercel.app)<br>
Site de restaurante gerado como HTML estático, que só carrega JavaScript onde há interação.
Os horários de funcionamento ficam em um único arquivo de dados que alimenta o selo "aberto
agora", os dados estruturados e os horários da reserva em três etapas.

**[Portfólio](https://github.com/joaomouravs/Portfolio)** · Next.js, TypeScript, GSAP · [no ar](https://joaovux.com.br)<br>
O código do meu portfólio: um porte da versão original em HTML/CSS/JS que manteve o design
valor por valor, reduziu as imagens de 21 MB para 2,27 MB e valida cada case com Zod no
build.

Projetos de clientes com código privado, como o **TuringBox** (empréstimo de equipamentos
para o CEFET/RJ) e o **Refúgio** (clube de sócios com pagamento recorrente ativado por
webhook), estão descritos como cases no [meu portfólio](https://joaovux.com.br).

#### Com o que trabalho

- **Front-end:** TypeScript, React, Next.js (App Router, Server Actions), Astro, Tailwind CSS, GSAP
- **Back-end:** Go, Node.js, PostgreSQL, Prisma, sqlc, Supabase com RLS, Auth.js, Zod, PHP
- **Testes e entrega:** Vitest, Playwright, k6, GitHub Actions, Docker, Vercel, Prometheus, Grafana
- **Design:** Figma, design systems e tokens, prototipação, acessibilidade com WCAG 2.1 AA como meta

#### Experiência

- **Estagiário de TI**, Procuradoria Geral do Estado do Rio de Janeiro (2025–2026)
- **Estagiário de TI**, Prefeitura de Nova Iguaçu, Meio Ambiente (2023–2024)
- **Freelancer** em desenvolvimento full-stack e design UI/UX

#### Formação

- Bacharelado em Engenharia de Software, UVA (em andamento)
- Ensino Médio Técnico em Informática, CEFET/RJ (2021–2025)

</details>
