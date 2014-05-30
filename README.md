## Rainbow Stream
Terminal-based Twitter Client with Streaming API support. 
Realtime tweetstream, compose, search ... and much more fun directly from terminal.
Only supports Python 2.7 or later.

This package build on the top of [Python Twitter Tool](http://mike.verdone.ca/twitter/) and [Twitter Streaming API](https://dev.twitter.com/docs/api/streaming) and inspired by [EarthQuake](https://github.com/jugyo/earthquake)

## Screenshot
![v0.0.1](https://raw.githubusercontent.com/DTVD/rainbowstream/master/screenshot/RainbowStreamvSS.png)

## Install
You will need Python 2.7+ and pip to install

**The recommened way:**
* Clone this repo
* Create virtualenv (optional but recommended)
* Install dependencies
* Install the package itself

```bash
git clone git@github.com:DTVD/rainbowstream.git
cd rainbowstream
virtualenv venv # Assume that you have virtualenv installed by "pip install virtualenv"
source venv/bin/activate
pip install -e .
```
**The quick way:**
* Install everything over the air

```bash
sudo pip install git+https://github.com/DTVD/rainbowstream.git
```

## Usage
#### The stream
Just type
```bash
rainbow
```
and see your stream.

In the first time you will be asked for authorization of Rainbow Stream app at Twitter.
Just click the "Authorize access" button and paste PIN number to the terminal, the rainbow will start.

#### The interactive mode
While the rainbow stream is continued, you are also ready to tweet, search, reply, retweet... directly from console.
Simply hit Enter key and type "h" to view the help

Input is in interactive mode. It means that you can use arrow key to move up and down history, tab-autocomplete or 2 tab to view available suggestion

Here is full list of supported command

__Stream Command__
* ```switch public #AKB48``` will switch current stream to public stream and track keyword ```AKB48```

* ```switch public #AKB48 -f ``` will do exactly as above but will ask you to provide 2 list:

    ```Only nicks``` decide what nicks will be include only.

    ```Ignore nicks```decide what nicks will be exclude.

* ```switch public #AKB48 -d ``` will apply filter to *ONLY_LIST* and *IGNORE_LIST*.
You can setup 2 list above at ```config.py```

* ```switch mine``` will switch current stream to personal stream. ```-f``` and ```-d``` will work as well.

__Action Command__

* ```home```will show your timeline. ```home 10``` will print exactly 10 tweet.

* ```view @mdo```will show @mdo 's timeline. ```view @dmo 9``` will print exactly 9 tweet.

* ```t the rainbow is god's promise to noah```will tweet exactly *'the rainbow is god's promise to noah'*

* ```rt 12```will retweet the tweet with *[id=12]*. You can see id of each tweet beside the time.

* ```rep 12 Really```will reply *'Really'* to the tweet with *[id=12]*.

* ```del 12```will delete thw tweet with *[id=12]*.

* ```s #noah```will search the word *'noah'*. Result will come back with highlight.

* ```fr```will list all friend (You are following people).

* ```fl```will list all follower.

* ```h```will show the help.

* ```c```will clear the screen.

* ```q```will quit.

For example see the screenshot above.

## Bug Report
Please [create an issue](https://github.com/DTVD/rainbowstream/issues/new) 
or contact me at [@dtvd88](https://twitter.com/dtvd88)

## License
Rainbow Stream are released under an MIT License. See LICENSE.txt for details
