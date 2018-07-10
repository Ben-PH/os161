# Foreword

This book was made using mdbook, and can be viewed in the browser as intended using mdbook, or as a regular .md documentation. [As of writing, internal links assume browser viewing](https://github.com/Ben-PH/os161/issues/2). It is distrubuted under a permissive BSD 3-Clause License[^1].

To install mdbook:

### Installing mdbook

* First, [install rust](https://www.rust-lang.org/en-US/install.html)
* Now, install mdbook:
    ```cmd
    cargo install mdbook
    ```
* while in the root directory of the book:
  ```cmd
  mdbook serve
  ```
* Open a browser to [local-host](localhost:3000) (default port 3000)

#### One of the goals is to get this published online in the style of [rust-book](https://doc.rust-lang.org/book/)
## Contributing

Constructive issue submissions are highly sought after, are greatly appreciated and looked at seriously. A passion project is best enjoyed when shared.

Feel free to make pull-requests to change existing book content.
* Book development will be branched to book-dev [See Issue](https://github.com/Ben-PH/os161/issues/15)
* The book is under BSD 3-clause licence at time of writing, whereas os161 is under its own permissive licence. Make sure any changes you make takes this into account.
* Test the book using `mdbook test`.

I look forward to pull-requests to add content. Pull requests are much more likely to be accepted if they are part of a discussion, which you can start yourself. [See Issue - a good one to get started on?](https://github.com/Ben-PH/os161/issues/16)

### Contributors
* Reserved - [Become the first](https://github.com/Ben-PH/os161/issues/15).

### Acknowledgements

I would like to thank Kevin Elphinstone and the staff involved in UNSW COMP3231 18s1 for providing such an excelent course, the authors of OS/161 for providing the community with such a powerful teaching tool, and all those who have provided constructive feedback to this publication. I would also like the thank the community (in advance, at time of writing), for constructive issues and pull-requests. 

[^1]:  *Copyright © 2018 Ben Pieters-Hawke. Licensed under the BSD 3-Clause License. This publication may not be copied, modified, or distributed except according to those terms.*
