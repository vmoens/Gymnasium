---
hide-toc: true
firstpage:
lastpage:
---

# Gymnasium is a standard API for reinforcement learning, and a diverse collection of reference environments


```{figure} _static/videos/box2d/lunar_lander_continuous.gif
   :alt: Lunar Lander
   :width: 500
```

**Gymnasium is a maintained fork of OpenAI’s Gym library. The Gymnasium interface is simple, pythonic, and capable of representing general RL problems, and has a [compatibility wrapper](content/gym_compatibility
) for old Gym environments:**

```{code-block} python

import gymnasium as gym
env = gym.make("LunarLander-v2", render_mode="human")
observation, info = env.reset(seed=42)
for _ in range(1000):
   action = policy(observation)  # User-defined policy function
   observation, reward, terminated, truncated, info = env.step(action)

   if terminated or truncated:
      observation, info = env.reset()
env.close()
```

```{toctree}
:hidden:
:caption: Introduction

content/basic_usage
content/gym_compatibility
```

```{toctree}
:hidden:
:caption: API

api/env
api/registry
api/spaces
api/wrappers
api/vector
api/utils
```

```{toctree}
:hidden:
:caption: Environments

environments/classic_control
environments/box2d
environments/toy_text
environments/mujoco
environments/atari
environments/third_party_environments
```

```{toctree}
:hidden:
:glob:
:caption: Tutorials

content/environment_creation
content/vectorising
content/handling_timelimits
tutorials/*
```

```{toctree}
:hidden:
:caption: Development

Github <https://github.com/Farama-Foundation/Gymnasium>
Donate <https://farama.org/donations>
```
