## intro

Javascript utilities functions and methods for browser and nodejs to 10x faster developer experience

> Fast, generic JavaScript browser and some nodejs utility functions.

Install with [npm](https://www.npmjs.com/)

## Install

```sh
npm i utilities-functions
```

## Overview

<!-- START -->

- [clipboard](#clipboard) JavaScript clipboard function browser
- [convert](#convert) convert utility string number etc.
- [cookies](#cookies) This cookies only works client side javascript
- [datetime](#datetime) convience function to convert date and time
- [detection](#detection) detection device theme scheme and browser information
- [exportion](#exportion) export pdt or doc file with client side javascript
- [generate](#generate) generate random number uuid and much more
- [storage](#storage) browser local storage or session management
- [str](#str) string utilies capitalize and firrsuppercase letters
- [types](#types) we also have typescript support for types safety
- [url](#url) manage url to string and string to url is very convenient
- [validation](#validation) validate client side email, number ete.
- [author](#author) project author details and github page
- [license](#license) license

<!--FINISHED-->

## Usage

## clipboard

**copyImageToClipboard**

```js
import { copyImageToClipboard } from "utilities-functions/clipboard";

//copy image to clipboard
const imageUrl = "path/to/image";

copyImageToClipboard(imageUrl);
//will return blob
```

**imageToBlob**

```js
import { imageToBlob } from "utilities-functions/clipboard";

const imageUrl = "path/to/image";

imageToBlob(imageUrl);
//will return blob
```

**toClipboard or copyToClipboard**

```js
import { toClipboard } from "utilities-functions/clipboard";

//copy text to clipboard
toClipboard("hello world");
```

## convert

**formatPrice**

```js
import { formatPrice } from "utilities-functions/convert";

//formate the prite for payment gateway : stipe or anything else
formatPrice(20.3);
```

**currencyToSymbol**

```js
import { currencyToSymbol } from "utilities-functions/convert";

//Currency to symbol
currencyToSymbol("USD");
//output: $
```

**objectToStr**

```js
import { objectToStr } from "utilities-functions/convert";

objectToStr({ a: "hello", b: " world" });
// will return string { a: "hello", b: " world" }
```

**errorToString**

```js
import { errorToString } from "utilities-functions/convert";

errorToString("any errors like: object or string");
//I will return only string
```

[Our online rgb to hex tool](https://appsaeed.github.io/ftools/rgb-to-hex)
**rgbToHex | hexToRgb**

```js
import { rgbToHex } from "utilities-functions/convert";
import { hexToRgb } from "utilities-functions/convert";

rgbToHex(10, 20, 100);
//I will return hex string: #0a1464

hexToRgb("#1a098b");
/*
 * will return hex object
 * @return { red: number, green: number, blue: number } or  null
 */
```

## cookies

**setCookie**

```js
import { setCookie } from "utilities-functions/cookies";

const cookieName = "cookie-name";
const cookieValue = "value";
const cookieDays = 30;
const cookiePath = ""; // optional

setCookie(cookieName, cookieValue, cookieDays);
```

**getCookie | hasCookie**

```js
import { getCookie } from "utilities-functions/cookies";
import { hasCookie } from "utilities-functions/cookies";

const cookieName = "cookie-name";

getCookie(cookieName);

hasCookie(cookieName); // reurn true or false;
```

## datetime

```js
import { dbTodate } from "utilities-functions/datetime";
import { dbTotime } from "utilities-functions/datetime";

dbTodate("2023-03-28 20:04:10");
// output: Mar 28, 23

dbTotime("2023-03-28 20:04:10");
// output: 08:04 PM
```

## detection

```js
import { isDark } from "utilities-functions/detection";
import { deviceTheme } from "utilities-functions/detection";

isDark(); // will return true or false

deviceTheme(); // will return dark or light
```

## exportion

```js
import { exportTopdf } from "utilities-functions/exportion";
import { exportToDocs } from "utilities-functions/exportion";

exportTopdf("filename", "dat content", options); //options is optional

exportToDocs("filename", "dat content");
```

## generate

```js
import { uuid } from "utilities-functions/generate";
import { uuidv1 } from "utilities-functions/generate";
import { uuidv4 } from "utilities-functions/generate";
import { avatar } from "utilities-functions/generate";

uuid(); //will return string unique uuid

uuidv1(); //will return string unique uuidv1

uuidv4(); //will return string unique uuidv4

avatar("name"); //will return avatar url by first latter
```

## storage

**Session storage**

```js
import {
  getSession,
  setSession,
  removeSession,
} from "utilities-functions/storage";

setSession("sessionName", "session data  with any data type");

getSession("sessionName");
// I will return session data with as some format data was saved

removeSession("sessionName");
// The session is removed
```

**localStorage**

```js
import { setLocalStorage } from "utilities-functions/storage";

setLocalStorage("storageName", "session data  with any data type");

getLocalStorage("sessionName");
// I will return local storage data with as some format data was saved
```

**themeStorage**

```js
import { setThemeStore } from "utilities-functions/storage";
import { getThemeStore } from "utilities-functions/storage";

setThemeStore("dark");

getThemeStore(); // output: dark
```

## str

```js
import { capitalize, firstUpper } from "utilities-functions/str";

capitalize("hello world"); // output: Hello world

firstUpper("hello world"); // output: Hello world
```

## url

**toSeoUrl**

```js
import { toSeoUrl } from "utilities-functions/url";

toSeoUrl("Hello: I am javascript");
//output: hello-i-am-javascript
```

**seoToString**

```js
import { seoToString } from "utilities-functions/url";

seoToString("hello-iam-javascript");
//output: hello i am javascript
```

**urlToString**

```js
import { urlToString } from "utilities-functions/url";

urlToString("hello-iam-javascript");
//output: hello i am javascript
```

**adslash**

```js
import { adslash } from "utilities-functions/url";

adslash("hello-iam-javascript");
//output: hello i am javascript
```

**unslash**

```js
import { unslash } from "utilities-functions/url";

unslash("hello-iam-javascript");
//output: hello i am javascript
```

## validation

```js
import { isMail, isPhoneNumber } from "utilities-functions/validation";

isMail("yourmail@domain.com"); // true or false

isPhoneNumber("abc10832749"); // false

isPhoneNumber("10986499204"); // true
```

## Typescript

## types (pre-defined types for typescript)

RangeOf(strint number and end numbe)

```ts
import { FileExtensions, FileOpenInfo } from "utilities-functions/types/files";

export type FileOpenInfo = {
  name: string;
  data: string;
  extension: FileExtensions;
};
//some more types will come sooner
```

```ts
import { ThemeType } from "utilities-functions/types/themes";
import { setThemeStore } from "utilities-functions/storage";

const theme: ThemeType = "light";

setThemeStore(theme);
```

## Author

**Saeed**

- [github/appsaeed](https://github.com/appsaeed)
- [email](appsaeed7@gmail.com)

## License

Copyright © 2023 appsaeed

[MIT](LICENSE)
