ansible-bash-improvements-role
=========

Ansible role that allows adding several configurable bash improvements.

Requirements
------------

None

Role Variables
--------------

```YAML
#
# Enables bash completion for interactive shells
#
bash_improve_completion: true

#
# Improves the bash history
#
bash_improve_history: true

#
# Set the size of the bash history file
#
bash_improve_history_file_size: 1000

#
# Set the memory size of the bash history
# The history is finally written to the history file at the end of the session
#
bash_improve_history_memory_size: 1000

#
# Improves the default directory / files colors
#
bash_improve_dircolors: true
bash_improve_dircolor_src: files/dircolors
bash_improve_dircolor_dest: /etc/dircolors

#
# Improves the coloring and format of the root prompt
#
bash_improve_prompt: true
bash_improve_root_prompt_code: |
  PS1="\[\033[01;31m\]\u\[\033[01;33m\]@\[\033[01;36m\]\h \[\033[01;33m\]\w\[\033[0;35m\]$(__git_ps1 " (%s)")\[\033[00m\] \[\033[01;35m\]\$ \[\033[00m\]"

bash_improve_user_prompt_code: |
  PS1="\[\033[01;32m\]\u\[\033[01;33m\]@\[\033[01;36m\]\h \[\033[01;33m\]\w\[\033[0;35m\]$(__git_ps1 " (%s)")\[\033[00m\] \[\033[01;35m\]\$ \[\033[00m\]"

#
# Improves the coloring and format of the users prompt
#
bash_improve_skip_users: ""
bash_improve_home_dirs: []

#
# Improves git
#
bash_improve_git: true

#
# Improves vim
#
bash_improve_vim: true
bash_improve_vimrc_file: /etc/vim/vimrc
```

Dependencies
------------

None

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: methorz.bash_improvements }

License
-------

BSD

Author Information
------------------

https://twitter.com/methor_z
