# LLM-genesis
## Journey of coding custom LRM- Large Reasoning model from scratch 
## Step by step implemenation 
1) sebastian - complete GPT2 architecture/Deepseek R1
2) Fine tuning both classification and Instruction on custom dataset
3) Rag Integration
4) Memory Managment
5) AI agents
6) custom protocols
7) Agentic AI system

## Production 
1) Inference & batching request
2) KV cache management
3) Batching strategies
4) GPU memory Mangement (CUDA) 
5) Serving Framework (vLLm, TGI, TesnorRT-LLM)
6) Token Budgeting and cost control
7) Database In llm
8) Scaling to Multiple user (Horizontal scaling, Load balancer, Autoscaler, Docker, Kubernetes, Cloudflare, cloud etc etc
9) Reliability and Observability


I will try to code everything with mathematical understanding and framework like pytorch tensorflow langchain langraph (maybe crewai, beeai, A2G)
## Research Implementation
1) custom neural network(Implementation + Optimization) using Np for Transformer no need of nn from pytorch
2) LLM Reasoning
    1. RLHF
    2. Neurosymbolic AI
    3. Causal Inference (causal graph and estimation using LLM augmented causal inference framwework??)
    4. All three in one research + Understanding existing Framework
    5. maybe quantum inspired causal inference for LLM Reasoning

  1. Causal RL for LLM Reasoning

Most RL for LLM reasoning (GRPO, PPO on chain-of-thought) treats reward as correlational. The frontier question is: can you use causal graphs to distinguish which reasoning steps actually caused the correct answer vs. which were spurious? You'd be combining your causal inference interest with LLM reasoning — this is largely unexplored.
2. Process Reward Models with Causal Credit Assignment

PRMs (like in DeepSeek-R1) assign reward to intermediate steps. The open problem is which step actually deserves credit? Causal intervention (do-calculus on the reasoning chain) is a principled answer. This is a paper waiting to happen.
3. Neurosymbolic Config Synthesis (from Lain)

Lain configures Hyprland — this is fundamentally a program synthesis problem. Research angle: can you train an LLM to reason over a formal DSL (Hyprland config grammar) using symbolic constraints + RL? The agent learns why a config works, not just what to paste. This maps directly to neurosymbolic AI, which you've already identified as high-payoff.

Area 3 — Causal Reward Shaping for RL Reasoning
The Problem
RL trains LLMs on outcome reward — correct answer = +1, wrong = 0. But this tells the model nothing about which reasoning steps caused success.
The Open Question

Can causal attribution over reasoning traces produce step-level rewards that make RL training more efficient and robust?

Current frontier:
Current reinforcement objectives offer no internal signal that rewards reasoning coherence — related efforts typically rely on external supervision or decoding-time control, acting post-hoc rather than shaping training.

Area 5 — Causal Representation Learning for Reasoning
The Problem
LLMs operate on token distributions. Causal structure operates on variables with semantic meaning. How do you find the causal variables inside a transformer?
The Open Question

Can you identify causal circuits inside LLMs that correspond to specific reasoning operations?
  
 COT reasoning, Zero shot cot reasoning,(spending more time on inference result better accuracy in llm also scale of model increases the reasoning capabilities as well  Bandit problem exploration and exploitation have been implemented
## for starter i am pasting my daily google colab work 
