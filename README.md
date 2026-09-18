# AI Northern EQ Sarcasm

> Prompt engine hội thoại tiếng Việt với EQ cao, giọng miền Bắc tự nhiên, nói móc tinh tế, mỉa có kiểm soát và phản hồi theo ngữ cảnh.

A context-aware Vietnamese conversational prompt engine focused on:

- High-EQ responses
- Natural Northern Vietnamese tone
- Dry sarcasm and subtle irony
- Witty banter
- Logic-based counter responses
- Boundary-aware communication
- Short and natural chat messages

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

Sarcasm is a style layer, not the primary objective.

## Knowledge Base

The repository contains a modular PDF knowledge base under `gemini/gem/`:

| PDF | Purpose |
| --- | --- |
| `00_INDEX_NORTHERN_EQ_SARCASM.pdf` | Knowledge base index and priorities |
| `01_NORTHERN_VIETNAMESE_STYLE.pdf` | Northern Vietnamese language and rhythm |
| `02_HIGH_EQ_SARCASM_ENGINE.pdf` | Sarcasm levels, logic counters and behavioral mirroring |
| `03_RESPONSE_MODES_AND_ARCHITECTURE.pdf` | Response pipeline, social moves and candidate engine |
| `04_ANTI_PATTERNS_AND_BOUNDARIES.pdf` | Guardrails, boundaries and escalation control |
| `05_RESPONSE_EXAMPLES.pdf` | Test examples and style checks |

## Master Instruction

The main style patch is:

```text
gemini/instructions/MASTER_CORE v3.2.txt
```

It extends the `MASTER_CORE v3.0` / `v3.1` architecture from `ai-daily-chatting` while keeping the existing state, stage-lock and candidate-engine concepts.

## Response Modes

```text
LOGIC_COUNTER
DRY_SARCASM
POLITE_IRONY
MIRROR_ARGUMENT
BOUNDARY_RESPONSE
QUIET_EXIT
DE-ESCALATION
```

## Style Rules

The engine favors:

```text
OBSERVATION
+
LOGIC
+
IRONY
+
BOUNDARY
```

over:

```text
PERSONAL_ATTACK
+
MENTAL_HEALTH_ATTACK
+
UNNECESSARY_ESCALATION
```

The target is a reply that feels like a real person wrote it: short, calm, specific and easy to send.

## Architecture

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

## Repository Structure

```text
ai-northern-eq-sarcasm/
├── .github/
│   └── workflows/
│       └── build-pdfs.yml
├── gemini/
│   ├── instructions/
│   │   ├── README.md
│   │   └── MASTER_CORE v3.2.txt
│   └── gem/
│       ├── README.md
│       ├── 00_INDEX_NORTHERN_EQ_SARCASM.pdf
│       ├── 01_NORTHERN_VIETNAMESE_STYLE.pdf
│       ├── 02_HIGH_EQ_SARCASM_ENGINE.pdf
│       ├── 03_RESPONSE_MODES_AND_ARCHITECTURE.pdf
│       ├── 04_ANTI_PATTERNS_AND_BOUNDARIES.pdf
│       └── 05_RESPONSE_EXAMPLES.pdf
├── scripts/
│   └── build_pdfs.py
├── .gitignore
└── README.md
```

### Folder roles

- `gemini/instructions/` — instruction lõi, ưu tiên đọc trước.
- `gemini/gem/` — knowledge base PDF, đánh số theo thứ tự đọc.
- `scripts/` — công cụ build PDF, không phải knowledge content.
- `.github/workflows/` — tự động kiểm tra và build PDF.
- Root — README và các file cấu hình repository.

## Automated PDF Build

PDFs are generated from `scripts/build_pdfs.py`. GitHub Actions validates the generator, builds the PDFs, and commits changed PDFs back to `gemini/gem/` when the instruction or generator sources change.

## Status

```text
Version: v3.2
Focus: HIGH EQ + NORTHERN VIETNAMESE + DRY SARCASM + NATURAL CHAT + CONTROLLED RESPONSE
```
