tmux
====
guide (good)

	# http://blog.roodo.com/dabinn/archives/19994974.html

someone says that "tmux" is better than "screen" (both are linux softwares).

	# sudo apt-get install tmux
	# cd ~

let its shortcuts be similar to screen's

	# git clone https://github.com/WayneHuangGo/tmux.git
	# cp -a ~/tmux/.tmux.conf ~

the above two commands can be replaced by commands below:

	# touch ~/.tmux.conf
	# cat /usr/share/doc/tmux/examples/screen-keys.conf >> ~/.tmux.conf
	# cat /usr/share/doc/tmux/examples/vim-keys.conf >> ~/.tmux.conf
	# vim ~/.tmux.conf

replace strings by the following commands

	# :1,$s/"bind Tab down-pane"/"bind Tab select-pane -t:.+"/g
	# :1,$s/"bind Tab up-pane"/"bind BTab select-pane -t :.-"/g
	# :1,$s/"bind j down-pane"/"bind j select-pane -t :.+"/g
	# :1,$s/"bind k up-pane"/"bind k select-pane -t :.-"/g
	# exit

open terminal again

	# tmux

after reset the shortcuts , try them!!

	# <C-a>+s	# spilt terminal horizontally
	# <C-a>+v	# spilt terminal vertically
	# <C-a>+<A-arrows>	# adjust the current windows size / resize the current windows (arrows = up, down, left, right)
	# <C-a>+?	# help list, use <C-c> to exit it
	# <C-a>+<arrows>	# switch between windows (arrows = up, down, left, right)
