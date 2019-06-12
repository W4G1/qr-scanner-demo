## Vereisten

- Node.JS [v12.4.0]
- Android Studio

# Installatie

#### Vue CLI installeren (globaal)
```shell
npm install -g @vue/cli
```

#### Capacitor installeren (in het project)
```shell
npm install @capacitor/core
```
```shell
npm install -D @capacitor/cli
```

#### Ionic Native installeren (in het project)
```shell
npm install @ionic-native/core
```

#### Barcode-scanner plugin installeren
> De daadwerkelijke plugin.
```shell
npm install phonegap-plugin-barcodescanner
```
> Sugar-syntaxed wrapper van de plugin.
```shell
npm install @ionic-native/barcode-scanner
```

# Commando's

#### Android platform toevoegen
```shell
npx cap add android
```

#### Project bouwen
>Een wijziging in het project wordt pas doorgevoerd in de app nadat dit commando is uitgevoerd.
```shell
npm run build && npx cap sync
```

#### Project openen in Android Studio
```shell
npx cap open android
```

# Configuratie

> capacitor.config.json
```json
{
  "appId": "com.example.app",
  "appName": "QR-Scanner App",
  "bundledWebRuntime": false,
  "npmClient": "npm",
  "webDir": "dist"
}
```