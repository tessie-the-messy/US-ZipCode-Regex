# Regex for a United States Zip Code

The original gist for this tutorial can be found at: https://gist.github.com/tessie-the-messy/d53feff191134f86ac7c7c87f9ff46af

Regex is a tool created to easily find patterns within text. In this gist, we will learn about a regex that is used to find a US zip code. This is guide is great for anyone who has never used regex, as the US zip code regex covers important topics, without being overwhelming. Great to use on text documents that provide a variety of locations.

## Summary

The US zip code regex is used to find text that contains 5 digits, possibly followed by a dash (-) and  4 digits. (e.g. 00000 or 00000-0000). This is because US zip codes can be entered as 5 digits to explain a more broad area, or those 5 digits, followed by 4 digits to specify a smaller area.

This is what the regex looks like: `/\d{5}(-\d{4})?/`

While this may seem intimidating at a brief glance, we will go over what this sequence of characters means by understanding the different kind of regex components that make up the US Zipcode regex. Thankfully, this regex only contains three types of regex components!

## Table of Contents

- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)

## Regex Components

### Quantifiers

Quantifiers are used to specify how many of a character will be contained in. We will discuss what `/d` represents under the character class section. However, in the regex, we can see that the first instance of `/d` is followed by `{5}` . This means that the `/d` metacharacter should occur 5 times within the sequence our regex is searching for. There is another one of this type of quantifier attached to the second `/d` as well; `{4}` .

The second type of quantifier is the `?` character. This character tells the regex to find something either once or not at all within an expression. In our case, the `?` is attached to the `(-\d{4})` group. This tells the regex to either find this group once, or not at all.

### Grouping Constructs

In our case, our grouping construct is super easy to catch. Briefly mentioned in the previous section, it is the part of the expression contained within the parentheses `()` . This part of the regex represents the dash and digits that come after the first 5 digits. Not every US zip code contains this dash and four digits, so we need to be able to tell our regex search that this specific part may or may not be in what we are looking for. 

### Bracket Expressions

Bracket expressions define a specific set of characters by containing them within, you guessed it, `[]`. Our regex expression does not explicitly contain a 'bracket expression'. Rather it contains the metacharacter of `/d` that, on a very basic level*, represents the bracket expression of `[0-9]` . Therefore, this metacharacter represents single digits, and indicates to our regex search that single digits are what we are looking for.
*Please note that there are differences between `/d` and `[0-9]` in certain situations. More can be read about these differences at: https://www.quora.com/Is-there-any-difference-between-the-regular-expressions-0-9-and-d?ch=17&oid=79803313&share=887f81d2&srid=u3FIj8&target_type=question


## Author

Hello, I am Tessa, a n00b developer. Thanks for checking out this gist! Hope it helped! 

Check me out @ https://github.com/tessie-the-messy
