## Basics of the CLI (command line interface for n00bs, some are missing below do to reordering)

1.    DONT DO THIS: rm -rf / (this means delete everything)
2.    ssh webadmin@1.2.3.4 (gets you into a server)
3.    mkdir hello (make a directory called hello)
4.    cd hello (changes your directory to hello, assumes it has been created)
5.    pwd (prints path)
6.    rm your-filename-here (remove filename (BE CAREFUL!)
7.    rmdir - remove directory, if empty
8.    rm -rf directory/xyz (removes whole directory with stuff in it)
9.    *.php (removes all files of that type in one directory)
10.    man your--program-here (shows you manual for that part)
11.    cd .. (jumps you back a directory)
12.    cd ../.. (jumps you back two directories)
13.    cd (jumps you back to the home directory)
14.    cd / (take you to the root directory)
15.    cd /home/your-username-here (!where you are!)
16.    mv /path/goes/here/filename /path/goes/here/your-file-name-2  (mv moves a file)
17.    cp /path/goes/here/filename /path/goes/here/your-file-name-2 (copies file in same folder)
18.    cp -a /path/goes/here/. /path/goes/here/ (copies the contents of an existing folder into a previously defined folder)
19.    try to put a first letter on the line, then use TAB key and it tries to autocomplete - nice!
20.    find -name hosts (get)
21.    sudo (switch user, do xyz...)
22.    /etc/hosts (where the host file lives)
23.    /etc/init/d (the folder usually the daemon to start programs live)
24.    /etc/init.d/sendmail start (starts mail on server)
25.    ~/ (Shortcut to go home directory of a given user)
26.    Control + C (kills the process on the command line)
27.    pbcopy < ~/.ssh/id_rsa.pub (copies something to your clipboard, so you can paste it like a human being - only in OSX. This example copies your SSH key.)
28.    cat - concatenate the key (for example, cat ~/.ssh/id_rsa.pub ), prints my ssh key
29.    gzip PATH-HERE - gzips a file for you, which is what phpmyadmin seems to like
30.    mysql -uUSERNAME -pPASSWORD DATABASENAME < MYDATABASE.sql (imports a DB)
31.    control c (stops the process on the command line)
32.    shift+control+v (paste into terminal)
33.    chmod +x or chmod 777 (execute permission to make scripts happen)
34.    cd ~/.ssh (see if you have ssh keys installed)
35.    ssh-keygen -t rsa -C "youremail@host.com" (installs SSH keys - needed for git transactions and other stuff)
36.    source .your-dot-file-here (this refreshes the file, makes life great)
37.    sudo your-samba-passwd-here -a quickstart (changes samba password, allows websites folder in quickstart to appear in mac os x finder)
38.    ssh your-user-name-here@your-ip-address-here (logs you into an SSH session)
39.    exit (logs you out of an SSH session)
40.    scutil --get HostName (prints your computer's hostname - OSX)
41.    scutil --set HostName your-name-hostname-here (changes your computer's hostname - OSX)
42.    hostname (prints your computer's hostname - Linux)
43.    clear (erases output in terminal window) 
44.    sudo smbpasswd -a your-name-here (changes your samba password for file transfer between OSes, good for virtual machines)
45.    sudo service smbd restart (restarts samba)
46.    rvm --default use 2.0.0 (forces Mac OSX to permanently use a newer version of Ruby)
47.    rvm --default use rubygems 2.0.03 (forces Mac OSX to permantenly use new rubygems - necessary to run Jekyll/Octopress)
48.    rubygems and ruby defaults have to be set everytime you open a new terminal session in OSX
49.    cordova platforms add ios
50.    cordova platforms add android
51.    cordova build && cordova emulate (will build your app and emulate it so you can see what you did)
52.    df (gives you a readout of the disk space your system has available)
53.    pwd | pbcopy (copies your current path in OSX only)
54.    xcode-select --install (installs command line tools for xcode - only necessary on osx 10.8 and down, comes standard on osx 10.9 and up)
55.    chrome://flags (IN BROWSER WINDOW, NOT COMMAND LINE - you play with chrome's plumbing, like disabling that stupid notifications center that tacked into OSX)
56.    If you install node.js, put it here: /usr/local/bin/npm
57.    sudo npm install -g yo (if you have node.js, this installs yeoman, bower and grunt)
58.    sudo npm install -g generator-webapp (puts scaffolding in for creating webapps)
59.	   sudo chown your-user-name-here /usr/local/your/root/path/here (changes ownership of various files via CLI)
60.
61.
62.
63.
64.
65.
66.
67.
68.    ssh root@192.###.###.### (gives you shell access to a server, will prompt for shell password)
69.    <Return> ~ . (kills an open ssh session) 
70.    service mysqld start (starts up the mysql server, assumes mysql is installed on the box)
71.    ls (spits out list of directory view)
72.    scp -r /Users/username-here/desktop/source ssh-username-here@ftp.domain.com:/home/user/public_html/dir/destination (scp securely copies a directory from one place to another - the directory on the left is the SOURCE, the right is the DESTINATION)
73.    pwd | tr -d '\n' | pbcopy (copies command line path in OSX - h/t: bradlanders.com) - make an alias of this so its less crazy next time: alias cpwd="pwd | tr -d '\n' | pbcopy"
74.    cpwd (will copy a path to your clipboard, after you make the alias in the above step - aliases will only work locally - YOUVE BEEN WARNED!)
75.    service httpd start (starts your apache server, assumes apache is installed on the box)
76.    ssh -p #### username-here@server-name-here (connect to a specific port (non-22) on a ssh server)
77.    CNTL + C (kills command line process dead)
78.    tar -cvzf youfilename-here-dump.tar.gz /home/your/path/here (tars up a directory for you)  
79.    ln -s /path/to/file /path/to/symlink (links file to a path with symlink)
80.    /System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources/airport -I | awk '/ SSID/ {print substr($0, index($0, $2))}' (OSX ONLY! - gets you the SSID of the wireless network you are on)
81.    Command + K (OSX clears Bash cache)
82.
83.
84.    htpasswd -c /user/your-name-here/domain.com/.htpasswd admin (sets up the encrypted .htpasswd file youll need to password protect your apache-based server - will prompt for password, assumes you have apache 2.x installed on your server)
85.    cd volumes (access remote drives - if already mounted, they will be at volumes/drive-name-nere)
86.    cd "Foldername with a Space" (must use quotes to espace space characters on the command line)
87.    /var/www/html or /usr/local/apache/htdocs (This is where your website should/could live on a linux server. Paths are from the root)


=============
## Front-end Tooling

01.    	sudo gem install sass (installs the CSS preprocessor SASS - you need to have Ruby + RVM installed first)
02.    	sass -v (calls up the sass version)
03.    	grunt test (preps your app for deployment)
04.    	grunt server (gets your localhost going)
05.    	grunt whatever-command-you-want-here --force (flag will override verbose testing periods)
06.    	bower search (shows entire bower JS library)
07.    	bower search your-JS-package-here (searches the directory)
08.    	bower install your-JS-package-here (adds a JS dependency to the project in your folder, works in conjunction with Yeoman)
09.		npm install -g yo generator-wordpress (installs the community's favorite wordpress yeoman generator - assumes you have yeoman and npm installed)


=============
## GIT! (super useful to do this on the command line versus GUI)

00.	  brew install git (installs git, assumes you have homebrew)
01.   git config --global user.name "Your Name" (tells Git what your name is)
02.   git config --global user.email "your_email@whatever.com" (tells Git what your email is)
03.   git init (creates a repository of the current directory)
04.   git add your-filename-here (adds a new file)
05.   git commit -m "First Commit" (Commits file with a message in quotes)
06.   git status (tells you all about the git repositories' files).   git diff head (shows me whats different between whats getting committed and whats in there now)
07.   git add (stages changes to your repository BUT does not officially add them yet)
08.   git add --all (stages ALL changes to your repository, new in Git 2.0)
09.   git reset HEAD filename-here (undoes / unstages changes before they are committed). If you dont specify a comment, the system will drop you into Vim (text editor).  Hit ESCAPE key to change modes after inserting text...
10.   git remote add local-repo-name-here git@github.com:jserrao/John-is-becoming-self-aware.git (basically this means you're connecting git to a remote git repository)
11.   git remote add --mirror=push state-blog-repo git@rcsm.beanstalkapp.com:/state-blog-repo.git (establishes that your local is going to push to the remote)
12.   git push local-repo-name-here master (pushes my local up to github, 'local-repo-name-here MUST be the name of your repo')
13.   git stash save (will save changes that are not committed yet, like a faux branch)
14.   git remote -v (tells you what remote repos are connected to your local repo)
15.   git config --global color.ui true (sets up the cool command line color coding)
16.   /home/your-name-here/.ssh/id_rsa.pub (this is where you SSH keys live, youll have to hand the public side of your key to github)
17.   git clone git://repo-url-goes-here.git destination-folder-here (just put a space after the standard clone command to get a nice destination folder)
18.   git clone -b branch-here remote-repo-here (clone a remote branch)
19.   git submodule add https://github.com/user-name-here/repo-name-here /destination/directory/here (puts a git submodule into your current repo)
20.   (FORCE FLAG example) git submodule add -f repo-here directory-here (-f forces something to be added, even over the .gitignore file)
21.   git status -s (does a shorter version of the status thing)
22.   git remote add origin https://github.com/user-name-here/repo-name-here
23.   git remote set-url -add origin https://github.com/user-name-here/repo-name-here (specifically set's the URL for a remote repo, 'origin' in this case)
24.   git push origin master (pushes your code up to a remote, 'origin' is remote, 'master' is your local branch - must setup a remote beforehand)
25.   git add -u (adds deleted files into the commit)
26.   git config core.autocrlf false (fixes line ending errors)
27.   git config core.safecrlf warn (allows git to actually convery CRLF (win) to LF (linux/osx) line endings)
28.   git config --global --add color.ui true (turns git's coloring on)
29.   git rm file-name-here.txt (removes file | directory from the repo)
30.   git ls-tree --full-tree -r HEAD (list of all files in your repo)
31.   git branch (shows you a list of all branches; the one with a '*' is your current branch)
32.   git tag -a v1.4 -m 'my version 1.4' (tags your branch with a version)
33.   git show v0.1 (git will show whats going on with a given tag)
34.   git rm -r -f .sass-cache/ (recursively removes a whole bunch of junk from your repo)
35.   git branch your-branch-here (makes a new branch)
36.   git checkout your-branch-here (switches to doing commits against that branch)
37.   git checkout -b your-name-here/your-topic-here (establishes a new branch and switches to it so that future commits will be made against it)
38.   git remote -v (shows you all of your remotes)
39.   git stash clear (deletes everything off of stash)
40.   git merge branch-name-here (will merge branch-name-here with whatever branch you are on, do 'git pull' on your branch and make sure it's up to date with origin before merging!)
41.   git reset --hard \[hash\] (resets git to a given commit in the past on your branch) 
42.   git branch -v (shows all branches, active one has '*' next to its name)
43.   git log -n 5 --author=your-name-here (shows the last 5 commits from a given author)
44.   git reset (undoes whatever you staged, all of it)


=============
## Homebrew (package manager for Mac)

00.	   ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)" (installs homebrew)
01.	   brew doctor (tells you whats wrong with homebrew's formulas, whats going in the 'cellar')
02.    brew update (updates homebrew)
03.    brew upgrade your-package-here (updates a given brew, like node, npm, yeoman, etc)
04.    brew link --overwrite your-package-here (forces symlink creation)
05.    brew prune (removes dead symlinks)
06.    brew [whatever] --dry-run (tells you whats going to happen before you do it)


=============
## Transferring things (SFTP, SCP, rsync)

# SCP
01.    [Everything SCP - go here](http://kb.iu.edu/data/agye.html)
02.    scp -r local-path-goes-here remote-user@remote-hostname:your-remote-path-goes-here (EXAMPLE: scp -r /users/your-name/documents/mapbox/export/tile-set.mbtiles user@61.56.90.123:/home/user/mapbox-tiles/tile-set.mbtiles, the -r makes it recurse through the entire folder)

# SFTP
01.    sftp your-host-here (gets you into)
02.    mput /your/path/here/filename.txt (puts your file on the server, navigate to where you want the file first!)

# rsync (the only way to fly)
01.    rsync -rv --exclude='.git' /Users/your-name-here/sites/personal/example.com username-here@you-site.com:/home/user/public_html/site-folder (move a file up to a server via SSH while excluding .git | -r = recursive, -v = verbose output)
03.    rsync -rv /Users/your-name-here/sites/personal.com/ username-here@you-site.com:/home/user/public_html/site-folder (NOTE - trailing slash on first path! this moves the contents of the folder, not the folder itself)


=============
## Ubuntu

001.    sudo apt-get upgrade (gets system updates)
001b.	sudo apt-get dist-upgrade (upgrades you to a new version of ubuntu)
002.    sudo apt-get update (installs system updates)
003.    sudo apt-get program-name-here (if the program has a binary build, you get it via this command)
004a.   sudo add-apt-repository ppa:webupd8team/sublime-text-2; (gets you sublime text but any repo could be put here after the ppa: part)
004b.   sudo apt-get update; (run update again)
004c.   sudo apt-get install sublime-text (installs sublime)

# Adds pbcopy to ubuntu
005a.   sudo apt-get install xsel
005b.   alias pbcopy='xsel --clipboard --input' (gets you pbcopy)
005c.   alias pbpaste='xsel --clipboard --output' (gets you pbpaste)

006.    sudo whereis your-filename-here (tells you where a certain file is, but it really doesnt work)
007.    sudo /usr/share/webmin/changepass.pl /etc/webmin root new-password (changes your webmin password, which is similar to an act of god)
008.    sudo a2enmod rewrite (sets up rewrite_mod for Apache2 - this powers pretty URLs in many CMSs)
009.    /Applications/VirtualBox.app/Contents/MacOS/VBoxGuestAdditions.iso (path for virtual box guest additions if you are running an Ubuntu dev machine from OSX)
010.    CNTL+H in file browser (shows hidden files in Ubuntu)


=============
##Vim (an annoying text editor that you will come into contact with on the command line)

01.    vim your-filename-here (vim will open OR create file)
02.    DD (delete's the current line)
03.    :w (write file)
04.    :q (quit Vim)
05.    :wq (write/quit Vim)
06.    o (lets you insert text on a new line)
07.    i (lets you insert text on same line)
08.    x (deletes a character)
09.    A (moves you to the end of content)
10.    G (end of line, go into insert mode)
11.    escape (exits you from editing content mode)
12.    :e (new file)
