<!-- TOC depthFrom:1 depthTo:6 withLinks:1 updateOnSave:1 orderedList:0 -->

- [Goal of this document](#goal-of-this-document)
- [Make logging into your Google account more secure using a Security Key](#make-logging-into-your-google-account-more-secure-using-a-security-key)
- [Terms](#terms)
	- [Phishing](#phishing)
	- [Two-Factor Authentication (2FA)](#two-factor-authentication-2fa)
	- [Universal 2nd Factor (U2F)](#universal-2nd-factor-u2f)
	- [U2F Keys](#u2f-keys)
- [Background](#background)
	- [Problem to solve: Phishing](#problem-to-solve-phishing)
		- [Good scenario](#good-scenario)
		- [Bad scenario](#bad-scenario)
		- [Wait, why was that a bad scenario!?](#wait-why-was-that-a-bad-scenario)
		- [That's bad indeed. How can I avoid this?](#thats-bad-indeed-how-can-i-avoid-this)
		- [But, how does a U2F Key make it more secure for me?](#but-how-does-a-u2f-key-make-it-more-secure-for-me)
		- [And, how does a U2F Key actually work?](#and-how-does-a-u2f-key-actually-work)
	- [Motivation](#motivation)
- [Sources](#sources)

<!-- /TOC -->

# Goal of this document

The goal here is to write a simple, easy to understand document that describes
the problem of [Phishing](#phishing), how using two-factor authentication helps
defeat it, and how physical security keys make Phishing impossible.

**It is targeted towards non-technical audience.**

Pull requests are most welcome and encouraged.

# Make logging into your Google account more secure using a Security Key

[Go do this. Now.]()

This will make logging into your Google account more secure for you, and harder
for anyone else.

Now that you've done that, allow me to tell you **how** it makes logging into
your Google account more secure.

# Terms

## Phishing

Phishing is the attempt to obtain sensitive information such as usernames,
passwords, and credit card details (and, indirectly, money), often for malicious
reasons, by disguising as a trustworthy entity in an electronic communication.

## Two-Factor Authentication (2FA)

Two-factor authentication (also known as 2FA) is a method of confirming a user's
claimed identity by utilizing a combination of two different components.

## Universal 2nd Factor (U2F)

Universal 2nd Factor (also known as U2F) is an open authentication standard that
strengthens and simplifies 2FA.

## U2F Keys

U2F Keys or Physical Security Keys are USB devices that provide a form of
identity verification for 2FA. It looks like this:

![U2F Key](U2FKey.jpg)

# Background

## Problem to solve: Phishing

### Good scenario

Let's say you want to read your Gmail emails, and let's assume that you do not
have 2FA enabled for your [Google](https://www.google.com) account.

Here's what you would do:

1. Open ```https://www.google.com/mail```
1. You are asked to login into your Google account.
1. You enter your username.
1. You enter your password.
1. You can now access your Gmail emails.

![Google Login Page](GoogleLoginPageSmall.png)

*Scenario 1: Google Login Page*

### Bad scenario

Now consider another scenario. Your cousin Vinny sends you an email that
contains a hyperlink to a **free lottery to win an iPad**. When you click on the
link, you are shown a login page similar to previous scenario and here's what
happens:

1. The link goes to ```www.gogle.com```
1. You are asked to login into your Google account.
1. You enter your username.
1. You enter your password.
1. Something happens. For instance, you may be told that your email address has
been entered in a raffle to win the promised iPad.

![Gogle Login Page](GogleLoginPageSmall.png)

*Scenario 2: Gogle Login Page*

### Wait, why was that a bad scenario!?

Did you notice the missing ```o``` there in the website name in the URL?
Let's take a closer look.

![Gogle.com?](AccountsGogleCom.png)

*Did you intend to enter your Google credentials (username and password) on ```gogle.com```?*

Here's what may have happened in the background:

1. You entered your Google credentials on ```gogle.com```.
1. Now the owner of ```gogle.com``` has your Google credentials.
1. They can now use those credentials to login on Google as you and do bad things such as read your email, send email as you (to your contacts or other people),
etc.

This is called phishing. Phishing works because the bad actor only needs your
login credentials to login as you.

### That's bad indeed. How can I avoid this?

I'm glad you asked that. One of the best ways to avoid this, currently, is to
enable [2FA](#two-factor-authentication-2fa) and use a [U2F Key](#u2f-keys) as
the second factor for authentication.

### How does a U2F Key make it more secure for me?

Put simply, even if someone manages to phish you and get the login credentials
for your Google account, they still need physical access to the U2F Key that
acts as the second factor for authentication.

### How does a U2F Key actually work?

For more details about how U2F keys work, see:

1. [Yubico’s take onU2F Key wrapping](https://www.yubico.com/2014/11/yubicos-u2f-key-wrapping/)
2. [FIDO Specifications Overview](https://fidoalliance.org/specifications/overview/)

## Motivation

[Zeynep Tufekci](https://en.wikipedia.org/wiki/Zeynep_Tufekci) spoke at the
[Engima 2017](https://www.usenix.org/conference/enigma2017) conference about
*[Security in the Wild for Low-Profile Activists](https://github.com/aawc/Enigma2017Notes#security-in-the-wild-for-low-profile-activists)*.

She mentioned how it was difficult for her to convince activists to use U2F keys
because they did not understand how they work and how to use them.

# Sources

- <https://en.wikipedia.org/wiki/Multi-factor_authentication>
- <https://en.wikipedia.org/wiki/Universal_2nd_Factor>
- U2F image source: [LogicLounge](https://www.youtube.com/watch?v=EVx3QkJ8_J0)
- https://www.yubico.com/about/background/fido/
