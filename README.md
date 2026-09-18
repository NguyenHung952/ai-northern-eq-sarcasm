# AI Northern EQ Sarcasm

A context-aware Vietnamese conversational prompt engine focused on:

* High-EQ responses
* Natural Northern Vietnamese tone
* Dry sarcasm and subtle irony
* Witty banter
* Logic-based counter responses
* Boundary-aware communication
* Short and natural chat messages

## Core Philosophy

> Không cần nói nặng. Chỉ cần nói đúng, nói tỉnh, và để người nghe tự hiểu.

The system prioritizes:

```text
NATURALNESS
    >
HIGH_EQ
    >
CONTEXT_FIT
    >
PRECISION
    >
SARCASM
    >
INTENSITY
```

Sarcasm is treated as a style layer, not the primary objective.

## Features

### High EQ

The engine analyzes:

* conversational context;
* emotional state;
* relationship stage;
* interaction pattern;
* boundaries;
* current topic.

### Northern Vietnamese Style

The system favors natural Vietnamese wording commonly associated with Northern conversational style:

```text
Ừ.
Vâng.
Thế à?
Ra là vậy.
Cũng hay.
Hay nhỉ.
Mình hiểu rồi.
Không sao.
Thôi, cứ thế đi.
```

The style avoids exaggerated regional imitation or forced slang.

### Controlled Sarcasm

Sarcasm can range from:

```text
0 — Neutral
1 — Dry
2 — Light Tease
3 — Sharp
4 — Very Sharp
5 — Maximum Controlled
```

Default:

```text
SARCASM_LEVEL = 1–3
```

### Response Modes

```text
LOGIC_COUNTER
DRY_SARCASM
POLITE_IRONY
MIRROR_ARGUMENT
BOUNDARY_RESPONSE
QUIET_EXIT
DE-ESCALATION
```

## Response Architecture

```text
INPUT
 ↓
CONTEXT_ANALYSIS
 ↓
EMOTIONAL_CALIBRATION
 ↓
SARCASM_LEVEL
 ↓
SOCIAL_MOVE
 ↓
CANDIDATE_ENGINE
 ↓
DIVERSITY_CHECK
 ↓
QC
 ↓
FINAL_RESPONSE
```

## Design Principle

Attack the argument, not the person.

Prefer:

```text
logic
+
observation
+
irony
+
boundaries
```

over:

```text
insults
+
personal attacks
+
unnecessary escalation
```

## Example

Input:

> "Mày nói thế mà cũng nghĩ là đúng à?"

Possible response:

> "Ừ, mình cũng vừa định hỏi lại câu đấy."

Or:

> "Vấn đề là dữ kiện chưa đồng ý với kết luận của bạn."

Or:

> "Thế thì chắc mình đang dùng hai bộ tiêu chuẩn khác nhau rồi."

## Structure

```text
gemini/
├── instructions/
│   ├── MASTER_CORE v3.0.txt
│   ├── MASTER_CORE v3.1.txt
│   └── MASTER_CORE v3.2.txt
│
└── gem/
    ├── 00_INDEX_*.pdf
    ├── 01_*.pdf
    ├── 02_*.pdf
    └── ...
```

## Status

Current version:

```text
v3.2
```

Focus:

```text
HIGH EQ
+
NORTHERN VIETNAMESE
+
DRY SARCASM
+
NATURAL CHAT
+
CONTROLLED RESPONSE
```
