# BrightSolitaire Lite

> **This is the Lite version.** BrightSolitaire Lite is built only with Light's official SDK, so it can go in the Light Tool Library. It does less than the full app. For the full app, get [BrightSolitaire](https://github.com/gi-os/BrightSolitaire) ([on BrightMarket](https://brightmarket.gzl.dev/app/com.thelightphone.solitaire/)).

Klondike solitaire for the Light Phone III, built with the official LightOS SDK for the Light Tool Library.

Draw one, unlimited redeals. Your game saves when you leave the tool. It asks for no permissions and never uses the network.

## How this relates to BrightSolitaire

This is the same game as [gi-os/LightSolitaire](https://github.com/gi-os/LightSolitaire), the sideloaded build. The only differences are the tool id and the package name. The sideloaded build uses `com.thelightphone.solitaire`, which sits in Light's own namespace. A Tool Library tool needs an id of its own, so this one is `com.gios.brightsolitairelite`. Both can be installed side by side. Saved games do not carry over between them.

## Build

```sh
./gradlew -DlightSdk.toolOnly=true :tool:assembleDebug
```

The tool lives in `tool/`. Everything else is the upstream SDK, unchanged.

Built on [lightphone/light-sdk](https://github.com/lightphone/light-sdk) (MIT).
