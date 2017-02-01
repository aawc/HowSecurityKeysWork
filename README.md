<!-- TOC depthFrom:1 depthTo:3 withLinks:1 updateOnSave:1 orderedList:0 -->

 - [Terms](#terms)

  - [Phishing](#phishing)
  - [Two-Factor Authentication (2FA)](#two-factor-authentication-2fa)
  - [Universal 2nd Factor (U2F)](#universal-2nd-factor-u2f)
  - [Physical Security Keys](#physical-security-keys)

- [Background](#background)
- [Sources](#sources)

<!-- /TOC -->

# Motivation

A simple, easy to understand document that aims to describe the problem of
[Phishing](#phishing), how using two-factor authentication helps defeat it, and
how physical security keys make Phishing impossible.

**It is targeted towards non-technical audience.**

Pull requests are welcome and encouraged.

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
identity verification for 2FA.

# Background

## Problem to solve

Let's say you want to read your Gmail emails, and let's assume that you do not
have 2FA enabled for your [Google](https://www.google.com) account.

Here's what you would do:

1. Open ```www.google.com/mail```
1. You are asked to login into your account.
1. You enter your username.
1. You enter your password.
1. You are logged in.

![Google Login Page](GoogleLoginPageSmall.png)
*Scenario 1: Google Login Page*

Now consider another scenario. You cousin Vinny sends you an email that contains
a link to a **free lottery to win an iPad**. When you click on the link, you are
shown a similar login page and here's what happens:

1. The link goes to ```www.gogle.com/mail```
1. You are asked to login into your account.
1. You enter your username.
1. You enter your password.
1. You are logged in.

![Gogle Login Page](GogleLoginPageSmall.png)
*Scenario 1: Gogle Login Page*

Did you notice the missing ```o``` there in the website name in the URL?
Let's take a closer look.

![Gogle.com?](AccountsGogleCom.png)
*Gogle.com?*


## Motivation: <https://github.com/aawc/Enigma2017Notes#security-in-the-wild-for-low-profile-activists>

- How do security keys work?

  - <http://www.explainthatstuff.com/how-security-tokens-work.html>
  - <https://www.yubico.com/about/background/fido/>
  - <https://www.facebook.com/notes/facebook-security/security-key-for-safer-logins-with-a-touch/10154125089265766>
  - http://heatherandwill.io/key

# Sources

- <https://en.wikipedia.org/wiki/Multi-factor_authentication>
- <https://en.wikipedia.org/wiki/Universal_2nd_Factor>
