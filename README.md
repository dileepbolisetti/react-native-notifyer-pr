### React Native Notifyer Pr

-----------------------

after removing view.prop types production bug in android..

thanks to the React Native Notifyer guy :)

Pure Javascript solution to display message views in your app, independently of routing or modals.

Lets you display **Toasts**, **Notifications** and **Loading indicators**, one at a time. If many messages are queued, they will be displayed in order, once the previous ones are hidden.

* Toast and notifications hide automatically after 5.5 seconds
* Loading indicators will not hide until you tell them to

## Usage

Install the package in your app project:

```bash
npm install react-native-notifyer-pr
```

Then, anywhere in your source code, import the functions you need:

```javascript
import {
	showToast,
	showNotification,
	showLoading,
	hideLoading,
	hide
} from 'react-native-notifyer-pr';
```

## Examples

### Loading

```javascript
showLoading("The content has been updated", "My App");

hideLoading(); // later on
```

![loading-full](./images/loading-full.png)

```javascript
showLoading("The content has been updated");

hideLoading(); // later on
```

![loading-mid](./images/loading-mid.png)

```javascript
showLoading()

hideLoading(); // later on
```

![loading-sm](./images/loading-sm.png)

### Notifications

```javascript
var id = showNotification("The content has been updated", "My App");
// var id = showNotification("The content has been updated", "My App", { duration: 10000, ... });

hide(id); // optional
```


![notification-full](./images/notification-full.png)

```javascript
var id = showNotification("The content has been updated");
// var id = showNotification("The content has been updated", { duration: 10000, ... });

hide(id); // optional
```

![notification-simple](./images/notification-simple.png)

### Toast

```
var id = showToast("The content has been updated");

hide(id); // optional
```

![toast](./images/toast.png)
