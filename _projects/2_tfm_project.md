---
layout: page
title: Master's Thesis - Be My Mate 
description: Award-winning framework for simulating Virtual Students using LLM-based Multi-Agent Systems.
img: assets/img/tfm_tutoragents_chat.png
importance: 2
category: research
related_publications: true
---

**🏆 Award Winner:** Recipient of the **València (Spain) Innovation Capital Award (5,000€)** for excellence in R&D and alignment with the "Valencia 2030" Urban Strategy.

[cite_start]**📄 Published Research:** This work was accepted and presented at the **17th International Natural Language Generation Conference (INLG 2024)** in Tokyo[cite: 447, 448].

---

**The Research Challenge:**
Traditional Intelligent Tutoring Systems (ITS) are solitary. They isolate students, preventing the "social construction of knowledge" that happens in real classrooms. My Master's Thesis asked: *Can we use Generative AI to simulate a classroom of peers for a single student?*

**The "Be My Mate" Framework:**
I designed and engineered **TutorAgents**, a Multi-Agent System (MAS) where AI agents act not as tutors, but as *virtual students*. These agents:
* Have distinct personalities and "knowledge levels" (e.g., a "confused" peer vs. a "knowledgeable" peer).
* Collaborate with the human student to solve math problems.
* Are powered by **Large Language Models (LLMs)** to generate natural, context-aware dialogue.

### Engineering

**Technical Stack:**
* **LLM Orchestration:** **LangChain** integrating **Llama-2-7b-chat** (quantized via `ollama` for local inference).
* **Backend:** **FastAPI** for the agent service.
* **Frontend:** **React** with WebSockets for real-time, multi-user chat synchronization.

<div class="row justify-content-sm-center">
    <div class="col-sm-10 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/tfm_tutoragents_chat.png" title="Collaborative Chat Interface" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    <strong>The User Experience:</strong> A student solving a problem while receiving "peer" support from an AI agent (Virtual Student) and a Tutor bot, all interacting in real-time.
</div>

### Impact & Results
The resulting framework, *Be My Mate*, allows researchers to "inject" virtual social dynamics into learning environments. It was validated through user studies showing that students felt "accompanied" and supported, effectively bridging the gap between personalized tutoring and collaborative learning.

**Read the Paper:** [Be My Mate: Simulating Virtual Students for Collaboration using Large Language Models (ACL Anthology)](https://aclanthology.org/2024.inlg-demos.1/)