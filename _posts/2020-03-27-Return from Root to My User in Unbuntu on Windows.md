---
layout: post
title: Funny/High Efficiency way to merge in Github/WSL/Return from Root to My User in Unbuntu on Windows 
date: 2020-03-27
categories: blog
tags: Research
description: I found that there are several ways incorrect on the Internet Q&A so I tried to write small notes of the tricks I learned recently.  Eg., Funny/High Efficiency way to merge in Github, Return from Root to My User in Unbuntu on Windows, Soft wrap in VS Code, Install the Toolkit for VS Code, Connect VS Code with AWS. 
---




## Return from Root to My User in Unbuntu on Windows
`su - username` In here my username is sophie.
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-27.jpg)
```
exit
CTRL +D
logout
```
Three ways above are the methods to close the window.


## How to wrap in Vscode?
If you want to use text word wrap in your Visual Studio Code editor, you have to press button `Alt + Z` for text word wrap. Its word wrap is toggled between text wrap or unwrap.

### Soft wrap in VS Code
To enable Soft wrap in VS Code you have to open your user settings file (open command pallet, type 'settings', select 'Open User Settings') and add the following line:
```
{
// there might be other custom settings you have in this file.
"editor.wrappingColumn": 0
}
```
Ref:
>https://marketplace.visualstudio.com/items?itemName=jsturtevant.softwrap
                     
![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-27-01.jpg)                     

## Funny/High Efficiency way to merge in Github

>(Xusheng taught me this, where he picked it up in Industrial Area, Amazon I suppose.)

```
#approach 1
git stash
git fetch
git pull
git stash apply
(fix...)
git commit

#Approach 2
git commit 
git branch tmp321
git checkout master
git fetch/pull
git checkout tmp321
git log
(手动记下来 commit XXX)
git checkout master
git cherrypick XXXX
(fix...)
git commit --amend
```

### Install the Toolkit for VS Code

>https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/setup-toolkit.html 
>https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/setup-credentials.html

### Obtaining AWS Access Keys
>https://docs.aws.amazon.com/toolkit-for-vscode/latest/userguide/obtain-credentials.html


### Using C++ and WSL in VS Code
>https://code.visualstudio.com/docs/cpp/config-wsl

![](https://raw.githubusercontent.com/SophieCXT/blog.io/master/img/research/2020-03-28.jpg)   

###Developing in WSL
>https://code.visualstudio.com/docs/remote/wsl#_getting-started