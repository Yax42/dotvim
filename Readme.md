# Vim settings.

## Install
### Linux
    
    git clone git://github.com/aliou/dotvim.git ~/.dotvim
    ln -s ~/.dotvim/vim ~/.vim
    ln -s ~/.dotvim/vimrc ~/.vimrc
    cd ~/.dotvim

Then install [Vundle][l2] and the plugins by running:

    git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle
    vim +BundleInstall +qall

Or just run the following command:
    
    curl -fsSL https://raw.github.com/gist/91851e576aa3917c0ab8 | sh

Read the script [here](https://gist.github.com/aliou/91851e576aa3917c0ab8).
### Windows (Visual studio)
	Install vsvim https://visualstudiogallery.msdn.microsoft.com/59ca71b3-a4a3-46ca-8fe1-0e90e3f79329/
	Create _vimrc file in your USERPROFILE or HOME directory
	
## Epitech

If you are an Epitech student, remember to change these [lines][l1] with your login
and name.

##Remap Caps lock
Windows: http://www.randyrants.com/2006/07/sharpkeys_211/

Caps lock is placed in a very convenient location and is very rarely used by
most programmers. Reclaim this valuable real estate by mapping it to Esc as it
was on the original HP 9000 ITF HIL keyboards. This is the approach I'm using
right now, and I LOVE IT. Remapping the key on X Windows is done as follows.

Create a file in your home directory called .Xmodmap

	remove Lock = Caps_Lock
	keysym Caps_Lock = Escape

Create a reference to .Xmodmap in your .xinitrc

	if [ -f ~/.Xmodmap ]; then
	  xmodmap ~/.Xmodmap
	fi
If you don't want to restart X, you can manually run xmodmap ~/.Xmodmap after
you create the first file.

[source](http://dailyvim.blogspot.fr/2008/04/ways-to-avoid-esc-key.html)

	xmodmap -e 'clear Lock' -e 'keycode 0x42 = Escape'

[l1]: https://github.com/aliou/dotvim/blob/master/vim/plugin/epitech/header.vim#L17-18
[l2]: https://github.com/gmarik/vundle
[l3]: https://gist.github.com/aliou/91851e576aa3917c0ab8
