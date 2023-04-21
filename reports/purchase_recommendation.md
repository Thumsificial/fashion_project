## Purchase Recommendation

Purchase recommendation seemed like a very interesting thing to me. It is very useful, because the better the recommendations, the less emissions from shipping and shipping costs for both the consumer and the seller. Also the better recommendations are, the more the user might buy, because they see exactly what they want or need. Also the store has a better estimate of how much they need to order and store.

The H&M has a lot of information about the different articles. As well as images and a lot of purchase history data.

I wanted to start by looking at the purchase history data.

I struggled a lot at the start, because I am not that good with pandas, so I didn't really get the data on the format I wanted.

I wanted to try collaborative filtering on the purchase data, to predict what items would be bought and not bought. But the dataset had no rating or return category, so the only metric I had was weather or not the items were bought.

This I thought would be good, so after working a bit with the transactions data, I added a column for bought/not bought, and set it to 1 if the items were bought, which resulted in a model that just set things to one... Not the greatest model.

But my idea was that if I were just able to add some purchases that didnt happen as 0, then it would work. However I did not get that far.

I also wanted to just have a list of products the individual customers had bought before some time, and then compare that to other customers before and after. However after struggelig for some time with this, I decided to instead use the rest of the time to explore the other competition from shopee.

After working with such a large dataset, the transaction history had almost 32 milion rows. It was obvious to me that there needs to be done quite a lot of work to use such a big dataset, with both optimization and some way of choosing what data to use and not use, because for me, every time I had to do something with the dataset, it took ages.