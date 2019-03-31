## Conekta Flutter Tokenizer

This is a very small library that allows Flutter applications using [Conekta](https://www.conekta.com/) payments service, tokenize credit cards directly in flutter apps without any strange hack or weird implementation. Feel free to tweak anything that you feel is neccesary for the implementation or to fullfill your applications specific needs.

The implementation of this library was mostly after a reverse engineering process D:.

Hey but I needed to do this because at this moment: Sunday, March 31, 2019; there is not SDK for using in Flutter.

I discarded the [platform channel](https://flutter.dev/docs/development/platform-integration/platform-channels) approach in talking to the existing native Conekta iOS and Android SDKs. I wanted to implement a smoothly payment feature in Dart code without relying on device native function calls.

Having said that these are the requirements:

### **Requirements:**

1. Add the tokenizer relying dependencies to your `pubspec.yaml` file:
   - [device_info](https://pub.dartlang.org/packages/device_info)
   - [http](https://pub.dartlang.org/packages/http)
2. I created an `PaymentMethod` class to encapsulate all the properties of a payment method sent to the Conekta API. Feel free to provide your own implementation or pass just only a `Map<String, String>` to the `tokenizePaymentMethod()` and do the little neccesary modifications.
