---
title: Diseño y Documentación
short-title: DisenoyDocs
description: The landing page for design and documentation.
---

{% for card in site.data.docs_cards -%}
  {% capture index0Modulo3 %}{{ forloop.index0 | modulo:3 }}{% endcapture %}
  {% capture indexModulo3 %}{{ forloop.index | modulo:3 }}{% endcapture %}
  {% if index0Modulo3 == '0' %}
  <div class="card-deck mb-4">
  {% endif %}
    <a class="card" href="{{card.url}}">
      <div class="card-body">
        <header class="card-title">{{card.name}}</header>
        <p class="card-text">{{card.description}}</p>
      </div>
    </a>
  {% if indexModulo3 == '0' %}
  </div>
  {% endif %}
{% endfor -%}

<a name="latest-release"></a>
## What's new on this site

To see changes to the site since our last release,
see the [What's new archive][].

## New to Flutter?

Once you've gone through [Get started][],
including [Write your first Flutter app][],
here are some next steps.

### Docs

Coming from another platform? Check out:
[Android][], [iOS][], [Web][], [React Native][],
[Xamarin.Forms][]

[Building layouts][]
: Learn how to create layouts in Flutter,
  where everything is a widget.

[Understanding constraints][]
: Once you understand that "Constraints
  flow up. Sizes flow down. Parents set
  positions", then you are well on your
  way to understanding Flutter's layout model.

[Adding interactivity to your Flutter app][]
: Learn how to add a stateful widget to your app.

[A tour of the Flutter widget framework][]
: Learn more about Flutter's react-style framework.

[FAQ][]
: Get the answers to frequently asked questions.

[A tour of the Flutter widget framework]: /docs/development/ui/widgets-intro
[Adding interactivity to your Flutter app]: /docs/development/ui/interactive
[Android]: /docs/get-started/flutter-for/android-devs
[Building layouts]: /docs/development/ui/layout
[FAQ]: /docs/resources/faq
[flutter-announce]: https://groups.google.com/forum/#!forum/flutter-announce
[Get started]: /docs/get-started/install
[iOS]: /docs/get-started/flutter-for/ios-devs
[React Native]: /docs/get-started/flutter-for/react-native-devs
[Understanding constraints]: /docs/development/ui/layout/constraints
[Web]: /docs/get-started/flutter-for/web-devs
[What's new archive]: /docs/whats-new-archive
[Write your first Flutter app]: /docs/get-started/codelab
[Xamarin.Forms]: /docs/get-started/flutter-for/xamarin-forms-devs

