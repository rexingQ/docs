---
title: 通知のためのメール設定
intro: 'ユーザが {% data variables.product.product_name %} のアクティビティにすばやく応答できるようにするために、{% data variables.product.product_location %} を設定して、Issue、プルリクエスト、およびコミットコメントのメール通知を送信できます。'
redirect_from:
  - /enterprise/admin/guides/installation/email-configuration
  - /enterprise/admin/articles/configuring-email
  - /enterprise/admin/articles/troubleshooting-email
  - /enterprise/admin/articles/email-configuration-and-troubleshooting
  - /enterprise/admin/user-management/configuring-email-for-notifications
  - /admin/configuration/configuring-email-for-notifications
versions:
  ghes: '*'
  ghae: '*'
type: how_to
topics:
  - Enterprise
  - Fundamentals
  - Infrastructure
  - Notifications
shortTitle: Configure email notifications
---

{% ifversion ghae %}
Enterprise オーナーは、通知用のメールを設定できます。
{% endif %}
## Enterprise 向けの SMTP を設定する

{% ifversion ghes %}
{% data reusables.enterprise_site_admin_settings.email-settings %}
4. **Enable email（メールの有効化）**を選択してください。 これでアウトバウンドとインバウンドのメールがどちらも有効化されますが、インバウンドのメールが動作するには[着信メールを許可する DNS とファイアウォールの設定](#configuring-dns-and-firewall-settings-to-allow-incoming-emails)に記述されているように DNS を設定する必要もあります。 ![アウトバウンドメールの有効化](/assets/images/enterprise/management-console/enable-outbound-email.png)
5. SMTP サーバーの設定を入力します。
      - [**Server address**] フィールドに SMTP サーバのアドレスを入力します。
      - [**Port**] フィールドには、SMTP サーバがメールを送信するのに使用するポートを入力します。
      - [**Domain**] フィールドには、SMTP サーバが HELO レスポンスを送信するドメイン名があれば入力してください。
      - [**Authentication**] ドロップダウンを選択し、SMTP サーバーで使用される暗号化の種類を選択します。
      - [**No-reply email address（No-replyメールアドレス）**] フィールドには、すべての通知メールの From および To フィールドに使うメールアドレスを入力してください。
6. no-replyメールアドレスへの着信メールをすべて破棄したい場合には、**Discard email addressed to the no-reply email address（no-replyメールアドレスへのメールの破棄）**を選択してください。 ![no-reply メールアドレス宛のメールを廃棄するチェックボックス](/assets/images/enterprise/management-console/discard-noreply-emails.png)
7. [**Support**] で、リンクの種類を選択してユーザに追加のサポートを提供します。
    - **Email:** An internal email address.
    - **URL:** A link to an internal support site. `http://` または `https://` を含める必要があります。 ![サポートのメールあるいは URL](/assets/images/enterprise/management-console/support-email-url.png)
8. [メール配信のテスト](#testing-email-delivery)。
{% elsif ghae %}
{% data reusables.enterprise-accounts.access-enterprise %}
{% data reusables.enterprise-accounts.settings-tab %}
{% data reusables.enterprise-accounts.email-tab %}
2. **Enable email（メールの有効化）**を選択してください。 ![メール設定の [Enable] チェックボックス](/assets/images/enterprise/configuration/ae-enable-email-configure.png)
3. メールサーバーの設定を入力します。
    - [**Server address**] フィールドに SMTP サーバのアドレスを入力します。
    - [**Port**] フィールドには、SMTP サーバがメールを送信するのに使用するポートを入力します。
    - [**Domain**] フィールドには、SMTP サーバが HELO レスポンスを送信するドメイン名があれば入力してください。
    - [**Authentication**] ドロップダウンを選択し、SMTP サーバーで使用される暗号化の種類を選択します。
    - [**No-reply email address（No-replyメールアドレス）**] フィールドには、すべての通知メールの From および To フィールドに使うメールアドレスを入力してください。
4. no-replyメールアドレスへの着信メールをすべて破棄したい場合には、**Discard email addressed to the no-reply email address（no-replyメールアドレスへのメールの破棄）**を選択してください。 ![メール設定の [Discard] チェックボックス](/assets/images/enterprise/configuration/ae-discard-email.png)
5. [**Test email settings**] をクリックします。 ![メール設定の [Test email settings] ボタン](/assets/images/enterprise/configuration/ae-test-email.png)
6. [Send test email to] で、テストメールを送信するメールアドレスを入力し、[**Send test email**] をクリックします。 ![メール設定の [Send test email] ボタン](/assets/images/enterprise/configuration/ae-send-test-email.png)
7. [**Save**] をクリックします。 ![Enterprise サポート連絡先設定の [Save] ボタン](/assets/images/enterprise/configuration/ae-save.png)
{% endif %}

{% ifversion ghes %}
## メール配信のテスト

1. **Email（メール）**セクションの上部で、**Test email settings（メール設定のテスト）**をクリックしてください。 ![メール設定のテスト](/assets/images/enterprise/management-console/test-email.png)
2. **Send test email to（テストメールの送信先）**フィールドに、テストメールを送信するアドレスを入力してください。 ![メールアドレスのテスト](/assets/images/enterprise/management-console/test-email-address.png)
3. **Send test email（テストメールの送信）**をクリックしてください。 ![テストメールの送信](/assets/images/enterprise/management-console/test-email-address-send.png)

  {% tip %}

  **Tip：**即時の配信失敗や送出メール設定のエラーなど、テストメールの送信時にSMTPエラーが生じたなら、それらはTest email settingsダイアログボックスに表示されます。

  {% endtip %}

4. テストメールが失敗したなら[メール設定のトラブルシューティング](#troubleshooting-email-delivery)をしてください。
5. テストメールが成功したなら、ページの下部で**Save settings（設定の保存）**をクリックしてください。 ![設定保存のボタン](/assets/images/enterprise/management-console/save-settings.png)
{% data reusables.enterprise_site_admin_settings.wait-for-configuration-run %}

{% ifversion require-tls-for-smtp %}
## Enforcing TLS for SMTP connections

You can enforce TLS encryption for all incoming SMTP connections, which can help satisfy an ISO-27017 certification requirement.

{% data reusables.enterprise_site_admin_settings.email-settings %}
1. Under "Authentication," select **Enforce TLS auth (recommended)**.

   ![Screenshot of the "Enforce TLS auth (recommended)" checkbox](/assets/images/enterprise/configuration/enforce-tls-for-smtp-checkbox.png)
{% data reusables.enterprise_management_console.save-settings %}
{% endif %}

## メール着信を許可する DNS とファイアウォールの設定

通知へのメールでの返信を許可したいなら、DNSを設定しなければなりません。

1. インスタンスのポート25がSMTPサーバにアクセスできることを確認してください。
2. `reply.[hostname]`を指すAレコードを作成してください。 DNSプロバイダとインスタンスのホスト設定によっては、 `*.[hostname]`を指す単一のAレコードを作成できる場合があります。
3. `reply.[hostname]`を指すMXレコードを作成して、このドメインへのメールがインスタンスにルーティングされるようにしてください。
4. `noreply.[hostname]` が `[hostname]` を指すようにする MX レコードを作成し、 通知メールの `cc` アドレスへの返信がインスタンスにルーティングされるようにしてください。 For more information, see {% ifversion ghes %}"[Configuring notifications](/github/managing-subscriptions-and-notifications-on-github/configuring-notifications){% else %}"[About email notifications](/github/receiving-notifications-about-activity-on-github/about-email-notifications){% endif %}."

## メール配信のトラブルシューティング

### Support Bundleの作成

If you cannot determine what is wrong from the displayed error message, you can download a [support bundle](/enterprise/admin/guides/enterprise-support/providing-data-to-github-support) containing the entire SMTP conversation between your mail server and {% data variables.product.prodname_ghe_server %}. Once you've downloaded and extracted the bundle, check the entries in *enterprise-manage-logs/unicorn.log* for the entire SMTP conversation log and any related errors.

unicornログは以下のようなトランザクションになっているはずです。

```shell
This is a test email generated from https://10.0.0.68/setup/settings
Connection opened: smtp.yourdomain.com:587
-> "220 smtp.yourdomain.com ESMTP nt3sm2942435pbc.14\r\n"
<- "EHLO yourdomain.com\r\n"
-> "250-smtp.yourdomain.com at your service, [1.2.3.4]\r\n"
-> "250-SIZE 35882577\r\n"
-> "250-8BITMIME\r\n"
-> "250-STARTTLS\r\n"
-> "250-ENHANCEDSTATUSCODES\r\n"
-> "250 PIPELINING\r\n"
<- "STARTTLS\r\n"
-> "220 2.0.0 Ready to start TLS\r\n"
TLS connection started
<- "EHLO yourdomain.com\r\n"
-> "250-smtp.yourdomain.com at your service, [1.2.3.4]\r\n"
-> "250-SIZE 35882577\r\n"
-> "250-8BITMIME\r\n"
-> "250-AUTH LOGIN PLAIN XOAUTH\r\n"
-> "250-ENHANCEDSTATUSCODES\r\n"
-> "250 PIPELINING\r\n"
<- "AUTH LOGIN\r\n"
-> "334 VXNlcm5hbWU6\r\n"
<- "dGhpc2lzbXlAYWRkcmVzcy5jb20=\r\n"
-> "334 UGFzc3dvcmQ6\r\n"
<- "aXRyZWFsbHl3YXM=\r\n"
-> "535-5.7.1 Username and Password not accepted. Learn more at\r\n"
-> "535 5.7.1 http://support.yourdomain.com/smtp/auth-not-accepted nt3sm2942435pbc.14\r\n"
```

このログからは、アプライアンスについて以下のことが分かります。

* SMTPサーバとのコネクションを開いている（`Connection opened: smtp.yourdomain.com:587`）。
* コネクションの作成には成功し、TLSの使用を選択している（`TLS connection started`）。
* `login`認証が実行されている（`<- "AUTH LOGIN\r\n"`）。
* SMTPサーバは、認証を不正として拒否している（`-> "535-5.7.1 Username and Password not accepted.`）。

### {% data variables.product.product_location %}ログのチェック

インバウンドのメールが機能していることを検証する必要がある場合、インスタンスの */var/log/mail.log* と */var/log/mail-replies/metroplex.log* との 2 つのログファイルを検証してください。

*/var/log/mail.log* verifies that messages are reaching your server. 以下は、成功したメールの返信の例です:

```
Oct 30 00:47:18 54-171-144-1 postfix/smtpd[13210]: connect from st11p06mm-asmtp002.mac.com[17.172.124.250]
Oct 30 00:47:19 54-171-144-1 postfix/smtpd[13210]: 51DC9163323: client=st11p06mm-asmtp002.mac.com[17.172.124.250]
Oct 30 00:47:19 54-171-144-1 postfix/cleanup[13216]: 51DC9163323: message-id=<b2b9c260-4aaa-4a93-acbb-0b2ddda68579@me.com>
Oct 30 00:47:19 54-171-144-1 postfix/qmgr[17250]: 51DC9163323: from=<tcook@icloud.com>, size=5048, nrcpt=1 (queue active)
Oct 30 00:47:19 54-171-144-1 postfix/virtual[13217]: 51DC9163323: to=<reply+i-1-1801beb4df676a79250d1e61e54ab763822c207d-5@reply.ghe.tjl2.co.ie>, relay=virtual, delay=0.12, delays=0.11/0/0/0, dsn=2.0.0, status=sent (delivered to maildir)
Oct 30 00:47:19 54-171-144-1 postfix/qmgr[17250]: 51DC9163323: removed
Oct 30 00:47:19 54-171-144-1 postfix/smtpd[13210]: disconnect from st11p06mm-asmtp002.mac.com[17.172.124.250]
```

クライアントがまず接続し、続いてキューがアクティブになっていることに注意してください。 そしてメッセージが配信され、クライアントがキューから削除され、セッションが切断されています。

*/var/log/mail-replies/metroplex.log* shows whether inbound emails are being processed to add to issues and pull requests as replies. 以下は成功したメッセージの例です:

```
[2014-10-30T00:47:23.306 INFO (5284) #] metroplex: processing <b2b9c260-4aaa-4a93-acbb-0b2ddda68579@me.com>
[2014-10-30T00:47:23.333 DEBUG (5284) #] Matched /data/user/mail/reply/new/1414630039.Vfc00I12000eM445784.ghe-tjl2-co-ie
[2014-10-30T00:47:23.334 DEBUG (5284) #] Moving /data/user/mail/reply/new/1414630039.Vfc00I12000eM445784.ghe-tjl2-co-ie => /data/user/incoming-mail/success
```

`metroplex` がインバウンドのメッセージをキャッチして処理し、ファイルを `/data/user/incoming-mail/success` に移動します。{% endif %}

### DNS設定の検証

インバウンドのメールを適切に処理するには、適切にAレコード（あるいはCNAME）と共にMXレコードを設定しなければなりません。 詳しい情報については、「[着信メールを許可するよう DNS およびファイアウォールを設定する](#configuring-dns-and-firewall-settings-to-allow-incoming-emails)」を参照してください。

### ファイアウォールあるいはAWSセキュリティグループの設定のチェック

If {% data variables.product.product_location %} is behind a firewall or is being served through an AWS Security Group, make sure port 25 is open to all mail servers that send emails to `reply@reply.[hostname]`.

### サポートへの連絡
{% ifversion ghes %}
依然として問題が解決できない場合は、{% data variables.contact.contact_ent_support %} に連絡してください。 問題のトラブルシューティングを支援するため、メールには`http(s)://[hostname]/setup/diagnostics`からの出力ファイルを添付してください。
{% elsif ghae %}
You can contact {% data variables.contact.github_support %} for help configuring email for notifications to be sent through your SMTP server. 詳しい情報については、「[{% data variables.contact.github_support %} からの支援を受ける](/admin/enterprise-support/receiving-help-from-github-support)」を参照してください。
{% endif %}
