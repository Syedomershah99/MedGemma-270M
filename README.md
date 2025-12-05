# MedGemma-270M
This notebook fine‑tunes Gemma 3 (270M) on MIRIAD‑4.4M using Unsloth FastModel for faster &amp; lower‑VRAM training (QLoRA, Unsloth gradient checkpointing, sequence packing). It includes:  Chat‑template formatting for supervised fine‑tuning (SFT) TRL SFTTrainer (packing=True) for speed &amp; memory savings 

🚀 Introducing MedGemma-270M - a compact, domain-tuned LLM for medical Q&A built on Gemma 3 (270M)

I fine-tuned Gemma-3 (270M) on the MIRIAD-4.4M medical QA corpus using Unsloth FastModel + QLoRA + LoRA, then exported a GGUF build for lightweight CPU/GPU inference.

🔗 Colab File: https://lnkd.in/gd4qNbmn
🔗 Model: https://lnkd.in/g7SAGMer
 (try it, fork it, or pull it into your own pipeline)

Why this matters:
- Small & fast: 270M params → runs comfortably on free-tier T4 and modest CPUs
- Low-VRAM training: QLoRA (4-bit) + Unsloth gradient-checkpointing + sequence packing
- Easy deployment: GGUF export for llama.cpp / Ollama / Kobold workflows
- Open tooling: TRL + PEFT + Transformers; simple to reproduce/extend

Tech highlights:
- Base: google/gemma-3-270m
- Task: supervised SFT on medical Q&A (MIRIAD)
- Method: LoRA adapters (Unsloth FastModel), chat-template formatting
- Deliverables: HF model repo + one-cell Colab to convert to GGUF

To get started:
- Pull from HF and run with Transformers
- Use the one-cell Colab to produce a .gguf for local/offline inference (I’ll drop the Colab snippet in the comments)
- (Optional) Deploy a Gradio Space / Ollama model for your team

🙏 Credits: Google AI for Developers (Gemma 3), the MIRIAD authors, Unsloth AI, Daniel Han, Michael Han (Unsloth), Mohamed Yasser (for the inspiration) and the Hugging Face ecosystem.

⚠️ Disclaimer: MedGemma-270M is for educational and research use only. It is not medical advice and must not be used for diagnosis or patient care.
