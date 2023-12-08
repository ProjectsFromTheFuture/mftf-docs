+++
title = 'bridges'
date = 2023-12-04T02:25:48+01:00
draft = true
weight = 1
linktitle = "Over bridges"
+++
Een bridge stelt je in staat berichten te ontvangen van, en te verzenden naar, je contacten bij andere communicatieplatformen in een applicatie die verbonden is met onze Matrixserver. Zo kun je al je communicatie onder één dak brengen.

## Beschikbaar op onze server

### {{% icon icon="fab fa-discord" %}} Discord

[{{% badge style="black" icon="fab fa-github" %}}GitHub{{% /badge %}}](https://github.com/mautrix/discord)
[{{% badge style="blue" icon="tag" %}}0.6.4{{% /badge %}}](https://github.com/mautrix/discord/releases/v0.6.4)

Gidslink

{{% button href="https://matrix.to/#/@discordbot:matrix.fromthefuture.nl" style="primary" icon="comment-medical" %}}discordbot{{% /button %}}

### {{% icon icon="fab fa-signal-messenger" %}} Signal

[{{% badge style="black" icon="fab fa-github" %}}GitHub{{% /badge %}}](https://github.com/mautrix/signalgo)
[{{%  badge style="orange" icon="tag" %}}0.1.0+dev.8f3f50eb{{% /badge %}}](https://github.com/mautrix/signalgo/commit/8f3f50eb87b0a81840e72c1e8b011d90b09af63d)

Gidslink

{{% button href="https://matrix.to/#/@signalbot:matrix.fromthefuture.nl" style="primary" icon="comment-medical" %}}signalbot{{% /button %}}

### {{% icon icon="fab fa-telegram" %}} Telegram

[{{% badge style="black" icon="fab fa-github" %}}GitHub{{% /badge %}}](https://github.com/mautrix/telegram)
[{{%  badge style="blue" icon="tag" %}}0.15.0{{% /badge %}}](https://github.com/mautrix/telegram/releases/tag/v0.15.0)

Gidslinks

{{% button href="https://matrix.to/#/@telegrambot:matrix.fromthefuture.nl" style="primary" icon="comment-medical" %}}telegrambot{{% /button %}}

### {{% icon icon="fab fa-whatsapp" %}} WhatsApp

[{{% badge style="black" icon="fab fa-github" %}}GitHub{{% /badge %}}](https://github.com/mautrix/whatsapp)
[{{%  badge style="orange" icon="tag" %}}0.10.4+dev.a8d19002{{% /badge %}}](https://github.com/mautrix/whatsapp/commit/a8d1900203cfe3d9b7158edfdddc81f2dc7ce4e0)

Gidslink

{{% button href="https://matrix.to/#/@whatsappbot:matrix.fromthefuture.nl" style="primary" icon="comment-medical" %}}whatsappbot{{% /button %}}

## Staat een app er niet bij?
Dan is het mogelijk dat er wel een bridge voor die app bestaat, maar dat die niet beschikbaar is gemaakt op onze server. Als je een app in gedachten hebt, kijk dan even of die ertussen staat in de [lijst](https://matrix.org/ecosystem/bridges/) van bestaande bridges, en geef je wens door aan een beheerder.

# Privacy
## Gebridgete berichten worden ontsleuteld

{{% notice warning "Let op" "exclamation-circle" %}}Om te functioneren moet de bridge je berichten kunnen ontsleutelen. Dit is een noodzakelijke tussenstap voor het aansluiten van twee platformen.{{% /notice %}}

De inhoud van je bericht is leesbaar voor de bridge waar je voor het leveren van dat bericht gebruik van maakt. Dit is noodzakelijk voor het functioneren van de bridge.

Wij hebben controle over de bridges; ze worden door ons gehost. Dat betekent dat het ontsleutelde bericht onze server niet verlaat. En door ons wordt er geen informatie bekeken of opgeslagen over de berichten die de bridges behandelen.

### Waarom is dat nodig?
Om dit te verklaren moeten we de reis van een bericht nader bekijken.

Al je berichten op matrix.fromthefuture.nl zijn versleuteld. Je berichten bij een ander platform kunnen ook versleuteld zijn als dat platform het ondersteunt.

Neem bijvoorbeeld WhatsApp, die gebruik maakt van standaard [end-to-end encryption](https://www.ibm.com/topics/end-to-end-encryption) om de inhoud van berichten te verbergen. Als je een bericht ontvangt van een WhatsAppcontact, dan komt deze versleuteld aan bij de bridge.

Deze wordt dan ontsleuteld—en dus leesbaar gemaakt—door de bridge. Dat kan de bridge doen omdat jij de bridge toegang verleent tot de sleutels waar je Whatsappaccount over beschikt. Je verleent meestal toegang door middel van het scannen van een QR-code. De bridge maakt hierbij gebruik van dezelfde methode waarop jij je WhatsAppcontacten kunt bereiken op [WhatsApp Web](https://web.whatsapp.com).

De bridge versleutelt het bericht opnieuw, maar dit keer met een sleutel verleend aan je matrix.fromthefuture.nl account.

Tenslotte stuurt de bridge het bericht door namens een "ghost" van je WhatsAppcontact naar de bestemde portal.

In het voorbeeld van hierboven is je Matrixaccount niet in staat om te beschikken over de sleutel waarmee je WhatsAppaccount berichten versleuteld

## Inherente kwetsbaarheden zijn onvermijdbaar 

{{% notice warning "Let op" "exclamation-circle" %}}Een gebridged bericht wordt blootgesteld aan de privacyzwaktes van het betrokken platform.{{% /notice %}}

Houd er rekening mee dat een bridge je niet kan beschermen tegen kwetsbaarheden van een communicatieplatform.

Stel dat je een bericht bridged naar een WhatsAppcontact. En dat dat contact een onversleutelde automatische chatbackup heeft geconfigureerd. Dan kan de bridge dat niet voorkomen. Lees dit [[WhatsApp Veilige Chat Back-up|artikel]] waarin wordt omschreven hoe je een veilige automatische chatbackup kunt maken in WhatsApp.

De bridges zijn bedoeld om je als gebruiker van onze Matrixserver je extra mogelijkheden in de applicatie te bieden. Het doel is al je communicatie onder één dak te faciliteren.