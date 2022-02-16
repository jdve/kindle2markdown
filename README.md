# kindle2markdown

This tool converts Kindle highlights both from [read.amazon.com](https://read.amazon.com/kp/notebook/) as
well as from `My Clippings.txt` retrieved from a Kindle device to Markdown format. Both highlight sources
are useful, because read.amazon.com doesn't include highlights made to documents (e.g., those received using
[Send to Kindle by Email](https://smile.amazon.com/sendtokindle/email?sa-no-redirect=1)).

This is achieved using two excellent libraries:

* [fyodor](https://github.com/rc2dev/fyodor): for parsing `My Clippings.txt` files retrieved from Kindle devices
* [kindle-highlights](https://github.com/speric/kindle-highlights): for downloading highlights from read.amazon.com

## Usage

```
./bin/kindle2markdown -c FILE -e EMAIL
```

By providing both a file path and an email address, the script will import data
from the given file as well as from the Amazon website. This data will then be
combined and output to the `./out` directory in Markdown format.
