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
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
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
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
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
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
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
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
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
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
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
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
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
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
$XmlDocument.loadXml($xml)
[void][Windows.UI.Notifications.ToastNotification, Windows.UI.Notifications, ContentType = WindowsRuntime]
$ToastNotification = [Windows.UI.Notifications.ToastNotification]::New($XmlDocument)
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
[void][Windows.Data.Xml.Dom.XmlDocument, Windows.Data.Xml.Dom.XmlDocument, ContentType = WindowsRuntime]
$XmlDocument = [Windows.Data.Xml.Dom.XmlDocument]::New()
$XmlDocument.loadXml($xml)
$AppId = '{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}\WindowsPowerShell\v1.0\powershell.exe'
[Windows.UI.Notifications.ToastNotificationManager, Windows.UI.Notifications, ContentType = WindowsRuntime]::CreateToastNotifier($AppId).Show($XmlDocument)
```

# References

https://github.com/kacos2000/Win10/blob/master/Notifications/readme.md
