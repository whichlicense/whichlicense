# RFC (Request for Comments) Process

The RFC (Request for Comments) process is a standardised approach for proposing
and discussing changes impacting an entire organisation, community, platform, or
ecosystem. Its purpose is to provide a formalised framework for contributors to
propose changes and to facilitate a collaborative environment for discussion and
evaluation while promoting transparency and accountability. The process involves
collecting, reviewing, and documenting proposals related to platform
enhancements, as well as process and infrastructure improvements.

The WhichLicense organisation has set out to create a FOSS license compliance
platform built on open-source software for the open-source community. As part of
this commitment and our overarching goal of making license compliance accessible
and understandable for everyone, we believe it is essential to design the
platform in collaboration with the FOSS community. This approach will ensure
that the platform's features and functionality are aligned with the community's
needs and preferences.

To facilitate this collaboration and innovation, the WhichLicense organisation
has decided to introduce this RFC (Request for Comments) process as the official
means of proposing and discussing changes to the platform and larger ecosystem.
This meta-level RFC is intended to serve as an introduction to the RFC process
and its role in promoting collaboration and innovation within the community.
Furthermore, by adopting the RFC process, the organisation hopes to provide a
transparent and accountable framework for community members to propose and
evaluate changes. Moreover, this process will help us ensure that the platform
remains relevant and valuable to the community while also promoting the
organisation's commitment to accessibility and understanding in the realm of
FOSS license compliance.

## Prior Art

