# Foreword

This book was made using mdbook, and can be viewed in the browser as intended using mdbook, or as a regular .md documentation. (As of writing, internal links assume browser viweing)

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

Constructive issue submissions are highly sought after, and are greatly appreciated and looked at seriously.

Feel free to make pull-requests to change existing book content.
* Book development is on master (will be branched to book-dev shortly)
* Book will be periodcally merged into all Learning Project branches to keep them up to date (I'm interested in suggestions, I can't immagine that's the best solution)
* The book is under BSD 3-clause licence at time of writing, whereas os161 is under its own permissive licence. Make sure any changes you make takes this into account.
* Test the book using mdbook utilities.

If you wish to add book content, please make sure it is part of an issue, and keep a discussion going. Taking the initiative on issues, discussons, and working on them is encouraged.

### Contributors
* Reserved

### Acknowledgements

I would like to thank Kevin Elphinstone and the staff involved in UNSW COMP3231 18s1 for providing such an excelent course, the authors of OS/161 for providing the community with such a powerful teaching tool, and all those who have provided constructive feedback. I would also like the thank the community (in advance, at time of writing), for constructive issues and pull-requests. 
