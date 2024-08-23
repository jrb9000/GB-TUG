---
icon: rocket-launch
description: MacBook Pro Setup - First boot, securing your Mac with best practices.
cover: >-
  https://docs-assets.developer.apple.com/published/554cce3cf44640dce126d5f03adca6cd/patterns-settings-intro~dark@2x.png
coverY: 0
---

# First Time MBP Setup

{% hint style="success" %}
## Key Notes

* The first thing you should do is update your system. To do that go: `Apple menu > About This Mac > Software Update`.&#x20;
* macOS is most secure running on [Apple hardware](https://support.apple.com/guide/security/hardware-security-overview-secf020d1074/1/web/1) with Apple silicon. The newer the Mac, the better. Avoid hackintoshes and Macs that don't support the latest macOS, as Apple doesn't [patch all vulnerabilities](https://support.apple.com/guide/deployment/about-software-updates-depc4c80847a) in versions that aren't the most recent one.
{% endhint %}

## First Boot & Essential Configurration

When macOS first starts, you'll be greeted by **Setup Assistant**.

### Users and Groups

{% hint style="info" %}
The first user account is always an admin account. Admin accounts are members of the admin group and have access to `sudo`, which allows them to usurp other accounts, in particular root, and gives them effective control over the system. Any program that the admin executes can potentially obtain the same access, making this a security risk.

— [macOS Security and Privacy Guide](https://github.com/drduh/macOS-Security-and-Privacy-Guide?tab=readme-ov-file#admin-and-user-accounts)
{% endhint %}

### First Mac User (Administrator)

**Create First User**

* [ ] Set **username** and **password** (w_hen creating the first account, use a_ [_strong password_](https://www.eff.org/dice) _without a hint._). <mark style="color:red;">**PLEASE NOTE — "**</mark>_If you enter your real name at the account setup process, be aware that your computer's name and local hostname will comprise that name (e.g., John Appleseed's MacBook) and thus will appear on local networks and in various preference files._
* [ ] Set **home folder** location for user (eg. `/Users/<USERNAME>`)

### CLI First User System Config…

<details>

<summary>Command-line verification</summary>

We'll use `scutil` - _Manage system configuration parameters. Require root privileges when setting configuration._ | [System Manager's Manual](https://keith.github.io/xcode-man-pages/scutil.8.html).

</details>

{% embed url="https://gist.github.com/jrb9000/4719279d0378eadfb3ecdeadc9a707e2" %}

{% hint style="danger" %}
Utilities like `sudo` have [weaknesses that can be exploited](https://bogner.sh/2014/03/another-mac-os-x-sudo-password-bypass/) by concurrently running programs.
{% endhint %}

***

{% content-ref url="personalization-checklists/user-account-apple-id-and-icloud.md" %}
[user-account-apple-id-and-icloud.md](personalization-checklists/user-account-apple-id-and-icloud.md)
{% endcontent-ref %}

