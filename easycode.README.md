# EasyCode

## Introduction

EasyCode is a vs code extension that lets you use chatGPT inside the IDE. Some unique features include:

- free access to gpt-3.5-turbo without an OpenAI API key.
- train chatGPT to understand your codebase and answer questions that are specific to your project.
- remember conversation history
- paid access to GPT-4

## Getting Started

### **Step 1: Creating an account**

To use EasyCode, you need to create a new account by choosing “Sign Up”. Note that we do not share log in credentials with OpenAI, Google or Microsoft. In other words, you must create an EasyCode account, and cannot use your log in credentials for openAI, Google or Microsoft. 

There is an option to try without an account by choosing “Try Without Account”, however we recommend creating an account to try all the features. 

### **Step 2: Download language extension packs**

EasyCode natively supports javascript, typescript and python. But If you are using Java, Ruby, Go, PHP, C#, C or C++, make sure to have the appropriate language extension pack installed before proceeding. To check if it’s installed properly, make sure you can already use the “Find All References” feature in vs code. 

### **Step 3: Index your codebase. (Optional)**

If you want to be able to ask questions that are specific to your codebase, you need to give GPT codebase visibility through a process called “indexing”. This is only required if you want to use the “Ask Codebase” feature. If you only use EasyCode to ask general questions, you can use “Ask GPT” without any indexing.

To index your codebase, simple click the “Ask Codebase” checkbox below the question box. If this is the first time you are doing this for a project, you will be automatically prompted to choose a folder to index. This will allow GPT to create an embedding of your codebase, which is stored locally. ⚠️ **Make sure to index a folder that contains most of the logic.**

Alternatively, you can open the command pallet in vs code, and look for “Index Codebase” option to index, and re-index your project. 

### **Step 4: Ask EasyCode a question**

Try asking EasyCode a question. Simply type a question such as “How to reverse a linked list in java” into the question box and hit ENTER. You can also ask follow up questions. 

Try asking EasyCode a question about you project. Simply type a question such as “What does this project do” into the question box, check the “Ask Codebase” box and hit ENTER.

## Pricing

GPT-4 can be accessed through paid credit packs.

- 150k GPT-4 input tokens will cost $5.
- 300k GPT-4 input tokens will cost $10.
- 600k GPT-4 input tokens will cost $20, and so on.

