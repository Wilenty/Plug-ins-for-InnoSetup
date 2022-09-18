# Plug-ins for InnoSetup

**It's modified version of this one: https://github.com/Wilenty/InnoSetup-with-latest-LZMA so, the license and copyrights are the same for all non-official InnoSetup builds.**

I start this text with warning:
I won't return the money for you if you don't read the explanation below "how to it work" and "how to use it", but you will report me that my plugin not works in your InnoSetup and you ask for your money back.
But, I will return the money when you will prove that my plugin does not work. Problems with implementing my functions in your script does not count. I share the plugin and ready made script to test it. I can help you with implementing it in the first one script of you.

A word of explanation:
InnoSetup is a good installer for beginners, but for example, if you want to get information about CPU, GPU, IP, etc. - you will have to create your own plugin (DLL). The installer extracts the plugin (DLL) to a temporary location and loads it, and it takes some time... I managed to "translate" some of Windows API functions to use them directly in the InnoSetup code. So, I share them as a plugins.

Note:
Examples to check/test are compiled executable protected from unpacking. So, if you don't trust unsigned files, please test/check them in the VM (virtual machine). Sometimes protected InnoSetup installers are detected as dangerous, because AV can't check "what's inside".
It's hard to share publicly an example to check by users, because there are many tools to de-compile InnoSetup installers, but without checking "how it works" and without knowing "what I offer" probably you will never decide to use my works... So, examples protected from unpacking is the only one way to show my works without showing "how it's done" - I hope you understand what I mean.

***Q:***
#### What is that and what is it used for?
***A:***
It's plugins for modified InnoSetup. I "translated" some of Windows API functions to use in pure InnoSetup code, so I share my works as plugins for modified InnoSetup. If you will need any other function or API - just ask, and I will check if I will be able to do it...
So, for example, you can use my plugins to get specific information of the user hardware (above mentioned), or in the GetCommandLine example you can get all command-line parameters in the latest InnoSetup, independent if they will change the way to parse the command-line parameters in the future.

***Q:***
#### Will these plugins work with any InnoSetup, even in the official one?
***A:***
No - these plugins work only with my modified versions of InnoSetup. But, if you need I can modify any version of the InnoSetup from the source, which was published on their download website.

***Q:***
#### With what versions of InnoSetup these plugins works?
***A:***
Here I share latest version (as for now), i.e. v6.2.1(U), but I also prepared versions of InnoSetup v5.6.1(U) and v6.0.5(U), so, I can share the older versions if you need them. ANSI versions of InnoSetup are very limited, so, I don't feel the need to work with it. 
If you want, you can use the "Setup.e32" and "SetupLdr.e32" from offical release, but you will lost the possibility to use latest LZMA, so, decision is yours.

***Q:***
#### These plugins are ANSI or UNICODE (A/W)?
***A:***
Usually these plugins are ANSI and UNICODE (A/W), but some of them are ANSI (A) and some UNICODE (W) only. Some of them supports both (A/W), like the GetCommandLine example, even if there's no CommandLineToArgvA Windows API function at all.
If there are separate API functions for ANSI and UNICODE (A/W), I trying to use both of them, otherwise the examples without A or W letters at the end of example name.

***Q:***
#### How does it work?
***A:***
In this same way as in the shared GetCommandLine example. I share example of GetCommandLine that you can compile it by yourself and test my plugin system, because InnoSetup owners removed some parameters forwarded to the script in the latest version (v6.2.1).

***Q:***
#### What does your plug-in do?
***A:***
Adds the necessary code to the script (during compilation), the functions used by the user are described in the *.isi file (InnoSetup include). It does not add anything else, nor does it change the way InnoSetup installers work.
So, my plug-in are not used in your installer, it's only used when you compile the installer.

***Q:***
#### It was tested and works?
***A:***
Yes - I test these plugins on real computer or virtual machine on Windows of XP, XP 64-bit, 7 and 10. I share compiled examples that you can check it on your OS.

***Q:***
#### Can I use two or more of your plugins in one InnoSetup script?
***A:***
Of course - I use long function naming to not make any collision between any of them.

***Q:***
#### How I can get it?
***A:***
#### 1 - Please support me for amount of $25 on Patreon or 25€ on ko-fi, per one plugin
#### 2 - Please provide the plugin name you want and your e-mail for which the plugin will be registered
#### 3 - After I get the money, I will create the plugin for you, I will test it and share in one working day (usually faster)

If you have any other question - ask, I will try to answer as best as I can...

By the way,
you can check this repository from time to time, if I will find other methods/functions - I will add them here as a compiled examples to test/check it.
