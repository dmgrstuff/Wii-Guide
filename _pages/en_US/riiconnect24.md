---
title: "RiiConnect24"
---

{% include toc title="Table of Contents" %}

If you need help for anything regarding this tutorial, please join [the RiiConnect24 Discord server](https://discord.gg/b4Y7jfD) (recommended) or [e-mail us at support@riiconnect24.net](mailto:support@riiconnect24.net).
{: .notice--info}

![RiiConnect24 Logo](/images/WiiRC24Logo.jpg)

[RiiConnect24](https://rc24.xyz/) allows you to use discontinued services from WiiConnect24, which include the News, Forecast, Everybody Votes, Nintendo and Check Mii Out Channel, along with Wii Mail.

{% capture notice-1 %}
This guide is for the original Wii only.

- Follow [this tutorial](riiconnect24-vwii) if you'd like to install RiiConnect24 on a vWii (the Wii mode of your Wii U).
- Follow [this tutorial](riiconnect24-dolphin) if you'd like to install RiiConnect24 on the Dolphin emulator.

There is no guide to installing RiiConnect24 on a Wii Mini, as attempting to install RiiConnect24 on a Wii Mini will result in a console brick.
{% endcapture %}

<div class="notice--warning">{{ notice-1 | markdownify }}</div>

#### What you need

* An SD card or USB drive
* A Wii with an Internet connection
* A computer
* [RiiConnect24 Patcher (Windows only)](https://github.com/RiiConnect24/RiiConnect24-Patcher/releases)

#### Instructions

##### Section I - Patching IOS

[If you want to see detailed instructions on how to install the WADs, click here!](wiimodlite)
{: .notice--info}

If you use Linux or macOS, please e-mail us and we will give you the things needed to install RiiConnect24. The patcher we provide is currently Windows-only.
{: .notice--info}

You will now patch your IOS, `IOS31` and `IOS80`. This is required to use the Channels we support to change an RSA key used to sign the files. You will also download patched versions of the Channels.

1. Download the required files based on your OS. On Windows run `RiiConnect24Patcher.bat`.
2. Follow the instructions it gives you.
3. You should get the Channels that you want. They need to be installed **even if you already have them on your Wii, because you will need to install the patched WAD instead**.
4. (`If RiiConnect24 Patcher copied everything to the SD card or USB drive, you can skip this step`) Copy the `apps` and `wad` folder to your SD card or USB drive.
5. Put your SD card or USB drive in your Wii.
6. Launch the Homebrew Channel on your Wii.
7. Launch Wii Mod Lite.
8. Using the +Control Pad on your Wii Remote, navigate to `WAD Manager`, and then navigate to the `wad` folder.
9. When `IOS31.wad` is highlighted, press +, then do the same for all the other WADs.
10. If you get an error saying a title with a higher version is already installed (error -1035), go back to the WAD selection menu and press - on the highlighted WAD to uninstall it, then try installing it again.
11. After they are successfully installed, press the HOME Button to exit back to the Homebrew Channel.

##### Section II - Patching nwc24msg.cfg

You will now patch your `nwc24msg.cfg` file which is required in order to use Wii Mail.

1. Launch RiiConnect24 Mail Patcher.
2. It should only take a few seconds to patch your nwc24msg.cfg. When it's done, press HOME to exit.

If the previous step failed with an "net_get_status: -24 - Couldn't request the data: -24" error, please check the internet connection on your Wii.
{: .notice--warning}

If you were unable to patch your nwc24msg.cfg correctly, e-mail us at [support@riiconnect24.net](mailto:support@riiconnect24.net).
{: .notice--info}

##### Section III - Connecting

You need to set your DNS in order to get the Forecast and News Channel to point to our servers. This DNS is also useful if you want to play Wiimmfi.

1. Go to `Wii Options`.
2. Go to `Wii Settings`.
3. Go to `Page 2`, then click on `Internet`.
4. Go to `Connection Settings`.
5. Select your current connection.
6. Go to `Change Settings`.
7. Go to `Auto-Obtain DNS` (Not IP Address), then select `No`, then `Advanced Settings`.
8. Type in `164.132.44.106` as the primary DNS.
9. Type in `1.1.1.1` as the secondary DNS (if it gives you problems, try `8.8.8.8`).
10. Select `Confirm`, then select `Save`.
11. Select `OK` to perform a connection test.
12. If the connection test was successful, select `No` to skip the Wii System Update.
13. Go to `WiiConnect24`, then `WiiConnect24` again, and make sure it is enabled.
14. Back on the WiiConnect24 menu, go to `Standby Connection` and make sure it is enabled.
15. At `Slot Illumination`, we recommend you set the disc light to `Dim` or `Bright`, but this is optional.
16. Finally, go to the `Internet` section, then `User Agreements` or `Agreement/Contact`, then `Yes`. Please read through this.


[Continue to Wiimmfi](wiimmfi)<br>
Wiimmfi lets you play games online after the discontinuation of Nintendo Wi-Fi Connection. This is optional to install.
{: .notice--info}

If you get error 107245, then you probably have failed to patch your IOS correctly.
{: .notice--info}

If you get error 107304, then perhaps your ISP blocks the use of custom DNS. A workaround for this can be running your own DNS server! See the [RiiConnect24 DNS Server on GitHub](https://github.com/RiiConnect24/DNS-Server), then use your PC's IP address in place of our DNS in Step 8.
{: .notice--info}

[If you get error FORE000006, following this tutorial should fix it.](riiconnect24-batteryfix)
{: .notice--warning}

[If you get error NEWS000006, following this tutorial should fix it.](news000006)
{: .notice--warning}

[If you're getting errors such as `WiiConnect24 and Wii Shop Channel currently not being offered in your country`, please go to Wii Settings -> Last Page -> Country and change it to United Kingdom. You will get this error when using a country that we don't support. Contact us at [support@riiconnect24.net](mailto:support@riiconnect24.net) if you need more help.
{: .notice--warning}

[If you're getting a discontinued message when opening the News or Forecast Channel, then following this tutorial should fix it.](deleting-vffs)
{: .notice--warning}
