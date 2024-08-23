# Finder QuickLook

### Resources

* [**Quick Look plugins**](https://github.com/sindresorhus/quick-look-plugins): _List of useful Quick Look plugins for developers_
* [**QuickLook Plugins List**](https://www.quicklookplugins.com/): _A directory of Quick Look Plugins for Apple's OS X_
*

### Overview

> Quick Look is a quick preview feature developed by Apple Inc. which was introduced in its operating system Mac OS X 10.5 Leopard. While macOS's Finder has always had smaller previews in Get Info windows or column view, Quick Look allows users to look at the contents of a file at full or near-full size in the Finder, depending on the size of the document relative to the screen resolution. It can preview files such as PDFs, HTML, QuickTime readable media, plain text and RTF text documents, iWork (Keynote, Pages, and Numbers) documents, ODF documents, Microsoft Office (Word, Excel, and PowerPoint) files (including OOXML), and RAW camera images.

### Paths

* `/System/Library/QuickLook/`
* `~/QuickLook`
*

```bash
brew install qlcolorcode \
    qlstephen \
    qlmarkdown \
    quicklook-json \
    qlimagesize \
    suspicious-package \
    apparency \
    quicklookase \
    qlvideo
```



#### QuickLook plugins location

* Path: `${HOME}/Library/QuickLook`

{% hint style="info" %}
_Remove Apple's quarantine so that they can be used._
{% endhint %}

```bash
xattr -r ~/Library/QuickLook
xattr -d -r com.apple.quarantine ~/Library/QuickLook
```

{% hint style="warning" %}
You may need to restart your MacBook's QuickLook manager `/usr/bin/qlmanage`

```bash
qlmanage -r
```
{% endhint %}



### The QuickLook Plugins & Apps

* &#x20;`{` 🔌 `=` QuickLook Plugin, 💻 `=` Application `}`&#x20;



🔌[**QLColorCode**](https://whomwah.github.io/qlstephen/)**:** _Renders source code with syntax highlighting._

```bash
brew install --cask qlcolorcode
#> ~/Library/QuickLook/QLColorCode.qlgenerator
```

💻[**QLMarkdown**](https://github.com/sbarex/QLMarkdown)**:** _Renders generated preview for markdown files._

```bash
brew install --cask qlmarkdown
#> ~/Applications/QLMarkdown.app
```

🔌[**QuickLookJSON**](http://www.sagtau.com/quicklookjson.html)**:** _Quick look json is a useful quick look plugin to preview JSON files. It will render files with a colorful view, and will allow to expand or compress nodes in the JSON tree._

```bash
brew install --cask quicklook-json
#> ~/Library/QuickLook/QuickLookJSON.qlgenerator
```

🔌[**qlImageSize**](https://github.com/Nyx0uf/qlImageSize)**:** _Display image info and preview unsupported formats in QuickLook._

```bash
brew install --cask qlimagesize
#> ~/Library/QuickLook/qlImageSize.qlgenerator
```

[💻**Suspicious Package**](https://www.mothersruin.com/software/SuspiciousPackage/)**:** _Application for inspecting installer packages._&#x20;

> _The built-in security features of macOS — such as Gatekeeper, package signing and most recently, notarization — might rule out malware ... if you're lucky. But there's still a huge gray area between that and a well-designed package._

```bash
brew install --cask suspicious-package
#> Applications/Suspicious Package.app
```

💻[**Apparency**](https://www.mothersruin.com/software/Apparency/): _The App That Opens Apps._&#x20;

```bash
brew install --cask apparency
#> ~/Applications/Apparency.app
```

**🔌**[**QLStephen**](https://whomwah.github.io/qlstephen/)**:** A QuickLook plugin that lets you view plain text files without a file extension.

```bash
brew install --cask qlstephen
#> ~/Library/QuickLook/QLStephen.qlgenerator
```

**🔌**[**QuickLookASE**](https://github.com/rsodre/QuickLookASE)_: QuickLook generator for Adobe Swatch Exchange files._

```bash
brew install --cask QuickLookASE
#> ~/Library/QuickLook/QuickLookASE.qlgenerator
```

[_**💻**_**Jupyter Notebook Viewer**](https://github.com/tuxu/nbviewer-app)**:** _A Jupyter notebook viewer for macOS_

```bash
brew install --cask jupyter-notebook-viewer
```



