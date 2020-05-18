---
layout: post
title: Miscellaneous
tags: misc tips
last_modified_on: 2020-05-13
read_time: true
---
A collection of stuffs that I am interested in and something I had to search more than once.

<!-- MarkdownTOC autolink="true" -->

- [Virtual Machines:](#virtual-machines)
- [Tips for professionalism](#tips-for-professionalism)
- [Websites for Machine Learning](#websites-for-machine-learning)
- [Command lines for an easy life](#command-lines-for-an-easy-life)
- [Visualization](#visualization)
- [Jokes](#jokes)
- [Data Science Workflow](#data-science-workflow)
- [Cheat sheet](#cheat-sheet)
	- [Vim](#vim)
	- [Tmux](#tmux)
	- [Conda virtual environment](#conda-virtual-environment)
- [Python tips](#python-tips)
- [Templates](#templates)
	- [1. Presentations](#1-presentations)

<!-- /MarkdownTOC -->


## Virtual Machines:
"Virtual machines are software computers that provide the same functionality as physical computers. Key files that make up a virtual machine include a log file, NVRAM setting file, virtual disk file, and configuration file."
1. [VirtualBox](https://www.virtualbox.org/wiki/VirtualBox)
2. [VmWare](https://www.vmware.com/asean.html)
3. [Vagrant](https://github.com/hashicorp/vagrant)

<hr color="#0F24F3">

## Tips for professionalism

1. [Ten simple rules for writing and sharing computational analyses in Jupyter Notebooks](https://journals.plos.org/ploscompbiol/article?id=10.1371/journal.pcbi.1007007#sec002)
2. [Cookiecutter Data Science](http://drivendata.github.io/cookiecutter-data-science)
3. [Principles for making things for the web](https://github.com/veltman/principles)
4. [Setup Keychain for SSH agent](https://help.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent)
5. [Jupyter Notebook Extensions](https://towardsdatascience.com/jupyter-notebook-extensions-517fa69d2231)
6. [Dealing with path in different OS](https://medium.com/@ageitgey/python-3-quick-tip-the-easy-way-to-deal-with-file-paths-on-windows-mac-and-linux-11a072b58d5f)
7. [PyAutoGUI](https://medium.com/datadriveninvestor/automating-your-job-with-python-f1952b6b640d): a cross-platform GUI automation Python module, used to programatically control the mouse and keyboard. This module can be applied to automate jobs with Python scripts.
8. [Auto format excel file from Python with XlsxWriter](https://xlsxwriter.readthedocs.io/index.html): no longer need to manually check and highlight the results in Excel. With xlsxwriter, we can format highlights (bold, font color, background color, etc. ) for the excel output.
9. [TOC generator in SublimeText](https://packagecontrol.io/packages/MarkdownTOC)

    * Enable TOC:
        * Press `Shift` + `Command` + `P` to open `Command Palette`.
        * Type `TOC` and choose `Insert TOC`  
        
    * Modification of TOC:
        * `levels="2,3"` --> Level of headers to be display in TOC
        * `autolink="true"` --> Link with the part
        * `style="ordered"` --> Add the number before header
        
    * Update TOC: Open `Command Palette` and choose `Update TOC`
<br><br>
10. Github Protips:

* [From Lee Reilly](https://github.blog/2020-04-09-github-protips-tips-tricks-hacks-and-secrets-from-lee-reilly/)
    * Fuzzy file finder
    * Octotree (Enterprise): Browse files and directories with ease
    * Mention highlighter
    * Linking to code snippets
    * Markdown formatting tips
* .gitignore
    * Create global .gitignore file: [http://egorsmirnov.me/2015/05/04/global-gitignore-file.html](http://egorsmirnov.me/2015/05/04/global-gitignore-file.html)
    * Generate `.gitignore` file for specific IDE, OS:  [https://gitignore.io/](https://gitignore.io/)
* List contents from remote github repo: [https://stackoverflow.com/a/38183088/11524628](https://stackoverflow.com/a/38183088/11524628)

    Examples:
    ```bash
    svn ls https://github.com/clauswilke/dviz.supp
    svn ls https://github.com/clauswilke/dviz.supp/branches/master/data/
    ```
<br>
11. Set up dotfiles
    * [Documents](https://dotfiles.github.io/)
    * [Examples](https://github.com/mathiasbynens/dotfiles)
<hr>

## Websites for Machine Learning
1. [Distil](https://distill.pub/about/)

    A powerful medium to share new ways of thinking.
    
<hr>

## Command lines for an easy life
1. Find files containing specific text
```bash
grep -Ril "text-to-find" <directory where to find>
```
Learn more [here](https://stackoverflow.com/questions/16956810/how-do-i-find-all-files-containing-specific-text-on-linux/16956844#16956844).

2. [Crontab](https://www.adminschoice.com/crontab-quick-reference): Allow tasks to be automatically run in the background at regular intervals by the cron daemon.
Example: To remove .DS_Store (a file that stores custom attributes of its containing folder in MacOS) every hour
```bash
@hourly find ~ -name ".DS_Store" -depth -exec rm {} \;
```

3. [Privacy](https://www.pluralsight.com/blog/it-ops/linux-file-permissions): Change directory and file permissions.

4. [Youtube downloader](https://github.com/ytdl-org/youtube-dl)

5. Mount/Unmount:
To mount:
```bash
# at your local machine
mkdir <new_folder>
sshfs <usrnam>@<hostname>:<path/to/folder> <path to new_folder>
```
To unmount with `umount`, we need super user permission.
As a normal user, you can use `fusermount`:
`fusermount -u mountpoint`

<hr>

## Visualization
1. [Graph gallery](https://www.r-graph-gallery.com/)
This page is a collection of beautiful charts with the R programming language. It also supplies many materials for visualizsation task.

<hr>
## Jokes
1. [Statistics Jokes](http://my.ilstu.edu/~gcramsey/Gallery.html?fbclid=IwAR2rM-nbwJYeQIIJSQBMzMNh9jJm-WUUw_jdhQuRAS66kHIwleiEnA-igPU): A gallery of statistics jokes by Dr. Ramseyer
Yihui Xei also gave his comment about those jokes in a presentation: [link](https://yihui.org/en/2007/10/jokes-in-statistics-a-talk-to-be-given-in-cueb/)

<hr>

## Data Science Workflow
1. [Dask](https://docs.dask.org/en/latest/)

<hr>

## Cheat sheet
### [Vim](https://vim.rtorr.com/)
### [Tmux](https://gist.github.com/MohamedAlaa/2961058)
* Prefix: `^b`
* Enable mouse scrolling in tmux: press `prefix` + `:`, then:
    
    **On linux**
    
     * For `tmux v < 2.1`: `setw -g mode-mouse on`
     * For `tmux v >= 2.1`: `setw -g mouse on`
                
    **On MacOSx**: can use `set` instead of `setw`
        
* Capture tmux scrollback to a file: [link](https://unix.stackexchange.com/questions/26548/write-all-tmux-scrollback-to-a-file)
    * `prefix` + `:`, then type: `capture-pane -S -3000` + `return`
    * `prefix` + `:`, then type: `save-buffer path/to/logfile` + `return`
     
### [Conda virtual environment](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html)

<hr>

## Python tips
1. [slots](https://stackoverflow.com/questions/472000/usage-of-slots): The special attribute __slots__ allows you to explicitly state which instance attributes you expect your object instances to have, with the expected results:
* faster attribute access.
* space savings in memory.
2. Install a jupyter kernel inside an virtual environment
```bash
ipython kernel install --user --name=<name of virlenv>
```

3. Show description of a function/module, type:
```bash
help(<name of function/module>)
```

<hr>

## Templates
### 1. Presentations
* [You Exec](https://youexec.com/keynote-presentation-free-sjwhsk)




