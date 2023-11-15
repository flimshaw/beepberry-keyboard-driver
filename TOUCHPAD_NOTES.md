# Touchpad Notes

This is very much a _proof of concept_ more than a thing you should be using. This gets the optical touchpad to register as a mouse, and should be able to work on a stock installation with the drivers etc installed.

## Step 1: build and install the driver

Pull this repo down to your beepberry, cd into wherever you pull it down and then run the following:

1. make clean
2. make
3. sudo make install

## Add the following line to /etc/udev/rules.d/99-com.rules
KERNEL=="event0", ENV{ID_INPUT_KEYBOARD}="1", ENV{ID_INPUT_MOUSE}="1"

## How to use

Reboot, and start xwindows. If you click the meta/mouse button twice, you will be able to control the cursor. Additional clicks will register as left mouse clicks. Hitting escape/the button to the right of the meta key will exit back out.
