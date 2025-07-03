OVERARCHING GOAL: Turn the content I give you into Anki flashcards

# FORMAT
Structure your output as a plain text file to import into AnkiApp. It will be similar to a CSV but use pipes (`|`) as separators instead of commas.
The text file should have a row for each card in the deck, with the following columns:
    
    1 Text for front of card
    2 Text for back of card
    3 List of up to 3 tags, space separated
    4 note type (either 'Basic' for a front/back flashcard or 'Cloze')

Begin with these file headers:
```
#separator:|
#html:true
#notetype column:4
```

Use `<br>` for new lines.

## CLOZE DELETIONS
Use cloze deletions where appropriate. Cloze deletion is the process of hiding one or more words in a sentence. Format-wise, cloze deletions put all of the core information in the "front of card" column (with optional back extra). The text is formatted as eg {{c1::Socrates}} famously died by {{c2::drinking hemlock}}.

# HOW TO DESIGN GOOD CARDS

## GENERAL PRINCIPLES FOR SPACED REPETITION (summarized from Piotr Wozniak)
1. Do not learn if you do not understand
2. Learn before you memorize - build the picture of the whole before you dismember it into simple items in SuperMemo. If the whole shows holes, review it again!
3. Build upon the basics - never jump both feet into a complex manual because you may never see the end. Well remembered basics will help the remaining knowledge easily fit in
4. Stick to the minimum information principle - if you continue forgetting an item, try to make it as simple as possible. If it does not help, see the remaining rules (cloze deletion, graphics, mnemonic techniques, converting sets into enumerations, etc.)
5. Cloze deletion is easy and effective - completing a deleted word or phrase is not only an effective way of learning. Most of all, it greatly speeds up formulating knowledge and is highly recommended for beginners
6. Use imagery - a picture is worth a thousand words
7. Use mnemonic techniques - read about peg lists and mind maps. Study the books by Tony Buzan. Learn how to convert memories into funny pictures. You won't have problems with phone numbers and complex figures
8. Graphic deletion is as good as cloze deletion - obstructing parts of a picture is great for learning anatomy, geography and more
9. Avoid sets - larger sets are virtually un-memorizable unless you convert them into enumerations!
10. Avoid enumerations - enumerations are also hard to remember but can be dealt with using cloze deletion
11. Combat interference - even the simplest items can be completely intractable if they are similar to other items. Use examples, context cues, vivid illustrations, refer to emotions, and to your personal life
12. Optimize wording - like you reduce mathematical equations, you can reduce complex sentences into smart, compact and enjoyable maxims
13. Refer to other memories - building memories on other memories generates a coherent and hermetic structure that forgetting is less likely to affect. Build upon the basics and use planned redundancy to fill in the gaps
14. Personalize and provide examples - personalization might be the most effective way of building upon other memories. Your personal life is a gold mine of facts and events to refer to. As long as you build a collection for yourself, use personalization richly to build upon well established memories
15. Rely on emotional states - emotions are related to memories. If you learn a fact in the sate of sadness, you are more likely to recall it if when you are sad. Some memories can induce emotions and help you employ this property of the brain in remembering
16. Context cues simplify wording - providing context is a way of simplifying memories, building upon earlier knowledge and avoiding interference
17. Redundancy does not contradict minimum information principle - some forms of redundancy are welcome. There is little harm in memorizing the same fact as viewed from different angles. Passive and active approach is particularly practicable in learning word-pairs. Memorizing derivation steps in problem solving is a way towards boosting your intellectual powers!
18. Provide sources - sources help you manage the learning process, updating your knowledge, judging its reliability, or importance
19. Provide date stamping - time stamping is useful for volatile knowledge that changes in time
20. Prioritize - effective learning is all about prioritizing. In incremental reading you can start from badly formulated knowledge and improve its shape as you proceed with learning (in proportion to the cost of inappropriate formulation). If need be, you can review pieces of knowledge again, split it into parts, reformulate, reprioritize, or delete.

## OTHER HEURISTICS

### Cloze deletions and context
When using cloze deletions, make sure that the covered information isn't critical for disambiguating the sentence. eg consider "{{c1::Turpentine}} is an effective {{c2::solvent}}". When c2 is covered, that's fine, but if c1 is covered, there are many effective solvents that are not turpentine, and merely viewing "___ is an effective solvent" gives the learner no way to infer that turpentine is the relevant one! So do not make clozes like this. Plan our your cloze deletions in advance and notice whether any of them have this issue, and address the issue. Often it may not be necessary to have that cloze deletion at all—it might be sufficient to memorize that turpentine is a solvent, without needing to memorize that one such solvent is turpentine. If it DOES seem necessary to include such a cloze deletion, then add additional info to disambiguate, eg "{{c1::Turpentine}}, originally made from distilling pine resin, is an effective {{c2::solvent}}".

However, don't include so much information outside the cloze deletion that it makes the answer already revealed even to someone who doesn't know it. If you want to include further explanation of why something makes sense, this extra info can go on the *back* of the card, to be revealed when the 

You may need to completely restructure the given text in order to satisfy these constraints and make good sentences for cloze deletions. That's okay! You're a master of paraphrasing. Try a few options and reason about which will be best.

Don't reference the source. 

## EXAMPLES OF EXCELLENT CARDS



# PURPOSE
These decks are for the purpose of understanding the world better in order to make better decisions, not for studying for a test (I'm not a school student but a man in my 30s: entrepreneur, researcher, philosopher, father). You can create some cards that are focused on recalling definitions, functions and explanations, where there are technical concepts worth knowing the names of, but I'm also interested in cards that ask me to recall the structure of things.

I will import the text file into AnkiApp to use as flashcards. For any acronyms, write the full term and then put the acronym in brackets, unless the card is specifically testing whether I know what the acronym stands for.
