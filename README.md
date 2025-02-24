<img width="779" alt="demo" src="https://github.com/capjamesg/web-reader/assets/37276661/610188cb-d035-40dc-8990-a1b7b908fa2f">

# Web Reader

A minimal web reader for following web feeds.

This project is intentionally not designed to be a real-time reader. Rather, it is designed to retrieve content in intervals (i.e. every hour, every day).

Web Reader supports the following feed formats:

- RSS
- Atom
- JSON Feed
- microformats2

Only posts published in the last two days will be displayed in the feed reader.

This is the predecessor to [Artemis](https://artemis.jamesg.blog), a calm hosted web reader.

## Installation

First, clone this repository and install the required dependencies:

```
git clone https://github.com/capjamesg/web-reader
cd web-reader
pip install -r requirements.txt
```

Then, update `feeds.txt` with the URLs of the feeds you want to follow.

Every feed should be on its own line in `feeds.txt`.

To poll for new posts, run:

```
python3 poll.py
```

To generate a site from the posts, run:

```
aurora build
```

Your feed will be available at `_site/index.html`.

This project uses the [Aurora](https://github.com/capjamesg/aurora) static site generator to generate web pagea. You can customise the site to your requirements. Reference material for Aurora is available on the [Aurora documentation website](https://aurora.jamesg.blog).

## License

This project is licensed under an [MIT license](LICENSE).
