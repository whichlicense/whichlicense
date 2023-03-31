# RFC (Request for Comments) Index

This proposal for an RFC Index aims to establish a centralised archive for RFCs,
which would serve as an efficient solution for achieving easy accessibility,
discoverability, and transparency of all ongoing and accepted RFC proposals.
Creating such an archive would facilitate ready access for all interested
parties, enabling them to review and scrutinise the proposals, which would be
readily visible and available. Consequently, the RFC Index would provide a
valuable tool for keeping abreast of the latest platform developments, fostering
a better-informed community.

## Prior Art

Establishing a central index is a venerable practice in open-source projects
that feature RFC-like processes. An exemplary instance of this practice is the
[Java Enhancement Proposal (JEP) 1](https://openjdk.org/jeps/1), which promotes
the creation of a centralised archive that preserves all Java language
proposals. The proposal strives to ensure easy accessibility and transparency
for all interested parties, enabling a meticulous review and scrutiny of
proposals, as well as the long-term preservation of all decisions and their
rationales. This notion is consistent with the essence of the RFC Index
proposal, which seeks to establish a centralised archive for RFCs related to
WhichLicense's platform and services. Moreover,
[JEP 1](https://openjdk.org/jeps/1) endeavours to encourage collaboration and a
more knowledgeable user base, which are also crucial objectives of the RFC Index
proposal. By utilising central web pages for publishing proposals, communities
and platforms can remain responsive, up-to-date, and pertinent to the needs of
their users.

Another notable example is the Rust community's employment of
[The Rust RFC Book](https://rust-lang.github.io/rfcs/0002-rfc-process.html),
which serves as the official source of truth for all proposals and provides a
structured approach to the Rust language development process. The book offers a
structured approach that ensures proposals are comprehensively documented,
easily accessible, and transparent, aligning with the goals of the RFC Index
proposal. Moreover, the book offers references that enable individuals and the
larger community to actively participate in the development process, promoting
collaboration and a more knowledgeable user base. By streamlining proposal
management, promoting transparency and accountability, and fostering a more
informed user base, The Rust RFC Book has proved highly beneficial for the Rust
community.

## Motivation

This proposal aims to present an intricate plan for translating the abstract
goals of the RFC Index proposal into a meticulously designed and functional
webpage. More specifically, the proposal delineates the process of automatically
converting the proposal format, currently in Markdown form as defined in RFC 1,
into sophisticated, static HTML pages. Accomplishing this objective mandates a
comprehensive analysis of the technologies and tools that will fuel and automate
the conversion process, as well as a discerning assessment of the design
elements that will render the resulting webpage user-friendly and aesthetically
pleasing. By executing this proposal, the WhichLicense organisation intends to
optimise the management of proposals, augment transparency and accountability,
and, above all, cultivate collaboration and engagement within the community.

### Goals

The following list of goals must be satisfied by the implementation of this
proposal:

- **Discoverability**: The RFCs must be hosted on a dedicated index to increase
  their visibility to search engines and developers who may not be familiar with
  GitHub or our specific RFC process, thus expanding the audience and fostering
  collaboration.
- **Navigation**: A chronological list of all RFCs must be created to allow for
  easy browsing and streamlined access.
- **Internal Linking**: Related RFCs must be linked to provide additional
  context and information for developers, enabling informed decision-making and
  feedback.
- **Enable Backlinking**: A static resource location with a standardised key
  should be provided to enable embedding references to proposals on other
  websites and mediums, thereby promoting the building of links from external
  sources to the RFCs. This hosting strategy will also enhance the website's
  authority and relevance in search engine rankings.
- **Content Optimisation**: The metadata encoded in the RFC structure, as
  provided by the template proposal, should be utilised to embed relevant
  keywords, optimised titles and meta descriptions, and apply appropriate tags
  and categories, thus increasing searchability and discoverability by search
  engines.
- **Multimedia Content**: To elucidate complex concepts and improve
  accessibility, multimedia content, such as images, code snippets, and
  diagrams, should be employed, ultimately benefiting search engine optimisation
  by providing additional context and information.
- **Call to Action**: Clear calls to action, such as "submit feedback" or "join
  the discussion," should be included to encourage developers to participate in
  the decision-making process and ensure that everyone has an opportunity to
  provide their input and contribute to the development of the WhichLicense
  platform.

### Non-goals

To ensure clarity and focus in the definition and implementation of the RFC
index, it is imperative to clearly define what it should not aim to achieve or
include:

- **Metadata Definition**: Standardise or limit the metadata to be displayed
  alongside the proposal content.
- **Promotion Strategy**: Create a social media promotion or general marketing
  strategy tied to the publication of the RFCs.

## Solution Proposal

By leveraging modern web technologies, we propose a sophisticated solution to
host RFCs on a website in a manner that is collaborative and optimised for
search engines. Through the integration of Next.js, gray-matter, remark, Prism,
GitHub Actions, GitHub Pages, and a dedicated subdomain on whichlicense.com, an
interconnected pipeline can be created that seamlessly converts raw markdown RFC
proposals with YAML Ain't Markup Language (YAML) metadata headers into stylised
webpages that are easily searchable and highly discoverable.

To ensure optimal Search Engine Optimisation (SEO), the solution extracts
metadata from each RFC proposal and generates appropriate SEO metadata to
enhance the website's searchability. In addition, by employing these techniques,
the RFC Index can help foster a thriving community around the RFC process and
build a collaborative environment where developers can easily submit, discuss,
and refine their proposals.

### Design Details

The design of the index for WhichLicense RFCs has been carefully crafted to
ensure an intuitive and visually pleasing experience for users. At the top of
the page, a minimalist header displays the organisation's name on the left-hand
side, while a link to the raw markdown RFC proposal on GitHub can be found on
the right-hand side.

WIREFRAME

To optimise usability, the index layout has been organised into a three-column
design, as illustrated in Figure 1. The middle column of the index displays the
rendered and stylised content of the selected RFC proposal, making it easy to
read and visually appealing. This centre column allows users to find the bulk of
the information they need to understand the proposal in question.

The left-hand column of the index provides links to all available RFCs, enabling
quick and easy navigation. This column is beneficial for users who want to
explore different proposals or compare and contrast the content of different
RFCs. By providing easy access to all available proposals, this column also
ensures that users can quickly find what they're looking for without manually
entering multiple page links.

Finally, the right-hand column of the index provides users with a structured
breakdown of associated metadata, such as the creator and champion of the
proposal or other dependent RFCs. This information is critical for users who
want to contact the relevant parties or understand the context behind a
particular proposal. By providing this information in a structured format, the
index ensures that users can quickly find the information they need to engage
with the proposals effectively.

### Risks and Mitigations

To enable the publication of the proposals on a subdomain of the WhichLicense
organisation, it is necessary to convert the markdown-based proposals hosted on
GitHub into distinct and aesthetically pleasing HTML pages using the process
mentioned above. However, since this process solely creates an HTML version of
the current snapshot of proposals in the repository, it poses the potential risk
of not being in sync with the latest changes without requiring regeneration. To
circumvent this issue, caching, Next.js's incremental content generation, and a
push-based GitHub Action workflow will be employed to recurrently re-publish the
webpage with every accepted change. This thorough approach guarantees that the
most recent version of the proposals is consistently available and that all
SEO-related metadata remains fresh, correct, and available for re-scans by
search engines.

## Alternatives

The decision to keep the RFCs hosted solely on GitHub may be a practical choice
due to its ease of use and convenience. However, it also has its limitations.
One of the major drawbacks is the lack of opportunities for community creation,
which is crucial for the success of any project. Without a community, generating
feedback, fostering collaboration, and gaining traction for the project becomes
challenging.

Another option is using the existing GitHub Page's markdown renderer, which can
automatically render markdown files into static HTML pages. This approach is
relatively straightforward and requires minimal effort. However, it does come
with limitations in terms of customisation options for navigation, content
layout, and other process-specific opportunities like call-to-action
integrations. As a result, it may not be suitable for more large-scale RFC
archiving needs or those with specific branding requirements.

To overcome these limitations, a custom pipeline can be implemented, as
previously mentioned. This approach allows for greater flexibility and
customisation, creating a more unique and engaging user experience.
Additionally, it enables the native integration of branding across the main
website, index, and cloud services in the future, providing a cohesive user
experience.

## Dependencies

The scope of this proposal builds upon the foundation laid by RFC 0 and RFC 1 by
expanding the availability and reach of the proposals beyond the hosting GitHub
repository and its associated issues and pull requests.

### Required Infrastructure

The RFC process currently utilises GitHub for storing proposals, associated
issues, and pull requests. This proposal extends the usage of GitHub by
leveraging GitHub Pages to host the generated static pages and by utilising
GitHub Actions to automate the deployment process. By doing so, the proposal
enhances the accessibility of the RFC process and makes it easier for developers
to participate in the decision-making process.

## Potential Future Developments

While this proposal provides a rudimentary yet flexible approach for an RFC
archive, it's important to note that there are numerous possibilities and
considerations to be made for the future development of the RFC Index. In
addition, as the technology landscape and community needs evolve, it's important
to reassess and update the RFC Index to ensure that it continues to meet the
needs of its users.

- **Unified Branding**: Having a unified branding for the WhichLicense
  organisation and services towards the index can create a consistent and
  recognisable brand identity, enhancing the credibility and trust of the
  organisation and its offerings.
- **Interactive Diagrams**: Integrating interactive multimedia such as
  Mermaid.js diagrams, which are already natively supported in markdown hosted
  on GitHub, can further enhance the readability and understanding of the RFC
  content, making it more accessible to a broader audience.
- **Version Control**: Providing a clear version history of the RFCs can help
  developers understand the proposals' evolution over time. Highlighting this
  metadata can also help track changes and ensure everyone is working with the
  most up-to-date information.
- **Content Organisation**: Organising the RFCs into different categories and
  subcategories can make it easier for developers to find what they need
  quickly. This structuring approach can also help with SEO, as search engines
  can understand the website's structure and provide more relevant search
  results. Moreover, a clear and concise navigation structure can enhance the
  user experience and increase engagement.
