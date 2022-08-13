# Toast notification examples for PowerShell

[The toast template catalog (Windows Runtime apps)](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh761494(v=win.10))

## [ToastText01](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh761494(v=win.10)#toasttext01)
![image](https://user-images.githubusercontent.com/12811398/184498009-653bd6e5-ad92-4c58-ad34-91c8d2da9cb9.png)

```powershell
$bodyText = 'A single string wrapped across a maximum of three lines of text.'

$ToastText01 = [Windows.UI.Notifications.ToastTemplateType, Windows.UI.Notifications, ContentType = WindowsRuntime]::ToastText01
$TemplateContent = [Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::GetTemplateContent($ToastText01)
$TemplateContent.SelectSingleNode('//text[@id="1"]').InnerText = $bodyText
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Show($TemplateContent)
```

## [ToastText02](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh761494(v=win.10)#toasttext02)
![image](https://user-images.githubusercontent.com/12811398/184498043-91662ac0-f9e0-4153-8f42-3b801312381b.png)

```powershell
$headlineText = 'One string of bold text on the first line.'
$bodyText = 'One string of regular text wrapped across the second and third lines.'

$ToastText02 = [Windows.UI.Notifications.ToastTemplateType, Windows.UI.Notifications, ContentType = WindowsRuntime]::ToastText02
$TemplateContent = [Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::GetTemplateContent($ToastText02)
$TemplateContent.SelectSingleNode('//text[@id="1"]').InnerText = $headlineText
$TemplateContent.SelectSingleNode('//text[@id="2"]').InnerText = $bodyText
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Show($TemplateContent)
```

## [ToastText03](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh761494(v=win.10)#toasttext03)
![image](https://user-images.githubusercontent.com/12811398/184498059-40b74dd3-3afd-4f37-85eb-ef99c2fe4590.png)

```powershell
$headlineText = 'One string of bold text wrapped across the first and second lines.'
$bodyText = 'One string of regular text on the third line.'

$ToastText03 = [Windows.UI.Notifications.ToastTemplateType, Windows.UI.Notifications, ContentType = WindowsRuntime]::ToastText03
$TemplateContent = [Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::GetTemplateContent($ToastText03)
$TemplateContent.SelectSingleNode('//text[@id="1"]').InnerText = $headlineText
$TemplateContent.SelectSingleNode('//text[@id="2"]').InnerText = $bodyText
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Show($TemplateContent)
```

## [ToastText04](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh761494(v=win.10)#toasttext04)
![image](https://user-images.githubusercontent.com/12811398/184498082-c70afdf0-08cb-4de4-94ae-0e1361aeba42.png)

```powershell
$headlineText = 'One string of bold text on the first line.'
$bodyText1 = 'One string of regular text on the second line.'
$bodyText2 = 'One string of regular text on the third line.'

$ToastText04 = [Windows.UI.Notifications.ToastTemplateType, Windows.UI.Notifications, ContentType = WindowsRuntime]::ToastText04
$TemplateContent = [Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::GetTemplateContent($ToastText04)
$TemplateContent.SelectSingleNode('//text[@id="1"]').InnerText = $headlineText
$TemplateContent.SelectSingleNode('//text[@id="2"]').InnerText = $bodyText1
$TemplateContent.SelectSingleNode('//text[@id="3"]').InnerText = $bodyText2
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Show($TemplateContent)
```

## [ToastImageAndText01](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh761494(v=win.10)#toastimageandtext01)
![image](https://user-images.githubusercontent.com/12811398/184498101-a7531a6d-70aa-404d-b4f3-dc5631b48631.png)

```powershell
$image = 'C:\Windows\IdentityCRL\WLive48x48.png'
$bodyText = 'A single string wrapped across a maximum of three lines of text.'

$ToastImageAndText01 = [Windows.UI.Notifications.ToastTemplateType, Windows.UI.Notifications, ContentType = WindowsRuntime]::ToastImageAndText01
$TemplateContent = [Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::GetTemplateContent($ToastImageAndText01)
$TemplateContent.SelectSingleNode('//image[@id="1"]').SetAttribute('src', $image)
$TemplateContent.SelectSingleNode('//text[@id="1"]').InnerText = $bodyText
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Show($TemplateContent)
```

## [ToastImageAndText02](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh761494(v=win.10)#toastimageandtext02)
![image](https://user-images.githubusercontent.com/12811398/184498119-38319dc4-fea3-4d68-b00a-7a99b1d35bda.png)

```powershell
$image = 'C:\Windows\IdentityCRL\WLive48x48.png'
$headlineText = 'One string of bold text on the first line.'
$bodyText = 'One string of regular text wrapped across the second and third lines.'

$ToastImageAndText02 = [Windows.UI.Notifications.ToastTemplateType, Windows.UI.Notifications, ContentType = WindowsRuntime]::ToastImageAndText02
$TemplateContent = [Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::GetTemplateContent($ToastImageAndText02)
$TemplateContent.SelectSingleNode('//image[@id="1"]').SetAttribute('src', $image)
$TemplateContent.SelectSingleNode('//text[@id="1"]').InnerText = $headlineText
$TemplateContent.SelectSingleNode('//text[@id="2"]').InnerText = $bodyText
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Show($TemplateContent)
```

## [ToastImageAndText03](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh761494(v=win.10)#toastimageandtext03)
![image](https://user-images.githubusercontent.com/12811398/184498135-b9384b33-f21c-4db4-8387-d4d681818f2e.png)

```powershell
$image = 'C:\Windows\IdentityCRL\WLive48x48.png'
$headlineText = 'One string of bold text wrapped across the first two lines.'
$bodyText = 'One string of regular text on the third line.'

$ToastImageAndText03 = [Windows.UI.Notifications.ToastTemplateType, Windows.UI.Notifications, ContentType = WindowsRuntime]::ToastImageAndText03
$TemplateContent = [Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::GetTemplateContent($ToastImageAndText03)
$TemplateContent.SelectSingleNode('//image[@id="1"]').SetAttribute('src', $image)
$TemplateContent.SelectSingleNode('//text[@id="1"]').InnerText = $headlineText
$TemplateContent.SelectSingleNode('//text[@id="2"]').InnerText = $bodyText
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Show($TemplateContent)
```

## [ToastImageAndText04](https://docs.microsoft.com/en-us/previous-versions/windows/apps/hh761494(v=win.10)#toastimageandtext04)
![image](https://user-images.githubusercontent.com/12811398/184498156-b2ce06df-2659-485b-8987-f23c8c87d3f0.png)

```powershell
$image = 'C:\Windows\IdentityCRL\WLive48x48.png'
$headlineText = 'One string of bold text on the first line.'
$bodyText1 = 'One string of regular text on the second line.'
$bodyText2 = 'One string of regular text on the third line.'

$ToastImageAndText04 = [Windows.UI.Notifications.ToastTemplateType, Windows.UI.Notifications, ContentType = WindowsRuntime]::ToastImageAndText04
$TemplateContent = [Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::GetTemplateContent($ToastImageAndText04)
$TemplateContent.SelectSingleNode('//image[@id="1"]').SetAttribute('src', $image)
$TemplateContent.SelectSingleNode('//text[@id="1"]').InnerText = $headlineText
$TemplateContent.SelectSingleNode('//text[@id="2"]').InnerText = $bodyText1
$TemplateContent.SelectSingleNode('//text[@id="3"]').InnerText = $bodyText2
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Show($TemplateContent)
```

The [image](https://msdn.microsoft.com/en-us/library/BR230844) is expressed using one of these protocols:

- http:// or https://

  A web-based image.

- ms-appx:///

  An image included in the app package.

- ms-appdata:///local/

  An image saved to local storage.

- file:///

  A local image. (Only supported for desktop apps.)

## New line `` `n ``
![image](https://user-images.githubusercontent.com/12811398/184498520-09fc7de9-cb9f-4b46-82fc-d3117c9eed20.png)

```powershell
$bodyText = "ASCII.JP`nWindows Info"

$ToastText01 = [Windows.UI.Notifications.ToastTemplateType, Windows.UI.Notifications, ContentType = WindowsRuntime]::ToastText01
$TemplateContent = [Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::GetTemplateContent($ToastText01)
$TemplateContent.SelectSingleNode('//text[@id="1"]').InnerText = $bodyText
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Show($TemplateContent)
```

## Logo image `placement="appLogoOverride"`
![image](https://user-images.githubusercontent.com/12811398/184499812-2503630c-4bdd-4d75-9406-ce9db00125de.png)

```powershell
$headlineText = 'One string of bold text on the first line.'
$bodyText = 'One string of regular text on the second line.'
$logo = 'C:\Windows\IdentityCRL\WLive48x48.png'
$image = 'C:\Windows\Web\Screen\img100.jpg'

$xml = @"
<toast>
    <visual>
        <binding template="ToastGeneric">
            <text>$($headlineText)</text>
            <text>$($bodyText)</text>
            <image placement="appLogoOverride" src="$($logo)"/>
            <image src="$($image)"/>
        </binding>
    </visual>
</toast>
"@
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Circle logo `hint-crop="circle"`
![image](https://user-images.githubusercontent.com/12811398/184500546-d45dc2d4-135a-42b3-9f69-a1b5ffd7d36e.png)

```powershell
$headlineText = 'One string of bold text on the first line.'
$bodyText = 'One string of regular text on the second line.'
$logo = 'C:\Windows\IdentityCRL\WLive48x48.png'
$image = 'C:\Windows\Web\Screen\img100.jpg'

$xml = @"
<toast>
    <visual>
        <binding template="ToastGeneric">
            <text>$($headlineText)</text>
            <text>$($bodyText)</text>
            <image placement="appLogoOverride" hint-crop="circle" src="$($logo)"/>
            <image src="$($image)"/>
        </binding>
    </visual>
</toast>
"@
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Hero image `placement="hero"`
![image](https://user-images.githubusercontent.com/12811398/184500761-fd9b58a9-b51d-4909-b4f1-cf6e4c99edcc.png)

```powershell
$headlineText = 'One string of bold text on the first line.'
$bodyText = 'One string of regular text on the second line.'
$logo = 'C:\Windows\IdentityCRL\WLive48x48.png'
$image = 'C:\Windows\Web\Screen\img100.jpg'

$xml = @"
<toast>
    <visual>
        <binding template="ToastGeneric">
            <text>$($headlineText)</text>
            <text>$($bodyText)</text>
            <image placement="appLogoOverride" src="$($logo)"/>
            <image placement="hero" src="$($image)"/>
        </binding>
    </visual>
</toast>
"@
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Basic
![image](https://user-images.githubusercontent.com/12811398/184501065-133d97bb-6526-4f89-a6c2-b416cc4a58ab.png)

```powershell
$xml = @"
<toast>
    <visual>
        <binding template="ToastGeneric">
        <text>Hello World</text>
        <text>This is a simple toast message</text>
        </binding>
    </visual>
</toast>
"@
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Alarm
![image](https://user-images.githubusercontent.com/12811398/184501154-a238869f-beae-486b-a465-a4dfa8d7212b.png)
![image](https://user-images.githubusercontent.com/12811398/184501167-126f8472-d9cc-4556-9224-ae5dd1b4d5c4.png)

```powershell
$xml = @"
<toast launch="action=viewAlarm&amp;alarmId=3" scenario="alarm">

  <visual>
    <binding template="ToastGeneric">
      <text>Time to wake up!</text>
      <text>To prove you're awake, select which of the following fruits is yellow...</text>
    </binding>
  </visual>

  <actions>

    <input id="answer" type="selection" defaultInput="wrongDefault">
      <selection id="wrong" content="Orange"/>
      <selection id="wrongDefault" content="Blueberry"/>
      <selection id="right" content="Banana"/>
      <selection id="wrong" content="Avacado"/>
      <selection id="wrong" content="Cherry"/>
    </input>

    <action
      activationType="system"
      arguments="snooze"
      content=""/>

    <action
      activationType="background"
      arguments="dismiss"
      content="Dismiss"/>

  </actions>

</toast>
"@
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```
