# chbs

An implementation of http://xkcd.com/936/

I.e. pick four random, common words and string them together to make a very
strong but easy to remember password.

The default corpus (word list) contains the most common words in TV and movie
scripts. A corpus of the most common words from Project Gutenberg is also
included, if you want your passwords to have a bit more of an old-timey feel.

## Installation

Add this line to your application's Gemfile:

    gem 'chbs'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install chbs

## Usage

Just running chbs with no options will be sufficient in most cases. Decrease
max rank, -R 1000 for example, to get more common words and thus more easily
remembered passwords. You can have chbs generate a bunch of passwords, -c 20
for example, and pick one that you like.

    Usage: chbs [options]
      -C, --corpus=CORPUS      Corpus of words
          --list-corpora       List included corpora
      -l, --min-length=MIN     Minimum word length [4]
      -L, --max-length=MAX     Maximum word length [10]
      -r, --min-rank=MIN       Minimum word rank [1]
      -R, --max-rank=MAX       Maximum word rank [10000]
      -n, --num-words=NUM      Number of words [4]
      -s, --separator=STRING   Word separator [-]
      -c, --count=COUNT        Number of passwords [1]

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
