# Verve N Veda

**A sovereign, privacy-respecting sanctuary of learning, creativity, public resources, and conscious exploration.**

Verve N Veda is a growing public ecosystem of free-access resource hubs, educational portals, creative tools, news and weather spaces, community projects, and browser-based applications.

The project is designed to help people find trustworthy pathways, learn without unnecessary barriers, create with independence, and move forward with greater clarity.

> **Pause. Learn. Verify. Find support. Create. Move forward with dignity.**

---

## Welcome

The Verve N Veda landing page serves as the front door to the entire ecosystem. Its calm, sanctuary-inspired design connects visitors to community resources, learning environments, creative spaces, public-interest tools, and related projects.

The landing page is built as a single self-contained `index.html` file using:

- Semantic HTML
- Modern CSS
- Vanilla JavaScript
- Inline SVG artwork
- Native browser accessibility features

It requires no framework, build system, database, account, analytics package, or external JavaScript dependency.

---

## Project Mission

Verve N Veda exists to make practical help, education, truth-centered inquiry, and creative opportunity easier to reach.

A parent may be searching for food, child care, school support, health services, or utility assistance. A veteran may need help locating benefits or community services. A person experiencing homelessness may need shelter, documents, legal aid, health care, or a safe first step. A student may need an accessible learning space. An artist may need tools to build, preserve, and share their work.

Verve N Veda brings those pathways together through portable, human-centered web tools designed around dignity rather than surveillance.

---

## The Landing Page

The root `index.html` includes:

- A responsive welcome experience inspired by the Verve N Veda visual identity
- An ivory, sage, charcoal, and muted-gold design system
- An original botanical lotus motif
- A searchable directory of Verve N Veda destinations
- A keyboard-accessible slide-out navigation menu
- Featured gateways for frequently visited spaces
- Responsive desktop, tablet, and mobile layouts
- Reduced-motion support
- Clear focus states and large interactive targets
- Automatic copyright-year display
- External links to the wider Verve N Veda ecosystem

The page directory and hamburger menu are generated from the same JavaScript destination list. A route only needs to be edited once for both navigation areas to update.

---

## Main Destinations

### Community and Support

- Family Hub
- Veteran Hub
- Homeless Hub
- Senior Hub
- LGBTQ+ Resources
- One Nation for All
- PLERA Live

### News, Weather, and Public Awareness

- The Verifier
- News Engines
- Weather
- Kids News Network
- River-to-Road

### Learning and Research

- Khaemenes Academy
- ARSHIF
- Firmament Law
- Games
- PLERA Search Gate

### Art, Music, and Creation

- Bazaar Art
- Music Hall
- Your Art Gallery
- My Art Gallery
- Professional Tools
- Web Site Design
- Editor

### Reflection and Wellbeing

- Journey Deeper
- The First Hour
- Sonic Sanctuary
- Faith
- Thyme to Mow

---

## Connected Sites

- **Verve N Veda:** `https://www.vervenveda.com`
- **Jennifer Pearl 2028:** `https://www.jenniferpearl2028.com`
- **Khaemenes Academy:** `https://www.khaemenesacademy.org`

---

## Design Principles

### Sovereign by Design

The core experience should remain portable, understandable, and independently hostable. Whenever practical, tools should function as static files without proprietary platforms or software lock-in.

### Privacy-Respecting by Default

The project avoids hidden tracking, unnecessary accounts, invasive profiling, and the collection of sensitive information. Browser storage may be used for clearly identified local preferences or saved work.

### Human Dignity First

Resource tools should help people without shame, stigma, accusation, or unnecessary barriers. Safety guidance should encourage pausing and verification rather than issuing unsupported verdicts.

### Accessible and Readable

Pages should use clear language, responsive layouts, strong contrast, keyboard-accessible controls, visible focus states, and practical navigation.

### Calm Rather Than Overwhelming

The interface should help visitors understand their choices and take the next useful step without being buried beneath visual noise.

### Easy to Preserve and Share

Single-file and static applications should be simple to download, archive, host, duplicate, and maintain.

---

## Technology

The core project intentionally uses a small and durable web stack:

```text
HTML5
CSS3
Vanilla JavaScript
Inline SVG
LocalStorage when appropriate
Static hosting
```

The current landing page does not require:

```text
React
Vue
Angular
Bootstrap
jQuery
Node.js
npm
A build pipeline
A server-side database
```

---

## Recommended Repository Structure

The repository can use clean route folders so each public page resolves through a simple first-word URL.

```text
vervenveda.github.io/
├── index.html
├── README.md
├── LICENSE.md
├── THIRD_PARTY_NOTICES.md
├── SECURITY.md
├── CODE_OF_CONDUCT.md
├── 404.html
├── CNAME
│
├── homeless/
│   └── index.html
├── veterans/
│   └── index.html
├── family/
│   └── index.html
├── senior/
│   └── index.html
├── verifier/
│   └── index.html
├── weather/
│   └── index.html
├── kids/
│   └── index.html
├── arshif/
│   └── index.html
├── music/
│   └── index.html
├── faith/
│   └── index.html
├── games/
│   └── index.html
├── khaemenes/
│   └── index.html
│
├── assets/
│   ├── images/
│   ├── icons/
│   └── posters/
│
└── docs/
    ├── deployment.md
    ├── contributing.md
    └── resource-review-policy.md
```

