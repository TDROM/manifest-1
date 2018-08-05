Project-Xtended:

A ROM Based on GZOSP, with features from almost all Custom ROMs available. 

We Thank all those Devs & Team from whom we have kanged/cherry-pick committs.

Getting Started
Initializing the environment
[Hint: This command updates the Ubuntu Packages List (Install Listing) and install the required version of Java]

$ sudo apt-get install openjdk-8-jdk
Let that install and then proceed. More copy and paste:

[Hint: Running this command installs the other required packages to build android]

$ sudo apt-get update && sudo apt-get install git-core gnupg flex bison gperf libsdl1.2-dev libesd0-dev libwxgtk3.0-dev squashfs-tools build-essential zip curl libncurses5-dev zlib1g-dev openjdk-8-jre openjdk-8-jdk pngcrush schedtool libxml2 libxml2-utils xsltproc lzop libc6-dev schedtool g++-multilib lib32z1-dev lib32ncurses5-dev gcc-multilib maven tmux screen w3m ncftp liblz4-tool pngquant rsync openssl libssl-dev build-essential libidn11-dev libidn11
Getting the Source
Making required directories Obtaining the repo binary Adding repo binary to your path Giving the repo binary proper permissions Initializing an empty repo Syncing the repo Alright, so now we’re getting there. I have outlined the basics of what we’re about to do and broke them down as I know them. This is all pretty much going to be copy/paste so it’ll be fairly difficult to screw this up :) Make directory for the repo binary

$ mkdir ~/bin
Add directory for the repo binary to its path

$ PATH=~/bin:$PATH
Downloading repo binary and placing it in the proper directory

$ curl http://commondatastorage.googleapis.com/git-repo-downloads/repo > ~/bin/repo
Giving the repo binary the proper permissions

$ chmod a+x ~/bin/repo

# ======== # ======== # ======== # ======== #

To initialize your local repository, use this command:

    repo init -u https://github.com/Project-Xtended/manifest.git -b xtended

To sync the repository, use this command:

    repo sync -f -c -j8 --force-sync --no-clone-bundle --no-tags

To Build, use following commands:

1) . build/envsetup.sh
2) lunch xtended_device-userdebug
3) mka bacon

Change device with your device code name. Ex.- oneplus3, dumpling, etc.
	
# ======== # ======== # ======== # ======== #

XDA Thread Title:

     [STABLE] MSM Xtended x9 [Oreo|Android 8.1] [Month Date, 2018]


