About
---------------------------------------
This is the manifest for my personal Android distro for my phone, the Galaxy Note 2. It's probably not something anybody else wants to run but can serve as an example for how to roll your own. It is based on Dirty Unicorns with a small custom vendor overlay and microg.

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
    repo init -u https://github.com/okeeblow/cooltrainer-android-manifest.git -b du44
    repo sync -f -j 4 | 8 | 16 | 24 | 32


Submitting Patches
------------------
DU is an open source project that lives because of contributions of the Android community.

With that said, patches are always welcome!

You can send patches by using these commands:

    cd <project>
    <make edits>
    git add -A
    git commit -m "commit message"
    git push ssh://<username>@gerrit.dirtyunicorns.com:29418/<project> HEAD:refs/for/<branch>

Register at gerrit.dirtyunicorns.com and use the username that you registered there in the above command

Commit your patches in a single commit. Squash multiple commit using this command: git rebase -i HEAD~<# of commits>

If you are going to make extra additions, just repeat steps (Don't start a new patch), but instead of git commit -m
use git commit --amend. Gerrit will recognize it as a new patchset.

Thank you,
DU Team
