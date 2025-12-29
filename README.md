# Initial Project Description

Mario agents that can adapt to newly seen levels. The plan is to use reinforcement learning by pitting the agent against an online level generator that crafts increasingly harder challenges as the agent improves.

## Outline

### Goal
Train an agent that reliably clears unseen Mario levels while an adversarial generator seeks to maximize difficulty without making levels impossible. We hope to achieve:
    - Good backtracking capabilities to recover from mistakes
    - Comprehend shifting sizes
    - Have flexibility to towards optimizing variable goals (speedrun, coin collection, exploration, kills, etc.)

### Setting
Two-player minimax game between Agent (policy) and Generator (level distribution). Success means robust play across a broad, shifting set of levels.

### Tools and approach sketch
- Environment: Mario simulator (gym-super-mario-bros or similar)
- Generator: adversarial PCGRL-style loop (e.g. https://github.com/amidos2006/gym-pcgrl)
- Agent: RL policy (PPO / IMPALA) with reward shaping for various goals
