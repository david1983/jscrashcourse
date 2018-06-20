### state management

State management can be done directly into react components, 

but when the application grows it becomes unmanageable

- The state needs to be passed down through props (aka: props drilling)
- Unrelated components needing the same state will cause more unnecessary props drilling
- The state can be changed by child components so there's not a single point to debug

