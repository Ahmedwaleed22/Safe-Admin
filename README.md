# Securing Admin Panel

<p>We will seperate this topic to multiple steps to always keep your admin panel safe and away from hackers and script kiddies</p>

## First: Specific Ip (Backend)

<p>This way can protect your admin panel from some users and script kiddies who don't know what are they doing.</p>

### How It Works:

<p>It works with getting the user ip on the request for example:</p>

<p>Getting the user ip on requesting "/admin" or whatever you call the route and checks if it is the allowed ip or not. (From Backend)</p>

<p>This method is using the "X-Forwarded-For" http parameter to access the user ip and it will be very easy for hackers to exploit it</p>

### How To Exploit

<p>Exploiting this method is very easy and you can use many programs / extention to exploit I will mention them soon</p>

<p>The way you can use to exploit it is by adding / Editing the "X-Forwarded-For" http parameter and appending the ip required for the request to be done or even appending some code to exploit the whole website</p>

##### Programs / Extentions Can Be Used For Exploiting

<ul>
	<li>Program -- Burp Suit</li>
	<li>Extention -- ModHeader</li>
</ul>


## Second: Common Credentials

<p>Please stop using admin as username and easy passwords as:</p>

<ul>
	<li>admin</li>
	<li>Putting your name in it</li>
	<li>Not using numbers and special characters</li>
</ul>

<p>Hackers can crack these passwords in some minutes</p>



## Third: Login Hints

<p>"YOU HAVE TO STOP SHOWING HINT MESSAGES" like:</p>

<ul>
	<li>Username Is Incorrect</li>
	<li>Username Doesn't Exist In Our Database</li>
	<li>Password Is Incorrect</li>
	<li>etc...</li>
</ul>

<p>You should stop using all of this message you can use other messages for wrong credentials like:</p>

<ul>
	<li>Something Went Wrong!</li>
	<li>You Are Not Allowed To Access This Part</li>
	<li>etc...</li>	
</ul>

<p>Messages like that will make the hacker confused he/she will not know what is the wrong thing username or password. and he/she will try to crack the username and the password with 2 wordlists one for username and one for password instead using only one for the password because they don't know the username yet</p>



## Fourth: Stopping Bots

<p>There are some ways to do this thing</p>

<ul>
	<li>Only Allowing Specific User Agents</li>
	<li>Implementing Google Recaptcha</li>
</ul>


### Limiting User Agents

<p>This way is not safe at all but it will prevent some tools / bots that don't allow changing it's user agent</p>


### Google Recaptcha

<p>This way is very good and it's being used on large websites</p>

<p>The only thing you will have to do is to check it and check the implementation way and etc.. from here:</p>

<a href="https://www.google.com/recaptcha/about/">Google Recptcha</a>



## Fifth: 2FA

<p>This is one of the preferred ways and one of the most secure ways until now</p>

### How It Works

<p>This is about making the website ask for a code sent on email / phone number just after login and don't allow the user to access the admin panel until he/she submit the code.</p>

<p>This code should be at least 6 digits and it's also preferred to has some letters in it and user will have only 3 tries and then the code should be deactivated and the account should be locked temporary until the admin changes the password with the link sent on the email / phone number</p>

<p>Also this code should have around 30 minutes to expire</p>


## Sixths: Specific Ip (Htaccess)

<p>This way is to only allow the admin ip address in the htaccess using the following code</p>

```htaccess
<RequireAll>
    Require ip xx.xx.xx.xx yy.yy.yy.yy
</RequireAll>

```


## Seventh: Uptodate Password

<p>This is also one of the most important ways to keep your admin panel safe it's about changing the admin password every 30 days to make sure that this password not cracked or leaked</p>


### Eighth: Password Generator

<p>This way is important for choosing the right password</p>

<p>You should keep in mind that password generators is better in creating passwords than your brain you should use one and it will be much better if it saves your passwords like <a href="https://masterkeypasswords.com">MasterKey</a></p>

# I hope I help you with keeping your admin panel safe, Best Wishes

# #Keep_It_Safe

