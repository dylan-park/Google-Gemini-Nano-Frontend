# Google-Gemini-Nano-Frontend
An extremely bare-bones frontend for interacting with the new local Google Gemini Nano model being tested right now. The interface provides a space to write your prompt, a few radio selectors for some premade prompt starters I was testing, and a timer showing how long it took to process your prompt, along with the result. It can be run entirely locally and offline (once you download the model).

This was not built with any serious usability in mind, and was mostly created to test and continue to track the developments on this feature as it progresses.
## Requirements
- Google Chrome Version >= 128
	- As of writing this, the only version of Chrome that fits this requirement is [Google Chrome Canary](https://www.google.com/chrome/canary/)
- Experimental Flags
	- [#prompt-api-for-gemini-nano](chrome://flags/#prompt-api-for-gemini-nano)
		- **Enabled**
	- [#optimization-guide-on-device-model](chrome://flags/#optimization-guide-on-device-model)
		- **Enabled BypassPerfRequirement**
		- After enabling and restarting with this flag, you must give Chrome time to download the model. There is no progress indicator for this process, but the download is not too large.
## Usage
Your prompt is processed as you type, previous prompts that were unfinished (such as ones generated while you were typing) are canceled as you continue to type. When you get an output, you will be able to see the amount of time generation took in milliseconds, and a Regenerate button will appear, allowing you to regenerate a new response off of the same prompt if you like.
## Starters
I added a couple radio selectors that contain some starter phrases as a way to speed up repeated prompt queries in testing. These are as follows:
- Normal - ""
- Japanese - "Translate to Japanese: "
- Slang - "Slang for "
- Define - "Define: "
These could be modified or swapped out for whatever you like in the code.
## Future To-Do
I don't have a lot of drive or reason to progress this project much further than it already is, but there are a couple more things that could be improved:
- [ ] Code Cleanup
- [ ] Better Styling
- [ ] Custom Starter Option - Gives you the ability to type your own starter in, automatically prepending it to all prompts