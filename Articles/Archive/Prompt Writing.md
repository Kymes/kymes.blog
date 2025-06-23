Prompt Writing
==============

Due to the “black box” nature of LLMs, responses to prompts are non-deterministic. This means that responses may differ based on phrasing/iteration and the LLM may not even provide a duplicate answer to the same prompt. There is also the chance of the model creating “hallucinations” in its response, which is another way of saying that occasionally AI can just make things up.

For this reason, a prompt writer must be very precise on what is being asked through the prompt to “winnow the grain from the chaff”.

An important skill for a prompt writer is being able to “ground” a prompt. Through grounding, the prompt writer makes the prompt as specific as possible as well as give the most context possible to reduce chances of hallucinations and biased responses. 

To begin the process of prompt writing and iteration, a foundation prompt must be built. The foundation prompt can be built in three parts, answering three questions about specificity, context, and constraints.

**What is being asked?:**

This is the first part of a foundation prompt. This is asking - in plain language - specifically what the prompt is meant to accomplish. A prompt writer can utilize the role-playing abilities of AI for added perspective.

1. *Specificity:*
  You are a gardening expert, come up with a simple gardening plan for a beginner to grow abundant produce, with a plan for preserving and canning excess produce after it’s been harvested.

**Why is this needed?:**

The second part of the prompt foundation is where context is given. The prompt writer can give deeper guidelines and expand on what the response will ultimately be.

2. *Context:*
  The gardening plan should also include tips on different methods of dealing with pests, as well as which organic fertilizers are ideal to increase produce yield.

**What are the constraints?:**

The last part of the foundational prompt tells the LLM what the response cannot include. The constraints both expand on the context, and reinforce the specificity part of the prompt. The constraints portion gives the prompt writer a chance to really narrow down the eventual response.
 
3. *Constraints:*
  The gardening plan must be presented as an outline, broken down by season. Each season must include only 5 seasonally appropriate crops: an herb, a leafy green, a root crop, a fruiting plant, and a flower.  

**Full Prompt:**

* "You are a gardening expert, come up with a simple gardening plan for a beginner to grow abundant produce, with a plan for preserving and canning excess produce after it’s been harvested. The gardening plan should also include tips on different methods of dealing with pests, as well as different organic fertilizers to increase produce yield. The gardening plan must be presented as an outline, broken down by season. Each season must include only 5 seasonally appropriate crops: an herb, a leafy green, a root crop, a fruiting plant, and a flower."

These questions are very basic and by no means are they “hard and fast” rules. This foundational prompt can be iterated. Other questions can be explored and added on but it’s important to not take any away as these are meant to form a solid (grounded) foundation to build from.
