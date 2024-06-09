gpt_shell.py allows the user to interact with models in a shell environment. The model can propose commands to be run, which are then reviewed by the user. The file also has classes allowing for the easy integration of additional models, which is demonstrated by the addition of a gpt-3.5 instance which evaluates the safety of the proposed command before the user reviews it. 

I took the full two hours (not including breaks away from the computer) to work on this. 

* I made extensive use of ChatGPT 4o - for example, simply pasting in the brief pretty quickly resulted in a model chatting to me in the terminal after some iteration (despite ChatGPT's insistence on using an outdated OpenAI api).
* I took a walk after implementing the initial system, during which I thought about possible designs to make the code somewhat reusable, and additional feature ideas, since I had pretty quickly met the basic requirements of the brief.
* Splitting the code into classes and implementing the second model took more manual intervention.
* I got into a flow state after my walk, and quickly reached the end of the time limit, despite having planned to include type checking before submitting.

There were a few additions I would have liked to make, given more time:

* Type checking: I noticed a few points when calling methods where I would have liked to see what data type I am expecting. I expect if other people were to use this code, they would also find this useful.
* Further consideration of the design: I would have liked to have spent some more time tinkering on the design, if this were to be a codebase I and others use for a lot of experiments. I don’t think I implemented object orientation principles very well, particularly single-responsibility and open-closed which perhaps would have made the code much easier to modify and extend. I do however put some credence on the possibility that such concepts are not particularly relevant in fast-moving labs - I guess it comes down to whether I'm running initial experiments to quickly get some data or creating an experimental setting that expects to see considerable use?
* More tinkering with system prompts: I pretty much just left it with the first system prompt I tried. I would perhaps have liked to consider in more depth how I would like the models to behave, and iterated on my system prompt with this intent.
* OpenAI Key: A more secure way of including the OpenAI Key would also have been desirable, as placing it in code at any point increases the risk it is submitted to public view. Perhaps instructing the user to set this as an environment variable after downloading the project would have been a better solution.

I did not really experience any difficulties, except for my desire to do more on this program than was allowed by the time limit.
