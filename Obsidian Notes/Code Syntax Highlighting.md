# Formatting
````
```ts
export function trimPathSuffix(fp: string): string {
  fp = clientSideSlug(fp)
  let [cleanPath, anchor] = fp.split("#", 2)
  anchor = anchor === undefined ? "" : "#" + anchor

  return cleanPath + anchor
}
```
````

```ts
export function trimPathSuffix(fp: string): string {
  fp = clientSideSlug(fp)
  let [cleanPath, anchor] = fp.split("#", 2)
  anchor = anchor === undefined ? "" : "#" + anchor
 
  return cleanPath + anchor
}
```

# Titles
This is more evident in the digital garden.
````
```js title="Example Content"

```
````

```js title="Example content"
export function trimPathSuffix(fp: string): string {
  fp = clientSideSlug(fp)
  let [cleanPath, anchor] = fp.split("#", 2)
  anchor = anchor === undefined ? "" : "#" + anchor
 
  return cleanPath + anchor
}
```

# Line Highlighting
This is more evident in the digital garden.
````
```js {1-3,4}

```
````

```js {1-3,4}
export function trimPathSuffix(fp: string): string {
  fp = clientSideSlug(fp)
  let [cleanPath, anchor] = fp.split("#", 2)
  anchor = anchor === undefined ? "" : "#" + anchor
 
  return cleanPath + anchor
}
```

# Word Highlighting
This is more evident in the digital garden.
````
```js /useState/
const [age, setAge] = useState(50);
const [name, setName] = useState('Taylor');
```
````

```
const [age, setAge] = useState(50)
const [name, setName] = useState("Taylor")
```

# Line Numbers
This is more evident in the digital garden.
````
```js showLineNumbers{number}

```
````

```js showLineNumbers{number}
export function trimPathSuffix(fp: string): string {
  fp = clientSideSlug(fp)
  let [cleanPath, anchor] = fp.split("#", 2)
  anchor = anchor === undefined ? "" : "#" + anchor
 
  return cleanPath + anchor
}
```
