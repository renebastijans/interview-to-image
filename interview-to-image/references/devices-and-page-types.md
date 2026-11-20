# Structural devices and page types

Pick one device per page. Check sibling pages first so no two pages repeat one. The devices below are invented examples of the pattern: an idea made visible by an absence or a constraint.

## Example devices

| Device | How it is written |
|---|---|
| The customer is only a voice | Participants on a video call are faceless grey silhouette tiles; every customer line comes out of the laptop in a lightning-bolt-tailed bubble. Only the researcher is drawn, and never speaks or reacts |
| The product never appears | No product name in any bubble, sign or screen. Final panel: the laptop is in view, screen blank grey, "the one place the cool light should be, and is not" |
| Redaction bar | Wherever a name would be said or shown, a solid hand-inked black bar about seven letters wide. List every place it appears. "Never replace it with a real or invented name" |
| Where the cool light falls | One screen lights the room and carries the key object; in the next scene a different screen lights the room and the key object is not on it |
| Absence in the last screen | The thing the person needed is not on the final screen; nothing else is drawn to explain why |
| Chart restyle | Exact chart attached; "restyle, not redesign" |
| Answered notebook | An earlier page's notebook with answers added in a second hand-colour (ochre pencil), different slant, so they read as added later |

## Page types

**Voice page.** Same desk and room in all panels; only posture and notebook content change. Final panel looks down over the shoulder at a notebook with exactly the stated lines. State: "forearm and sleeve visible running from body to hand, nothing cropped between them". Ban numbers, charts, faces, names, titles. If two meetings are drawn as one, flag it and offer a "A WEEK LATER..." gutter.

**Story page.** Four panels, one gutter for time ("ON THE WAY HOME...", "MONTHS LATER..."), final panel the quiet centre. Panels 1 to 3 can be a success; the last is not a failure. See the rules below.

**Data page.** Restyle of a chart you built. Figure groups drawn as small markers (no bubbles, no faces), a flat band for constant things, no arrows linking an occasion to a bar. Fallback if the generator distorts bars: keep its paper, wash and figures, and place the exact SVG bars on top.

**Answers or recommendations page.** Top panel full ink and wash (what was heard); bottom row grey pencil on cream, no wash (what is proposed, nothing has happened). Every count "of N", no percentages, a closing line that says there is no outcome data. With two reference images, if the generator redraws the sketches, recheck all lettering or generate the halves separately and join them.

## Story-page rules

- **Make rank or role legible without a label.** E.g. a manager wears a long grey coat in every panel, the team wears shirts only, and "nothing in the panel may label them as manager".
- **In-scene lines only.** Lines said afterwards, in the interview, about the moment do not go into the scene as speech or thought. Put them in "must not say" or outside the panels as an unattributed quote.
- **Pick the line that carries the finding**, not the most dramatic one.
- **Say what a disclosure is about.** Do not add a motive, reward or detail to a line the source does not have.
- **Do not show mechanism the source lacks:** how a document was passed on, QR codes, sign-up sheets, tallies, crowds.
- **Do not show results** the source does not report.
- **Not doing something is not difficulty.** If the person says they did not bother, do not draw a struggle with a phone, a search or a broken link.
- **Do not claim whether something counted or worked** unless the source says so.
- **When two story pages run together**, make characters different at a glance (hair, build, age, setting), and mirror the last panels deliberately.
- **Disclosures go first.** If the person disclosed a bias before explaining, the page opens that panel with the disclosure.
- **Text on walls and screens:** only the exact words given; "no wall charts with lettering".

## Generator behaviour seen in testing (Gemini, Nano Banana, "Pro" mode)

- Without a lettering block it added an extra title, repeated and garbled a line for a third speaker, and drew a QR-like pattern on a phone.
- Continuity across panels of one scene: give each person a fixed seat (left, middle, right) and a distinct look (hair, skin tone, clothing); say "panel 2 is the next moment of panel 1, same table, same seats" and "the bubble tail points to the speaker". Without this it redrew people as different characters and attached a line to the wrong person.
- A long lettering block turned "four panels in a row" into a 2x2 grid. Say "four panels in one row, left to right" if it matters.
- The vertical gutter text may come back horizontal.
