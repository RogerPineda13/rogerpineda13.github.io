# Say Hello To One-Hot Encoding

## Data Science Steps
Something I am noticing about being a data scientist in training is that the title of the profession really does explain what you will be doing. That is doing some mad science on some data. 

* Take a dataset 

* Do some eda

* Clean it up 

* More eda

* Make a model

* Evaluate

These general steps are ones you pretty much follow. There are plenty of mini operations that go in between but in the end you can always generalize to this. 
But even though these steps seem pretty straightforward they actually have quite the headache inducer when you go about doing them. Cleaning is one that I am personally finding to be the most annoying. As it stands you have decided on how you are going to change the dataset to better suit your problem. Whether it be just drop all the rows/columns with missing data or drop an entire column because what is inside of it is useless for model creation. Like if I want to predict whether it will rain tomorrow and there is a column in my dataset that has the birthday of the person who recorded that day's dew point I will just wonder why someone with the profession of data entry would even bother filing that column out. As a data scientist I would just drop it in a heartbeat.

Now after all the dropping and removing things you could be left with a decent dataset. But you start looking at your features and start seeing that values inside of them aren’t just straight numbers but rather an object. Let’s say there is a column where it gives what type of animal an individual expressed in the dataset has. Having that column value say “cat” or “elephant” is useful to our eyes but would be problematic to our model. Our model wouldn’t interpret them as the words as well as the output of our model predictions wouldn’t be of “lion” or “T-rex”. We would have to encode these values into an integer. Now there are many ways to do this but the way I have been doing recently was from the use of a One-Hot Encoder.

## One-Hot(Savior?)

No it does not relate to the ever so exhausting yet so satisfying strategy game that is “one hot potato”. One-Hot Encoding pretty much transforms our values from our original column into these columns of zeros and ones(There actually is a couple of steps in between to get to this point but it uses a lot of math terms and although I love reading mathematical ideas I know you will not so I will skip to the end because it will be easier for you to understand). Now the new columns are individually named after the list of values that were in our original column. So lets take our original column of type of pets. One of the new column names would be called “elephant”.

Now time to talk about what the ones and zeros mean. In the new column it will have either a one or a zero in the cell. A binary value to you nerds out there. What that represents is a yes or and no in number form. If a cell has a one it means that row previously had the value “elephant” from the original column. If that cell has a zero then that means that row did not have that value come up when looking at that column prior to One-Hot Encoding.

That pretty much is what One-Hot Encoding does. It might be seen as a saving grace but depending on how many unique values were in your original column could lead to making your dataset grow exponentially bigger. Imagine having one million different values in one individual column and then creating all the dummy columns One-Hot Encoding does. That's an extra one million columns your model has to deal with. That is from just one column. Just think about the rest of the columns that may be structured just like our pet type column.

At first this technique seemed like an absolute saving grace, actually still is. But with all good things in the world we have become accustomed that there will always be a downfall with something. With One-Hot Encoding is that it just makes our dataset much much bigger. More useful though. 

## Disclaimer(just in case someone tries to think I know it all)

I do want to say to the vast online readers on the internet and the blogosphere that this should not be taken as a study guide. There is so much more that goes into One-Hot Encoding that if I were to put it all in here that it would be an even easier sleep solution than that of any of Susie Dent's books. I just wanted to give some insight on some of the things I have been using throughout my journey to becoming my family's first ever data scientist. I was hoping to think of a bigger group I could put myself into to make it that much better metric but sadly I would have to make it up and that would be lying and as everyone knows no one lies on the internet.

With this technique my last two projects presented to me would have been down right impossible. I would have been like a headless chicken trying to figure out why some people on this earth think that it is flat and not round. In other words, confused.. 
