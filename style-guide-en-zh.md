# Style guide — en → zh-CN
version 1

Starter guide for English→Simplified Chinese game localization.

8 rules — 1 advisory, 4 llm, 3 mechanical

## Morphology (glossary compliance)

- strategy: `none`
- capitalization is NOT part of term identity (see the style rules)
- Chinese has no inflection; any accepted alternate rendering must be recorded as a glossary `variants` entry.

| id | rule | applies to | enforcement | severity |
|---|---|---|---|---|
| `EN-ZH-01` | Use full-width punctuation (，；？！) in Chinese targets, not half-width. | all | mechanical | high |
| `EN-ZH-02` | No spaces between Han characters. | all | mechanical | medium |
| `EN-ZH-03` | Insert a space between Han characters and Latin letters or digits. | all | mechanical | low |
| `EN-ZH-10` | UI labels are short — prefer 2–4 characters for buttons; never translate an English label word for word if a shorter idiomatic term exists. | ui | llm | medium |
| `EN-ZH-11` | Dialogue uses natural spoken Chinese with sentence-final particles (吧/啊/呢) where the tone calls for them; avoid translationese word order. | dialogue, marketing | llm | medium |
| `EN-ZH-12` | System messages use 请 for instructions and avoid 你 when addressing the player directly. | system | llm | medium |
| `EN-ZH-13` | Do not translate English possessives literally with 的 chains; restructure ("the guard's sword" → 卫兵之剑 or 卫兵佩剑, not 卫兵的的剑). | all | llm | medium |
| `EN-ZH-20` | Match the game's established register: wuxia/xianxia settings take classical flavour (之/其), modern settings take plain Mandarin. | all | advisory | low |

## Notes and examples

**EN-ZH-01** — Use full-width punctuation (，；？！) in Chinese targets, not half-width.
  - why: Half-width punctuation in CJK text is the standard machine-translation artifact.
  - ✓ 生命值不足，无法施放。
  - ✗ 生命值不足, 无法施放.

**EN-ZH-03** — Insert a space between Han characters and Latin letters or digits.
  - ✓ 获得 100 金币
  - ✗ 获得100金币

**EN-ZH-10** — UI labels are short — prefer 2–4 characters for buttons; never translate an English label word for word if a shorter idiomatic term exists.
  - ✓ 确认
  - ✗ 点击此处进行确认

**EN-ZH-12** — System messages use 请 for instructions and avoid 你 when addressing the player directly.
  - ✓ 请稍后重试。
  - ✗ 你应该稍后再试。

