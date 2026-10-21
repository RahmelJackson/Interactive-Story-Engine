# Interactive Story Engine

**Play AI text adventures with real characters, real choices, and a story that goes somewhere. No coding, no setup: just upload two files to an AI chat.**

The **engine** is a set of rules that turns an AI chat (DeepSeek, ChatGPT, Claude, Gemini, and others) into a storyteller: thick accents, characters with lives of their own, places you can smell, secrets that stay secret, and you in control of your character. A **story packet** tells it which world to run. This repository includes a zombie survival generator to start with and a builder for making your own.

[Support on Patreon](https://patreon.com/rahmel/) · [Donate with PayPal](https://paypal.me/RahmelJackson?country.x=US&locale.x=en_US) · [Donate with Cash App](https://cash.app/$RahmelJackson)

---

## Try it in 2 minutes

1. Download **[Interactive_Story_Engine_R74.txt](Interactive_Story_Engine_R74.txt)** and **[Zombie_Generator_Packet.txt](Zombie_Generator_Packet.txt)**.
2. Open a **new chat** in your AI app and upload both files.
3. Send this:

```text
Run the Interactive Story Engine with this story packet. Read both files completely before you start. Then follow the packet's start instructions, and in the opening assume I know nothing about the world or my own character. Write every character's accent and language strong on the page from their first line, spelled the way they sound, even when it's harder to read; I'd rather work to understand them.
```

That's it. You'll see three ways to start:

- **Quick Start:** give your name and gender (or let it pick), and a fresh zombie survival story begins.
- **Build Your Own:** choose your character, location, and zombie type in three short steps.
- **Describe Freely:** tell it what you want in your own words ("fast zombies on a cruise ship, I'm a bartender").

It will also ask what your character is after. Answer it, or say **"let the story find it"**; the main story is built around your goal.

**No packet? No problem.** Upload just the engine and describe any story you want ("a heist in 1920s Havana, I'm the getaway driver"). It builds the world from that.

---

## How to play

Each reply is the next page of the story, followed by a menu like this:

```text
1. [Something you could do now]
2. [Something else you could do]
3. [A third option]
4. Type what you want to do or want to have happen.
5. Summarize the scene and situation.
6. OOC / change, retcon, or compact for a new chat.
```

- **Pick a number,** or just **type anything**: an action, dialogue, a question, or several things at once.
- **5** gives you a recap whenever you're lost.
- **6** lets you step outside the story: ask a question, fix a mistake, change something you don't like ("OOC: make her older," "OOC: undo that"), or **compact** the story to continue in a new chat.
- You control your character's actions, words, and feelings. The AI controls everyone and everything else.
- **If it starts slipping** (flat accents, characters nobody described, characters telling you what you feel, repeated lines, the menu missing), type **`OOC: refresh`**. It rereads the engine and gets back on track.

**Keeping it in story mode.** The AI copies its own recent replies more than its instructions, so small slips snowball. **The strongest fix is to regenerate or edit a bad reply the moment you see it** (a flat accent, a repeated line, a character lecturing you): a slip left in the chat becomes a pattern, while a regenerated one never happened. Write your turns as actions and dialogue rather than requests ("I lean on the bar and ask her name," not "can you describe the bar?"), keep OOC notes short, use `OOC: refresh` at the first sign of drift, and in long games, compact and continue in a fresh chat. Most turns you'll just pick a number, so the menu steers the story: if the options keep circling the same kind of talk, type your own move instead.

### Extra tools for keeping it on track

**A quick reminder you can paste with your turn** when things start slipping, cheaper than a full refresh:

```text
(OOC: write every accent and language out, nobody tells me what I feel, fresh options, full menu.)
```

**If your app has an Author's Note, memory, or custom-instructions box** (SillyTavern, AI Dungeon, many others), put this in it. Text placed there sits near the end of what the AI reads every turn, which is where instructions steer hardest:

```text
[Interactive Story Engine: every speaker in their own accent and language; people chase their own lives; places press on bodies; no lessons or therapy talk; show the thing itself; quiet scenes stay quiet; secrets stay secret; finish the moment, then the six-entry menu.]
```

**If you play through an API or a frontend like SillyTavern,** sampler settings fight repetition at a level no prompt can reach. Reasonable starting points: repetition penalty about 1.1, Min-P 0.02-0.08, DRY (multiplier 0.8, base 1.75, allowed length 2), and XTC (threshold 0.15, probability 0.5). Most chat apps, including DeepSeek's, don't expose these; that's fine.

---

## What's in this repository

| File | What it is | When you need it |
| --- | --- | --- |
| [Interactive_Story_Engine_R74.txt](Interactive_Story_Engine_R74.txt) | The rules that run any story | Every time you play |
| [Zombie_Generator_Packet.txt](Zombie_Generator_Packet.txt) | A zombie survival story generator (zombies inspired by classic films and games, scavenging, raiders, weather) | To play the zombie story |
| [Story_Packet_Builder_R37.txt](Story_Packet_Builder_R37.txt) | A tool for creating your own stories | To make your own world |

To download everything at once, use **Code → Download ZIP** at the top of this page. To download one file, open it and click the download button (↓) at the top right of the file view.

---

## Make your own story

1. Open a **new chat** and upload **Story_Packet_Builder_R37.txt**.
2. Send this:

```text
Run the story packet builder.
```

3. Pick how you want to work: step by step, describing your idea freely, or importing something you already have (a story, a CYOA, screenshots, or another generator).
4. When you're happy, say **"finalize"**. The builder gives you a finished story packet.
5. Save the packet as a `.txt` file.

**To play it:** open a new chat, upload the Story Engine and your packet, and send the same start message as above.

**Importing a CYOA?** Include all its pages and rules, not just your selections. If your chat can't read images, paste the text instead.

---

## Compact and continue in a new chat

Chats don't remember each other, and long chats drift: the AI starts copying its own old replies. A compact packs the whole story (characters, voices, places, threads, your corrections, and where you left off) into one block you can carry to a fresh chat.

1. Choose **6** and type **compact** (or send `OOC: compact`).
2. Copy the compact block into a text file.
3. Open a new chat, upload the same files you started with plus the compact, and send `Continue from this compact.`

The new chat picks up exactly where you stopped, at full strength. Compact whenever a game starts feeling flat or repetitive, not just when it gets long. The compact ends with a spoiler section the AI needs for hidden plot; skip reading it if you'd rather not know.

---

## Which AI chat should I use?

My favorite is **DeepSeek**. Any chat should work if it can:

- **Read uploaded text files** (or let you paste long text), and
- **Handle long documents.** The engine and a packet together are about 18,000 tokens before play even starts, so long sessions need a model with a large context window.

Results vary between models. If one struggles, try another.

---

## If something goes wrong

| Problem | Try this |
| --- | --- |
| It summarizes the files instead of starting | Send: `Don't summarize. Run the story engine now.` |
| The menu disappeared | Send: `OOC: show the menu.` |
| Accents flattened, new characters weren't described, or places feel blank | Send: `OOC: refresh` |
| The narration switched to "you," or into someone else's head | Send: `OOC: close third person through my character.` |
| Someone keeps bursting in during a quiet scene or a conversation | Send: `OOC: no interruptions outside action. Let this scene play out.` |
| People keep offering you jobs or missions, or your phone rings with one | Send: `OOC: no job offers or calls. Let people just be people; I'll pick what to do from the menu.` |
| Secrets come out too easily, or characters know things they shouldn't | Send: `OOC: they keep that secret unless I find proof or earn it, and nobody knows what they didn't see or hear.` |
| The narration explains what every moment means | Send: `OOC: show, don't explain. Trust me to get it.` |
| The story feels aimless | Tell it what your character is after (Build Your Own asks), or send: `OOC: my goal is ...` |
| Replies stop mid-moment, or every reply ends on a question | Send: `OOC: finish the moment before you stop.` |
| It did something you didn't choose for your character | Send: `OOC: undo that. My character wouldn't do that.` |
| Characters keep telling you what you feel, or everyone gives you the same lecture | Send: `OOC: nobody tells my character what to feel or what to learn.` Then `OOC: refresh` if it continues. |
| Missions happen without you, or over the radio | Go yourself, or send: `OOC: bring the mission's big moment to me in person.` |
| It keeps repeating lines, scenes, or menu options | Send: `OOC: you're repeating yourself.` In a long game, compact and continue in a new chat. |
| It forgot something important | Choose 5 to check its recap, then correct it with 6. |
| A long game starts losing track | Choose 6, type `compact`, and continue from the compact in a new chat. |
| Your chat can't upload files | Paste the full text of each file into the chat, engine first. |

**Found a bug or have an idea?** Open an issue with which files you used, what you typed, what the AI did, and what you expected. Short examples help most.

---

*This toolkit guides an AI model; it can't guarantee perfect memory or perfect instruction-following. Playtesting and feedback make it better.*
