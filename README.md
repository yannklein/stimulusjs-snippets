# StimulusJS Snippets for VS code
A very simple set of snippets to simplify your StimulusJS dev life.

## Kudos to:
- [Nejdet Kadir Bektaş](https://github.com/nejdetkadir) for adding the Hotwire dedicated snippets

## Available snippets
So far, that's all we provide:

- `sc`: creates a StimulusJS controller template for Webpack

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

- `si`: StimulusJS Initialization for Webpack

Generates: 

```
import { Application } from "stimulus"
import { definitionsFromContext } from "stimulus/webpack-helpers"

// init for Stimulus
const application = Application.start()
const context = require.context("./controllers", true, /\.js$/)
application.load(definitionsFromContext(context))
```

- `sch`: creates a StimulusJS controller template for Ruby on Rails with hotwire

Generates: 

```
import { Controller } from '@hotwired/stimulus'

export default class extends Controller {
  // static targets = [ 'test' ]
  
  connect() {
    console.log('Hello from my_controller.js')
  // console.log(this.testTarget)
  }
}
```


- `sih`: StimulusJS Initialization for for Ruby on Rails with hotwire

Generates: 

```
import { Application } from "@hotwired/stimulus"
import { definitionsFromContext } from "@hotwired/stimulus-webpack-helpers"

window.Stimulus = Application.start()
const context = require.context("./controllers", true, /\.js$/)
Stimulus.load(definitionsFromContext(context))
```