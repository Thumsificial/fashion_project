## Similarity

The Shopee Price Match competition seemed pretty easy to me at first. Just compare some images and compare some titles, and then I am good. However, it is not always as easy as it seems, which I found out while working on it.

I started by looking at the images. Each post had an image, and these could be compared. I started by using these picture to predict the labels of the posts that were provided. But this didn't really solve what I wanted to do, which was comparing the images, instead it tried to label the similar ones using a similar label. But this is a limitation, because the labels are specific, and there are a lot of them, so the model would need to see some data on most of the labels to be able to use all of them correctly, or there has to be a relationship between the number of the labels, so it would understand what a missing label meant, by the difference to another label. Which I don't know if is the case.

So after that I wanted to compare two and two posts and see if they had a matching label.

To do this I created a dataframe which had two and two posts matched together with the corresponding info and a alike column which showed if they had the same label or not.

At this point, the size of the data that was outputted was really big, and just creating this dataframe took a long time, because I had to loop through the data twice and 30 000 * 30 000 is not a pretty number. I did a little optimizing, and cut some of the data, but another problem arose. The data was very uneven. The amount of posts that were similar were a very little part of the whole dataset, and I ended up with an enourmus 99.9% being not similar, which resulted in a model that just predicted everything to be different and got very good validation results.

After this I started by comparing the titles using nlp. I borrowed a lot of the same things from the fastai course, and was able to put the titles together, tokenize them, make them into numbers and running them through the learner. But then the problem of uneven data started showing.

I wanted to continue with nlp, but I was also curious about working further on the images. I didn't know how to put two images as seperate outputs into a model, but instead i could put them together into one image and put that through a vision learner.

So I created a function to stitch the images together horizontaly, and then I put that into the dataloader.

This was a struggle, but after getting some help with the get_items and get_x functions I finally figured it out.

I also tried to filter the dataset down so the results wouldn't be so uneven, but it still ended up being pretty uneven.

All these things also took a lot of time, and at the end I had used up all my GPU time on kaggle. Which made it very hard to test the last part.

I tried to do some gradiant accumulation to run it through some different models, but it still took a lot of time, so that had to be the end of the project for me.

If I could work more with this dataset I would want to use more data, but keep the ratio of similar to not similar a bit higher, so it wouldn't score so well by just calling all different. I also wanted to try to ensamble the nlp and the vision model to get a better overall result.