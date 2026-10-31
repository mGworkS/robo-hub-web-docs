# UI concept and open questions

Updated: 31 October 2026

## Product foundation

The [product concept](https://github.com/mGworkS/learning-platform-docs/blob/main/docs/en/concept.md) defines demanding technical audio lectures for experienced, curious engineers. Listening is the core experience; cheatsheets supplement the same subject matter. Learning editions are German and English. The interface should be modern and simple on computers, tablets, Android and Apple devices.

The content hierarchy is subject area → series → episode. A learning path can connect episodes across series. Humanoids is the current subject; robotics and perception and RAG systems follow later.

## Confirmed UI choices

The following choices were confirmed in the UI clarification on 31 October 2026.

| ID | Choice | Meaning |
| --- | --- | --- |
| D01 | Learning paths structure discovery and progression. | Represent the existing learning offer and its progression, using the humanoids structure below as the example. This does not yet decide whether the interface also offers an equally prominent catalogue. |
| D02 | Visitors without signing in can listen to teasers and selected complete lectures. | Complete samples must be distinguishable from teasers. The particular sample episodes and access to other lectures remain open. |

## Learning path example: Humanoids

Follow the [agreed humanoids structure](https://github.com/mGworkS/humanoid-pod-assets-docs/blob/main/docs/en/humanoids_structure.md) and the [series concept](https://github.com/mGworkS/humanoid-pod-assets-docs/blob/main/docs/en/concept.md). The German terms below come from the existing [language and series mapping](https://github.com/mGworkS/humanoid-pod-assets-docs/blob/main/docs/en/storage_and_webapp.md); final navigation wording remains open.

| Place in the offer | Existing German term | Canonical English series | Role |
| --- | --- | --- | --- |
| Entry when needed | Vorwissen | Prerequisites | Establish required knowledge; listeners may skip knowledge they already have. |
| Main path 1 | Grundlagen | Foundations | Build a systematic understanding. |
| Main path 2 | Vertiefung | Advanced | Develop deeper technical connections. |
| Main path 3 | Praxis und Integration | Practice and Integration | Select, connect and assess systems in practice. |
| Main path 4 | Strategie und Management | Strategy and Management | Build and lead a robotics department. |
| Supplementary | Deep Dives | Deep Dives | Answer concrete questions arising during listening or application. |
| Time specific | What’s Hot | What’s Hot | Put scientific, technical and business developments in context. |

The main path follows the order shown after any needed prerequisites. Deep Dives can be relevant during the main path or afterwards; they are not a compulsory final stage. What’s Hot supplies time specific context. The source concept uses Deep Dives in place of the former Hot Takes label.

This is a content progression, not a confirmed sequential unlocking rule. Episode counts and content prerequisites remain owned by the content documentation and are not generalised from humanoids to other subjects.

## Information available to the UI

Existing [editorial metadata](https://github.com/mGworkS/humanoid-pod-assets-docs/blob/main/docs/en/metadata_and_versioning.md) supplies episode titles, short descriptions, subject and series, audience, objectives, readable prerequisites and keywords. Public episode references use full titles; stable IDs associate content and language editions internally.

Detailed page layouts, player behaviour, navigation labels and language switching are still to be specified. The bilingual learning offer does not itself decide the languages of interface controls.

## Open UI questions

| ID | Question | Why it matters |
| --- | --- | --- |
| Q01 | Is the main path a recommendation with direct access to any entitled episode, or does completing an episode unlock the next one? | Determines navigation, episode actions and completion states. Skipping familiar prerequisites is already allowed. |
| Q02 | What listening position and path progress should be remembered, and should it be available across devices? | Determines the return experience and whether an account is needed for synchronisation. |
| Q03 | Which complete episodes serve as public samples, and how is access to the rest obtained? | Determines access labels and entry points. Prices, paid scope and Spotify entitlements remain open in the product documentation. |
| Q04 | Which player controls and playback continuity are required? | Determines how listening works while browsing or returning later. |
| Q05 | How should users select interface and content languages and reach the equivalent episode? | Determines language navigation and edition availability states. |
| Q06 | Where should descriptions, prerequisites, teasers and supplementary cheatsheets appear? | Determines episode and learning path page structure. |
| Q07 | What is the first delivery scope, and how should the path, catalogue and visual presentation relate? | Determines the page set, navigation emphasis and prototype boundaries. |

A framework, hosting provider, account system, payment mechanism and platform RAG feature have not been chosen. Technical implementation belongs in the web application repository after the relevant requirements are clarified.

## Clarification record

| Date | Source | Result |
| --- | --- | --- |
| 31 October 2026 | User points to the existing learning offer as the learning path example. | D01; retain the source structure and clarify the remaining interaction rules. |
| 31 October 2026 | User selects teasers and selected complete lectures for visitors without signing in. | D02; sample selection and access to remaining lectures are unresolved. |
