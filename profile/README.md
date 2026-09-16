# ConfigDirector

Remote configuration and feature flags with productivity and safety built in.

Every config has a type. Values can be validated against a JSON Schema before they are saved.
A flag that is live in production can be renamed without breaking the clients that read it.
Start for free, no card needed: https://www.configdirector.com

## SDKs

| Platform | Package | Docs |
| --- | --- | --- |
| JavaScript (browser) | [`@configdirector/client-sdk`](https://github.com/ConfigDirector/js-sdks) | [docs](https://docs.configdirector.com/sdks/browser/javascript) |
| React | [`@configdirector/react-web-sdk`](https://github.com/ConfigDirector/js-sdks) | [docs](https://docs.configdirector.com/sdks/browser/react) |
| Vue | [`@configdirector/vue-sdk`](https://github.com/ConfigDirector/js-sdks) | [docs](https://docs.configdirector.com/sdks/browser/vue) |
| React Native | [`@configdirector/react-native-sdk`](https://github.com/ConfigDirector/js-sdks) | [docs](https://docs.configdirector.com/sdks/mobile/react-native) |
| Next.js | [`@configdirector/nextjs-sdk`](https://github.com/ConfigDirector/js-sdks) | [docs](https://docs.configdirector.com/sdks/meta/nextjs) |
| Nuxt | [`@configdirector/nuxt-sdk`](https://github.com/ConfigDirector/js-sdks) | [docs](https://docs.configdirector.com/sdks/meta/nuxt) |
| Node.js | [`@configdirector/server-sdk`](https://github.com/ConfigDirector/js-sdks) | [docs](https://docs.configdirector.com/sdks/server/node-js) |
| Flutter | [flutter-client-sdk](https://github.com/ConfigDirector/flutter-client-sdk) | [docs](https://docs.configdirector.com/sdks/mobile/flutter) |
| Swift (iOS, macOS, tvOS, watchOS) | [swift-sdk](https://github.com/ConfigDirector/swift-sdk) | [docs](https://docs.configdirector.com/sdks/mobile/swift) |
| Android (Kotlin, Java, Compose) | [android-sdk](https://github.com/ConfigDirector/android-sdk) | [docs](https://docs.configdirector.com/sdks/mobile/android) |
| Java | [java-sdks](https://github.com/ConfigDirector/java-sdks) | [docs](https://docs.configdirector.com/sdks/server/java) |
| .NET | [dotnet-sdks](https://github.com/ConfigDirector/dotnet-sdks) | [docs](https://docs.configdirector.com/sdks/server/dotnet) |
| Python | [python-server-sdk](https://github.com/ConfigDirector/python-server-sdk) | [docs](https://docs.configdirector.com/sdks/server/python) |

## OpenFeature

ConfigDirector ships [OpenFeature](https://openfeature.dev) providers for the
[web](https://docs.configdirector.com/sdks/browser/openfeature-web) and for
[Node.js](https://docs.configdirector.com/sdks/server/openfeature-node), so you can keep your
code on the vendor-neutral API.

## Infrastructure as code

[terraform-provider-configdirector](https://github.com/ConfigDirector/terraform-provider-configdirector)
manages projects, environments, configs, and targeting rules from Terraform.

## Get help

- [Documentation](https://docs.configdirector.com)
- [Quickstart](https://docs.configdirector.com/getting-started/quickstart)
- [Support](https://www.configdirector.com/support)
- [@configdirector.com on Bluesky](https://bsky.app/profile/configdirector.com)
