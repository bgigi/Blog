# Philosophies Conclude - instructions

This repository uses the Jekyll template [Clean Blog Jekyll](http://startbootstrap.com/template-overviews/clean-blog-jekyll/) is a stylish, responsive blog theme for [Bootstrap](http://getbootstrap.com/) created by [Start Bootstrap](http://startbootstrap.com/). This theme features a blog homepage, about page, contact page, and an example post page along with a working contact form powered by [Formspree](https://formspree.io/).

## Preview

[View Blog](https://philosophiesconclude.github.io/Blog/)

## Installation & Setup

1. Install [Ruby](https://www.ruby-lang.org/en/documentation/installation/) - Install version listed in section [WHICH VERSION TO DOWNLOAD?](https://rubyinstaller.org/downloads/)
2. Setup Jekyll - From a plain cmd window run `gem install jekyll bundler`
3. Install [Git](https://git-scm.com/downloads) - click [windows](https://git-scm.com/download/win) select latest 64bit version.
4. Type cmd.exe in the windows search on the start bar and then open it.
5. To create your working folder run the following command in the cmd window. `md c:\git\github\pc`
6. To navigate to your working folder run the following command in the cmd window. `cd /d c:\git\github\pc`
7. To enlist in this git repo run the following command in the cmd window. `git clone https://github.com/PhilosophiesConclude/Blog.git`
8. Set local checkin info
   - `git config --local user.name "Philosophies Conclude"`
   - `git config --local user.email philosophiesconclude@hotmail.com`

### Making an update to the site

The github pages site is configured to pull from the master branch.

1. Update the site content under c:\git\github\pc\Blog -- if it is just adding a new post then put it c:\git\PC\Blog\_posts
2. From a cmd line window at c:\git\github\pc\Blog and run the following command. `Jekyll serve`
3. After it is finished building the _site folder it will give you a server address to navigate to usually http://127.0.0.1:4000//
4. Navigate to the site and double check everything looks correct. The comments section may not load with an error saying site isn't configured.  Ignore that error.
5. From a cmd line window at c:\git\github\pc\Blog and run the following command. `git add .` - notice that period at the end of the git add command it is important.
6. From a cmd line window at c:\git\github\pc\Blog and run the following command. `git commit -m"A simple description of my change"`
7. From a cmd line window at c:\git\github\pc\Blog and run the following command. `git push`
8. Wait from 10min-2hours and your changes should be live.

### Updating the site to use the latest version of the template.

If you already have this enlistment setup and configured skip to step 4.

1. Enlist in https://github.com/PhilosophiesConclude/startbootstrap-clean-blog-jekyll
   - Open cmd.exe prompt
   - `cd /d c:\git\github\pc`
   - `git clone https://github.com/PhilosophiesConclude/startbootstrap-clean-blog-jekyll.git`
   - `cd startbootstrap-clean-blog-jekyll`
2. Set local checkin info
   - `git config --local user.name "Philosophies Conclude"`
   - `git config --local user.email philosophiesconclude@hotmail.com`
3. Set upstream to original fork branch
   - `git remote add upstream https://github.com/BlackrockDigital/startbootstrap-clean-blog-jekyll.git`
4. Fetch upstream data
   - `git fetch upstream`
5. Merge upstream changes into master.
   - `git checkout master`
   - `git merge upstream/master`
   - `git push`
6. Merge master into template (template is the branch we have customizations in)
   - `git checkout template`
   - `git merge master`
   - `git push`
7. Navigate to Blog enlistment
   - `cd /d c:\git\github\pc\Blog` 
8. Setup template upstream
   - `git remote add upstream https://github.com/PhilosophiesConclude/startbootstrap-clean-blog-jekyll.git`
9. Fetch template upstream
   - `git fetch upstream`
10. Merge template in.
   - `git checkout master`
   - `git merge upstream/template --squash`
11. See if any changes need to be resolved.
   - `git status` - if this shows no open files then skip to the push.
12. Resolve changes
   - Any files in red you need to reason about if it is a file you have deleted from the site intentionally then run `git rm myfilename`.
   - If it is a file with conflicting changes then open in notepad and search for >>>> and resolve the conflicting section and then run `git add myfilename`.
13. Checkin resolved files
   - `git commit -m"Merge from template"`
14. Test changes
   - `Jekyll serve` - poke around website especially any manual resolve areas
15. Push changes
   - `git push`
