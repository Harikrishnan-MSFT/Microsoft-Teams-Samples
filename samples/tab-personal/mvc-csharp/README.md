---
page_type: sample
description: Sample app showing custom personal Tab with ASP. NET Core
products:
- office-teams
- office
- office-365
languages:
- csharp
extensions:
 contentType: samples
 createdDate: "07/07/2021 01:38:27 PM"
urlFragment: officedev-microsoft-teams-samples-tab-personal-mvc-csharp
---

# Personal Tab with ASP. NET Core MVC

In this quickstart we'll walk-through creating a custom personal tab with C# and ASP. Net Core MVC. We'll also use App Studio for Microsoft Teams to finalize your app manifest and deploy your tab to Teams.

## Interaction with app

![personaltab](Images/PersonalTabModule.gif)

## Prerequisites

- [.NET Core SDK](https://dotnet.microsoft.com/download) version 6.0

  determine dotnet version
  ```bash
  dotnet --version
  ```
- [Ngrok](https://ngrok.com/download) (For local environment testing) Latest (any other tunneling software can also be used)
  
- [Teams](https://teams.microsoft.com) Microsoft Teams is installed and you have an account

## Setup

1. Run ngrok - point to port 3978
   ```ngrok http -host-header=rewrite 3978```

2. Clone the repository
   ```bash
   git clone https://github.com/OfficeDev/Microsoft-Teams-Samples.git
   ```

3. If you are using Visual Studio
 - Launch Visual Studio
 - File -> Open -> Project/Solution
 - Navigate to ```samples\tab-personal\mvc-csharp``` folder
 - Select ```PersonalTabMVC.sln``` file and open the solution

4. Modify the `manifest.json` in the `/AppManifest` folder and replace the following details:
   - <<Guid>> with any random GUID.
   - `<<Base-url>>` with base Url domain. E.g. if you are using ngrok it would be `https://1234.ngrok.io` then your domain-name will be `1234.ngrok.io`.
   - `validDomains` with base Url domain. E.g. if you are using ngrok it would be `https://1234.ngrok.io` then your domain-name will be `1234.ngrok.io`.

5. Upload the manifest.zip to Teams (in the Apps view click "Upload a custom app")
   - Go to Microsoft Teams. From the lower left corner, select Apps
   - From the lower left corner, choose Upload a custom App
   - Go to your project directory, the ./AppManifest folder, select the zip folder, and choose Open.


## Running the sample

![personaltab](Images/personaltab.png)

![Greytab](Images/Greytab.png)

![tab](Images/Redtab.png)

## Fruther Reading
[Tab-personal](https://learn.microsoft.com/en-us/microsoftteams/platform/tabs/what-are-tabs)
[Create a Custom Personal Tab with ASP. NET Core MVC](https://learn.microsoft.com/en-us/microsoftteams/platform/tabs/how-to/create-personal-tab?pivots=mvc-csharp)


