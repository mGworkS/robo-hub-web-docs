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
| D03 | The main path is a recommendation; all episodes available to the listener can be selected directly. | Starting an available episode does not depend on completing earlier episodes. Keep the recommended order and content prerequisites visible as guidance. |
| D04 | Listening positions are available across devices. | A listener can resume the same episode on a smartphone at the position saved while listening on a computer, and vice versa. How the service recognises the same listener remains open. |
| D05 | Audio continues while the listener browses other pages within the platform, with a compact player that remains accessible. | Internal page navigation preserves the current playback session. The compact player remains reachable on the supported device sizes; its detailed controls and placement remain open. |
| D06 | At the end of a lecture, offer the next available episode and wait for the listener to start it. | Where a next episode exists, present it as a choice. Playback of the next episode begins only after the listener explicitly starts it. |
| D07 | The application interface is available in German and English. | Provide navigation, controls and interface text in both languages. Whether interface and listening languages are selected independently remains open. Repository documentation remains English. |
| D08 | Show completed episodes and progress for each learning path. | Display the listener's completion status and path progress in addition to the saved listening position. The completion rule and path progress calculation remain open. Progress indicators do not restrict episode selection under D03. |

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

The progression above is recommended guidance under D03. Episode counts and content prerequisites remain owned by the content documentation and are not generalised from humanoids to other subjects.

## Information available to the UI

Existing [editorial metadata](https://github.com/mGworkS/humanoid-pod-assets-docs/blob/main/docs/en/metadata_and_versioning.md) supplies episode titles, short descriptions, subject and series, audience, objectives, readable prerequisites and keywords. Public episode references use full titles; stable IDs associate content and language editions internally.

Detailed page layouts, additional player controls, navigation labels and language switching remain to be specified. Playback during internal navigation and at the end of a lecture is defined in D05 and D06. German and English are confirmed for both learning editions and the application interface; their selection behaviour remains open.

## Open UI questions

| ID | Question | Why it matters |
| --- | --- | --- |
| Q02 | What counts as completing an episode, can the listener change its completion status manually, and which episodes contribute to path progress? | Defines the rules behind the episode completion and path progress indicators confirmed in D08. Device availability of the listening position is already confirmed in D04. |
| Q03 | Which complete episodes serve as public samples, and how is access to the rest obtained? | Determines access labels and entry points. Prices, paid scope and Spotify entitlements remain open in the product documentation. |
| Q04 | Which controls and placement should the compact and full player provide, including seeking and playback speed? | Defines the player details. Continued playback during internal navigation is settled in D05; offering the next episode with an explicit start is settled in D06. |
| Q05 | Should interface and listening languages be selected independently, and how should users switch to the equivalent episode? | German and English interface availability is settled in D07. Selection, switching behaviour and edition availability states remain open. |
| Q06 | Where should descriptions, prerequisites, teasers and supplementary cheatsheets appear? | Determines episode and learning path page structure. |
| Q07 | What is the first delivery scope, and how should the path, catalogue and visual presentation relate? | Determines the page set, navigation emphasis and prototype boundaries. |
| Q08 | How should a listener be recognised across devices, and how should the UI handle a new device, no saved position or unavailable synchronisation? | Specifies access and resume states needed for D04 without choosing an account system or technical architecture. |

A framework, hosting provider, account system, payment mechanism and platform RAG feature have not been chosen. Technical implementation belongs in the web application repository after the relevant requirements are clarified.

## Clarification record

| Date | Source | Result |
| --- | --- | --- |
| 31 October 2026 | User points to the existing learning offer as the learning path example. | D01; retain the source structure and clarify the remaining interaction rules. |
| 31 October 2026 | User selects teasers and selected complete lectures for visitors without signing in. | D02; sample selection and access to remaining lectures are unresolved. |
| 31 October 2026 | User chooses a recommended main path with all accessible episodes directly selectable. | D03 resolves Q01; sequential completion is not an access condition. |
| 31 October 2026 | User confirms continuing on a smartphone from the listening position saved on a computer. | D04 resolves the device availability part of Q02; completion tracking and listener recognition remain open. |
| 31 October 2026 | User chooses continued playback with an accessible compact player while browsing the platform. | D05 resolves the internal navigation part of Q04. |
| 31 October 2026 | User chooses to offer the next episode and wait for the listener to start it. | D06 resolves the end of lecture behaviour in Q04; detailed player controls remain open. |
| 31 October 2026 | User selects German and English for the application interface. | D07 settles interface language availability; language selection and switching remain open in Q05. |
| 31 October 2026 | User chooses to display completed episodes and progress for each learning path. | D08 settles whether these indicators are included; completion and calculation rules remain open in Q02. |
