How to map capslock in linux as another "Enter" key
===================================================

1. Disable the default action of capslock

	setxkbmap -option caps:none
  
2. Set the new behaviour of the capslock key

	xmodmap -e "keycode 66 = Return"

Bonus:

How to get the Keycode of other keys?

	xev | sed -ne '/^KeyPress/,/^$/p'

How to reset the keyboard to the defaults?

	setxkbmap -option
