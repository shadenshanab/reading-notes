# class 17

## Automation

--------------

## Python Regular Expression

--------------

### Regular Expressions, often shortened as regex, are a sequence of characters used to check whether a pattern exists in a given text (string) or not. If you've ever used search engines, search and replace tools of word processors and text editors - you've already seen regular expressions in use. They are used at the server side to validate the format of email addresses or passwords during registration, used for parsing text data files to find, replace, or delete certain string, etc. They help in manipulating textual data, which is often a prerequisite for data science projects involving text mining.

### Regular Expressions in Python

--------------

#### In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import

### Basic Patterns: Ordinary Characters

--------------

#### You can easily tackle many basic patterns in Python using ordinary characters. Ordinary characters are the simplest regular expressions. They match themselves exactly and do not have a special meaning in their regular expression syntax.

#### Examples are 'A', 'a', 'X', '5'.

#### Ordinary characters can be used to perform simple exact matches. Most alphabets and characters will match themselves, as you saw in the example.

#### The match() function returns a match object if the text matches the pattern. Otherwise, it returns None. The re module also contains several other functions, and you will learn some of them later on in the tutorial.

#### For now, let's focus on ordinary characters!

#### Do you notice the r at the start of the pattern Cookie?This is called a raw string literal. It changes how the string literal is interpreted. Such literals are stored as they appear.

#### For example, \ is just a backslash when prefixed with an r rather than being interpreted as an escape sequence. You will see what this means with special characters. Sometimes, the syntax involves backslash-escaped characters, and to prevent these characters from being interpreted as escape sequences; you use the raw r prefix.

#### TIP: You don't actually need it for this example; however, it is a good practice to use it for consistency.

### Wild Card Characters: Special Characters

--------------

#### Special characters are characters that do not match themselves as seen but have a special meaning when used in a regular expression. For simple understanding, they can be thought of as reserved metacharacters that denote something else and not what they look like.

#### Let's check out some examples to see the special characters in action...

#### But before you do, the examples below make use of two functions namely: search() and group().

#### With the search function, you scan through the given string/sequence, looking for the first location where the regular expression produces a match.

#### he group function returns the string matched by the re. You will see both these functions in more detail later.

