# TestClickOnce
TestClickOnce

* First Test Update Success - Value Config
  * **Publishing Foler** use ftp like ftp://localhost/testinstall/
  * **Installation Folder** use http like http://localhost:33333/
  * **Update Location** in Update Button leaves empty
* Some Discussion
  * When click publish in VS, it'll publish to the `publish folder`, but not to `installation folder`
  * when the program is launch, it'll goto `installation folder` to check for update, not goto `publish folder`
  * so if the publish folder and installation folder is the **same**, when you publish new version of program to `publish folder`, the new version also add to the `installation folder`, so if the program execute it'll ask you want to update or not.
  * but if the publish folder and `installation folder` is **different**, when you publish new version of program to `publish folder`, it's **not** added to the `installation folder`, so if the program execute it'll **not** ask you want to update or not. you have to use other way to copy the  new version of program to the `installation folder` to let the program can ask update when launch.
  * After Testing, I found that the key file to let program know whether there is new version in `installation folder` is `{ProgramName}.application`, guess it record the version information, and when it detect newer version of program, it'll download the bew version file from `Application Files` folder.
  
  
* Tutorial Article  
  * [[.NET] 組件自動更新 使用 ClickOnce 佈署](https://dotblogs.com.tw/yc421206/archive/2012/03/02/70464.aspx)
  * [How to create a ClickOnce application | lynda.com tutorial](https://www.youtube.com/watch?v=t4BTLdIMYEY)
  * [Problem: ClickOnce Deployment via Internet May Not Always Upgrade an Application](https://www.codeproject.com/Questions/120664/My-ClickOnce-Application-Not-Updating-Why)
  * [How to: Publish a ClickOnce Application using the Publish Wizard
](https://msdn.microsoft.com/en-us/library/31kztyey.aspx)
  * [Where does ClickOnce put files?](https://social.msdn.microsoft.com/Forums/en-US/c6e3d328-1deb-49c9-99cf-98fe3830702a/where-does-clickonce-put-files?forum=winformssetup)
  * [Change installation folder for a Click Once App](https://social.msdn.microsoft.com/Forums/windows/en-US/5c7d00c2-2473-4fd5-b815-30066383eb47/change-installation-folder-for-a-click-once-app?forum=winformssetup)
  
