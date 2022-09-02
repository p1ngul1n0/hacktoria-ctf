# Tiberian Order Contracts Write-ups

Here i list the solution of all **Tiberian Order Contracts** i completed.

## Dialogues from Atlantis [EASY]

### Description
Greetings, Special Agent K. One of our clients, a wealthy art collector from Monaco, is requesting we help her find a recorded dialogue between Critias, Hermocrates, Timaeus and Soscrates.

In her quest to unravel the mysteries regarding the ancient city of Atlantis, our client wishes to gather all evidence possible as to where the location of the lost city truly is. Getting stuck a fair bit into her endeavors, she has reached out to the Tiberian Order to decipher a piece of text.

Our client believes this text to be of vital importance to prove the existence of Atlantis as a city. Whether it will lead directly to the discovery of the city is doubtful. Nonetheless, it’s of great importance to unravel it’s meaning.

I trust your ability to deal with ciphers and ancient dialogues in this matter. You find the text below. In the end, this will lead to another Contract Card if you manage to complete this assignment.

As always. Special Agent K, the contract is yours, if you choose to accept.

### HEX Code
`27 76 3d 45 2a 28 27 60 34 4a 63 38 24 76 68 62 78 77 23 40 2a 28
64 43 2b 3f 27 44 78 74 3c 38 2a 28 5f 44 78 75 7d 47 2a 62 79 39`
`[...]`

### Solution 💡

#### Step 1
As we have a HEX Code, the first thing you would think is to decode it to ASCII, so let's do it using  [CyberChef](https://gchq.github.io/CyberChef/).

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step1.png)

And we ain't got nothing really readable 😟

#### Step 2
But let's not give up right away, we can begin trying out with the most basic Cryptography algorithms, like ROT.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step2.png)

Using ROT 47 you will notice a `==` in the end of the decoded string `QgdGhpbmdzLg==`.

#### Step 3
If you have already encoded anything with `Base64` you know that it's a standard for encoded strings to have `==` at the end, so let's decode it.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step3.png)

Now we have a readable text 😀

#### Step 4
But we ain't having any Flag in our hands yet, we need to find the flag hidden in the text.

If you copy the text and paste in any text editor, you will notice that its all in one line, let's organize to each phrase be in one line, to do that we will use Notepad++ substitute feature to overwrite `\.` with `\n`.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step4.png)

Now the text should be correct.

#### Step 5
Observing the first Words of each phrase you can see that some don't make sense, identifying the word `bit` with `ly` right after it, could be this a bitly link? 🤯

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step5.png)

#### Step 6
Assuming that this is a bitly link, let's search for a ID to build a valid URL.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step6.png)

Now we can build a valid Bitly URL
`https://bit.ly/3pB2oiW`

And Voilà here is the flag 🏴 
