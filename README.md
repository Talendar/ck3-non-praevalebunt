# Non Praevalebunt – Catholic Doctrine Guard

*"…et portae inferi non praevalebunt adversum eam."* (Matthew 16:18)

A Crusader Kings III mod for **By God Alone** that keeps the Church's rites faithful to Catholic teaching. Rites may still differ in custom and discipline (liturgy, married priests, fasting, monastic rules), but never in faith or morals.

> **Status: v0.1.1.** The first in-game test passed (867 start, with Shadows of the Cross). Expect rough edges.

## What it does

- **Guards the Church's rites.** If a rite of the Church picks up a forbidden doctrine or tenet (for example divorce allowed, polygamy, or a heresy like Adoptionism), the Church sets it right. Rites in good standing are checked after every rite change and once a month.
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
- **Heresies still happen.** Heresy outbreaks and historical heresies (Cathars, Waldensians…) work as in the base game. The guard leaves heretical rites alone.

## Compatibility

- Requires CK3 **1.21.x**. Built for the **By God Alone** DLC.
- Works **with or without Shadows of the Cross**, with no patch needed.
- Replaces these definitions: tenets `tenet_be_fruitful_and_multiply`, `tenet_adaptive`, `tenet_alexandrian_catechism`; the doctrine `doctrine_pluralism_righteous`; the triggers `pam_tenet_can_be_permitted_trigger`, `pam_tenet_can_be_permitted_no_actor_trigger`, `pam_tenet_can_be_prohibited_trigger`, `pam_tenet_can_be_prohibited_no_actor_trigger`; the effect `pam_bull_notify_faith_rulers_effect`; and the names of the faith `christian_faith`. Other mods that change the same ones may conflict.

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
