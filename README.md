# Configuring-Remote-Desktop

This is a project centered around configuring and using Windows' Remote Desktop feature. I will be using Windows Server 2019 and Windows 10 Enterprise by way of VirtualBox.

# Enabling Remote Desktop

The first step is to make sure that Remote Desktop has been enabled on both our Windows Server 2019 and Windows 10 Enterprise systems. I will focus on Windows Server 2019 first. On the Windows Server 2019 system: 

1. Open `Settings` and click into `System`.
2. On the panel to the left of the `System` page, click on `Remote Desktop` to open up the respective page on the right side of the page.
3. Then, click on the slider under `Enable Remote Desktop` to enable the remote desktop feature. The slider should be blue, indicating that it has been enabled.

![1  SErver Manager](https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/b4994405-317b-4247-abc3-9750ba12d45f)

Second, it is a good idea to make sure that you have network discovery enabled. The steps to do so are the following:

1. Open `Control Panel` 
2. If not done so already, change the icons to `Small icons` or `Large icons`
3. Click into `Network and Sharing Center`
4. On the left hand side of the window, click on `Change advanced sharing settings`
5. In the network profile for the domain, enable `Turn on network discovery` and `Turn on file and printer sharing`.

![Capture](https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/8cc2b96d-2e19-401d-a6c3-28a560434bf3)

You will also want to make sure that the following services have started, or you can set them to start automatically, which is what I have done. The services are as follows:

* DNS Client
* Function Discovery Resource Publication
* SSDP Discovery
* UPnP Device Host

Services can be managed in the `Services` app. There are several ways to open up this app. You can simply typed in `Services` in the search bar located on the taskbar. Or you can press `Windows + R` keys to open the `Run` console, and type in `services.msc`. Or you can run Command Prompt or PowerShell and enter in `services.msc`. In the `Services` app, locate each of the services listed above, open up their properties and change `Startup type:` to `Automatic`. 

![2](https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/edf8a0cd-e687-4bf5-bcf1-f0d0a40252e7)
![3](https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/3f90062f-ac82-4bd0-bb83-0d198691bafc)
![4](https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/04baa21c-a91d-48cb-947e-cc0f2a5f9a8d)
![5](https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/6b31c31d-a3d9-432e-829d-0ad468f9d23d)

We will then need to enable Remote Desktop on the Windows 10 Enterprise system. This will required administrative privilege. It is best that you log into an administrator account to enable Remote Desktop. The steps to do so are the same used for the Windows Server 2019 system.

1. Open `Settings` and click into `System`.
2. On the panel to the left of the `System` page, click on `Remote Desktop` to open up the respective page on the right side of the page.
3. Then, click on the slider under `Enable Remote Desktop` to enable the remote desktop feature. The slider should be blue, indicating that it has been enabled.

![6](https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/20908ff4-116f-4583-80e2-9e785421bff6)

It is also a good idea to enable network discovery as well. Once again, the steps are the same that were used for the Windows Server 2019 system.

1. Open `Control Panel` 
2. If not done so already, change the icons to `Small icons` or `Large icons`
3. Click into `Network and Sharing Center`
4. On the left hand side of the window, click on `Change advanced sharing settings`
5. In the network profile for the domain, enable `Turn on network discovery` and `Turn on file and printer sharing`.

After this, you can log off of the administrator account, and log in as a regular domain user. 


