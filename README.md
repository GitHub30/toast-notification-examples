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
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
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
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
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
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
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
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Audio
![image](https://user-images.githubusercontent.com/12811398/184664019-308bf1d6-63a0-4c98-90b1-213dd3bf97bb.png)

```powershell
$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>

  <audio src="ms-winsoundevent:Notification.Reminder"/>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

Available audio
https://docs.microsoft.com/en-us/uwp/schemas/tiles/toastschema/element-audio#attributes

## Loop audio
![image](https://user-images.githubusercontent.com/12811398/184664280-a2e08b5c-e48a-47b8-912b-700802f0a96d.png)

```powershell
$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>

  <audio src="ms-winsoundevent:Notification.Reminder" loop="true"/>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Silent
![image](https://user-images.githubusercontent.com/12811398/184664597-2e5a27ca-c44b-4a96-8b98-bfc2e6bb7606.png)

```powershell
$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>

  <audio silent="true"/>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Audio from URL
![image](https://user-images.githubusercontent.com/12811398/184780608-d4d2dc26-a330-4b51-b122-741beec4ca94.png)

```powershell
$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>

  <audio silent="true"/>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)

$MediaPlayer = [Windows.Media.Playback.MediaPlayer, Windows.Media, ContentType = WindowsRuntime]::New()
$MediaPlayer.Source = [Windows.Media.Core.MediaSource]::CreateFromUri('https://nyanpass.com/nyanpass.mp3')
$MediaPlayer.Play()
```

## Audio from File
![image](https://user-images.githubusercontent.com/12811398/184780608-d4d2dc26-a330-4b51-b122-741beec4ca94.png)

```powershell
$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>

  <audio silent="true"/>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)

$MediaPlayer = [Windows.Media.Playback.MediaPlayer, Windows.Media, ContentType = WindowsRuntime]::New()
$MediaPlayer.Source = [Windows.Media.Core.MediaSource]::CreateFromUri('C:\Users\Admin\Downloads\nyanpass.mp3')
$MediaPlayer.Play()
```

## Speak
![image](https://user-images.githubusercontent.com/12811398/184780608-d4d2dc26-a330-4b51-b122-741beec4ca94.png)

```powershell
$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>

  <audio silent="true"/>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)

Add-Type -AssemblyName System.speech
([System.Speech.Synthesis.SpeechSynthesizer]::New()).Speak('Hello world')
```

## Open link
![image](https://user-images.githubusercontent.com/12811398/184736015-b54756d0-d521-4193-afea-d459e3a88f43.png)

```powershell
$xml = @"
<toast activationType="protocol" launch="https://www.google.com/" >
  
  <visual>
    <binding template="ToastGeneric">
      <text>Click to open Google</text>
    </binding>
  </visual>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Open link when button is clicked
