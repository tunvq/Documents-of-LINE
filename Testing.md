# Create Line Business Account
## 1.Create Personal LINE Account
### 1.1 Sign up for new account
<span style="color:red">*Note: you have to have smartphone has been installed LINE on android or IOS to verify code.	</span>
<br/>
<span style="color:red">*Note: if you already have an account please login into it. </span>
<br/>
![Picture1](C:/Users/tu.nvq/Desktop/Document1/Picture1.png)
#### 1.1.1 Next verify on your smartphone by sms.
![Picture2](C:/Users/tu.nvq/Desktop/Document1/Picture2.png)
#### 1.1.2 Sign up for new account
![Picture3](C:/Users/tu.nvq/Desktop/Document1/Picture3.png)
<br/>
Enter your password,Display name, choose image for you avatar => click done
<br/>
![Picture4](C:/Users/tu.nvq/Desktop/Document1/Picture4.png)
<br/>
<span style="color:red">Note: You have to input email when register a new which uses to create a line business account, please do not click skip in this step.</span>
<br/>
![Picture5](C:/Users/tu.nvq/Desktop/Document1/Picture5.png)
<br/>
After click next ,you need to go to your mail and get the verify code ,see the picture below
<br/>
![Picture6](C:/Users/tu.nvq/Desktop/Document1/Picture6.png)
<br/>
Copy and paste the code
<br/>
![Picture7](C:/Users/tu.nvq/Desktop/Document1/Picture7.png)
-----------------------------
## 2.Create business line account under personal line account 
### 2.1 Go to https://developers.line.me/en/
<span style="color:red">*Note: Use email and password of personal line account</spna>
<br/>
![Picture9](C:/Users/tu.nvq/Desktop/Document1/Picture9.png)
#### 2.1.1 Login with your line account that you have registered above.
![Picture10](C:/Users/tu.nvq/Desktop/Document1/Picture10.png)
#### 2.1.2 Register Developer Line,Fill your infomation then click “confirm” and “Register”.
![Picture11](C:/Users/tu.nvq/Desktop/Document1/Picture11.png)
<br/>
Finish
<br/>
![Picture11 1](C:/Users/tu.nvq/Desktop/Document1/Picture11-1.png)
### 2.2 Creating Channel.
![Picture12](C:/Users/tu.nvq/Desktop/Document1/Picture12.png)
#### 2.2.1 Step 1.
![Picture13](C:/Users/tu.nvq/Desktop/Document1/Picture13.png)
#### 2.2.2 Step 2.
![Picture14](C:/Users/tu.nvq/Desktop/Document1/Picture14.png)
![Picture15](C:/Users/tu.nvq/Desktop/Document1/Picture15.png)
#### 2.2.3 Step 3.
Finish and checking again your bot 
<br/>
![Picture16](C:/Users/tu.nvq/Desktop/Document1/Picture16.png)
### 2.3 Config the channel.
#### 2.3.1 Click “Configuration not yet compelete”.
![Picture17](C:/Users/tu.nvq/Desktop/Document1/Picture17.png)
#### 2.3.2 Check your infomation again and update some settings.
![Picture20](C:/Users/tu.nvq/Desktop/Document1/Picture20.png)
![Picture21](C:/Users/tu.nvq/Desktop/Document1/Picture21.png)
![Picture22](C:/Users/tu.nvq/Desktop/Document1/Picture22.png)
<span style="color:red">*note</span>
1. Click and get the token
2. You must enable that “WebHook URL” is available to use .
3. The syntax is ‘line-api.azurewebsites.net/api/linemessage/1537852224’
### 2.4 Add your bot to your contact
*Fastest way is the QR code in “channel settings” by app “LINE” in you smartphone
#### 2.4.1 Add Bot by QR code
##### 2.4.1.1 Login in to line app then find “icon add friend” choose “QR code” then clear you camera to the “QR code” in “Channel settings”.
![Q R Code](C:/Users/tu.nvq/Desktop/QRCode.png)
<br/>
Clear your camera to the red square and wait for a second
<br/>
![Picture24](C:/Users/tu.nvq/Desktop/Document1/Picture24.png)
<br/>
![Addfriend](C:/Users/tu.nvq/Desktop/Addfriend.png)
Then Click “Add”
#### 2.4.2 Add Bot by Bot ID
##### 2.4.2.1 go to => https://admin-official.line.me and login with you email that you registered, remember to verify login with you phone by the code that website give you.
### 2.5 Finished everything else.
#### 2.5.1 Check again you bot that in you contact friend.




































<br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>
<br/>
See the official API documentation for more information.
English: https://devdocs.line.me/en/ <br/>
Japanese: https://devdocs.line.me/ja/

