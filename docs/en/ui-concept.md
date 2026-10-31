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
| D04 | Listening positions are available across devices. | A listener can resume the same episode and language edition on a smartphone at the position saved while listening on a computer, and vice versa. D11 defines positions per language edition. How the service recognises the same listener remains open. |
| D05 | Audio continues while the listener browses other pages within the platform, with a compact player that remains accessible. | Internal page navigation preserves the current playback session. The compact player remains reachable on the supported device sizes; its detailed controls and placement remain open. |
| D06 | At the end of a lecture, offer the next available episode and wait for the listener to start it. | Where a next episode exists, present it as a choice. Playback of the next episode begins only after the listener explicitly starts it. |
| D07 | The application interface is available in German and English. | Provide navigation, controls and interface text in both languages. Selection is independent of listening language under D10. Repository documentation remains English. |
| D08 | Show completed episodes and progress for each learning path. | Display the listener's completion status and path progress in addition to the saved listening position. D09 defines the completion trigger and manual correction; path progress calculation remains open. Progress indicators do not restrict episode selection under D03. |
| D09 | Mark an episode as completed automatically at the end of its lecture audio, and allow manual changes. | The listener can manually mark an episode as completed or undo that status. The shared status across language editions is defined in D12. |
| D10 | Interface language and listening language can be selected independently. | German menus can accompany an English lecture, and English menus can accompany a German lecture. Changing one selection does not force a change of the other. |
| D11 | Keep a separate listening position for each language edition. | Switching the listening language of an episode uses the saved position of the target edition; if no position is saved, that edition starts at the beginning. Positions remain available across devices under D04. |
| D12 | Share episode completion across German and English editions. | Completing either edition marks the logical episode as completed in both languages. Manual changes affect this common status. The same episode is counted once within a learning path, regardless of listening language. |

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

Detailed page layouts, additional player controls and navigation labels remain to be specified. Playback during internal navigation and at the end of a lecture is defined in D05 and D06. German and English interface and listening languages are independently selectable under D07 and D10. D11 defines the saved position used when switching listening language; D12 defines the shared episode completion.

## Proposed episode page

Proposal P01 for discussion: bring the full title, short description, learning objectives, readable prerequisites, place in the learning path, listening language, player, completion control and cheatsheet access together on one episode page. Present teaser or full lecture actions according to the listener's access. Q06 will determine whether the cheatsheet is readable on the page, downloadable as a PDF, or both. This proposed page arrangement remains separate from the confirmed decisions above.

## Open UI questions

| ID | Question | Why it matters |
| --- | --- | --- |
| Q02 | Which episodes contribute to the path progress total, including optional prerequisites and supplementary episodes? | D09 settles automatic completion and manual correction, and D12 settles completion across editions. The set of episodes included in the path total remains open. |
| Q03 | Which complete episodes serve as public samples, and how is access to the rest obtained? | Determines access labels and entry points. Prices, paid scope and Spotify entitlements remain open in the product documentation. |
| Q04 | Which controls and placement should the compact and full player provide, including seeking and playback speed? | Defines the player details. Continued playback during internal navigation is settled in D05; offering the next episode with an explicit start is settled in D06. |
| Q05 | How should initial language preferences be chosen and remembered, and how should an unavailable language edition be presented? | Independent selections and position handling are settled in D10 and D11. Defaults, preference persistence and edition availability states remain open. |
| Q06 | Should the cheatsheet be readable on the episode page, available as a PDF download, or both, and is the page arrangement in P01 appropriate? | Determines how supplementary material and episode information fit into the listening experience. |
| Q07 | What is the first delivery scope, and how should the path, catalogue and visual presentation relate? | Determines the page set, navigation emphasis and prototype boundaries. |
| Q08 | How should a listener be recognised across devices, and how should the UI handle a new device, no saved position or unavailable synchronisation? | Specifies access and resume states needed for D04 without choosing an account system or technical architecture. |

A framework, hosting provider, account system, payment mechanism and platform RAG feature have not been chosen. Technical implementation belongs in the web application repository after the relevant requirements are clarified.

## Decision provenance

D01 through D12 were confirmed by the user during the UI clarification on 31 October 2026. The open questions above retain the details that have not yet been decided. P01 is a proposed layout for clarification.
