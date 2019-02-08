# Wait for Response's categories

## Less is more! Trust the power of a simple Wait for Response's category

One of the greatest features of RapidPro resides at Wait for Response's sorting options.
It can help your poll have a huge response rate and 100% accuracy if used correctly, but you can get in trouble if miss-typed words or actionset links.

Let's overview the feature and understand best practices.

That's a common Wait for Response:

![WFR](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/d84f4b1a-d5ed-4149-a43e-e5130ce7c176.png "Common Wait for response")

The first column is related to the filter type, that is the rule used to validate the user message. Try it out and see there's plenty more than just the usual "has any of these words".
The second column is where you must enter the parameters that will be used to filter the content. Taking the usual "has any of these words" you can type many similar ***words*** that would be interpreted as the same category.
The third one is just the category name, or how all that previous values could be interpreted as. This is simple but very relevant, see why in the image below.

I will use numbers to demonstrate the feature, but it's also applicable to strings.

![SameCategory](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/e8ef998d-2704-41d8-ad7c-6a211283c435.png "Using the same category name")

It has a lot of different categorization filters right? But see how it looks once done.

![SameCategoryWFR](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/b954e7dd-f921-4236-8e4d-a2ca34affdaa.png "Many categories type as one")

Well, that's just a sample with no valid use in real life.
Now lets improve it a bit more. Take a look at the image below and see if you can find the mistake? Some previous images also contain the same mistake...

![CategorizationMistake](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/ef5fd1ba-ee66-4945-ac13-3b9655f0f7df.png "Can you find what's wrong with this?")

## Don't cheat, think!

![Joking](https://media.giphy.com/media/SabSYEpsVh0di/giphy.gif "Time to think!")

Take a look at the first categorization type, as the user types any numeric reply it will always be the system path chosen!

![WrongOrder](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/ca61043b-52b6-475a-be33-44ef16722b69.png "Pay attention to categories order")

The **has a number**, highlighted in red, has a similar work as the **has a number between**, in purple. To filter users' replies correctly that order must be changed.
My goal is to filter replies at 1 to 5 range differently from any other, but still having numeric values such as 2019. That can be done correctly, only using **has a number between** on the first categorization. Then, only if the range isn't found, the ruleset searches for different categorization methods.

![RightOrder](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/1414c878-09b4-4c1b-bbbc-e1d38ea8e550.png "Correct categories order")

Using the right strategy you'll be able to build flows to deal with many exceptions categories filtering the users' replies to search for some piece of valid info. Like this:

![CategoriesSample](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/f2d37621-e1af-4b26-aa27-ae7e07fc06a1.png "Advanced sample")

## Now, what you should avoid using

Capitalized characters are irrelevant as using commas to separate strings. So there's no difference between this:

![Avoid001](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/c57d15a3-27a2-4b62-90d1-d4c0d2e0fd06.png "No need to capitalize or using commas")

To this:

![Avoid002](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/da6b8d60-7e1d-479b-abae-1c32da8f9856.png "Just type the strings")

Another behavior that may put you in trouble is using more than one word/string without choosing the correct categorization type. See the image and look for the error:

![Avoid003](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/1810ea93-77c1-4b09-8d08-4a2937a9fe5b.png "Carefully choose categories type")

As **has any of these words** categorization type is set, the **Yes** category option will never be filled! Because the same words are present at the first string, so the system will always use that category.

The correct type in this case is **has all of this words**. And most important, the order also matters! If inverted, the accuracy would also be compromised!

![Avoid004](https://rapidpro-static-app.s3.amazonaws.com/attachments/4/5804/steps/6993d960-8f87-4d0d-bd4f-9dfe6fdf4e16.png "Pay attention to string's order and similar words")

That's it for today! Remember you can always reach us at support@ilhasoft.com.br