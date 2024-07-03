```shell0
# copy to clipboard 'pbcopy < <filename>'
$ pbcopy < my.text
```

```shell
.bash_profile
# terminal color
export PS1="\[\033[36m\]\u\[\033[m\]@\[\033[32m\]\h:\[\033[33;1m\]\w\[\033[m\]\$ "
export CLICOLOR=1
export LSCOLORS=ExFxBxDxCxegedabagacad

# ls
alias ls='ls -aGFh'

# Apache Configuration
# Start and stop apache server
alias apRS='sudo apachectl restart'
alias apSA='sudo apachectl start'
alias apST='sudo apachectl stop'

# Start mysql server
alias sqST='sudo mysql.server start'

#Command prompt php 7.1 instead of 5.1
export PATH=/usr/local/php5/bin:$PATH

#Command for pretty print json
alias jsonpp='python -m json.tool'

#Command to show tree map
alias tree="find . -print | sed -e 's;[^/]*/;|____;g;s;____|; |;g'"

#Mysql server
alias mysqlstart='sudo /usr/local/mysql/support-files/mysql.server start'
alias mysqlstop='sudo /usr/local/mysql/support-files/mysql.server stop'

# Add Visual Studio Code (code)
export PATH="$PATH:/Applications/Visual Studio Code.app/Contents/Resources/app/bin"
export PATH="${HOME}/.pyenv/shims:${PATH}"

# Setting PATH for Python 3.12
# The original version is saved in .bash_profile.pysave
PATH="/Library/Frameworks/Python.framework/Versions/3.12/bin:${PATH}"
export PATH
```
