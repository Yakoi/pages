



## 記録
### 20180614 
PackageManagementというものを知った。今まで何故知らなかったのか、Windows標準のパッケージマネージャである。
しかし。。。ホームページを見ながらインストール手順をこなしても、何故かインストールされない。
Install-Packageして、質問にYで答えて、なんかダウンロードした仕草を見せるけど、なぜかアプリが導入されていない。
以下はFireFoxでの例。

```
PS C:\WINDOWS\system32> install-package firefox

パッケージは、信頼済みとマークされていないパッケージ ソースから取得されています。
'chocolatey' からソフトウェアをアンインストールしますか?
[Y] はい(Y)  [A] すべて続行(A)  [N] いいえ(N)  [L] すべて無視(L)  [S] 中断(S)  [?] ヘルプ (既定値は "N"): Y

Name                           Version          Source           Summary
----                           -------          ------           -------
Firefox                        60.0.2           chocolatey       Bringing together all kinds of awesomeness to make ...
```


ちなみに、chocolateyコマンドでFirefoxをインストールしようとすると、できる。もうなぞです。
```
PS C:\WINDOWS\system32> choco install firefox
Chocolatey v0.10.11
Installing the following packages:
firefox
By installing you accept licenses for the packages.

Firefox v60.0.2 [Approved]
firefox package files install completed. Performing other installation steps.
The package Firefox wants to run 'chocolateyInstall.ps1'.
Note: If you don't run this script, the installation will fail.
Note: To confirm automatically next time, use '-y' or consider:
choco feature enable -n allowGlobalConfirmation
Do you want to run the script?([Y]es/[N]o/[P]rint): y

Downloading Firefox 64 bit
  from 'https://download-installer.cdn.mozilla.net/pub/firefox/releases/60.0.2/win64/ja/Firefox%20Setup%2060.0.2.exe'
Progress: 100% - Completed download of C:\Users\Shimpei\AppData\Local\Temp\chocolatey\Firefox\60.0.2\Firefox Setup 60.0.2.exe (37.22 MB).
Download of Firefox Setup 60.0.2.exe (37.22 MB) completed.
Hashes match.
Installing Firefox...
Firefox has been installed.
  firefox may be able to be automatically uninstalled.
 The install of firefox was successful.
  Software installed to 'C:\Program Files\Mozilla Firefox'

Chocolatey installed 1/1 packages.
 See the log for details (C:\ProgramData\chocolatey\logs\chocolatey.log).
```