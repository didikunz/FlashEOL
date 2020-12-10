# FlashEOL
Adobe Flash reaches EOL (End Of Life) by the end of 2020. To be able to use Flash templates in CasparCG after that deadline the following things need to be done.
* Update Flash Player ActiveX (.ocx) to the most recent version. That is version 32.0.0.445 or above.
* Update CasparCG to a version that corrects [issue 1352](https://github.com/CasparCG/server/issues/1352).
* Add a mms.cfg file to your Flash installation. This will keep Flash installed after the deadline and will let Flash player show CasparCG's templates. 

Read the full text before proceeding and be aware of the __Disclaimer__ bellow.

## Update Flash Player
In Windows 10, let Windows Update install the Flash player. If you have anything blocking auto update, disable it and run "Search for Update". Make sure, that the Flash update is listed and let Windows proceed.

In Windows 7 use Internet Explorer to download and install the most recent Flash Player ActiveX. Do that __before the end of 2020__. Adobe will disable the download pages after that date.

## Update CasparCG
At time of writing there is only a CasparCG version 2.3.0 available, that works with Flash after the deadline. The list bellow will be updated when other versions become available.
* [Version 2.3.0](http://casparcg.com/builds/CasparCG%20Server/master/casparcg-server-f4879b8ecde2f2b5b6916b73ffe46c304c8f6c64-windows.zip)
* [Version NRK 2.1.12](https://github.com/nrkno/tv-automation-casparcg-server/releases/tag/v2.1.12_NRK)
* [Version 2.0.7.1](https://github.com/CasparCG/server/releases/tag/v2.0.7.1-flash-eol)

## Add mms.cfg
This is the tricky, but most important part. You can either read through [Adobe Administration Guide](https://www.adobe.com/devnet/flashplayer/articles/flash_player_admin_guide.html) and create the files yourself or you can download and _Run As Administrator_ this little [program](https://github.com/didikunz/FlashEOL/files/5654113/FlashCfgWriter.zip)

![Screenshot](https://user-images.githubusercontent.com/6048776/101338596-77635c80-387d-11eb-8462-44e860fd40b3.png)

It has three buttons. The "Browse..." button let you browse to your CasparCG's template folder, as this folder must be added to the allow-list of Flash Player. The "Write Config" button let you write the mms.cfg files to the folders where they belong. The "Check Version" button shows the version of the installed Flash Player ActiveX.

### Disclaimer
Be aware, that if you add this mms.cfg files to your installation and __NOT__ use a supported CasparCG build, Flash templates will not work anymore. So, if that applies to you, please only update Flash Player ActiveX, as this needs to be done asap, to make sure you do not miss it, before it gets unavailable.
