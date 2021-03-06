# Program.java.rb.ws.txt
[`Program.java.rb.ws.txt`](Program.java.rb.ws.txt) is a “simple” piece of esoteric script. Even though it looks like a mess when viewed as plaintext, it is, in fact, valid for not one, not two, but *three* programming languages:
* When compiled by Java (`Program.java`), it will print ‘`Java`’;
* When interpreted with Ruby (`Program.java.rb`), it will print ‘`Ruby`’; and
* I even squeezed the easy-to-interlace (but no-so-easy-to-actually-write) language [Whitespace](https://en.wikipedia.org/wiki/Whitespace_(programming_language)) (`Program.java.rb.ws`) into the mix. Yup, it will print ‘`Whitespace`’.

## How the heck did I mix three programs together
The esoteric programming language Whitespace only reads Spaces (` `), Tabs (`\t`) and Line-Feeds (`\n`). Non-whitespace characters are ignored and therefore can even code for another programming language. This inspired me to see if two practical languages can be mixed into a single file.

I am familiar with Ruby and Java, and conveniently, ‘`//`’ begins a single-line comment but makes an empty RegExp in Ruby. With it, Java ignores the first line of the script and reads after it, whereäs Ruby takes it as a function whose parameter is the lengthy Java code and whose computed value unused. Because Java does not bother with whitespaces, splitting its code among multiple lines is the cherry I placed on the top.

To include the Ruby script, the Java side wraps it inside a multi-line comment (`/* … */`). The Ruby side then close the String parameter, do its job, and closes Java’s comment with its own single-line comment. Finally, the Whitespace script was inserted back in as a “cheap” freebie.
