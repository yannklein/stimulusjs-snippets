# StimulusJS Snippets for VS code
A very simple set of snippets to simplify your StimulusJS dev life.

## Available snippets
So far, that's all we provide:

- `sjc`: creates a StimulusJS controller template

Generates:

```
import { Controller } from 'stimulus'

export default class extends Controller {
  // static targets = [ 'test' ]

  connect() {
    console.log('Hello from my_controller.js')
  // console.log(this.testTarget)
  }
}
```

- `sjw`: StimulusJS Initialization for Webpack

Generates: 

```
import { Application } from "stimulus"
import { definitionsFromContext } from "stimulus/webpack-helpers"

// init for Stimulus
const application = Application.start()
const context = require.context("./controllers", true, /\.js$/)
application.load(definitionsFromContext(context))
```

- `sjr`: StimulusJS Initialization for Ruby on Rails with hotwire

Generates: 

```
import { Controller } from '@hotwired/stimulus'

export default class extends Controller {
  connect() {

  }
}
```