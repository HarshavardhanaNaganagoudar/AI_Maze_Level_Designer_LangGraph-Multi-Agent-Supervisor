
# 🧠 LangGraph Maze Generator 🕹️  
*A Text-to-Level Generation System for 2D Tile-Based Games using Multi-Agent AI*

![Architecture](./architecture.png)

---

## 📌 Overview

**LangGraph Maze Generator** is a multi-agent AI system that allows users to generate 2D mazes for games using natural language descriptions. It combines LangGraph's coordination power with Python-based rendering tools to create fully playable levels.

---

## 🎯 Project Goals

- Convert natural language prompts into structured maze levels.
- Use agent collaboration to design, test, and render maps.
- Offer a playable visual representation using Python tools.
- Provide a user-friendly Gradio interface.

---

## 🧠 Multi-Agent Architecture

```
┌────────────┐
│  __start__ │
└────┬───────┘
     ▼
 ┌───────────┐
 │ Supervisor│
 └────┬──────┘
      ├────────────> Design Intent Agent
      ├────────────> Layout Agent
      ├────────────> Test Agent
      └────────────> Render Image Agent
           ↓
        __end__
```

### Agent Responsibilities

| Agent Name             | Role Description |
|------------------------|------------------|
| **Supervisor**         | Controls execution and routing between agents. |
| **Design Intent Agent**| Extracts key level info like theme, enemies, traps, and size from text. |
| **Layout Agent**       | Builds a 2D NumPy grid maze layout. |
| **Test Agent**         | Validates level solvability using BFS. |
| **Render Image Agent** | Converts the grid into an image using `matplotlib`. |

---

## 🧩 Sample Prompts

```text
- "Create a maze with 2 enemies and 1 goal"
- "Design a maze with traps and hidden exits"
- "A 10x10 horror level with 3 enemies and 2 traps"
```
---

## 📸 Sample Outputs

| Prompt | Rendered Maze |
|--------|---------------|
| "spooky maze with 1 enemy and 2 traps" | ![](./maze_design_new_5.png) |
| "maze with a 1 enemy and 1 trap" | ![](./maze_design_new_4.png) |

---

## 🛠 Tech Stack

- ⚙️ `LangGraph` for multi-agent coordination
- 🧮 `NumPy` for maze representation
- 🧭 `NetworkX` for BFS/pathfinding
- 🖼️ `Matplotlib` for image rendering
- 🌐 `Gradio` for interactive UI
- 🐍 Python 3.10+

---

## 🔧 Features

- ✅ Multi-agent level generation
- ✅ Text-to-tile layout translation
- ✅ BFS-based path validation
- ✅ Visual maze export and gallery
- ✅ Hugging Face Spaces compatible

---

## 🚀 Try the Demo

> **Run on Hugging Face Spaces:**  
[![HF Spaces](https://img.shields.io/badge/%F0%9F%A4%97%20Try%20on-Hugging%20Face%20Spaces-blue?logo=huggingface)](https://huggingface.co/spaces/nharshavardhana/AI_Maze_Level_Designer)

---

## 🎥 Watch Demo Video

> **YouTube Walkthrough:**  
[![YouTube](https://img.shields.io/badge/▶️%20Watch%20on-YouTube-red?logo=youtube)](https://youtube.com/your-demo-video-link)


---

## 🧠 Future Improvements

- [ ] 🌍 Add support for level themes (e.g., forest, dungeon, sci-fi)
- [ ] 🧠 Integrate maze difficulty tuning (easy, medium, hard)
- [ ] 🧩 Extend to 3D maze generation
- [ ] 🎮 Export levels to Unity (via JSON or custom plugin)
- [ ] 🕹️ Export levels to Unreal Engine (via Blueprint-compatible format)
- [ ] 🤖 Add NPC behavior generation (patrol, chase, etc.)
- [ ] 🧠 Incorporate reinforcement learning agents to auto-play/test mazes


---

## 📝 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---
