Bighops Board Taplist
=====================

The files in this git repository are the systemd user units that are used to
start and display the bighops gastropub taplist.

This should be cloned to ~/.config/systemd/user/

Then you need the [user-session-units](https://github.com/sofar/user-session-units) and [xorg-launch-helper](https://github.com/sofar/xorg-launch-helper) to launch xorg.

    [bighops@alarmpi ~]$ tree .config/systemd/user/
    .config/systemd/user/
    ├── default.target -> dwm.target
    ├── dwb.service
    ├── dwm.service
    ├── dwm.target
    ├── dwm.target.wants
    │   └── dwm.service -> /home/bighops/.config/systemd/user/dwm.service
    ├── final.target
    ├── mailer.service
    ├── midori.service
    ├── mystuff.target
    ├── mystuff.target.wants
    │   ├── dwb.service -> /home/bighops/.config/systemd/user/dwb.service
    │   ├── mailer.service -> /home/bighops/.config/systemd/user/mailer.service
    │   ├── taplist.timer -> /home/bighops/.config/systemd/user/taplist.timer
    │   ├── unclutter.service -> /home/bighops/.config/systemd/user/unclutter.service
    │   └── xset.timer -> /home/bighops/.config/systemd/user/xset.timer
    ├── taplist.service
    ├── taplist.timer
    ├── unclutter.service
    ├── xorg.target.wants
    │   └── xorg.service -> /usr/lib/systemd/user/xorg.service
    ├── xset.service
    └── xset.timer

The mailer unit is used to email what the devices natted ip address is.
