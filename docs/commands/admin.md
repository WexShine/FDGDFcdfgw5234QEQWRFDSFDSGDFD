# ⚙ Admin

{% hint style="danger" %}
Это команда для тех, кто имеет **MANAGE\_SERVER** пермишион
{% endhint %}

### Set Prefix

* **Описание**: Установить префикс бота
* **Использование**: `!setprefix <newPrefix>`

### Automod Configuration

|                                              |                                                                |
| -------------------------------------------- | -------------------------------------------------------------- |
| **!lotusbotconfig status**                    | view configuration status                                      |
| **!lotusbotconfig strikes \<amount>**         | Set the maximum number of strikes before taking an action      |
| **!lotusbotconfig action \<kick\|mute\|ban>** | Set the action to be performed after receiving maximum strikes |
| **!lotusbotconfig debug \<on\|off>**          | turns on lotusbot for messages sent by admins and moderators    |

{% hint style="info" %}
By default, Auto moderation events are ignored for members who have the following permissions since they are assumed to be channel/server moderators

**KICK\_MEMBERS**, **BAN\_MEMBERS**, **MANAGE\_GUILD**, **MANAGE\_MESSAGES**

`!lotusbotconfig debug on` disables this
{% endhint %}

### Automod Events

| Name                                   | Description                                                                 |
| -------------------------------------- | --------------------------------------------------------------------------- |
| **!lotusbot antighostping \<on\|off>**  | Logs ghost mentions in your server (Requires `/modlog` channel to be setup) |
| **!lotusbot antiinvites \<on\|off>**    | Allow or disallow sending discord invites in message                        |
| **!lotusbot antilinks \<on\|off>**      | Allow or disallow sending links in message                                  |
| **!lotusbot antiscam \<on\|off>**       | Enable or disable antiscam detection                                        |
| **!lotusbot maxlines \<amount>**        | Sets maximum lines allowed per message                                      |
| **!lotusbot maxmentions \<amount>**     | Sets maximum user mentions allowed per message                              |
| **!lotusbot maxrolementions \<amount>** | Sets maximum role mentions allowed per message                              |

{% hint style="warning" %}
Each time a member tries to break the automated rule, he/she **receives a strike**. After receiving the maximum number of strikes (default 5), the moderation action (default MUTE) is performed on them
{% endhint %}

### Counter Channels

* ** Описание: ** настройка встречного канала в гильдии
* **Использование**: `!счетчик <тип счетчика> <имя>`
* **Доступные счетчики** **типы**
  * ПОЛЬЗОВАТЕЛИ: подсчитывает общее количество участников сервера (участники + боты)
  * УЧАСТНИКИ: подсчитывает общее количество участников.
  * БОТЫ: подсчитывает общее количество ботов

### Max Warn

* **!maxwarn limit \<amount>**: Установить лимит варнов
* **!maxwarn action \<mute|kick|ban>**: Установить действие после получения <amount> варнов

### Flag Translations

_Enabling эта функция позволит пользователям просто реагировать на любое сообщение с помощью эмодзи с флагом страны, переводя содержимое этого сообщения на региональный язык_

* **Описание**: Настроить язык бота LotusMine
* **Использование**: `!flagtr <on|off>`

![](../.gitbook/assets/image.png)

### Moderation Logging

* **Описание**: Включить/выключить систему логов для администрации
* **Использование**: `!modlog <channel|off>`

{% hint style="info" %}
Ведение журнала модерации включить ведение журнала всех **moderation actions** и **lotusbot events**
{% endhint %}

### Mute Setup

* **Описание**: Установить систему мутов
* **Использование**: `!mutesetup`

### XP System

* **Описание**: Включить/выключить систему рангов
* **Использование**: `!xpsystem <on|off>`

### Greeting

{% tabs %}
{% tab title="Welcome" %}
**!welcome status \<on|off>**

* Включить или выключить приветсвие бота

**!welcome channel <#channel>**

* Выбор где будет отправляться приветсвие бота

**!welcome preview**

* Посмотреть превью приветсвия бота

**!welcome desc \<content>**

* установить описание для встраивания приветствия

**!welcome footer \<content>**

* установите нижний колонтитул для встраивания приветствия

**!welcome thumbnail \<on|off>**

* включить или отключить миниатюру приветственного сообщения

**!welcome color <#hex>**

* установите цвет вставки приветствия
{% endtab %}

{% tab title="Farewell" %}
**!farewell status \<on|off>**

* Включить или отключить прощальное сообщение

**!farewell channel <#channel>**

* настройте канал, по которому должны отправляться прощальные сообщения

**!farewell preview**

* отправить прощальный предварительный просмотр

**!farewell desc \<content>**

* установить описание для встраивания

**!farewell footer \<content>**

* установите нижний колонтитул для встраивания

**!farewell thumbnail \<on|off>**

* включить или отключить миниатюру прощального сообщения

**!farewell color <#hex>**

* set farewell embed color
{% endtab %}
{% endtabs %}

{% hint style="success" %}
#### Allowed Content Replacements

* \n : Новая строка&#x20;
* {server} : Название сервера&#x20;
* {count} : Число участников на сервере#x20;
* {member:name} : Имя участника&#x20;
* {member:tag} : Member Tag&#x20;
* {inviter:name} : Имя пригласившего&#x20;
* {inviter:tag} : Тег пригласившего&#x20;
* {invites} : Приглашения
{% endhint %}

### Reaction Roles

#### Create Reaction Role

* **Использование**: !addrr <#channel> \<messageId> \<role> \<emote>
* **Описание**: Установить реакцию на роль

#### Remove Reaction Roles

* **Использование**: !removerr <#channel> \<messageId>
* **Описание**: Убрать реакцию на роль

### Ticketing

**Configuration**

* **!ticket setup**: настройка нового сообщения о тикете
* **!ticket log <#channel>**: настройка канала журнала для тикеты
* **!ticket limit \<amount>**: установить максимальное количество одновременно открытых тикеты
* **!ticket closeall**: закрыть все открытые тикеты

#### Ticket Channel Commands

* **!ticket add \<userId|roleId>**: добавление пользователя/роли в тикет
* **!ticket remove \<userId|roleId>**: удалить пользователя/роль из заявки