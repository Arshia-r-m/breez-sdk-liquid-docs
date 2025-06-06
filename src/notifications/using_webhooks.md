# Using Webhooks

<h2 id="registering-a-webhook">
    <a class="header" href="#registering-a-webhook">Registering a Webhook</a>
    <a class="tag" target="_blank" href="https://breez.github.io/breez-sdk-liquid/breez_sdk_liquid/sdk/struct.LiquidSdk.html#method.register_webhook">API docs</a>
</h2>

Once your vendor [NDS is set up](setup_nds.md) and can accept POST requests from the SDK services, you can register the webhook URL within your main application by calling the register webhook API as follows

<custom-tabs category="lang">
<div slot="title">Rust</div>
<section>

```rust,ignore
{{#include ../../snippets/rust/src/webhook.rs:register-webook}}
```
</section>

<div slot="title">Swift</div>
<section>

```swift,ignore
{{#include ../../snippets/swift/BreezSDKExamples/Sources/Webhook.swift:register-webook}}
```
</section>

<div slot="title">Kotlin</div>
<section>

```kotlin,ignore
{{#include ../../snippets/kotlin_mpp_lib/shared/src/commonMain/kotlin/com/example/kotlinmpplib/Webhook.kt:register-webook}}
```
</section>

<div slot="title">Javascript</div>
<section>

```typescript
{{#include ../../snippets/wasm/webhook.ts:register-webook}}
```
</section>

<div slot="title">React Native</div>
<section>

```typescript
{{#include ../../snippets/react-native/webhook.ts:register-webook}}
```
</section>

<div slot="title">Dart</div>
<section>

```dart,ignore
{{#include ../../snippets/dart_snippets/lib/webhook.dart:register-webook}}
```
</section>

<div slot="title">Python</div>
<section>

```python,ignore 
{{#include ../../snippets/python/src/webhook.py:register-webook}}
```
</section>

<div slot="title">Go</div>
<section>

```go,ignore
{{#include ../../snippets/go/webhook.go:register-webook}}
```
</section>

<div slot="title">C#</div>
<section>

```cs,ignore
{{#include ../../snippets/csharp/Webhook.cs:register-webook}}
```
</section>
</custom-tabs>

When the NDS receives a POST request for the registered webhook URL, it will forward the request data via push notification to the applications Service Extension (iOS) or Foreground Service (Android) to be handled by the [Notification Plugin](setup_plugin.md).

<h2 id="unregistering-a-webhook">
    <a class="header" href="#unregistering-a-webhook">Unregistering a Webhook</a>
    <a class="tag" target="_blank" href="https://breez.github.io/breez-sdk-liquid/breez_sdk_liquid/sdk/struct.LiquidSdk.html#method.unregister_webhook">API docs</a>
</h2>

When a webhook is no longer needed you can unregister the webhook as follows:

<custom-tabs category="lang">
<div slot="title">Rust</div>
<section>

```rust,ignore
{{#include ../../snippets/rust/src/webhook.rs:unregister-webook}}
```
</section>

<div slot="title">Swift</div>
<section>

```swift,ignore
{{#include ../../snippets/swift/BreezSDKExamples/Sources/Webhook.swift:unregister-webook}}
```
</section>

<div slot="title">Kotlin</div>
<section>

```kotlin,ignore
{{#include ../../snippets/kotlin_mpp_lib/shared/src/commonMain/kotlin/com/example/kotlinmpplib/Webhook.kt:unregister-webook}}
```
</section>

<div slot="title">Javascript</div>
<section>

```typescript
{{#include ../../snippets/wasm/webhook.ts:unregister-webook}}
```
</section>

<div slot="title">React Native</div>
<section>

```typescript
{{#include ../../snippets/react-native/webhook.ts:unregister-webook}}
```
</section>

<div slot="title">Dart</div>
<section>

```dart,ignore
{{#include ../../snippets/dart_snippets/lib/webhook.dart:unregister-webook}}
```
</section>

<div slot="title">Python</div>
<section>

```python,ignore 
{{#include ../../snippets/python/src/webhook.py:unregister-webook}}
```
</section>

<div slot="title">Go</div>
<section>

```go,ignore
{{#include ../../snippets/go/webhook.go:unregister-webook}}
```
</section>

<div slot="title">C#</div>
<section>

```cs,ignore
{{#include ../../snippets/csharp/Webhook.cs:unregister-webook}}
```
</section>
</custom-tabs>
<div class="warning">
<h4>Developer note</h4>
Any payments that use a swap service will use the same registered webhook URL until the swap is complete.
</div>
