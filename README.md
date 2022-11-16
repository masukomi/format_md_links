# format_md_links

A python3 command line tool to switch between inline and relative markdown links. The new version of the file is printed to Standard Out.


```text
USAGE: format_md_links [-i|-r|-h] <path/to/markdown/file>
               -i use inline style links
               -r use relative style links
               -h print this usage⏎
```

## Examples (using the provided test files):

Convert from relative links to inline:
``` text
❯ ./format_md_links -i file_with_relative_links.md
The quick brown [fox](http://en.wikipedia.org/wiki/Fox) jumped over the lazy [dog](http://en.wikipedia.org/wiki/Dog).

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.⏎
```

```text
❯ ./format_md_links -r file_with_inline_links.md
The quick brown [fox][1] jumped over the lazy [dog](http://en.wikipedia.org/wiki/Dog
).

Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.


[1]: http://en.wikipedia.org/wiki/Fox⏎
```




## Credit where credit is due

The [original version](https://github.com/seth-brown/format_md_links/tree/3e08bc679dabe8ea402b373820c3c990ffee013f) was written by [Seth Brown](https://github.com/seth-brown/) in python 2.x.

They've since [rewritten it in Typescript](https://github.com/seth-brown/format_md_links). 

This repository [casts resurrection](https://www.dndbeyond.com/spells/resurrection) on the old version, brings it up to python3, and changes how you invoke it. Really though, Seth did most of the work. 
