---
title: "Swtiching between different github accounts in mac terminal"
date: 2019-12-19T13:34:30+08:00
categories:
  - how-to
tags:
  - github
  - jekyll
  - macos
---

I work on multiple projects using github. From time to time I need to switch between different accounts to do github push. I recalled in my first attempt, the following message pop up.

```console
remote: Permission to [github username]/[github repo] denied to ifeng.
fatal: unable to access 'https://[github username]/[github repo]/Myshantou.git/': The requested URL returned error: 403
```

The logic is...if you are logged onto account A but want to push files into a repo in account B, most likely the error message above will appear.

I have searched and most answers suggested to change "--global user.name". For examples this one on [superuser][superuser], this [practical guide][practical guide] and [another one][3] suggesting to make change an ssh. Stackoverflow also have a number of questios on this, here is [one example][stackoverflow].

While these might work as proper solutions, I found a quick one that worked for me and just what I needed - Delete Login Info on Keychain!

If you encountered a similar issue, try open your keychain and search for github, then delete the record there. 

![github switch account delete keychain][keychain]

After that, when you push again, then terminal should prompt you to enter your login name and password of the account you are pushing to.

![github switch account delete keychain - git push][gitpush]

<!-- Links -->
[superuser]: https://superuser.com/questions/1064197/how-to-switch-git-user-at-terminal
[practical guide]: https://medium.com/the-andela-way/a-practical-guide-to-managing-multiple-github-accounts-8e7970c8fd46
[3]: https://medium.com/@pinglinh/how-to-have-2-github-accounts-on-one-machine-windows-69b5b4c5b14e
[stackoverflow]: https://stackoverflow.com/questions/7548158/having-trouble-switching-github-accounts-on-terminal

<!-- Images -->
[keychain]: /assets/images/2019_12_keychain.jpg
[gitpush]: /assets/images/2019_12_gitpush.jpg
