[@aiteq/messenger-bot](../README.md) > [ListTemplateMessageBuilder](../classes/listtemplatemessagebuilder.md)

# Class: ListTemplateMessageBuilder

Helps to create a [List Template](https://developers.facebook.com/docs/messenger-platform/send-api-reference/list-template) message.

## Hierarchy

[ButtonHoldingTemplateMessageBuilder](buttonholdingtemplatemessagebuilder.md)

**↳ ListTemplateMessageBuilder**

## Index

### Constructors

* [constructor()](listtemplatemessagebuilder.md#constructor)

### Methods

* [addCallButton(title, phoneNumber)](listtemplatemessagebuilder.md#addcallbutton)
* [addElement(elementBuilder)](listtemplatemessagebuilder.md#addelement)
* [addExtensionButton(title, extension, [options])](listtemplatemessagebuilder.md#addextensionbutton)
* [addLocationQuickReply()](listtemplatemessagebuilder.md#addlocationquickreply)
* [addLoginButton(url)](listtemplatemessagebuilder.md#addloginbutton)
* [addLogoutButton()](listtemplatemessagebuilder.md#addlogoutbutton)
* [addPostbackButton(title, id, [data])](listtemplatemessagebuilder.md#addpostbackbutton)
* [addQuickReply(title, id, [data, [imageUrl]])](listtemplatemessagebuilder.md#addquickreply)
* [addShareButton(builder)](listtemplatemessagebuilder.md#addsharebutton)
* [addUrlButton(title, url, [options])](listtemplatemessagebuilder.md#addurlbutton)
* [setTopElementStyle(topElementStyle)](listtemplatemessagebuilder.md#settopelementstyle)

---

## Constructors

<a id="constructor"></a>
### `new ListTemplateMessageBuilder()`

**Returns:** [ListTemplateMessageBuilder](listtemplatemessagebuilder.md)

---

## Methods

<a id="addcallbutton"></a>
### `addCallButton(title, phoneNumber)`

Creates and adds a [Call Button](https://developers.facebook.com/docs/messenger-platform/send-api-reference/call-button).

*Inherited from [ButtonHoldingTemplateMessageBuilder](../classes/buttonholdingtemplatemessagebuilder.md).*

**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| title | `string`   | title of the button, max length is 20 characters |
| phoneNumber | `string`   | phone number, format must have `"+"` prefix followed by the country code, area code and local number (e.g. +16505551234) |

**Returns:** `this` - for chaining
___

<a id="addelement"></a>
###  `addElement(elementBuilder)`

Adds an Element. Number of Elements must be 2-4.

**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| elementBuilder | [ElementBuilder](elementbuilder.md)   | |

**Returns:** `this` - for chaining
___

<a id="addextensionbutton"></a>
###  `addExtensionButton(title, extension, [options])`

Creates and adds a [URL Button](https://developers.facebook.com/docs/messenger-platform/send-api-reference/url-button) linking a Chat Extension.

*Inherited from [ButtonHoldingTemplateMessageBuilder](../classes/buttonholdingtemplatemessagebuilder.md).*

**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| title | `string`   | a title of the button, max length is 20 characters |
| extension | [ChatExtension](../classes/chatextension.md) | a Chat Extension to be opened when the button is tapped |
| options | `object` |  |

`options` object can contain:

| Property | Type | Description |
| ------ | ------ | ------ |
| webviewHeightRatio | [HeightRatio](../modules/webview.heightratio.md) | optional height of the [Webview](https://developers.facebook.com/docs/messenger-platform/send-api-reference/webview) |
| webviewShareButton | `boolean` | set to `false` to disable sharing in the Webview (e.g. for sensitive info) |
| fallbackUrl | `string`   | URL to use on clients that don't support [Messenger Extensions](https://developers.facebook.com/docs/messenger-platform/send-api-reference/webview) |

**Returns:** `this` - for chaining
___

<a id="addlocationquickreply"></a>
###  `addLocationQuickReply()`

*Inherited from [MessageBuilder](messagebuilder.md)*

Adds a Quick Reply button to quickly send user's location.

**Returns:** `this` - for chaining
___

<a id="addloginbutton"></a>
###  `addLoginButton(url)`

Creates and adds a [Login Button](https://developers.facebook.com/docs/messenger-platform/account-linking/link-account).

*Inherited from [ButtonHoldingTemplateMessageBuilder](../classes/buttonholdingtemplatemessagebuilder.md).*

**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| url | `string`   | authentication callback URL (must use HTTPS protocol) |

**Returns:** `this` - for chaining
___

<a id="addlogoutbutton"></a>
###  `addLogoutButton()`

Creates and adds a [Logout Button](https://developers.facebook.com/docs/messenger-platform/account-linking/unlink-account).

*Inherited from [ButtonHoldingTemplateMessageBuilder](../classes/buttonholdingtemplatemessagebuilder.md).*

**Returns:** `this` - for chaining
___

<a id="addpostbackbutton"></a>
###  `addPostbackButton(title, id, [data])`

Creates and adds a [Postback Button](https://developers.facebook.com/docs/messenger-platform/send-api-reference/postback-button).

*Inherited from [ButtonHoldingTemplateMessageBuilder](../classes/buttonholdingtemplatemessagebuilder.md).*

**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| title | `string`   | a title of the button, max length is 20 characters |
| id | `string` | an identification of the postback |
| data | `string` | optional data to be send with postback |

**Returns:** `this` - for chaining
___

<a id="addquickreply"></a>
###  `addQuickReply(title, id, [data, [imageUrl]])`

*Inherited from [MessageBuilder](messagebuilder.md)*

Adds a Quick Reply button to the message.

**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| title | `string` | title of the Quick Reply |
| id | `string` | ID of the button (required for proper generation of webhook events) |
| data | `any` | optional data to be send when the user click on the Quick Reply button |
| imageUrl | `string` | URL of optional image |

**Returns:** `this` - for chaining
___

<a id="addsharebutton"></a>
###  `addShareButton(builder)`

Creates and adds a [Share Button](https://developers.facebook.com/docs/messenger-platform/send-api-reference/share-button).

*Inherited from [ButtonHoldingTemplateMessageBuilder](../classes/buttonholdingtemplatemessagebuilder.md).*

**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| builder | [GenericTemplateMessageBuilder](../classes/generictemplatemessagebuilder.md) | a generic template message builder |

**Returns:** `this` - for chaining
___

<a id="addurlbutton"></a>
###  `addUrlButton(title, url, [options])`

Creates and adds a [URL Button](https://developers.facebook.com/docs/messenger-platform/send-api-reference/url-button).

*Inherited from [ButtonHoldingTemplateMessageBuilder](../classes/buttonholdingtemplatemessagebuilder.md).*

**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| title | `string`   | a title of the button, max length is 20 characters |
| url | `string` | a URL to be opened in a mobile browser when the button is tapped |
| options | `object` |  |

`options` object can contain:

| Property | Type | Description |
| ------ | ------ | ------ |
| webviewHeightRatio | [HeightRatio](../modules/webview.heightratio.md) | optional height of the [Webview](https://developers.facebook.com/docs/messenger-platform/send-api-reference/webview) |
| messengerExtensions | `boolean`   | must be `true` if using [Messenger Extensions](https://developers.facebook.com/docs/messenger-platform/send-api-reference/webview) |
| webviewShareButton | `boolean` | set to `false` to disable sharing in the Webview (e.g. for sensitive info) |
| fallbackUrl | `string`   | URL to use on clients that don't support [Messenger Extensions](https://developers.facebook.com/docs/messenger-platform/send-api-reference/webview) |

**Returns:** `this` - for chaining
___

<a id="settopelementstyle"></a>
###  `setTopElementStyle(topElementStyle)`

Sets a style for the first list item.

**Parameters:**

| Param | Type | Description |
| ------ | ------ | ------ |
| topElementStyle | [ListTopElementStyle](../modules/send.listtopelementstyle.md) | |

**Returns:** `this` - for chaining