![image](https://user-images.githubusercontent.com/12811398/184735491-05f13e37-c089-4300-b880-f58e5cdb6f77.png)

```powershell
$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>
  
  <actions>
    <action content="Open Google" activationType="protocol" arguments="https://www.google.com/" />
  </actions>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Execute Python Script
![image](https://user-images.githubusercontent.com/12811398/184744179-a55604dc-35fa-45ce-bfb4-82d8acb3eb65.png)

```powershell
$PSDefaultParameterValues['Out-File:Encoding'] = 'utf8'
'import webbrowser; webbrowser.open("https://www.python.org")' > handler.pyw
$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>
  
  <actions>
    <action content="Execute Python Script" activationType="protocol" arguments="$($PWD)\handler.pyw" />
  </actions>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Long duration
![image](https://user-images.githubusercontent.com/12811398/184664978-1bd036ac-e208-440b-8685-8b68d04e6070.png)

```powershell
$xml = @"
<toast duration="long">
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

displayed for 25 seconds

## No timeout
![image](https://github.com/GitHub30/toast-notification-examples/assets/12811398/0e6a836e-0bfd-4236-a7ce-e48cf8455187)

```powershell
$xml = @"
<toast scenario="incomingCall">
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

The scenario your toast is used for, like an alarm, reminder, incomingCall or urgent.

https://learn.microsoft.com/en-us/uwp/schemas/tiles/toastschema/element-toast#:~:text=None-,scenario,-The%20scenario%20your

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
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Breaking news
![image](https://user-images.githubusercontent.com/12811398/184501258-88141d56-fc97-43c9-ad63-02849a483039.png)

```powershell
$xml = @"
<toast launch="action=viewStory&amp;storyId=92187">

    <visual>
        <binding template="ToastGeneric">
            <text>Tortoise beats rabbit in epic race</text>
            <text>In a surprising turn of events, Rockstar Rabbit took a nasty crash, allowing Thomas the Tortoise to win the race.</text>
            <text placement="attribution">The Animal Times</text>
        </binding>
    </visual>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Event invite
![image](https://user-images.githubusercontent.com/12811398/184501365-3c125a67-a7d3-45d1-aeed-3b136891d434.png)
![image](https://user-images.githubusercontent.com/12811398/184501378-af4599a2-287c-493c-8b59-078e94c1bfec.png)

```powershell
$xml = @"
<toast launch="action=viewEvent&amp;eventId=63851">
  
  <visual>
    <binding template="ToastGeneric">
      <text>Surface Launch Party</text>
      <text>Studio S / Ballroom</text>
      <text>4:00 PM, 10/26/2015</text>
    </binding>
  </visual>

  <actions>
    
    <input id="status" type="selection" defaultInput="yes">
      <selection id="yes" content="Going"/>
      <selection id="maybe" content="Maybe"/>
      <selection id="no" content="Decline"/>
    </input>

    <action
      activationType="background"
      arguments="action=rsvpEvent&amp;eventId=63851"
      content="RSVP"/>

    <action
      activationType="system"
      arguments="dismiss"
      content=""/>
    
  </actions>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Friend request
![image](https://user-images.githubusercontent.com/12811398/184501497-61aea9a2-7391-43eb-8c95-92f8e9cbae25.png)

```powershell
$xml = @"
<toast launch="action=viewFriendRequest&amp;userId=49183">

  <visual>
    <binding template="ToastGeneric">
      <text>Matt sent you a friend request</text>
      <text>Hey, wanna dress up as wizards and ride around on our hoverboards together?</text>
      <image placement="appLogoOverride" hint-crop="circle" src="C:\Windows\IdentityCRL\WLive48x48.png"/>
    </binding>
  </visual>

  <actions>
    <action content="Accept" activationType="background" arguments="action=acceptFriendRequest&amp;userId=49183"/>
    <action content="Decline" activationType="background" arguments="action=declineFriendRequest&amp;userId=49183"/>
  </actions>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Incoming call
![image](https://user-images.githubusercontent.com/12811398/184645411-5e9391d1-897a-4f63-9b95-7f6e00a302f9.png)

```powershell
$xml = @"
<toast launch="action=answer&amp;callId=938163" scenario="incomingCall">

  <visual>
    <binding template="ToastGeneric">
      <text>Andrew Bares</text>
      <text>Incoming Call - Mobile</text>
      <image hint-crop="circle" src="https://unsplash.it/100?image=883"/>
    </binding>
  </visual>

  <actions>

    <action
      content="Text reply"
      imageUri="https://storage.googleapis.com/rppico.appspot.com/message.png"
      activationType="foreground"
      arguments="action=textReply&amp;callId=938163"/>

    <action
      content="Reminder"
      imageUri="https://storage.googleapis.com/rppico.appspot.com/reminder.png"
      activationType="background"
      arguments="action=reminder&amp;callId=938163"/>

    <action
      content="Ignore"
      imageUri="https://storage.googleapis.com/rppico.appspot.com/cancel.png"
      activationType="background"
      arguments="action=ignore&amp;callId=938163"/>

    <action
      content="Answer"
      imageUri="https://storage.googleapis.com/rppico.appspot.com/telephone.png"
      arguments="action=answer&amp;callId=938163"/>

  </actions>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = 'Microsoft.WindowsTerminal_8wekyb3d8bbwe!App'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Messaging
![image](https://user-images.githubusercontent.com/12811398/184646024-7cb557af-27bd-4483-a924-a834e0aa1d80.png)

```powershell
$xml = @"
<toast launch="action=openThread&amp;threadId=92187">

    <visual>
        <binding template="ToastGeneric">
            <text hint-maxLines="1">Jill Bender</text>
            <text>Check out where we camped last weekend! It was incredible, wish you could have come on the backpacking trip!</text>
            <image placement="appLogoOverride" hint-crop="circle" src="https://unsplash.it/64?image=1027"/>
            <image placement="hero" src="https://unsplash.it/360/180?image=1043"/>
        </binding>
    </visual>

    <actions>

        <input id="textBox" type="text" placeHolderContent="reply"/>

        <action
          content="Send"
          imageUri="https://storage.googleapis.com/rppico.appspot.com/send.png"
          hint-inputId="textBox"
          activationType="background"
          arguments="action=reply&amp;threadId=92187"/>

    </actions>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = 'Microsoft.WindowsTerminal_8wekyb3d8bbwe!App'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Photo tagged
![image](https://user-images.githubusercontent.com/12811398/184646358-96a4d36d-aad2-4f48-a2fc-a80f63a49aae.png)

```powershell
$xml = @"
<toast launch="action=viewPhoto&amp;photoId=92187">

  <visual>
    <binding template="ToastGeneric">
      <image placement="appLogoOverride" hint-crop="circle" src="https://unsplash.it/64?image=669"/>
      <text>Adam Wilson tagged you in a photo</text>
      <text>On top of McClellan Butte - with Andrew Bares</text>
      <image src="https://unsplash.it/360/202?image=883"/>
    </binding>
  </visual>

  <actions>

    <action
      content="Like"
      activationType="background"
      arguments="likePhoto&amp;photoId=92187"/>
    
    <action
      content="Comment"
      arguments="action=commentPhoto&amp;photoId=92187"/>
    
  </actions>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = 'Microsoft.WindowsTerminal_8wekyb3d8bbwe!App'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Progress bar
![image](https://user-images.githubusercontent.com/12811398/184655641-78e7032f-526f-4cac-b2c4-62ecdb070d8a.gif)

```powershell
$xml = @"
<toast launch="action=viewDownload&amp;downloadId=9438108">
  
  <visual>
    <binding template="ToastGeneric">
      <text>Downloading this week's new video...</text>
      <progress
        title="{progressTitle}"
        value="{progressValue}"
        valueStringOverride="{progressValueString}"
        status="{progressStatus}"/>
    </binding>
  </visual>

  <actions>

    <action
      activationType="background"
      arguments="action=pauseDownload&amp;downloadId=9438108"
      content="Pause"/>

    <action
      activationType="background"
      arguments="action=cancelDownload&amp;downloadId=9438108"
      content="Cancel"/>
    
  </actions>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$ToastNotification = [Windows.UI.Notifications.ToastNotification, Windows.UI.Notifications, ContentType = WindowsRuntime]::New($XmlDocument)
$ToastNotification.Tag = 'my_tag'
$Dictionary = [System.Collections.Generic.Dictionary[String, String]]::New()
$Dictionary.Add('progressTitle', 'YouTube')
$Dictionary.Add('progressValue', '0')
$Dictionary.Add('progressValueString', '0/15 videos')
$Dictionary.Add('progressStatus', 'Downloading...')
$ToastNotification.Data = [Windows.UI.Notifications.NotificationData]::New($Dictionary)
$ToastNotification.Data.SequenceNumber = 1
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($ToastNotification)


for ($index = 1; $index -le 15; $index++) {
  Start-Sleep 1
  $Dictionary = [System.Collections.Generic.Dictionary[String, String]]::New()
  $Dictionary.Add('progressValue', $index / 15)
  $Dictionary.Add('progressValueString', "$index/15 videos")
  $NotificationData = [Windows.UI.Notifications.NotificationData]::New($Dictionary)
  $NotificationData.SequenceNumber = 2
  [Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Update($NotificationData, 'my_tag')
}

$Dictionary = [System.Collections.Generic.Dictionary[String, String]]::New()
$Dictionary.Add('progressStatus', 'Completed!')
$NotificationData = [Windows.UI.Notifications.NotificationData]::New($Dictionary)
$NotificationData.SequenceNumber = 2
[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier($AppId).Update($NotificationData, 'my_tag')
```

## Reminder
![image](https://user-images.githubusercontent.com/12811398/184656689-ac527ef2-63cb-453f-a6bc-40dbc58e4816.png)
![image](https://user-images.githubusercontent.com/12811398/184656722-33bca4d1-9461-4bc6-acb2-fc3ac160682a.png)

```powershell
$xml = @"
<toast launch="action=viewEvent&amp;eventId=1983" scenario="reminder">
  
  <visual>
    <binding template="ToastGeneric">
      <text>Adaptive Tiles Meeting</text>
      <text>Conf Room 2001 / Building 135</text>
      <text>10:00 AM - 10:30 AM</text>
    </binding>
  </visual>

  <actions>
    
    <input id="snoozeTime" type="selection" defaultInput="15">
      <selection id="1" content="1 minute"/>
      <selection id="15" content="15 minutes"/>
      <selection id="60" content="1 hour"/>
      <selection id="240" content="4 hours"/>
      <selection id="1440" content="1 day"/>
    </input>

    <action
      activationType="system"
      arguments="snooze"
      hint-inputId="snoozeTime"
      content=""/>

    <action
      activationType="system"
      arguments="dismiss"
      content=""/>
    
  </actions>
  
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Restaurant
![image](https://user-images.githubusercontent.com/12811398/184657839-68edfc06-e199-450c-a035-3bf20243a363.png)

```powershell
$xml = @"
<toast launch="action=viewRestaurant&amp;restaurantId=92187">

    <visual>
        <binding template="ToastGeneric">
            <image placement="hero" src="https://storage.googleapis.com/rppico.appspot.com/Food1.jpg"/>
            <text hint-maxLines="1">New suggested restaurant</text>
            <text>There's a popular chinese restaurant near you that we think you'd like!</text>
            <image src="https://storage.googleapis.com/rppico.appspot.com/RestaurantMap.jpg"/>
            <group>
                <subgroup>
                    <text hint-style="body">Pho Licious</text>
                    <text hint-style="captionSubtle">4.6 stars</text>
                </subgroup>
                <subgroup hint-textStacking="bottom">
                    <text hint-style="captionSubtle" hint-wrap="true" hint-align="right">4018 148th Ave NE, Redmond, WA 98052</text>
                </subgroup>
            </group>
        </binding>
    </visual>

    <actions>

        <action
          content="Map"
          arguments="bingmaps:?q=4018 148th Ave NE, Redmond, WA 98052"
          activationType="protocol"/>

        <action
          content="Reviews"
          arguments="action=viewRestaurantReviews&amp;restaurantId=92187"/>

    </actions>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = 'Microsoft.WindowsTerminal_8wekyb3d8bbwe!App'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Weather
![image](https://user-images.githubusercontent.com/12811398/184658678-f99094fe-0fbe-4eb0-a9ec-026ee497c388.png)

```powershell
$xml = @"
<toast>

    <visual baseUri="https://storage.googleapis.com/rppico.appspot.com/">
        <binding template="ToastGeneric">
            <text>Today will be sunny with a high of 63 and a low of 42.</text>

            <group>
                <subgroup hint-weight="1">
                    <text hint-align="center">Mon</text>
                    <image src="Mostly Cloudy.png" hint-removeMargin="true"/>
                    <text hint-align="center">63°</text>
                    <text hint-style="captionsubtle" hint-align="center">42°</text>
                </subgroup>
                <subgroup hint-weight="1">
                    <text hint-align="center">Tue</text>
                    <image src="Cloudy.png" hint-removeMargin="true"/>
                    <text hint-align="center">57°</text>
                    <text hint-style="captionsubtle" hint-align="center">38°</text>
                </subgroup>
                <subgroup hint-weight="1">
                    <text hint-align="center">Wed</text>
                    <image src="Sunny.png" hint-removeMargin="true"/>
                    <text hint-align="center">59°</text>
                    <text hint-style="captionsubtle" hint-align="center">43°</text>
                </subgroup>
                <subgroup hint-weight="1">
                    <text hint-align="center">Thu</text>
                    <image src="Sunny.png" hint-removeMargin="true"/>
                    <text hint-align="center">62°</text>
                    <text hint-style="captionsubtle" hint-align="center">42°</text>
                </subgroup>
                <subgroup hint-weight="1">
                    <text hint-align="center">Fri</text>
                    <image src="Sunny.png" hint-removeMargin="true"/>
                    <text hint-align="center">71°</text>
                    <text hint-style="captionsubtle" hint-align="center">66°</text>
                </subgroup>
            </group>
        </binding>
    </visual>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = 'Microsoft.WindowsTerminal_8wekyb3d8bbwe!App'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Download Finished
![image](https://user-images.githubusercontent.com/12811398/184659716-5f717351-d4a7-4de2-aec7-1fae31042d0d.png)

```powershell
$xml = @"
<toast>
  <visual>
    <binding template="ToastGeneric">
      <text>Music Player</text>
      <text>Download Finished</text>
    </binding>
  </visual>
  <actions>
    <action content="Play" activationType="protocol" arguments="C:\Windows\Media\Alarm01.wav" />
    <action content="Open Folder" activationType="protocol" arguments="file:///C:/Windows/Media" />
  </actions>
</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## No content
![image](https://user-images.githubusercontent.com/12811398/184665839-3f812765-346f-418d-b495-1b12e1cf0a67.png)

```powershell
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml('<toast></toast>')
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

## Listening to events

`$PSVersionTable`

### PowerShell 7.1

```powershell
Invoke-WebRequest https://github.com/Windos/BurntToast/raw/main/BurntToast/lib/Microsoft.Windows.SDK.NET/WinRT.Runtime.dll -OutFile WinRT.Runtime.dll
Add-Type -Path WinRT.Runtime.dll
Invoke-WebRequest https://github.com/Windos/BurntToast/raw/main/BurntToast/lib/Microsoft.Windows.SDK.NET/Microsoft.Windows.SDK.NET.dll -OutFile Microsoft.Windows.SDK.NET.dll
Add-Type -Path Microsoft.Windows.SDK.NET.dll

$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>
  
  <actions>
    <input id="textBox" type="text"/>
    <action content="Send" activationType="system" arguments="dismiss" />
  </actions>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
$XmlDocument.loadXml($xml)
$toast = [Windows.UI.Notifications.ToastNotification]::New($XmlDocument)

Register-ObjectEvent -InputObject $toast -EventName Activated -Action {
  Write-Host $Event.SourceArgs.Arguments
  Write-Host $Event.SourceArgs.UserInput.Value
}

[Windows.UI.Notifications.ToastNotificationManager]::CreateToastNotifier().Show($toast)
```

https://github.com/PowerShell/PowerShell/issues/13042#issuecomment-653357546

https://toastit.dev/2020/08/08/actionable/

You can install the latest PowerShell in the Microsoft store

![スクリーンショット 2022-08-19 125139.png](https://qiita-image-store.s3.ap-northeast-1.amazonaws.com/0/208363/76965774-2fe8-d2e0-5b56-8c122154528f.png)

### PowerShell 5.1

```powershell
Invoke-WebRequest https://github.com/GitHub30/PoshWinRT/releases/download/1.2/PoshWinRT.dll -OutFile PoshWinRT.dll

$xml = @"
<toast>
  
  <visual>
    <binding template="ToastGeneric">
      <text>Hello World</text>
      <text>This is a simple toast message</text>
    </binding>
  </visual>
  
  <actions>
    <input id="textBox" type="text"/>
    <action content="Send" activationType="system" arguments="dismiss" />
  </actions>

</toast>
"@
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]::New()
$XmlDocument.loadXml($xml)
$toast = [Windows.UI.Notifications.ToastNotification, Windows.UI.Notifications, ContentType = WindowsRuntime]::New($XmlDocument)

function WrapToastEvent {
  param($target, $eventName)

  Add-Type -Path PoshWinRT.dll
  $wrapper = new-object "PoshWinRT.EventWrapper[Windows.UI.Notifications.ToastNotification,System.Object]"
  $wrapper.Register($target, $eventName)
}

Register-ObjectEvent -InputObject (WrapToastEvent $toast 'Activated') -EventName FireEvent -Action {
  Write-Host arguments:, $args[1].Result.arguments
  Write-Host textBox:, $args[1].Result.userinput['textBox']
}

$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($toast)
```

![スクリーンショット 2022-08-18 133524](https://user-images.githubusercontent.com/12811398/185521954-fc59d0b8-fcd2-4859-a30e-67c2b8851931.png)


https://github.com/PowerShell/PowerShell/issues/2181

# References

https://github.com/kacos2000/Win10/blob/master/Notifications/readme.md
