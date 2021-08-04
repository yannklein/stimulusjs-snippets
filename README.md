# StimulusJS Snippets for VS code
A very simple set of snippets to simplify your StimulusJS dev life.

## Available snippets
So far, that's all we provide:

- `sjc`: creates a StimulusJS controller template
Example:
```
import { Controller } from 'stimulus'

export default class extends Controller {
  static target = [ 'test' ]

  connect() {
    console.log('Hello from my_controller.js')
    console.log(this.testTarget)
  }
}
```