# Non Praevalebunt – Catholic Doctrine Guard

*"…et portae inferi non praevalebunt adversum eam."* (Matthew 16:18)

A Crusader Kings III mod for **By God Alone** that keeps the Church's rites faithful to Catholic teaching. Rites may still differ in custom and discipline (liturgy, married priests, fasting, monastic rules), but never in faith or morals.

> **Status: v0.3.0.** Tested in game with Shadows of the Cross: 867 and 1066 starts (heresy outbreaks, signature heresies, condemnation, Seek Communion, mending the Schism). Expect rough edges.

## What it does

- **Guards the Church's rites.** If a rite of the Church picks up a forbidden doctrine or tenet (for example divorce allowed, polygamy, or a heresy like Adoptionism), the Church sets it right. Rites in good standing are checked after every rite change and once a month.
- **Locks the doors (v0.2).** Forbidden choices are refused or undone on the spot, with no banner or cost: the AI's yearly drift, newly founded rites, the AI Pope's choices, ecumenical councils (the Pope does not confirm a ruling against the faith, and writes to the faithful) and your own rite editor ("Confirm" refuses). See [`docs/v02-plan.html`](docs/v02-plan.html).
- **Keeps faithful rites from the heresy line (v0.2).** A rite that holds nothing forbidden is pulled back toward Roman practice before it reaches the game's heresy line, and no Pope can brand it a heresy.
- **Uses an approved list.** Every doctrine and tenet is marked allowed or forbidden. See [`docs/allowed-list.html`](docs/allowed-list.html).
- **Keeps the Pope Roman.** Every new Pope takes the Roman rite, so a drifted rite can never become "Catholicism".
- **Guards the Pope's bulls.** Within the Church, no bull can declare a forbidden tenet "in good standing" (for example Literalism), and none can condemn true Catholic teaching (for example Purgatory). If one slips through another route, the Pope sets it aside and writes to the faithful.
- **Pope as head before the Great Schism** (game rule, on by default). In 867 starts the Papacy heads the undivided Church, and Rome keeps that primacy even if the schism is prevented.
- **Calls the undivided Church Catholic.** Before the Great Schism the base game names it "Chalcedonianism". The mod names it "Catholicism", as the Church called herself.
- **Fixes start-of-game errors.** For example, the Mozarabic rite no longer starts with same-sex relations accepted.
- **Tenets corrected:**
  - *Be Fruitful and Multiply* no longer makes chastity a sin. It now costs −5% county tax, and within the Church parents gain piety for each child born of their marriage.
  - *Alexandrian Catechism* no longer makes zeal a sin.
  - *Adaptability* no longer makes fickleness a virtue.
- **Living heresies (v0.3).** Heresy outbreaks come about twice as often in the Church and hit its minor rites first. A rite that falls takes one classic heresy of its place and era (Adoptionism in Iberia before 1000, Monophysitism near the East, Gnosticism in the Balkans and Occitania, Simony elsewhere), so the game sees a real heresy. If Rome has not condemned it about five years later, the Pope does, with the game's own bull. A fallen rite that lays down every error comes home. See [`docs/v03-plan.html`](docs/v03-plan.html).
- **Seek Communion is a true return (v0.3).** When the Pope accepts a heresy back, its rites rejoin the Church and lay down every error; their leaders are absolved.
- **Mending the Schism always reunites with Rome (v0.3).** Whoever mends it, Orthodoxy rejoins Catholicism under the Pope.

## Compatibility

- Requires CK3 **1.21.x**. Built for the **By God Alone** DLC.
- Works **with or without Shadows of the Cross**, with no patch needed.
- Replaces these definitions. Other mods that change the same ones may conflict.
  - Tenets: `tenet_be_fruitful_and_multiply`, `tenet_adaptive`, `tenet_alexandrian_catechism`.
  - Doctrines: `doctrine_pluralism_righteous`, `doctrine_clerical_marriage_allowed`, `doctrine_clerical_marriage_disallowed`.
  - Triggers: `pam_tenet_can_be_permitted_trigger`, `pam_tenet_can_be_permitted_no_actor_trigger`, `pam_tenet_can_be_prohibited_trigger`, `pam_tenet_can_be_prohibited_no_actor_trigger`, `pam_tenet_ai_may_permit_trigger`, `pam_rite_can_be_declared_heresy_trigger`.
  - Effects: `pam_bull_notify_faith_rulers_effect`, `rite_yearly_hor_divergence_drift_commit_effect`, `rite_growth_resolve_differences_effect`, `ecumenical_council_conservative_backlash_effect`, `ecumenical_council_host_rite_adopt_doctrine_effect`, `pam_heresy_c1_pick_diverging_rite_effect`, `pam_heresy_fervor_reset_effect`, `pam_seek_communion_reconcile_faith_effect`, `mend_great_schism_scripted_effect`.
  - Script values: `pam_heresy_fervor_reset_component_1_value`, `_2_value`, `_3_value`, `pam_heresy_pulse_no_event_value`.
  - Decisions: `mend_the_great_schism_decision`.
  - The names of the faith `christian_faith`.

## Install (manual)

1. Copy the `non-praevalebunt/` folder into your CK3 user folder's `mod/` directory, for example `Documents/Paradox Interactive/Crusader Kings III/mod/non-praevalebunt/`.
2. In that same `mod/` directory, create `non-praevalebunt.mod` with the contents of `non-praevalebunt/descriptor.mod`, plus one line:
   `path="mod/non-praevalebunt"`
3. Enable **Non Praevalebunt** in your playset in the launcher.

## Repository layout

| Path | What it is |
|---|---|
| `non-praevalebunt/` | The mod itself. This is the folder the game loads. |
| `docs/` | Design pages (HTML): the recommendation, the allowed list, the heresy plan, the Great Schism, and more. |

## License

The mod's own code and docs are under the [MIT License](LICENSE).

`non-praevalebunt/common/religion/tenet_types/np_tenet_overrides.txt` and `non-praevalebunt/common/religion/doctrine_types/np_doctrine_overrides.txt` contain modified copies of definitions from Crusader Kings III. Those parts remain the property of Paradox Interactive and are included, as is usual for CK3 mods, only so the mod can change them. Crusader Kings III is a trademark of Paradox Interactive. This mod is not affiliated with or endorsed by Paradox Interactive.