This present section provides a brief overview of the history and origins of the
Request for Comments (RFC) process, drawing upon
[Heather Flanagan's seminal work, "Fifty Years of RFCs" (RFC 8700)](https://www.rfc-editor.org/rfc/rfc8700.html).

The RFC Series is a fundamental document collection encompassing guidance,
experimental protocols, informational materials, and internet standards. Its
origins date back to 1969 when Steve Crocker published "Host Software," with the
original goal being to initiate conversations rather than establish an archival
record of a standard or best practice. However, as the community grew, the
publication process became more formal, and the purpose shifted to create a
canonical source of material published by the RFC Editor and preserve it
perpetually.

The RFC process was established to create a platform for communication and
collaboration among the ARPANET and internet networking communities. The concept
was to provide an open forum for discussions and the development of new ideas
and protocols. The RFC Series played a critical role in the internet's early
development and continues to be an essential tool for the internet community. As
a result, the RFC process has become an integral part of the internet's growth
and development, enabling the community to discuss and experiment with new
protocols and ideas.

Over 8500 RFCs have been published to date, and the material is accepted for
publication through the IETF, the IAB, the IRTF, and the Independent Submissions
streams, each with clear processes on how drafts are submitted and potentially
approved for publication as an RFC. The role of the RFC Editor was formalised in
1984, and the editor's goal is to produce readable, clear, consistent, and
reasonably uniform documents while maintaining the archival record of what has
been published.

The RFC Series has evolved from distribution through postal mail to electronic
distribution via FTP and email. The editorial process became more structured,
and authors were provided guidance on how to write an RFC. The RFC Editor
structure was reviewed, refined, and refined again, and in recent years, the
process to change the format of the RFC documents themselves has started.

Beyond the official RFC Series, its publication process has inspired many
project-specific RFC or general enhancement proposal processes across major
open-source community projects. These processes enable community-driven
discussions and collaborations on new ideas and enhancements, much like the
original RFC process.

Some examples of these projects include Java Enhancement Proposals (JEP) for
Java platform enhancements, Python Enhancement Proposals (PEP) for Python
language and library enhancements and Kubernetes Enhancement Proposals (KEP) for
Kubernetes enhancements. Moreover, many open-source projects such as Rust and
React have adopted the RFC process as their primary means of discussing new
proposals and improvements. As a result, the RFC process has become an essential
tool for open-source communities to collaborate, innovate, and drive the growth
and development of their projects.

## Motivation

The primary objective of the WhichLicense organisation is to establish a FOSS
license compliance platform that simplifies and streamlines license compliance,
making it accessible to all. Achieving this requires the creation of a unified
process that oversees all enhancements, ensuring the platform's features and
functionality align with the community's needs and preferences.

Adopting an RFC (Request for Comments) process offers a crucial advantage, as it
enables a clear differentiation between routine bug fixes and critical platform
decisions. This differentiation guarantees that changes are evaluated on their
individual merits, and significant modifications are subject to heightened
scrutiny and debate. Additionally, the RFC process yields detailed documentation
that outlines the feature designer and proposal champion's thought process,
making it easier for future contributors to build upon their initial vision and
proposed feature set.

To qualify as an enhancement in the context of this process, a proposed change
must meet specific criteria, including requiring two or more weeks of
engineering effort, making a significant change to the platform or the processes
and infrastructure by which it is developed, or being in high demand by the
community. This approach ensures that the efforts focus on the most impactful
changes that will provide the most meaningful benefit to the community.

### Goals

The following list of goals must be satisfied by the RFC process:

- **Community Involvement**: The RFC process should encourage active
  participation and contribution from the community to ensure the proposal
  reflects the users' needs.
- **Clear Documentation**: The RFC process should provide clear and concise
  documentation on how the RFC process works and what is expected of every
  proposal.
- **Reviews**: The RFC process should include a review and feedback mechanism to
  ensure the proposal has been thoroughly vetted and received constructive
  criticism.
- **Consistency**: The RFC process should ensure consistency and quality control
  by adhering to proposed standards or guidelines.
- **Transparency**: The RFC process should provide transparency by making the
  proposals and their progress publicly accessible.
- **Accessibility**: The RFC process should be accessible to all community
  members, regardless of their technical expertise.
- **Timeliness**: The RFC process should ensure proposals are reviewed and
  addressed promptly, without unnecessary delays.
- **Long-term Goals**: The RFC process should leverage a roadmap for future
  proposals to ensure that they are aligned with the long-term goals and
  objectives of the project.

### Non-goals

To ensure a clear and focused approach to the RFC process, it is vital to
establish what it should exclude in terms of its objectives and inclusions.
These exclusions can be outlined as follows:

- **Naming Process**: The RFC process should not aim to define a naming process
  for the proposals.
- **Template**: The RFC process should not define a content template that
  outlines writing instructions for creating RFCs.
- **Archive**: The RFC process should not establish an index that hosts all
  accepted RFCs nor an archive for all rejected or withdrawn ones.
- **Commitment**: The presence of an RFC on the roadmap only indicates that the
  proposal has been recorded from a technical perspective. There is no guarantee
  that anyone will work on it, much less that its end result will appear in
  future releases.

## Solution Proposal

The RFC process consists of distinct phases, roles, responsibilities, and
scenarios to provide a comprehensive and structured approach to the development
and implementation of proposed changes. The following sections outline these
components in detail to ensure a thorough understanding of the process.

### Lifecycle

A successful RFC passes through the following stages:

1. **Draft**: The author circulates the RFC for initial review and
   consensus-building.
2. **Published**: The RFC has been associated with a GitHub pull request on the
   WhichLicense organisation and is now available for a broader review by the
   community or specific committees.
3. **Submitted**: The RFC author declares the proposal ready for evaluation and
   becomes the proposal's champion.
4. **Candidate**: The RFC has been preliminarily accepted by a Platform Working
   Group for inclusion in the roadmap.
5. **Adopted**: The RFC has been accepted, realised and delivered in a release.

The author of a proposal has the ability to advance it from the _**Draft**_
phase to the _**Published**_ stage and from the _**Published**_ phase to the
_**Submitted**_ phase. In addition, the author has the option to revert the
proposal from the _**Candidate**_ phase to the _**Published**_ phase. It is
important to note that the champion of an RFC proposal holds the responsibility
and authority to move the proposal forward from any stage, with the exception of
_**Adopted**_ or _**Rejected**_, to the following stage:

- _**Withdrawn**_: Withdrawn by the author or champion from its current stage or
  even the roadmap. The proposal may be re-drafted and reintroduced at a later
  date.

The Platform Working Group has the authority to move a proposal from
_**Candidate**_ to _**Adopted**_, as well as from _**Published**_,
_**Submitted**_, or _**Candidate**_ to:

- **Rejected**: The proposal has been deemed unviable for further consideration,
  either due to being unfeasible, unlikely to come to fruition, or of little
  value in being maintained on the roadmap.

Long-lived informational or meta-level process RFCs, such as the current one,
may also be subjected to an additional state in the RFC process:

- **Prevailing**: This proposal state is characterised by the proposal being
  actively in use or not yet being superseded by any other existing proposal.

### Roles and Responsibilities

The RFC process involves several distinct roles working collaboratively to
facilitate successful proposal reviews and implementations. At its core, the
process is composed of the following three key roles:

- **Champion**: The Champion is the individual who proposes the change and takes
  responsibility for drafting the RFC document. They are responsible for
  articulating the need for the proposed change and ensuring that the RFC
  document is comprehensive and well-organised.
- **Community or Committee**: This group comprises individuals responsible for
  reviewing and providing initial feedback on the RFC documents. They are
  typically composed of subject matter experts, stakeholders, and other relevant
  individuals with the expertise necessary to assess the merits and feasibility
  of the proposed change.
- **Platform Working Groups**: These individuals or groups hold the authority to
  approve or reject the proposed change. They are responsible for assessing the
  feasibility and implications of the proposed change, including its potential
  impact on the existing system architecture, dependencies, and ecosystem.
  Ultimately, they are responsible for ensuring that the proposed change aligns
  with the overarching goals and objectives of the project.

### Risks and Mitigations

To ensure the efficacy of the RFC process, it is highly recommended that each
RFC contain a single key proposal or new idea, focusing on maintaining its
clarity and specificity. Additionally, public vetting of ideas before creating
an RFC can save significant time for the champion and help prevent the
submission of proposals that have previously been rejected or do not apply to
the broader WhichLicense community. Moreover, for an RFC to be accepted, it must
meet specific criteria, including a clear and comprehensive description of the
proposed enhancement, a net improvement over the current implementation,
approach or idea, and a solid proposed realisation that does not unduly
complicate the interpreter.

## Alternatives

While the notion of adopting an existing process was initially entertained by
the WhichLicense organisation, it is crucial to thoroughly evaluate whether such
a process was developed with the necessary assumptions and considerations
required for this specific project. Furthermore, replicating an unrelated
process carries the risk of yielding suboptimal outcomes, underscoring the need
for a bespoke approach tailored to the unique needs and requirements of the
project.

## Dependencies

Although this proposal does not have any direct dependencies on other proposals,
it is worth noting that RFCs 1, 2, 3, 4, and 5 serve as extensions of this
proposal, encompassing supplementary topics such as the definition of the RFC
template, establishment of an archival system, implementation of best practices
for community building, and development of a roadmap for enhanced tracking of
RFC progress and status. These complementary RFCs effectively expand upon the
core tenets of this proposal, providing a more comprehensive framework for its
successful execution.

### Required Infrastructure

All RFCs will be hosted and managed on GitHub, utilising the default fork and
pull request model. To ensure streamlined and efficient processes, it is vital
that the RFC adheres to the provided template and that the pull request is only
initiated upon approval by the proposal champion or developer(s) co-authoring
the RFC.

## Unresolved Issues

The current revision of the process lacks definitive guidelines regarding
contributions, thus compromising the quality and consistency of the codebase and
associated processes. As a result, it is of utmost importance that clear and
concise submission guidelines be established in a future revision, specifically
within the context of this proposal and repository.

## Potential Future Developments

As the project grows, expanding and improving its processes is essential.
Therefore, although the current version of the process might suffice for the
present project state and trajectory, there is always potential for further
enhancement. In this regard, several hypothetical scenarios and future
enhancement possibilities detailed in the subsequent sections could be
considered for inclusion in a revised version of the process as the project
advances.

### Pre-draft Discussions

Suppose the workload and amount of submitted proposals increase significantly,
or the quality of the proposals drops. In that case, it may be worth considering
adding a supplementary prerequisite step to encourage people to engage with the
community ahead of submitting their proposal in hopes that it can help to:

- **Gauge community interest**: Encouraging champions to present their ideas in
  a forum setting like GitHub Discussions could help determine whether the
  community is interested in the proposal, which can save time and effort for
  both the champion and the review team.
- **Flesh out the proposal**: Soliciting community feedback can lead to a more
  well-thought-out and detailed proposal and generate interest and momentum
  around the idea, increasing its chances of acceptance and implementation.
- **Reduce review workload**: Allowing the community to provide input on
  proposals before submission can reduce the number of proposals requiring
  review by the team, thus lightening their workload.

### Funding Model

Many open-source projects struggle with a lack of resources, such as committers
and contributors, which can lead to delays and inefficiencies in the RFC
process. As a result, proposals may not be accepted in due time or abandoned
altogether due to the lack of support. Therefore it might be advantageous to
assign group leads to oversee the availability of resources. By monitoring the
resources required for the individual proposals, the group leads can identify
and proactively address potential issues. For example, they can identify areas
where additional resources are needed and allocate resources to support the
proposal. This approach helps to ensure that proposals are adequately funded and
to complete the work required for the RFC process. This model takes inspiration
from [JEP1](https://openjdk.org/jeps/1) and may require a lifecycle extension to
include a "funded" phase. During this phase, the project would be judged by a
group or area lead to determine if it is fully funded. This approach aims to
increase efficiency and ensure the RFC process runs smoothly.

## Acknowledgements

This RFC process is heavily inspired by [IETF RFCs][ietf-rfc],
[JDK Enhancement-Proposals][jdk-jeps],
[Python Enhancement Proposal][python-peps], [Kubernetes KEPs][k8s-keps],
[Rust RFCs][rust-rfcs] and [React RFCs][react-rfcs].

[ietf-rfc]: https://www.ietf.org/standards/rfcs/
[jdk-jeps]: https://openjdk.org/jeps/1
[python-peps]: https://peps.python.org/pep-0001/
[k8s-keps]: https://github.com/kubernetes/enhancements/blob/master/keps/README.md
[rust-rfcs]: https://github.com/rust-lang/rfcs
[react-rfcs]: https://github.com/reactjs/rfcs
