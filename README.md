# Instruction
This package is for generate lorem ipsum

For install type this command
```
composer require baki/loremipsum
```
After installation, on the page where you use the package you need to insert this part of the code
```
use Baki\LoremIpsum\LoremIpsum;
```

#Simple text
For generate simple text
```
LoremIpsum::generate();
```

#Text size
There are 4 text sizes. They are listed as methods.
- LoremIpsum::short()->generate();
- LoremIpsum::medium()->generate();
- LoremIpsum::long()->generate();
- LoremIpsum::verylong()->generate();

#Methods
All possible parameters (References as methods):
- short
- medium
- long
- verylong
- decorate
- link
- ul
- ol
- dl
- bq
- code
- headers
- allcaps
- prude

#Counting
the ``count`` method is used to obtain the desired paragraph number.

`Example`

``` 
LoremIpsum::short()->count(2)->generate(); 
```

#Here are a few examples

`Short text, order list` : `` LoremIpsum::short()->ol()->generate(); ``

`Verylong text, unorder list, code` : `` LoremIpsum::verylong()->ul()->code()->generate(); ``

`Medium text 2 paragrafhs, link, headers` : `` LoremIpsum::medium()->link()->headers()->count(2)->generate(); ``

`Allcaps text, long, decorate` : `` LoremIpsum::long()->decorate()->allcaps()->generate(); ``

`Long text, headers, unorder list` : `` LoremIpsum::long()->headers()->ul()->generate(); ``

#Only text
For return only text without html tags, use method text();

``Example`` : ``LoremIpsum::short()->ol()->text()->generate();``