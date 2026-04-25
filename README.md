# How to Install Microsoft Office LTSC Pro Plus 2024

This repository provides a step-by-step guide to install Microsoft Office LTSC Pro Plus 2024 on a Windows PC using the Office Deployment Tool (ODT).

For the full article and additional software resources, visit:
https://digitalkeysdepot.com/how-to-install-microsoft-office-ltsc-pro-plus-2024/

> Important: This guide is for Windows PC only. It is not for Mac.

## Before You Start

Before installing Office LTSC Pro Plus 2024, make sure you have:

- A Windows PC
- A stable internet connection
- A valid Microsoft Office LTSC Pro Plus 2024 product key
- Administrator access on your computer

## Step 1: Uninstall Previous Office Versions

Uninstall any previous Office versions from your PC to reduce the risk of conflicts during installation.

## Step 2: Download the Office Deployment Tool

Download the official Office Deployment Tool from Microsoft.

Office Deployment Tool:
https://www.microsoft.com/en-us/download/details.aspx?id=49117

## Step 3: Create a Setup Folder

Open File Explorer and create a new folder on your C: drive.

Example:

`C:\Office2024Setup`

## Step 4: Extract the Office Deployment Tool

- Run the file you downloaded in Step 2
- If prompted by User Account Control, click **Yes**
- Accept the Microsoft Software License Terms and click **Continue**
- When asked where to extract the files, choose your new folder:

`C:\Office2024Setup`

- Click **OK**

## Step 5: Create the Configuration File

Open Notepad and paste the following configuration.

Replace the placeholder product key with your own valid key.

```xml
<Configuration>
  <Add OfficeClientEdition="64" Channel="PerpetualVL2024">
    <Product ID="ProPlus2024Volume" PIDKEY="XXXXX-XXXXX-XXXXX-XXXXX-XXXXX">
      <Language ID="en-us" />
    </Product>
  </Add>
  <RemoveMSI />
  <Display Level="None" AcceptEULA="TRUE" />
  <Property Name="AUTOACTIVATE" Value="1" />
</Configuration>
```

Then save the file as:

`configuration.xml`

Use these settings when saving:

- **Save as type:** All Files
- **Encoding:** UTF-8
- **Folder:** `C:\Office2024Setup`
> Note: Make sure the product ID, channel, and key type match the license you purchased.

## Step 6: Verify Your Folder Contents

Your setup folder should now contain at least:
- `setup.exe`
- `configuration.xml`

You may also see additional XML files extracted by the Office Deployment Tool. That is normal.

## Step 7: Open Command Prompt as Administrator
- Click the Windows Start button
- Type `cmd`
- Right-click **Command Prompt**
- Select **Run as administrator**

## Step 8: Navigate to the Setup Folder
In Command Prompt, type:

`cd C:\Office2024Setup`

Then press **Enter**.

## Step 9: Start the Office Installation

Run the following command:

`setup.exe /configure configuration.xml`

Then press **Enter**.

## Important Notes
- The installation runs silently in the background, so you may not see a normal installer window
- Do not close Command Prompt while the installation is running
- The installer will attempt activation automatically
- Installation is usually complete when Command Prompt becomes available again and Office apps appear in the Start Menu

## Troubleshooting Tips
If the installation or activation fails, check the following:
- Your product key matches the correct edition
- You are using a Windows PC, not a Mac
- Previous Office versions were removed properly
- Your internet connection is active
- Command Prompt was opened as administrator

## FAQ

### Does this work on Mac?
No. This guide is for Windows PC only.

### Can I reuse the key after reinstalling Windows?
That depends on the license type and whether it is being reactivated on the same PC.

### Do I need internet during installation?
Yes, it is recommended.

## Conclusion
Installing Microsoft Office LTSC Pro Plus 2024 with the Office Deployment Tool provides a controlled and streamlined setup process. If you use the correct edition, key type, and configuration file, the installation should complete smoothly on a Windows PC.

## More Microsoft Product Keys
Explore more Microsoft software keys and setup resources at: https://digitalkeysdepot.com/
