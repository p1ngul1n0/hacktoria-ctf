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

#### Step 1 📇
As we have a HEX Code, the first thing you would think is to decode it to ASCII, so let's do it using  [CyberChef](https://gchq.github.io/CyberChef/).

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step1.png)

And we ain't got nothing really readable 😟

#### Step 2 🤐
But let's not give up right away, we can begin trying out with the most basic Cryptography algorithms, like ROT.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step2.png)

Using ROT 47 you will notice a `==` in the end of the decoded string `QgdGhpbmdzLg==`.

#### Step 3 ⛏️
If you have already encoded anything with `Base64` you know that it's a standard for encoded strings to have `==` at the end, so let's decode it.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step3.png)

Now we have a readable text

#### Step 4 📄
But we ain't having any Flag in our hands yet, we need to find the flag hidden in the text.

If you copy the text and paste in any text editor, you will notice that its all in one line, let's organize to each phrase be in one line, to do that we will use Notepad++ substitute feature to overwrite `\.` with `\n`.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step4.png)

Now the text should be correct.

#### Step 5 🔗
Observing the first Words of each phrase you can see that some don't make sense, identifying the word `bit` with `ly` right after it, could be this a bitly link? 

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step5.png)

#### Step 6 🏴
Assuming that this is a bitly link, let's search for a ID to build a valid URL.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Dialogues%20from%20Atlantis/step6.png)

Now we can build a valid Bitly URL
`https://bit.ly/3pB2oiW`

And Voilà here is the flag 

## Cold War Enemies [EASY]

### Description
Greetings Special Agent K. Perhaps you remember our old friend Maksim Kotova? After his capture in Panama he was more than willing to cooporate for reduced sentences.

Following up on the leads he’s given us until this point has resulted in the arrest of several high ranking officials and members of various underground organizations. One of his more promising leads, is a military parts smuggling operation organized by one of Maksim’s former Cold War friends, Vasili Semenov.

Semenov is quietly making a fortune selling Russian military spare parts for scraps to the highest bidder. A lot of these parts aren’t even spares in the literal sense of the word. These parts are all brought together through various air bases around Russia and the world, then routed to a central air base. Where they’re exchanged for cash.

Given the current sticky situation around Russian activity. Not to mention the limited jurisdiction of our client. You are tasked with finding the air base where these sales take place.

The old man wasn’t very much into modern technology, so all we have for you is a sattilite image of the air base. Other items found, are sent to a forensics lab by our client.

Finding the Air Base will lead you to the password for unlocking your link-file.

Password format sample, no caps:

country-governate-district-airbasename-air-base

### Airbase Picture
![alt text](https://hacktoria.com/wp-content/uploads/2022/09/cold-war-enemies-target-1024x618.jpg)


### ZIP Locked File
![linkfile-cold-war-enemies.zip](https://hacktoria.com/wp-content/contracts/items/linkfile-cold-war-enemies.zip)


### Solution 💡

#### Step 1 🔍
We have a image of the airbase we need to locate, but nothing really recognizable, except for the blue Fighter Jets that looks like Russian aircrafts.

So let's start with the most basic proccess to identify a image, reverse search it.

Using TinEye we can locate a couple of Russian and Vietnamise websites that have a similar image.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Cold%20War%20Enemies/step1.png)

#### Step 2 📌
Accessing the first TinEye result we can learn that the Airbase in the picture is called `Khmeimim airport base`

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Cold%20War%20Enemies/step2.png)

#### Step 3 🔑
Searching for `Khmeimim airport base` in Google Maps we can find the real location of the Airbase.

It's located at `Jableh, Latakia, Syria`

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Cold%20War%20Enemies/step3.png)

With that information we can discover the password.

#### Step 4 🏴 
The password format is:

`country-governate-district-airbasename-air-base`

Completing it, it becomes:

`syria-latakia-jableh-khmeimim-air-base`

And with that we can unlock the ZIP file, open the TXT file in it and obtain the URL to the FLAG:

`https://bit.ly/3DAZZNB`

## Nightmare Fuel [EASY]

### Description
Greetings Special Agent K. Yesterday evening around 2100 hours, two officers of the New York Police Department entered the premise of an abandoned building in Brownsville New York. Neighbors had complained about strange sightings. Supposedly a woman had been squatting inside the building.

Reports also state that over the course of the two years the building has been abandoned, several residents of the surrounding houses had complained about junkies occupying the building. Often making terrible screeching like noises during the night.

Normally, this would not get the attention of the NYPD, however, a neighbors’ security camera had caught several people entering the building, but never seen them emerge. Upon closer inspection, a neighbor reported that all windows were closed and intact. Her security camera had also been on the whole time, surveying the only entrance to the building.

This eventually got the NYPD to investigate the building. While clearing rooms, the officers noticed someone moving around at the end of a hallway. Upon repeated calls and commands, the individual retreated behind a door. Both officers approached the door and told the person to come out. After a few seconds, we could see a woman move past the door frame.

Unresponsive to any commands given by the officers, they continued their search. Never to find the woman again. The officers called for backup and had a team of twelve officers and a K-9 unit sweep the building.

Nobody was ever found. Even the dog didn’t find a trail. Which is odd, given all the smells clearly lingering around an old building like that. Strangely enough, upon inspecting the body cam footage, the audio appeared to be missing entirely.

We need you to take a look at the video and see what you can find.

As always, Special Agent K, the contract is yours. If your choose to accept.

Find the password to open the Linkfile, wherever or whatever that might be.

### Officer 1 Bodycam Video
![bodycam-officer-1.mp4](https://hacktoria.com/wp-content/contracts/items/bodycam-officer-1.mp4)

### ZIP Locked File
![linkfile-nightmare-fuel.zip](https://hacktoria.com/wp-content/contracts/items/linkfile-nightmare-fuel.zip)

### Solution 💡

#### Step 1 📹
We have a chilling video 😬, a girl in a white dress crossing the hall in the dark

The video don't have any audio and upon watching it, we can't see any readable text, but we can see it metadata ☺️.

Using Metadata2go we can upload it and view all metadata.

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Nightmare%20Fuel/step1.png)

#### Step 2 🏴
Scrolling down the results, we can see that there is a comment in the metadata, which looks like a pretty strong password, doesn't it?

![alt text](https://github.com/p1ngul1n0/tiberian-order-contracts/blob/main/easy/Nightmare%20Fuel/step2.png)

`fh453n3fk45b384gm$&%#fjksdfmo94853ff`

And with that we can unlock the ZIP file, open the TXT file in it and obtain the URL to the FLAG:

`https://bit.ly/3fYWbvM`
