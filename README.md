# Readme

Localise app

```bash
ng build --prod --localize
```

Test locally using selected language

```bash
ng serve --configuration=de --port 4201
ng serve --configuration=fr --port 42012
```

Notes:

When creating a new language source file (*.XLF) it does not auto-add the `<target>` tag. e.g.:

```html
<source>Title with manual ID</source>
<target>french id</target>
```
