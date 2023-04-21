## Outfit Recommendation

Since chatGPT is very hot right now, I wanted to see if I could use it to get some simple fashion recommendations fast and easy, without doing much with the prompt.

I first started by going to the chatGPT website.

https://chat.openai.com/

There I just speciefied that I wanted chatgpt to give me answers like a fashion expert. And to my, not so big, suprise the answers made a lot of sense. Of course I had to specify some things, but thats what is good about chatgpt, the fact that I can do it without redoing the initial prompt.

![Chat part 1](https://github.com/Thumsificial/fashion_project/blob/master/images/gpt1.png?raw=true)

Here it got me some great ideas, but I forgot to specify that I am a boy.

![Chat part 2](https://github.com/Thumsificial/fashion_project/blob/master/images/gpt2.png?raw=true)

After specifying my gender and age, some more appropriate outfits were generated for me.

![Chat part 3](https://github.com/Thumsificial/fashion_project/blob/master/images/gpt3.png?raw=true)

Some additional jewelry were added, by my request, and all in all I would say that these responses are pretty good for my need. I might not be a fashion expert, so I can't really fully validate it, but I thing it would help a lot of people that have no idea of how to start.

### Using the openai api

Now I wanted to try getting this information using the openai api. This was easier than I expected.

I imported the libraries, plus an added one called dotenv, which made it possible to store the api key without sharing it on github.

Then I just chose the gpt 3.5 model and sendt a system message and a user message. And it returned the same type of response as before, just like I wanted to.

At this point I thought about making this into a simple application, however I chose to instead start working on the competitions, since I knew that they would take a significant amount of time.

This is something I would like to do later tho.

