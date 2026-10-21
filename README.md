# Interactive Story Engine

**Turn any AI chat into a storyteller.** Real characters, real choices, and a story that goes where you take it. It's free and needs no coding: you upload two text files and start playing. Works with DeepSeek, ChatGPT, Claude, Gemini, and other AI chats.

[Support on Patreon](https://patreon.com/rahmel/) · [Donate with PayPal](https://paypal.me/RahmelJackson?country.x=US&locale.x=en_US) · [Donate with Cash App](https://cash.app/$RahmelJackson)

---

## Quick start

1. **Download two files:** [Interactive_Story_Engine_R74.txt](Interactive_Story_Engine_R74.txt) (the rules) and [Zombie_Generator_Packet.txt](Zombie_Generator_Packet.txt) (a zombie survival story). To get everything at once, click **Code → Download ZIP** at the top of this page.
2. **Open a new chat** in your AI app and upload both files.
3. **Copy this message, paste it in, and send it:**

```text
Run the Interactive Story Engine with this story packet. Read both files completely before you start, then follow the packet's start instructions. Assume I know nothing about the world or my own character. Write every character's accent strong and spelled the way it sounds, even when it's harder to read; I'd rather work to understand them.
```

The game opens with a short setup. Pick **Quick Start** if you just want to play.

> **Can't upload files?** Open each file, copy all of its text, and paste it into the chat (the engine first). Then send the message above.

---

## How to play

Each reply is the next page of your story, and it always ends with a menu:

```text
1. [Something you could do]
2. [Something else you could do]
3. [A third option]
4. Type what you want to do or want to have happen.
5. Summarize the scene and situation.
6. OOC / change, retcon, or compact for a new chat.
```

- **Pick a number, or type anything:** an action, something to say, a question.
- **5** catches you up when you're lost.
- **6** steps outside the story ("OOC" means out of character) to fix a mistake, change something, or ask a question. For example: `OOC: make her older.`

You play your character. The AI plays everyone and everything else.

At the start, it asks what your character is after. Answer, or say **"let the story find it."** The bigger story grows from your goal.

---

## Tips for better stories

- **Fix a bad reply right away.** Regenerate or edit it. Mistakes left in the chat get copied.
- **Write as your character.** "I lean on the bar and ask her name" works better than "describe the bar."
- **Type `OOC: refresh`** when things start slipping (weaker accents, a missing menu, repeated lines). It rereads the rules.
- **Start fresh when a game feels flat.** A compact (below) carries your story into a new chat at full strength.

---

## Play any story you want

You don't need a packet. Upload only the engine file and describe your idea:

```text
Run the Interactive Story Engine. My story: a heist in 1920s Havana, and I'm the getaway driver.
```

---

## Make your own story packet

A packet saves a world so you can replay it or share it.

1. Open a new chat and upload [Story_Packet_Builder_R37.txt](Story_Packet_Builder_R37.txt).
2. Send: `Run the story packet builder.`
3. Build it step by step, describe your idea, or import something you already have (a story, a CYOA, screenshots).
4. Say **finalize** to get the finished packet, and save it as a `.txt` file.
5. To play, upload the engine and your packet to a new chat and send the Quick start message.

**Importing a CYOA?** Include all of its pages and rules, not just your picks.

---

## Continue a long game in a new chat

Long chats slowly lose quality. A **compact** packs your whole story (characters, voices, places, and where you left off) into one block you can carry to a fresh chat.

1. Choose **6** and type **compact**.
2. Copy the block it gives you into a text file.
3. In a new chat, upload the files you started with plus the compact, and send `Continue from this compact.`

The end of the compact holds hidden plot notes for the AI. Skip that part if you don't want spoilers.

---

## If something goes wrong

| Problem | Send this |
| --- | --- |
| It summarizes the files instead of starting | `Don't summarize. Run the story engine now.` |
| The menu disappeared | `OOC: show the menu.` |
| Accents, descriptions, or the writing got weaker | `OOC: refresh` |
| It did something you didn't choose for your character | `OOC: undo that. My character wouldn't do that.` |
| Someone keeps interrupting a quiet scene, or offering you jobs | `OOC: no interruptions or job offers. Let this scene play out.` |
| It's repeating itself or losing track | Compact and continue in a new chat (see above). |

<details>
<summary><b>More fixes</b></summary>

| Problem | Send this |
| --- | --- |
| The narration switched to "you," or into someone else's head | `OOC: close third person through my character.` |
| Characters tell you what you feel, or lecture you | `OOC: nobody tells my character what to feel or what to learn.` |
| Secrets come out too easily, or characters know things they shouldn't | `OOC: they keep that secret unless I find proof or earn it.` |
| The narration explains what every moment means | `OOC: show, don't explain. Trust me to get it.` |
| Replies stop mid-moment, or always end on a question | `OOC: finish the moment before you stop.` |
| The story feels aimless | `OOC: my goal is ...` |
| A mission's big moment happens without you, or over the radio | `OOC: bring the big moment to me in person.` |
| It forgot something important | Choose **5** to check its recap, then correct it with **6**. |

</details>

---

## Which AI should I use?

My favorite is **DeepSeek**, but any AI chat works if it can read uploaded text files (or long pasted text) and handle long conversations. The rules and a packet take up about 18,000 tokens before you start, so choose a model with a large context window. If one struggles, try another.

<details>
<summary><b>Advanced: extra controls</b></summary>

**A quick reminder** you can add to any turn when things slip:

```text
(OOC: write every accent out, nobody tells me what I feel, fresh options, full menu.)
```

**Author's Note, memory, or custom instructions** (SillyTavern, AI Dungeon, and similar apps). Text here is reread every turn, so it steers strongly:

```text
[Interactive Story Engine: every speaker in their own accent and language; people chase their own lives; places press on bodies; no lessons or therapy talk; show the thing itself; quiet scenes stay quiet; secrets stay secret; finish the moment, then the six-entry menu.]
```

**Sampler settings** for APIs and SillyTavern (most chat apps don't show these, and that's fine): repetition penalty about 1.1, Min-P 0.02-0.08, DRY (multiplier 0.8, base 1.75, allowed length 2), and XTC (threshold 0.15, probability 0.5).

</details>

---

## What's in this repository

| File | What it's for |
| --- | --- |
| [Interactive_Story_Engine_R74.txt](Interactive_Story_Engine_R74.txt) | The rules that run every story. Always upload this one. |
| [Zombie_Generator_Packet.txt](Zombie_Generator_Packet.txt) | A ready-to-play zombie survival story, different every time. |
| [Story_Packet_Builder_R37.txt](Story_Packet_Builder_R37.txt) | A helper for making your own story packets. |

To download one file, open it and click the download button (↓) at the top right.

---

## Feedback

Found a bug or have an idea? [Open an issue](https://github.com/RahmelJackson/Interactive-Story-Engine/issues) and include which files you used, what you typed, what the AI did, and what you expected.

*The engine guides an AI; it can't guarantee perfect memory or perfect rule-following. Your feedback makes it better.*
