# Register line bot in DecAds system
## 1. Running “Project” and login to DecAds DashBoard.
![Picture34](https://i.imgur.com/ZHm5Rfr.png)
<br/>
![Picture35](https://i.imgur.com/WAJW3Sh.png)
## 2. Create Logic.
Choose “Logic” in the left menu, then click “+” to redirect to “create a new logic 	model” Page.
<br/>
![Picture36](https://i.imgur.com/NUrmWyk.png)
<br/>
Insert Name and description for your bot then click save you will be redirect to “Logic Model” Page.
![Picture37](https://i.imgur.com/1BAgvte.png)
## 3. Create your entity for your logic model.
Click “+” then fill your infomation then click save.
<br/>
![Picture38](https://i.imgur.com/HuhCzCf.png)
<br/>
Should create 2 entity with different (phase 1, phase 0).
## 4. Create your response.
![Picture39](https://i.imgur.com/5PZEINB.png)
![Picture40](https://i.imgur.com/U0LTQ8Y.png)
## 5. Create profile.
Fill all infomation then save.
<br/>
![Picture41](https://i.imgur.com/nsUFL0I.png)
## 6. Create Bot Service.
Fill information,choose the correct profile and correct Logic.
<br/>
![Picture42](https://i.imgur.com/4U8PIsF.png)
<br/>
## 7. Create Bot line in Line Dashboard.
![Picture43](https://i.imgur.com/pEtjfn2.png)
<br/>
7.1. Line Bot ID: Can get in “Channel Settings” => “Channel ID”<br/>
7.2. Line Bot Name:your bot name<br/>
7.3. Choose correct bot service<br/>
*note: if you don’t see anything to choose that mean you don’t have	permission.<br/>
If have **“Dev management”**,Then click follow the number
<br/>
![Picture44](https://i.imgur.com/9en3zWx.png)
![Picture45](https://i.imgur.com/WDTLsBH.png)
<br/>
Finally choose the ‘Roles’ then save. Go back to “Create line bot” your value 	will be change<br/>
7.4. Line Channel Secrect: Can get in “Channel Settings” => “Channel serect”<br/>
7.5. Line Channel Token: Can get in “Channel Settings” => Channel access token (long-lived).
## 8. Check “Channel Settings”.
![WebhookURL](https://i.imgur.com/tb4NQVl.png)
<br/>
The syntax should be
<br/>
=> “line-api.azurewebsites.net/api/linemessage/1537852224“.
## 9. Finally Chat with your bot.
![Picture47](https://i.imgur.com/AGpgnOW.png)
<br/>
Make sure that you type your sentence match with logic that you have been created before.
