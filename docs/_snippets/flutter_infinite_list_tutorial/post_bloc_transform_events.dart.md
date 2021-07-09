```dart
@override
Stream<Transition<PostEvent, PostState>> transformEvents(
  Stream<PostEvent> events,
  TransitionFunction<PostEvent, PostState> transitionFn,
) {
  return super.transformEvents(
    events.throttleTime(const Duration(milliseconds: 500)),
    transitionFn,
  );
}
```
