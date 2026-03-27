# PULSE QUEST

Prestigious Data Science Competition hosted by Elan & nVision, IIT Hyderabad presented by KLA

---

## PROBLEM STATEMENT

Automatic text summarization is a core task in natural language processing that aims to condense long or complex text into a shorter version while preserving the most important information. In this competition, the focus is on dialogue summarization, which introduces additional challenges compared to summarizing formal documents.

Dialogues are interactive, informal, and often contain multiple speakers, interruptions, slang, and implicit context. A good summary must identify key actions, decisions, or outcomes from a conversation rather than simply compressing the text.

## SPECIFICATIONS

Model : `linydub/bart-large-samsum` (Hugging Face)

Training Arguments :

    learning_rate = 5e-6,
    per_device_train_batch_size = 1,
    num_train_epochs = 2,
    weight_decay=0.01,
    logging_steps = 100,
    save_total_limit=2,
    report_to="none",
    fp16=True

Generation Hyperparameters :

     num_beams=8,
     length_penalty=0.7,
     no_repeat_ngram_size=3,
     max_new_tokens=150,
     decoder_start_token_id=tokenizer.pad_token_id,
     eos_token_id = tokenizer.eos_token_id,
     pad_token_id = tokenizer.pad_token_id,
     early_stopping=True

## RESULT

**Secured 1st Position among 100+ teams.**

ROUGE-L Score (Public-68%) : `0.5039148`  
ROUGE-L Score (Private-32%) : `0.5124484`

---

