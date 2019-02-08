---
id: wn003
title: RapidPro & U-Report news
sidebar_label: Website polls - Graphic vs. Words cloud
---

# RapidPro & U-Report news: Website polls - Graphic vs. Words cloud

## Hello

Let's talk about the website today? One very interesting option to display Reporters' responses is using **Words cloud** instead of only graphics between replied categories.
It's very simple to use it, but there are some points that I would like to share in order to be sure things works as it should.

## That's how words cloud looks like

![WordsCloud](https://udo-rapidpro-static-app.s3.amazonaws.com/attachments/211/5850/steps/a18594d7-6492-4bdb-beab-4cc2ef23fa7b.png "How a words cloud look like")

Now let's see what's necessary to have it working. Let me share some RapidPro examples.

This is the most common way to have Reporters replies, using categories filter at the Wait for response:

![GraphicsCategory](https://udo-rapidpro-static-app.s3.amazonaws.com/attachments/211/5850/steps/95322453-7fc9-4ffe-91ba-25195a729243.png "Wait for Response sorted by categories")

That's how categorizing looks like on the inside:

![CategorizedWaitForResponse](https://udo-rapidpro-static-app.s3.amazonaws.com/attachments/211/5850/steps/29e14eb1-3e1f-419f-b404-f2d38d922785.png "Categorized Wait for Response")

Using the **Wait for response** ruleset like this will make the website displays Reporters replies with the graphics bar percentage feature. Like this:

![CategorizedGraphics](https://udo-rapidpro-static-app.s3.amazonaws.com/attachments/211/5850/steps/c2f997ab-aa73-4103-90c6-1804dceb5089.png "Website's graphics for categorized Wait for response")

Ok, and what about the words cloud? All you have to do is leave the **Wait for response** without any categories. And it's needed to be without any categories at all! Just by adding a single validation like "***it's not empty***" or "***has a number***" will make the website display it like a graphics bar instead. Take a look how should your Wait for response look like to have words cloud working:

![UncategorizedRapidPro](https://udo-rapidpro-static-app.s3.amazonaws.com/attachments/211/5850/steps/78794c17-0341-4010-91ed-bcd3178cca39.png "Uncategorized Wait for response")

## Let's review. What should you do?

![Do](https://udo-rapidpro-static-app.s3.amazonaws.com/attachments/211/5850/steps/f9bc6857-56a9-4871-b594-4824020c3716.jpeg "Your flow should look like this")

## What you shouldn't do?

![Dont](https://udo-rapidpro-static-app.s3.amazonaws.com/attachments/211/5850/steps/809b0bd9-48c0-4b6f-aa3a-c9e37cc24a2e.jpeg "This won't create a words cloud")

Last but not least... I'll never be tired to remember you that modifying the flow having Reporters that already responded will make all previous responses to be lost! I know I've already said that... 😅 but caution is never too much.👍