With this structure, a file stored at:

```text
homeless/index.html
```

can be reached at:

```text
https://www.vervenveda.com/homeless
```

---

## Editing the Navigation

The landing page keeps its destinations in one JavaScript array near the bottom of `index.html`.

Example:

```javascript
const destinations = [
  {
    title: "Homeless Hub",
    path: "/homeless",
    category: "Resources",
    description: "National resources, services, and pathways toward stability."
  }
];
```

To add a destination:

1. Create a route folder containing its own `index.html`.
2. Add a new object to the `destinations` array.
3. Add the destination to the `featured` array only when it should appear as a featured gateway.
4. Commit and publish the changes.

The directory and hamburger menu will update automatically.

---

## Running Locally

The site can usually be opened directly by selecting `index.html` in a browser.

For local testing through a simple web server:

```bash
python3 -m http.server 8080
```

Then visit:

```text
http://localhost:8080
```

A local server is recommended when testing route folders, browser security behavior, or features that do not run reliably from a `file://` address.

---

## Publishing with GitHub Pages

1. Place the landing page at the repository root as `index.html`.
2. Place each destination inside its matching route folder.
3. Open the repository's **Settings**.
4. Select **Pages**.
5. Publish from the intended branch and root folder.
6. Add the custom domain `www.vervenveda.com` in GitHub Pages settings.
7. Confirm the required DNS records with the domain provider.
8. Enable HTTPS after GitHub verifies the domain.

A `CNAME` file may be maintained at the repository root with:

```text
www.vervenveda.com
```

---

## Resource Review Standard

Public resource hubs should prioritize durable and accountable pathways, including:

- Official government agencies
- Public health and safety organizations
- Established nonprofit resource locators
- Crisis and support hotlines
- Legal-aid and benefit-navigation services
- Educational institutions
- Libraries, archives, and public learning resources

Whenever possible, resources should be reviewed for:

- Accuracy
- Availability
- Accessibility
- Geographic relevance
- Clear contact information
- Privacy and safety considerations
- Date of last review

A listed resource is not automatically an endorsement of every statement, policy, or service offered by the linked organization.

---

## Safety Notice

Verve N Veda tools are educational and informational. They are not substitutes for emergency services, medical care, legal advice, crisis counseling, law enforcement, or professional case management.

A person in immediate danger should contact local emergency services or an appropriate verified crisis service in their location.

Resource availability can change. Visitors should confirm time-sensitive details directly with the responsible organization.

---

## Privacy Notice

Core Verve N Veda applications are designed to function locally in the browser whenever practical.

When a tool uses browser storage, saved information remains on the user's device unless the user chooses to export, copy, clear, or share it. Contributors should avoid adding analytics, advertising trackers, fingerprinting, unnecessary third-party scripts, or server-side collection of personal information.

Any future feature that transmits or stores user information should be:

- Necessary
- Clearly disclosed
- Purpose-limited
- Securely designed
- Optional whenever possible
- Reviewed before deployment

---

## Accessibility Goals

Verve N Veda aims to support:

- Semantic page structure
- Keyboard navigation
- Visible focus indicators
- Screen-reader-friendly labels
- Strong text contrast
- Responsive text and layouts
- Large touch targets
- Reduced-motion preferences
- Plain-language instructions
- Printable and saveable resources

Accessibility improvements and careful testing are welcome.

---

## Contributing

Contributions should strengthen dignity, safety, education, accessibility, creativity, and public usefulness.

Helpful contributions may include:

- Repairing broken links
- Updating public resources
- Improving keyboard or screen-reader access
- Strengthening mobile layouts
- Reviewing safety language
- Adding printable materials
- Correcting factual errors
- Improving documentation
- Building new privacy-respecting tools
- Testing pages across browsers and devices

Please do not add features that:

- Collect unnecessary sensitive information
- Introduce hidden tracking or surveillance
- Make unsupported accusations about individuals
- Create barriers for vulnerable visitors
- Depend on inaccessible or proprietary systems without a clear reason
- Quietly transmit local user content to third parties

---

## Security

Potential security or privacy concerns should be handled according to `SECURITY.md`.

Do not publish sensitive vulnerability details in a public issue before the maintainer has had a reasonable opportunity to review them.

---

## Maintainer

Created and maintained by **Jennifer Pearl** as part of the Verve N Veda and Khaemenes Academy public-resource and learning ecosystem.

---

## License

Use of this repository is governed by the terms in [`LICENSE.md`](LICENSE.md).

Third-party materials, when present, should be documented in [`THIRD_PARTY_NOTICES.md`](THIRD_PARTY_NOTICES.md).

---

## Closing Statement

Verve N Veda is built as a calm place to begin.

Whether a visitor is seeking support, learning something new, verifying information, protecting a family member, exploring civic life, building a creative practice, or simply searching for a clearer path forward, the purpose remains the same:

> **Offer a trustworthy first step, preserve human dignity, and leave the door open for discovery.**
