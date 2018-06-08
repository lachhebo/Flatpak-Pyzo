# Flatpak-Pyzo
A Flapack version of Pyzo

More information about Pyzo here : 

>    https://github.com/pyzo/pyzo

# Installation : 

To try it, you need to install flatpak and flatpak-builder on your distribution.

Then you need the kde runtime :

```
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo
flatpak install flathub org.kde.Platform//5.10
flatpak install flathub org.kde.Sdk//5.10

```

Then you need to build the flatpak and create a repo by using the command line :

```
flatpak-builder --repo=pyzo-repo python3-pyzo org.kde.python3-pyzo.json 
flatpak --user remote-add --no-gpg-verify --if-not-exists pyzo-repo pyzo-repo
flatpak --user install pyzo-repo org.kde.python3-pyzo

```

Eventually, to run it, you need to use the command line :  
`flatpak run org.kde.python3-pyzo`



## Todo 

It may be post on flathub 