##Install
You can install package from Nuget.
> Install-Package LineMessagingAPI.CSharpaaaaa

You can also use Visual Studio 2015 Template for jump start. <br/>
See [here](https://github.com/kenakamu/line-bot-sdk-csharp/tree/master/LineBotApplication) for more detail.

# LineClient
LineClient class is the main proxy class.

#### Instantiate
```csharp
LineClient lineClient = new LineClient("<Channel Access Token>");
```
#### Get Meida Content
To download image, video or audio, use GetContent method. See https://devdocs.line.me/en/#get-content for more detail.
```csharp
Media media = await lineClient.GetContent("<content id>");
```

#### Get Line User Profile
You can get Line User Profile. See https://devdocs.line.me/en/#bot-api-get-profile for more detail.
```csharp
Profile profile = await lineClient.GetProflie("<LineMid>");
```

#### Reply Message
You can reply to Line Platform either by using reply or push. See https://devdocs.line.me/en/#reply-message for more detail.
```csharp
await lineClient.ReplyToActivityAsync(replyMessage);
```

#### Push Message. 
You can reply to Line Platform either by using reply or push. See https://devdocs.line.me/en/#push-message for more detail.
```csharp
await lineClient.PushAsync(replyMessage);
```

# Line Event
LineEvent class contains incoming message. See https://devdocs.line.me/en/#webhook-event-object for detail.

#### Create Reply
You can create reply easily from LineEvent.
```csharp
var reply = lineEvent.CreateReply(replyMessage);
```

# Create Reply Message
Following examples demonstrate how to construct reply message.
See https://devdocs.line.me/en/#send-message-object for detail of each message type.

#### Text Reply
```csharp 
var replyMessage = new TextMessage(textMessage.Text);
```

#### Image Reply
```csharp       
var replyMessage = new ImageMessage("https://github.com/apple-touch-icon.png", "https://github.com/apple-touch-icon.png");
```

#### Audio Reply
```csharp
var replyMessage = new AudioMessage("pass to mp4 file", 3600);
```

#### Video Reply
```csharp
var replyMessage = new VideoMessage("pass to video", "pass to video thumbnail");
```

#### Sticker Reply
```csharp
var replyMessage = new StickerMessage("1","1");
```

#### Location Reply
```csharp
var replyMessage = new LocationMessage("Title","Address","<latitude>","<longitude>");
```

#### Button Template Reply
```csharp
List<TemplateAction> actions = new List<TemplateAction>();
actions.Add(new MessageTemplateAction("Message Label", "sample data")); 
actions.Add(new PostbackTemplateAction("Postback Label", "sample data"));
actions.Add(new UriTemplateAction("Uri Label", "https://github.com/kenakamu"));

ButtonsTemplate buttonsTemplate = new ButtonsTemplate("https://github.com/apple-touch-icon.png", "Sample Title", "Sample Text", actions);                
var replyMessage = new TemplateMessage("Buttons", buttonsTemplate);
```

#### Confirm Template Reply
```csharp
List<TemplateAction> actions = new List<TemplateAction>();
actions.Add(new MessageTemplateAction("Yes", "yes"));
actions.Add(new MessageTemplateAction("No", "no"));

ConfirmTemplate confirmTemplate = new ConfirmTemplate("Confirm Test", actions);
replyMessage = new TemplateMessage("Confirm", confirmTemplate);
```

#### Carousel Template Reply
```csharp
List<TemplateColumn> columns = new List<TemplateColumn>();
List<TemplateAction> actions = new List<TemplateAction>(); 
actions.Add(new MessageTemplateAction("Message Label", "sample data"));
actions.Add(new PostbackTemplateAction("Postback Label", "sample data"));
actions.Add(new UriTemplateAction("Uri Label", "https://github.com/kenakamu"));               

columns.Add(new TemplateColumn() { Title = "Casousel 1 Title", Text = "Casousel 1 Text", ThumbnailImageUrl = "https://github.com/apple-touch-icon.png", Actions = actions });   
columns.Add(new TemplateColumn() { Title = "Casousel 2 Title", Text = "Casousel 2 Text", ThumbnailImageUrl = "https://github.com/apple-touch-icon.png", Actions = actions }); 

CarouselTemplate carouselTemplate = new CarouselTemplate(columns);                
replyMessage = new TemplateMessage("Carousel", carouselTemplate);
```
![alt text](https://i.imgur.com/oqgkt3T.jpg)

[a relative link](README1.md)
#### Release Note
v1.2
  - Support Multicast
  - Add more comments
  - Bug fixes
v1.1 
  - Fix download content bug
v1.0
  - Initial Release
