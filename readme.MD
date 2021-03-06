## Init

```javascript
const u = new Util();
```

## Format

```javascript
console.log(u.format('Hi {0}. Did you see the {1}?', ['Pikachu', 'Meow']));
console.log(u.format('Hi {Pikachu}. Did you see the {Boss}?', {'Pokemon': 'Pikachu', 'Boss': 'Meow'}));
```

## Includes

```javascript
console.log(u.includes('Ali Baba', 'Baba'))
```

## Is Validation

```javascript 
console.log(u.is([1, 2, 3], u.Array));

console.log(u.is({'a': 'v'}, u.Object))

console.log(u.is(5.1, u.Integer));

console.log(u.is(3.2, u.Double));

console.log(u.is('Ali' + 123, u.String));

console.log(u.is(a = (d) => {}, u.Function));
console.log(u.is(function a (d) {}, u.Function));

console.log(u.is(class b {}, u.Class));

console.log(u.is('#button', 'visible'));

console.log(u.is("#chk", 'checked'));

console.log(u.is("#rdb", 'checked'));

let t = '';
let b = ' ';
console.log(u.is(t, u.Empty));

console.log(u.is(b, u.Blank));

let anElement = '';

console.log(u.is(anElement, u.Element));

anElement = document.querySelector("button");

console.log(u.is(anElement, u.Element));

console.log(u.is('goren.ali@yandex.com', u.Email));

console.log(u.is('tchİŞ@hotmaıl.com', u.Email));

console.log(u.is('tchİŞ@hotmaıl.', u.Email));

console.log(u.is('https://aligoren.com', u.Url));

console.log(u.is('ftp://github.com', u.Url));

console.log(u.is('http://localhost', u.Url));

console.log(u.is('www.google.com', u.Url));
```

## Count

**Word Count**:

```javascript
console.log(u.count('My name is no name when I do not like names. What is your name? Can u say your naming conversion', 'name'));
```

**Letter Count**:

```javascript
console.log(u.count('😚 You now I\'ll be happy', u.Letter));
```

**Array Count**:

```javascript
console.log(u.count([1, 2, 3], u.Array));
```

**Object Key Count**:

```javascript
console.log(u.count({'w': 't', 'w2': 't2', 'wf': 'wf', 'wfs': 'wfs2'}, u.Object));
```

## Url

**All**

Values: `['hash', 'host', 'hostname', 'href', 'origin', 'pathname', 'port', 'protocol', 'search']`

```javascript
console.log(u.url(null, true));
```

**Single**

```javascript
console.log(u.url('pathname'));
```

## Page

**Get Title**

```javascript
console.log(u.page('title'));
```

**Set Title**

```javascript
u.page('title', 'New Page title');
```

**Get Charset**

```javascript
console.log(u.page('charset'));
```

**Set Charset**

```javascript
console.log(u.page('charset', 'UTF-8'));
```

**Get Doc Type**

```javascript
console.log(u.page('doctype'));
```

**Get Location**

```javascript
console.log(u.page('location'));
```

**Set Location**

```javascript
console.log(u.page('location', 'https://www.google.com.tr'));
```

**Get Design Mode Status**

```javascript
console.log(u.page('design'));
```

**Set Design Mode Status**

Values must be `on` or `off`

```javascript
console.log(u.page('design', 'on'));
```

**Get Scripts Src**

```javascript
console.log(u.page('scripts'));
```

**Get Style Links**

```javascript
console.log(u.page('styles'));
```

**Get Document Referrer**

```javascript
console.log(u.page('referrer'));
```

**Get Modified Date**

```javascript
console.log(u.page('modified'));
```

## When

**Click etc. Events**

```javascript
u.when('button', 'click', (data) => {
    console.log(data.event);
    console.log(data.index);
    console.log(data.text);
    console.log(data.html);
});

u.when('document', 'click', (data) => {
    console.log(data.event);
    console.log(data.index);
    console.log(data.text);
    console.log(data.html);
});
```

**Page Load Events**

```javascript
u.when('document', 'DOMContentLoaded', (data) => {
    console.log(data); // from event
});

u.when('document', 'load', (data) => {
    console.log(data); // from event
});
```

## Where

```javascript
const arr = [
    {
        name: 'test',
        surname: 'test1'
    },
    {
        name: 'test23',
        surname: 'newsname'
    },
    {
        name: 'test23',
        surname: 'newsname'
    }
]

console.log(u.where(arr, 'surname', 'newsname'));
```