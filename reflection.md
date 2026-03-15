# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").

The hint was backwards.
You had to click button twice to submit.
The new game button didn't remove the Game Over notification from the screen

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

Used Claude Code
When the hint was backward, I was able to get the fix instantly.
However, when I try to fix the problem of need to double click the submit, it was giving me misleading answers.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?

I checked the features by myself in the beginning but later wrote tests with the help of AI.

- Describe at least one test you ran (manual or using pytest) and what it showed you about your code.

I fixed the test code winning guess

- Did AI help you design or understand any tests? How?

Yes AI did help me get over my first pytest. I was able to figure out how to import the logic from a root directory with the help of AI.

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.

The secret number keeps changing in the original app because we are using a random int generator between our low and high bounds.

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
Streamlit runs the app again and again everytime the user interacts with the application. So we need a session to keep track of the state that we are in. This session serves as a persistent volume for our variables.

- What change did you make that finally gave the game a stable secret number?
When new game is clicked, originally, we would generate a secret with range 1 through 100 no matter the difficulty, but I fixed the code so that the difficult is accounted for during secret generation.


---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
  I would like to write tests for each feature or a bug that I fix to make sure it is working. In order to do that, I will like to think of edge cases for which my bug fix might fail.

- What is one thing you would do differently next time you work with AI on a coding task?
After my bug fix, I will like to reflect on the edge cases and run the test instead of a manual test.

- In one or two sentences, describe how this project changed the way you think about AI generated code.
The AI generated code definitely makes it efficient for us to code but at the same time sometimes it may generate a complicated code which one may not understand at the time and then later the codebase becomes large enough that one may not be able to have the human loop. So, even if the AI gives me the code, i will definitely have to review the logic and its complexity, document it and test it.