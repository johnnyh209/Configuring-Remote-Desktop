# Enabling Remote Desktop

The first step is to make sure that Remote Desktop has been enabled on both our Windows Server 2019 and Windows 10 Enterprise systems. I will focus on Windows Server 2019 first. On the Windows Server 2019 system: 

1. Open `Settings` and click into `System`.
2. On the panel to the left of the `System` page, click on `Remote Desktop` to open up the respective page on the right side of the page.
3. Then, click on the slider under `Enable Remote Desktop` to enable the remote desktop feature. The slider should be blue, indicating that it has been enabled.

<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/b4994405-317b-4247-abc3-9750ba12d45f" Width="700" />

Second, it is a good idea to make sure that you have network discovery enabled. The steps to do so are the following:

1. Open `Control Panel` 
2. If not done so already, change the icons to `Small icons` or `Large icons`
3. Click into `Network and Sharing Center`
4. On the left hand side of the window, click on `Change advanced sharing settings`
5. In the network profile for the domain, enable `Turn on network discovery` and `Turn on file and printer sharing`.

<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/f7c6476b-1845-4b87-b703-883c6628ca95" Width="700" />

You will also want to make sure that the following services have started, or you can set them to start automatically, which is what I have done. The services are as follows:

* DNS Client
* Function Discovery Resource Publication
* SSDP Discovery
* UPnP Device Host

Services can be managed in the `Services` app. There are several ways to open up this app. You can simply typed in `Services` in the search box located on the taskbar. Or you can press `Windows + R` keys to open the `Run` console, and type in `services.msc`. Or you can run Command Prompt or PowerShell and enter in `services.msc`. In the `Services` app, locate each of the services listed above, open up their properties and change `Startup type:` to `Automatic`. 

<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/edf8a0cd-e687-4bf5-bcf1-f0d0a40252e7" Width="700" />
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/3f90062f-ac82-4bd0-bb83-0d198691bafc" Width="700" />
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/04baa21c-a91d-48cb-947e-cc0f2a5f9a8d" Width="700" />
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/6b31c31d-a3d9-432e-829d-0ad468f9d23d" Width="700" />

We will then need to enable Remote Desktop on the Windows 10 Enterprise system. This will required administrative privilege. It is best that you log into an administrator account to enable Remote Desktop. The steps to do so are the same used for the Windows Server 2019 system.

1. Open `Settings` and click into `System`.
2. On the panel to the left of the `System` page, click on `Remote Desktop` to open up the respective page on the right side of the page.
3. Then, click on the slider under `Enable Remote Desktop` to enable the remote desktop feature. The slider should be blue, indicating that it has been enabled.

<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/20908ff4-116f-4583-80e2-9e785421bff6" Width="700" />

It is also a good idea to enable network discovery as well. Once again, the steps are the same that were used for the Windows Server 2019 system.

1. Open `Control Panel` 
2. If not done so already, change the icons to `Small icons` or `Large icons`
3. Click into `Network and Sharing Center`
4. On the left hand side of the window, click on `Change advanced sharing settings`
5. In the network profile for the domain, enable `Turn on network discovery` and `Turn on file and printer sharing`.

After this, you can log off of the administrator account, and log in as a regular domain user. 

From there, we return to the Windows Server 2019 system. On the search box located in the taskbar, type in `Remote Desktop Connection` and select the entry that matches the search term you entered, `Remote Desktop Connection`. The Remote Desktop Connection window should open, where it prompts you to type in the name of the computer that you want to remote into. For me, the name of the computer that I am trying to remote into is called `josedesktop`. I enter that into the `Computer:` textbox and clicked on the `Connect` button. 

<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/5ac2fc67-e376-47cc-b587-9842e4a5bb69" Width="700" />

After a few seconds, my Windows Server 2019 system should be connected to josedesktop (in other words, the Windows 10 Enterprise system). Because I am still logged in to the Windows 10 Enterprise system, Remote Desktop is asking me if I want to continue remoting into the Windows 10 Enterprise system. Doing so would disconnect the domain user currently logged in. Press `Yes` to continue. 

<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/15a5b2b1-9f5d-4ae6-8954-5110e059a03b" Width="700" />

On the Windows 10 Enterprise system, the domain user that is logged in will see the following message, asking the user if they will allow another user (in my case, an administrator) to connect to their system: 

<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/6434c678-0315-4a94-9099-793600221ab1" Width="700" />

The user can click `OK`, or simply do nothing and the user will be disconnected. Once you have successfully maneuvered through all of these prompts, you should be able to see the desktop of the Windows 10 Enterprise system on the screen of your Windows Server 2019. On the top of the screen, you will see the name of the computer that you have connected to using Remote Desktop. 

<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/51146ebb-a336-4467-bb38-6d26b3f26209" Width="700" />
