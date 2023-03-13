# Sir Mix-a-bot Rides Again!

## Brief Backstory

In 2002, I (legally!) came into possession of a PUMA 260 6-dof robot arm from 1980s. Although the arm was in good shape mechanically, the controller wasn't. I spent quite a bit of time over the subsequent decade hacking together a bunch of electronics and software (with much help from friends and relatives), and got it all working. I turned it into a bartender, in fact, and it was dubbed Sir Mix-a-bot. If you're interested you can read more here: http://dsz123.net/Projects/RobotArm/

## Reboot

After another decade, Sir Mix-a-bot had languished in storage for a few years (thanks COVID-19), and when we decided to get rid of our storage unit, it finally came time to figure out what exactly was gonna happen with the robot. Scrap? Pass it on to some other hapless young engineer? No! We can rebuild it, make it bigger, stronger, and faster! Well, at least the last one. It had always been a bit sluggish, due in large part to the fact that my kludgy software was running an ancient Macbook Pro and the motor driver boards' serial comms topped out at 19200 baud, which ultimately limited how quickly I could update the motion control loop.

Plus, in the intervening years, I'd gotten a host of emails from folks asking for help in various ways getting their own robots up and running. One of the more recent email exchanges led me to learn about LinuxCNC, which is a quite powerful platform for controlling a variety of things (including robot arms). So I started over.

## Software

LinuxCNC, in my brief experience, is one of those systems that is phenomally powerful, but almost because of that fact, is also stupidly complex. Infinitely configurable; nearly impossible to document completely. Fortunately, there is a really active discussion forum where project maintainers jump in on almost every thread, helping folks navigate the system. Here's my takeaway:

1. LinuxCNC runs on top of / within Linux (duh). It relies on a real-time kernel since you wouldn't want normal OS stuff preempting your machine commands.
2. Unless you're just simulating your CNC/robot, you need to connect some hardware to the PC that's running LinuxCNC. That can happen via:
  - one or more parallel ports (old school!)
  - one or more PCI cards
  - ethernet
3. LinuxCNC has several graphical user interfaces to choose from, most (all?) of which are further configurable.
4. LinuxCNC is fundamentally all about G-code, a scripting language used to control all manner of machines and robots.

## Electronics



## G-Code

## Contents

In this repo, you'll find:
- The LinuxCNC configuration files required to connect the various pieces of the puzzle.
- Some 
- G-code scripts that are highly specific to Sir Mix-A-Bot, but perhaps helpful to other folks for some reason?

## Manipulator


