## Base Info
The main hub of my iOS, iPadOS and macOS shortcut sub-projects.

The idea for this website is to provide API services for my shortcuts, however I'm clearly not good at this stuff.
I will work on it soon. Until then, here are my shortcuts!

1. Spring Lock at [RoutineHub](https://routinehub.co/shortcut/8552/)
2. Ultimate Updater at [RoutineHub](https://routinehub.co/shortcut/8666/)
3. Go Academic! (Beta) at [RoutineHub](https://routinehub.co/shortcut/8670/)

And yeah, that's it as of now.

# Overview: Spring Lock
## Notice:-
HSAG Applock has become Spring Lock. This shortcut works with all major versions of iPadOS, iOS after iOS 15, & macOS Monterey and later too.

## Short Description:-
Mostly, it tries to lock apps by using an automation. The passwords are secured with Cryptokit, so that no one can read them off the configuration files easily. You can also lock the shortcuts app with it too, if you’re paranoid about someone deleting the automations themselves.

## Features:-
1. Uses a good UI
2. Secures your apps using CryptoEngine, a light-weight JavaScript engine…
3. Can be reset!
4. Can clean up its files if you would like to delete it.
5. Has a ⚙️ Settings menu.
6. Uses HSAG Ultimate Updater (Embed) to keep it manually  updated.
7. Uses a 2 step set-up process. One set-up is during installation. The other set-up is activated during the activation of the login credentials system.

I would like to inform that if the set-up process is skipped, then the shortcut will be rendered unusable.

## More details about its internal mechanisms:-
Hmm… It looks like I forgot to clearly explain how it works. Let me break it down for you.

- It is a shortcut that is used to lock apps.
- It uses normal actions and stays well within the limits and security boundaries of shortcuts to this… (because back then there was a really cool shortcut that used to use FaceID/TouchID for authentication, but it kinda exposed a bug in the clock app, and springboard to do so. It was later rendered useless with latest iOS releases, and the dev stopped pushing out updates. However, kudos to that dev for taking such a effort.)
- The shortcut first checks if it has any config files. If it does, it will cross-check its files with MD5 hashing to check its files haven’t been tampered with… and restores any unauthorised changes. If it does not have config files it will enter set-up mode.
- The shortcut exits the running app and goes to the Home Screen. Then it shows the main menu with options.
- If you choose to set-up the shortcut, it will run the set-up… or if you choose to log in, it will show a list of users that are present on the device…. with “guest” users for accounts that have not been set-up yet. No one can try to login as Guest, unless you have configured the guest users with some password. Otherwise, all of them have a random encrypted password that no one knows, nor can access with; including me.
- If you login or set-up the first user, it will regard those credentials as admin credentials. Then, if you log-in as the first user, it will show admin options along with app-access. There, you have the options to see the security log, delete or reset the shortcut, or check for updates; and maybe some other options to control your experience.
- If you login as other registered users, you will directly be allowed to access the app.
- However, if an unauthorised user or you enter the wrong password, or PIN (because this shortcut has two-key authentication - a PIN and a password); it will take a photo of the user trying to gain access in the background and save it to the log. IT NEVER ASKS FOR ACCESS TO THE PHOTOS LIBRARY. It will save the photo to a security log that is saved along with the config files.)

Miscellaneous points:-

- The security log is a log of all the actions that the user(s) performed with the shortcut. It is visible only to the admin.
- The shortcut can work completely offline, and it also has a included guide video to guide you through the set-up process.
- If the set-up process is interrupted, it will always resume from where you left off, with no data loss. Only if you click on “Finish set-up” will it finish the set-up.
- The passwords are encrypted with the Stanford Java CryptoLibrary, and CryptoKit (a another Redditor’s shortcut) which I forked into “CryptoEngine”, a lightweight barebones version.
- There is, yes, some redundancy in the shortcut which I am clearing up. I have a lot planned for this shortcut, and I hope to excute it if possible.
- It stores the config files in the system’s “Shortcut” folder.
- Its files are hidden from normal view using a ‘.’ in front of the folder, a system files identifier.
- It has a “About this shortcut” menu and “Get Support” options, which I’m honestly trying to slim down and trim out the useless parts.
- The inbuilt Updater is my own, which I had also released later as “Ultimate Updater”. Unfortunately, it can’t embed Updaters inside shortcuts anymore, so I have to refresh that shortcut too. However, the embedded Updaters still work surprisingly well, and I will definitely try to optimise that part too.

> It’s been a while since I had touch this shortcut, and I honestly forgot some of its workings. That’s why I’m hesitant to bring too much change in the code. Over time, I will try my best to make this shortcut better.

------
## Your feedback matters!

Well, I would love to hear your ways on how to trim down this shortcut. Honestly, I’ve been trying to do the same, but since I’ve kinda forgot how it works, it will take some time. As I’ve previously mentioned, in my first attempt, I’ve trimmed down 102 actions from the shortcut, while also enhancing its usability.

- It was over engineered in particular because, during its initial days (Versions 1 to 4), it was highly exploited and mocked on by peers. So, it has a lot of internal mechanisms to double-check itself to prevent its config files, actions from being tampered or abused with..

- I really wanted to provide the best experience possible to the users without them worrying about its safety, so I used to think of doomsday or ZDA scenarios and code it for those scenarios.

And yes, there is one bloaty menu, the “About this Shortcut” part… It uses some 30 actions, and I am trying to trim that part down too. In my recent versions, I've trimmed down a huge part of it. I'll continue to do so.

## Last release of HSAG AppLock:-

[![HSAG AppLock](https://i.imgur.com/rVqUGRl_d.webp?maxwidth=1520)](https://youtu.be/0e2y5R6UTKs)

____

## Credits:-


- @Schl3ck  - For their invaluable work on CryptoKit, from which this shortcut’s Crypto Engine is forked.
- @SpaceNeb - For pointing out the error found in Version 3 of this shortcut.
- @HSAG (Defunct) - For the HSAG Icon Pack UI 4, which I use in this shortcut. It's basically mine now, yes, but since it belonged to the "company" while it was functioning, I kinda have to attribute it anyway. Anyways, here's the "poster" for the Icon Pack.

![Poster for HSAG Icon Pack's HSAG UI 4](https://i.imgur.com/Ii53XRM.png)

# Overview: Ultimate Updater (Defunct Plans for the future)
![HSAG Ultimate Updater](https://i.imgur.com/PHRHVZI.jpg)
![HSAG Ultimate Updater](https://i.imgur.com/ZCQFo6x.png)
![HSAG Ultimate Updater](https://i.imgur.com/Ii53XRM.png)
![HSAG Ultimate Updater](https://i.imgur.com/zO2AYbf.png)
![HSAG Ultimate Updater](https://i.imgur.com/ZE4vXOv.png)
![HSAG Ultimate Updater](https://i.imgur.com/oofhL22.png)

# Overview: Go Academic (Beta)
Let’s study, together!

Hi, I’m Sugeeth! I used to be an active shortcut developer during the COVID-19 Lockdown. However, due to educational demands, I couldn’t continue developing general-release shortcuts.

However, I continued to develop shortcuts for personal use, and this is one of them.

When I was CBSE (India) Class 10 student in 2023, I had a difficult time trying to find and download good materials for practice quickly. 
This shortcut aims to resolve that problem.

The UI is a bit cranky, and it’s not completely stable, but it works.

I resolved most of the stability issues that used to plague this shortcut, such as memory buffer overflow, shortcut stack integration problems etc…

Yet there’s still room for improvement.
If you’d like to give any ideas or create your own improved spin-offs, feel free to do so, I’m all ears!
