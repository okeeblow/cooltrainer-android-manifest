About
---------------------------------------
This is the manifest for my personal Android distro for my phone, the Galaxy Note 2. It's probably not something anybody else wants to run but can serve as an example for how to roll your own. It is based on Dirty Unicorns with a small custom vendor overlay and microg.

The canonical location for this repository is [cooltrainer.org/source](https://cooltrainer.org/source/). The GitHub remote is for social features.

Get Repo
---------------------------------------

    mkdir ~/bin
    PATH=~/bin:$PATH
    curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
    chmod a+x ~/bin/repo

Syncing the Source
---------------------------------------

    mkdir -p ~/android/cooltrainer
    cd ~/android/cooltrainer
    repo init -u https://cooltrainer.org/source/git/gynoid_manifest.git -b coolkat
    repo sync -f -j 4 | 8 | 16 | 24 | 32

