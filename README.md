<h2 align="center"><br>ChatGPT 4, by EasyCode<br></h2>
<p align="center">Experience ChatGPT with codebase integration in your IDE</p>

<p align="center">
    <a href="https://discord.gg/VgE3tQuKrg" target=”_blank”><b>Discord</b></a> |
    <a href="#getting-started">Getting Started</a> |
    <a href="#faqs">FAQs</a>
</p>


- **Free & easy setup,** no session key or OpenAI key required.
- **GPT-4** & GPT-3.5 support.
- Generations are **relevant to your codebase**.
- Ask **Follow up questions**.
- **Security**, data not stored, or used for training.
- NEW: Added **In-Line Autocomplete** (Like Copilot).

### Supported Languages
- Works natively: `Javascript`, `Typescript`, `Python`
- Also supported, but requires Language Extension Pack installed <b style="color:red">before indexing</b>:
`Java` `Ruby` `Go` `PHP` `C#` `C` `C++` (see [FAQs](#faqs) for details).

### ChatGPT + ability to answer questions specific to your project.
<img src="https://github.com/chuangli94/easycode_assets/blob/main/demo_final.gif?raw=true" width="100%">

### Code Suggestion

![Code Suggestion](https://github.com/chuangli94/easycode_assets/blob/main/code_suggestion_annotated.jpg?raw=true)

### Code Explanation

![Code Explanation](https://github.com/chuangli94/easycode_assets/blob/main/code_explanation_annotated.jpg?raw=true)

### Semantic Search

![Semantic Search](https://github.com/chuangli94/easycode_assets/blob/main/semantic_search_annotated.jpg?raw=true)

### General Search

![General Search](https://github.com/chuangli94/easycode_assets/blob/main/general_search_annotated.jpg?raw=true)

## Getting Started

0. Make sure you can already use the `Find All References` feature in vs code. If you are using Java, Ruby, Go, PHP, C#, C or C++, make sure to have the appropriate language extenion pack installed before proceeeding.

<img src="https://github.com/chuangli94/easycode_assets/blob/main/find_all_references.png?raw=true" width="50%">


1. **`Index codebase`** (optional) → Upon installation, you will see the option to “Index codebase”, this is an important step that helps AI provide answers that are **relevant** to your specific situation. This is required to use **`Ask Codebase`** feature. ⚠️ **Make sure to index a folder that contains most of the logic.**

    ![Index](https://github.com/chuangli94/easycode_assets/blob/main/index_codebase.gif?raw=true)

2. **`Ask Codebase`** → ask a question that is related to your specific codebase, such as “How does this application work?"
3. **`Ask Internet`** → ask a questions such as “how to send http request in react native?”

## How to use ChatGPT 4

### **Understanding the Big Picture**

<img src="https://github.com/chuangli94/easycode_assets/blob/main/main_panel.png?raw=true" width="50%">

- **`Ask Codebase` →** For understanding how things work at a high level that are specific to your codebase. For example:
    - “What does this application do?”
    - “How does the user registration work?”

    Can also be used for finding relevant code:

    - “Where is user authentication handled?”

    And of course code generation:

    - “What are the changes needed to do (insert feature) ?”
    - “How do I implement (inser idea)?”
- **`Ask Internet` →** Think of this as chatGPT in your IDE. Good for understanding concepts that are general, not related to your codebase. For example:
    - “How to sort an array in python?”
    - “How to handle exceptions in python?”

### **Understandings the Specifics**

<img src="https://github.com/chuangli94/easycode_assets/blob/main/context_menu.png?raw=true" width="50%">

- **`Ask GPT` →** For open ended questions that are specific to the code you selected. Useful for questions that have a narrower scope.

- **`Ask GPT: What does this do?` →** Explains in detail what the code is doing. Useful for code that’s hard to read for various reasons (unfamiliar language, next level regex, yaml/config files, etc).

- **`Ask GPT: How is this method used?` →** Explains the usages of the method, ie how the method affects or is affected by other parts of codebase.

- **`Ask GPT: How is this file used?` →** Similar to “How is this method used”, but for a file or class.

- **`Ask GPT: Write Code` →** Get code suggestion that are specific to the code you selected. For example
    - “Modify a function so that it does ____”
    - “Write a test case that tests _____”
    - “Write documentation for this function”

- **`GPT: Explain Stack Trace` →** Analyze stack trace errors to figure out the cause

**`GPT: Index Codebase` →** Allows for re-indexing of codebase, or indexing a different part of the codebase.

## FAQs

<details>
<summary>What languages are supported?</summary>

`Ask Internet` and the Context Menu features work for most common languages.

`Ask Codebase` works natively for: `Javascript`, `Typescript`, `Python`. Also supported, but requires Language Extension Pack installed <b style="color:red">before indexing</b>:
`Java` `Ruby` `Go` `PHP` `C#` `C` `C++`

Potential language extension options:
- [Java](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)
- [Ruby](https://marketplace.visualstudio.com/items?itemName=rebornix.Ruby)
- [Go](https://marketplace.visualstudio.com/items?itemName=golang.Go)
- [PHP](https://marketplace.visualstudio.com/items?itemName=xdebug.php-pack)
- [C#](https://marketplace.visualstudio.com/items?itemName=ms-dotnettools.csharp)
- [C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)
- [C](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)

</details>

<details>
<summary>Indexing codebase is not working?</summary>

First check if your language is supported (see above).

If it requires language extension back, please have the extension installed **before indexing the codebase**. See above for a list of potential options.

After installing the language extension pack, make sure that you can use the `Find All References` feature in vs code.

<img src="https://github.com/chuangli94/easycode_assets/blob/main/find_all_references.png?raw=true" width="50%">

Re-index the codebase.

Still not working? Let us know on <a href="https://discord.gg/VgE3tQuKrg" target=”_blank”><b>Discord</b></a>.

</details>

<details>
<summary>Is ChatGPT 4 free to use?</summary>

ChatGPT 4 is free to use during alpha. We may introduce paid plans in the future, but there will also be a free version.
</details>

<details>
<summary>Do I have to index my code base?</summary>

No. Indexing is required to use the **`Ask Codebase`** feature which provides answers relevant to your codebase. If you don’t want to index your codebase, you can still use all the other features.
</details>

<details>
<summary>What happens to my data?</summary>

We never store your code. Your data is **not being used** for training other AI models.

We use OpenAI to process the data. Your data does leave the machine. It is retained for 30 days by OpenAI for abuse & misuse monitoring, after which it is automatically deleted.

See OpenAI’s [Privacy Policy](https://openai.com/privacy/).
</details>

<details>
<summary>How do I know this extension is safe to use?</summary>

We are a YC funded startup (link: https://www.ycombinator.com/companies/easycode) and we take security very seriously.

We never store your code. Your data is **not being used** for training other AI models. The indexed codebase remains on your local machine.

We use OpenAI to process the data. Your data does leave the machine. It is retained for 30 days by OpenAI for abuse & misuse monitoring, after which it is automatically deleted.

See OpenAI’s [Privacy Policy](https://openai.com/privacy/).
</details>

<details>
<summary>How are you able to offer the service for free?</summary>

Similar to how OpenAI is making chatGPT is free, we are absorbing some of the cost to provider a great service to the most number of developers. Revenue from paid users also help offset some of the cost.
</details>

<details>
<summary>How does codebase indexing work?</summary>

At a high level, we use embeddings to create a vectorization of your codebase and use it to intelligently query GPT.
</details>

<details>
<summary>Can I use my own OpenAI key?</summary>

Not at the moment. But we are considering adding this option.
</details>

<details>
<summary>Is this really GPT-4? I asked if it's GPT-3 or GPT-4, it says it's GPT-3.</summary>

GPT-4 is trained on pre-2021 data, so it shouldn't know about GPT-4, but in rare cases, it can hallucinate and tell you its GPT-4 as well. In other words, you can't trust the answer.

I recommend testing it by asking questions that hard & complex. You will see an obvious difference in the answer quality.
</details>

<details>
<summary>How do I reset my password?</summary>

Use the "Forgot password" option on the top right.
</details>

<details>
<summary>I subscribed to the professional version, how can I cancel the subscription and get a refund?</summary>

Please email paul@personabo.com with the email you used for registration.
</details>

## Troubleshooting

<details>
<summary>I'm stuck on "Loading..."</summary>

First make sure you are on the latest extension version. If you are, then try the following:
- switch to gpt-3 in settings.
- restarting vs code
- uninstalling and re-installing the vscode extension
- if you are behind VPN, try without VPN.

If you still have the issue, contact us using the methods under "Contact".
</details>

<details>
<summary>The extension is not working for me, it's not giving me answers.</summary>

First make sure you are on the latest extension version. If you are, then try the following:
- switch to gpt-3 in settings.
- restarting vs code
- uninstalling and re-installing the vscode extension
- if you are behind VPN, try without VPN.

If you still have the issue, contact us using the methods under "Contact".
</details>

<details>
<summary>How do I re-index?</summary>

Open command pallet by pressing CMD+SHIFT+P, and search for "index codebase".
</details>

<details>
<summary>I'm having trouble creating an account or registration.</summary>

Please email paul@personabo.com with the email you used for registration.
</details>

<details>
<summary>I'm having trouble logging in.</summary>

Please email paul@personabo.com with the email you used for registration.
</details>

## Contact

Join our <a href="https://discord.gg/VgE3tQuKrg" target=”_blank”><b>Discord</b></a> server. Or email **[paul@personabo.com](mailto:paul@personabo.com)** with your feedback & questions!