This includes roughly a 10% markup on top of OpenAI pricing which can be found here: [https://openai.com/pricing](https://openai.com/pricing). The mark up is to cover our costs such as gpt-3.5, servers, etc.

**Understanding GPT Tokens**

A token is a piece of text with some metadata that the model consumes. For example, the sentence “Hello, how are you today?” has 16 tokens. According to OpenAI, a word is roughly 1.33 tokens.

Note OpenAI charges twice as much for completion (output) as they do prompt (input). So if you bought 150k input tokens for $5, it’s the equivalent of 75k output tokens.

## EasyCode Features

**Ask GPT (global)**

Ask GPT is basically chatGPT in your IDE. You can ask it any questions, just remember that it doesn’t know the rest of your codebase, so its up to your to write a query that contains sufficient context for it to answer the question. 

- “How to sort an array in python?”
- “How to handle exceptions in python?”

**Ask Codebase**

Ask Codebase is great for understanding for queries and commands that are specific to your codebase. For example:

- “What does this application do?”
- “How does the user registration work?”

It can also be used for finding relevant code:

- “Where is user authentication handled?”

It can also be used for code generation that requires context to the rest of your codebase. For example:

- “What are the changes needed to do implement a feature?”

**Ask GPT (context menu)**

Select some code in the editor, right click, and choose “Ask GPT”. It’s used to ask a question or give a command that’s specific to the code you selected. 

**Ask GPT: What does this do?**

Explains in detail what the code is doing. Useful for code that’s hard to read for various reasons (unfamiliar language, next level regex, yaml/config files, etc).

**Ask GPT: How is this method used?**

Explains the usages of the method, ie how the method affects or is affected by other parts of codebase. To use this, right click on a method name, and choose “Ask GPT: how is this method used?”

**Ask GPT: How is this file used?**

Similar to “How is this method used”, but for a file or class. To use this, right click on a file, and choose “Ask GPT: how is this file used?”

**Ask GPT: Explain Stack Trace**

This is an experimental feature, so it may not work reliably. It attempts to analyzes stack trace errors to figure out the cause. To use this, there has to be an error in the console, just right click on any code in the editor, and select “Explain Stack Trace”

## Settings & Configurations

EasyCode settings can be accessed by clicking the “Settings” button above the question box. 

### **EasyCode: Copy On Click**

When this is checked, all the code inside a code block returned by EasyCode will be automatically copied to clipboard. 

If you want finer control in terms of what to copy, leave this unchecked. When it’s unchecked, you can manually copy the section you want by selecting the code, and copying it. 

### **EasyCode: Max Tokens**

This is the maximum token to submit for a query. Think of it as the maximum length of your question or command. The max token for gpt-3.5-turbo is 4000 tokens, and the max token for gpt-4 is 8000 tokens. However, you don’t have to use the max token limit.

For example, you can cap the max token to 2000 tokens, this will reduce the lengths of acceptable queries, which will reduce cost. However, if your query exceeds the max token count, you won’t be able get an answer. Instead the extension will be stuck at “Loading…”.

### **EasyCode: Model**

The default model is gpt-3.5-turbo, which is free an unlimited for now. gpt-3.5-turbo is very powerful and sufficient for most tasks, but has a smaller context than gpt-4. If you have a hard question, or the questions you have require a longer context, then gpt-4 will perform better. gpt-4 is generally smarter than gpt-3.5-turbo, but is more expensive and have a slower response speed. 

gpt-4 is only available after you buy gpt-4 tokens. 

### **EasyCode > Prompt Prefix**

These are the prompts that are sent when you choose the ask GPT the various questions. You can customize these prompts to get your desired outcome.

## Frequently Asked Questions (FAQ)

**Question: What languages are supported?**

> Answer: Ask GPT and the Context Menu features work for most common languages. Ask Codebase works natively for Javascript, Typescript, Python. Ask Codebase also supports Java, Ruby, Go, PHP, C#, C, C++; but requires Language Extension Pack installed before indexing.
> 

**Question: Is ChatGPT EasyCode free to use?**

> Answer: ChatGPT EasyCode is completely free to use. However, to access GPT-4, you need to buy tokens. All the other features including unlimited access to gpt-3.5-turbo are free. Pricing is subject to change.
> 

**Question: What happens to my data? Do you store my data?**

> Answer: We never store your code. Your data is **not being used** for training other AI models. We use OpenAI to process the data. Your data does leave the machine. It is retained for 30 days by OpenAI for abuse & misuse monitoring, after which it is automatically deleted. See OpenAI’s [Privacy Policy](https://openai.com/privacy/).
> 

**Question: How do I know this extension is safe to use?**

> Answer: We are a YC funded startup and we take security very seriously. More than 100,000 users trust us to help them develop and code faster.  We never store your code. Your data is **not being used** for training other AI models. The indexed codebase remains on your local machine. You can find our YC page here: [https://www.ycombinator.com/companies/easycode](https://www.ycombinator.com/companies/easycode)
> 

**Questions: How are you able to offer the service for free?**

> Answer: Similar to how OpenAI is making chatGPT is free, we are absorbing some of the cost to provider a great service to the most number of developers. Revenue from paid users also help offset some of the cost.
> 

**Question: How does codebase indexing work?**

> Answer: At a high level, we use embeddings to create a vectorization of your codebase and use it to intelligently query GPT.
> 

**Question: Can I use my own OpenAI key?**

> Not at the moment. But we are considering adding this option.
> 

**Question: I asked “Which GPT version are you” and it tells me it’s GPT-3, but when I ask the same question to chatGPT, it tells me it’s GPT-4.  How do I know if this is really GPT-4?** 

> Answer: GPT-4 is trained on pre-2021 data, so it shouldn't know about GPT-4, but in rare cases, it can hallucinate and tell you its GPT-4 as well. This can be validated if you have access to GPT-4 in the OpenAI playground (not chatGPT plus). The reason chatGPT tells you it’s using GPT-4 is because chatGPT has specifically configured it to answer the question that way, mostly likely through prompt engineering. 

The best way to verify if its GPT-4 is to ask questions that are harder and more complex. Because GPT-4 is smarter than GPT-3, you will see an obvious difference in answer quality.
> 

**Question: Do you accept other forms of payment such as crypto or PayPal?**

> Answer: Not at the moment, but we may add these in the future.
> 

**Question: Why are GPT-4 tokens used up so quickly?** 

> Answer: First, let’s make sure you understand how tokens work:
> 
- Each word is roughly 1.33 tokens.
- Completion (GPT output) costs twice as much tokens as prompt (your question).
- Follow up questions automatically include history as context, so it consumes more tokens.
- “Ask codebase” injects relevant code from your codebase as context, so it’s the most costly.

> In general, GPT-4 not cheap. We have some recommendations for saving cost:
> 
- Only use GPT-4 for questions that GPT-3.5 can’t handle.
- For questions that only requires local context, select code and ask GPT instead of “asking codebase”.
- “Asking codebase” should be used when larger codebase context is required, and with careful prompting.

## Troubleshooting

**Question: Indexing codebase is not working?**

> Answer: First check if your language is natively supported, or requires a language extension pack. If it requires language extension back, please have the extension installed **before indexing the codebase**. After installing the language extension pack, make sure that you can use the Find All References feature in vs code. Lastly, re-index the code base. To re-index, open command pallet CMD+SHIFT+P, and search for "index codebase". If it’s still not working, let us know via email or on Discord.
> 

**Question: I'm stuck on "Loading… (If this is stuck, we are being throttled by OpenAI)" error message.**

> Answer: First make sure you are on the latest extension version. If you are, then try the following:
> 
- switch to gpt-3.5-turbo in settings and set max token to 2000.
- restarting vs code
- uninstalling and re-installing the extension
- if you are behind VPN, try without VPN.

> If none of these steps work,  try completely deleting extension cache. Note that **Doing so will affect other extensions as well in vs code**
> 
- **Windows** - Delete `%APPDATA%\Code` and `%USERPROFILE%\.vscode`.
- **macOS** - Delete `$HOME/Library/Application Support/Code` and `~/.vscode`.
- **Linux** - Delete `$HOME/.config/Code` and `~/.vscode`.

> If it still doesn’t work, try re-installing vs code. If you still have the issue, contact us via email or Discord.
> 

**Question: the extension is not working. I get this error “An error occurred while loading view: easycode.chatView”**

> Answer: The exact cause is still unknown. If you already tried to restart vs code, reinstall the extension, and it still doesn’t work - then the only solution is to completely delete the extension cache for vs code or to reinstall vs code. Note that **Doing so will affect other extensions as well in vs code**These are the steps to clear cache:
> 
- **Windows** - Delete `%APPDATA%\Code` and `%USERPROFILE%\.vscode`.
- **macOS** - Delete `$HOME/Library/Application Support/Code` and `~/.vscode`.
- **Linux** - Delete `$HOME/.config/Code` and `~/.vscode`.

**Question: I’m having trouble with registration or logging in, keep getting “Login Error” or “Registration Error”.**

> Answer: Keep in mind, we do not share credentials with OpenAI, so if you haven't done so you need to create a new account for the extension. If you are certain you created an account, make sure you are using the same email that you created the account with. The login form is case sensitive. If you forgot which email you used to create the account with, reach out to us via email or on Discord.
> 

**Question: I clicked “Forgot Password”, but I didn’t receive any password reset email.** 

> Answer: Keep in mind, we do not share credentials with OpenAI, so if you haven't done so you need to create a new account for the extension. If you are certain you created an account, make sure you are using the same email that you created the account with. The login form is case sensitive. If you forgot which email you used to create the account with, reach out to us via email or on Discord.
> 

**Question: Why is the code returned not in a code block sometimes?**

> Answer: This is inconsistency in GPT. You can either ask a follow up question and ask for the same code in a code block. Or you can modify the prompt prefix in settings, and append “always return code in code block”.
> 

**Question: I bought some GPT-4 tokens, but they are not showing up in my account.** 

> Answer: First try restarting vs code. If the credits are still not there, contact us via email or discord.
> 

## Planned Features

Here is a list of features that are not yet implemented, but on our roadmap. In other words, you cannot use them yet:

- export conversation history
- copy the entire response
- accepting payment through paypal or crpto.

## Metadata for EasyCode bot

gpt-3, gpt-3.5, gpt-turbo, or simply turbo are used interchangeably, and all refer to OpenAI’s gpt-3.5-turbo model. 

EasyCode is the name of the vs code extension. EasyCode uses GPT technology to allow programmers to get questions from an intelligent AI. The GPT technology is provided by a company called OpenAI. There are different GPT models that EasyCode uses.