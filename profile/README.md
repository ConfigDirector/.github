# ConfigDirector

Remote configuration and feature flags with productivity and safety built in.

Every config has a type. Values can be validated against a JSON Schema before they are saved.
A flag that is live in production can be renamed without breaking the clients that read it.
Start free, no card: https://www.configdirector.com

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
| Swift (iOS, macOS, tvOS, watchOS) | [configdirector-swift-sdk](https://github.com/ConfigDirector/configdirector-swift-sdk) | [docs](https://docs.configdirector.com/sdks/mobile/swift) |
| Android (Kotlin, Java, Compose) | [android-sdk](https://github.com/ConfigDirector/android-sdk) | [docs](https://docs.configdirector.com/sdks/mobile/android) |
| Java | [java-sdks](https://github.com/ConfigDirector/java-sdks) | [docs](https://docs.configdirector.com/sdks/server/java) |
| .NET | [dotnet-sdks](https://github.com/ConfigDirector/dotnet-sdks) | [docs](https://docs.configdirector.com/sdks/server/dotnet) |
| Python | [python-server-sdk](https://github.com/ConfigDirector/python-server-sdk) | [docs](https://docs.configdirector.com/sdks/server/python) |
| Go | [go-sdks](https://github.com/ConfigDirector/go-sdks) | [docs](https://docs.configdirector.com/sdks/server/go) |
| PHP | [`configdirector/server-sdk`](https://github.com/ConfigDirector/php-sdks) | [docs](https://docs.configdirector.com/sdks/server/php) |

## OpenFeature

ConfigDirector ships an [OpenFeature](https://openfeature.dev) provider for each platform below,
so you can keep your code on the vendor-neutral API.

| Platform | Package | Docs |
| --- | --- | --- |
| Web | [`@configdirector/openfeature-web-provider`](https://github.com/ConfigDirector/js-sdks) | [docs](https://docs.configdirector.com/sdks/openfeature/web) |
| Node.js | [`@configdirector/openfeature-server-provider`](https://github.com/ConfigDirector/js-sdks) | [docs](https://docs.configdirector.com/sdks/openfeature/node-js) |
| Flutter (beta) | [`configdirector_openfeature_flutter_provider`](https://github.com/ConfigDirector/flutter-client-sdk) | [docs](https://docs.configdirector.com/sdks/openfeature/flutter) |
| Swift | [configdirector-swift-openfeature-provider](https://github.com/ConfigDirector/configdirector-swift-openfeature-provider) | [docs](https://docs.configdirector.com/sdks/openfeature/swift) |
| Android | [`com.configdirector:openfeature-android-provider`](https://github.com/ConfigDirector/android-sdk) | [docs](https://docs.configdirector.com/sdks/openfeature/android) |
| Java | [`com.configdirector:openfeature-server-provider`](https://github.com/ConfigDirector/java-sdks) | [docs](https://docs.configdirector.com/sdks/openfeature/java) |
| .NET | [`ConfigDirector.OpenFeature.ServerProvider`](https://github.com/ConfigDirector/dotnet-sdks) | [docs](https://docs.configdirector.com/sdks/openfeature/dotnet) |
| Python | [`configdirector-openfeature-server-provider`](https://github.com/ConfigDirector/python-server-sdk) | [docs](https://docs.configdirector.com/sdks/openfeature/python) |
| Go | [`github.com/ConfigDirector/go-sdks/configdirector-openfeature`](https://github.com/ConfigDirector/go-sdks) | [docs](https://docs.configdirector.com/sdks/openfeature/go) |
| PHP | [`configdirector/openfeature-server-provider`](https://github.com/ConfigDirector/php-sdks) | [docs](https://docs.configdirector.com/sdks/openfeature/php) |

## CLI

The [ConfigDirector CLI](https://github.com/ConfigDirector/cli) finds where your code reads each
config, fails the build when it reads a key that does not exist or has the wrong type, and manages
configs, targeting rules, and segments from the terminal.

```sh
npm install --global @configdirector/cli
```

Or with Homebrew: `brew install ConfigDirector/tap/configdirector`. The
[CLI docs](https://docs.configdirector.com/integrations/cli) cover sign-in and CI setup.

## GitHub Action

[ConfigDirector Code Scan](https://github.com/ConfigDirector/scan-code) runs the CLI in your
workflow. It fails the job when your code reads a config key that does not exist or has the wrong
type, and on pushes to your default branch it uploads where each config is read, so the dashboard
shows which code reads a config.

```yaml
steps:
  - uses: actions/checkout@v7
  - uses: ConfigDirector/scan-code@v1
    with:
      token: ${{ secrets.CONFIGDIRECTOR_TOKEN }}
```

The [CI docs](https://docs.configdirector.com/integrations/cli#run-it-in-ci) cover the token and
the full workflow.

## Agent skills

The [ConfigDirector agent skills](https://github.com/ConfigDirector/agent-skills) teach your coding
agent to add an SDK to your project, wrap a change in a feature flag, roll it out, and remove the
flag once it has settled. They are a pre-release and install into Claude Code, Cursor, Codex,
GitHub Copilot, Gemini CLI, and
[other agents](https://github.com/vercel-labs/skills#supported-agents).

```sh
npx skills add ConfigDirector/agent-skills
```

The [agent skills docs](https://docs.configdirector.com/integrations/agents) explain how the skills
reach your account and the safety rules they follow.

## Infrastructure as code

[terraform-provider-configdirector](https://github.com/ConfigDirector/terraform-provider-configdirector)
manages projects, environments, configs, and targeting rules from Terraform.

## Questions and help

[Discussions](https://github.com/orgs/ConfigDirector/discussions) is the place to ask questions
about any SDK, the dashboard, or the API, and to share what you are building. Bug reports go to
the issue tracker of the SDK's repository.

- [Documentation](https://docs.configdirector.com)
- [Quickstart](https://docs.configdirector.com/getting-started/quickstart)
- [Support](https://www.configdirector.com/support) for account and billing questions
- [@configdirector.com on Bluesky](https://bsky.app/profile/configdirector.com)
