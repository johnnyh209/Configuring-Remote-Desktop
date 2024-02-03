#Remote Desktop (2nd Attempt)

My goal of this attempt was to simplify the process of enabling remote desktop on Windows. I will be using Windows Server 2019 and Windows 10 Enterprise LTSC, where the systems are in a domain named `testdomain`. 

**Step 1**
On the computer that you want to remotely **connect to** (in my case, I want to connect to a Windows 10 system in my domain), open up the `Settings` app. Use the search bar if needed.
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/a9a8f921-2542-4fce-aa9f-af101e0bd173" Width="700" />

**Step 2**
In the main page of the `Settings` app, click into `System`. 
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/e6b5f0ed-7c7f-464a-a257-5e2bd59d6019" Width="700" />

**Step 3**
Once inside of the `System` page, look for `Remote Desktop` on the left hand side of the window, and click into it. 
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/38a6fd8f-efc2-436c-8bb3-ff66c84c2e22" Width="700" />

**Step 4**
Enable remote desktop by clicking on the toggle button, turning it from off to on.
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/3843ec4b-6fa8-419f-895b-86e1f5ef7260" Width="700" />

If you are not using an account with elevated privileges (such as an Admin account) you will see that the toggle button will be greyed out as seen in the screenshot below. If that is the case, then log out of the current account and log back in with an Admin account. After doing so, the toggle button will no longer be greyed out, indicating that it is clickable.
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/8968f882-f6c9-4df3-80fc-011663a9a403" Width="700" />

**Step 4.1**
After turning on remote desktop, you will be presented with a pop-up window that asks you to confirm that you are enabling remote desktop. Click on the `Confirm` button to finalize the change.
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/b49bc143-d6a1-451a-bca5-ba2b90a0980e" Width="700" />
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/231fbe51-cd16-47dd-8a42-44f837af339f" Width="700" />

**Step 5**
On the computer that you want to **remote from** (in my case, this is my Windows Server 2019 machine), open up the `Remote Desktop Connection` app. 
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/11c1a105-b1c3-4846-ac47-e6b431c3bc36" Width="700" />

**Step 6**
Enter the name of the system that you want to use remote desktop to connect to. In my case, the Windows 10 Enterprise system I am connecting to is named JuanPC. After entering the computer name, click on the `Connect` button.
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/5617ba06-bcb0-463e-9898-411085581424" Width="700" />

To find the name of a computer, you can do so in two ways:
1. Settings > System > About
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/a6c317fe-5699-4d7d-af83-5e8f9bcdbf61" Width="700" />

2. In PowerShell or CMD, use the `hostname` command
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/acf51c71-b07e-47b9-a34b-ed8c3d0f4c47" Width="700" />

**Step 7**
After clicking `Connect`, you will be prompted to enter in credentials. Click `OK` after entering all required information.
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/4ed8a010-641e-4f5e-be20-7faf327b36d5" Width="700" />

**Step 8**
After clicking `OK` in the previous step, on the computer that you are trying to remote into, there will be a popup. You don't need to click on anything here.
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/55b7ab36-8fd6-4f3b-938e-dc00341fbd9d" Width="700" />

On the computer that you are remoting from, after clicking `OK`, you will then be shown the following screen. Simply click `Yes`.
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/538b90df-5724-4a00-890b-7829cbc408f6" Width="700" />

If done correctly, you should see the desktop of the computer that you remoted into:
<img src="https://github.com/johnnyh209/Configuring-Remote-Desktop/assets/33064730/3f9b651b-a4ea-43ef-b29f-7a9248128ecb" Width="700" />

