karma-jasmine-eventually
======================

A [Karma](http://karma-runner.github.io/) plugin to inject
[Jasmine-Eventually](https://github.com/dgrekov/jasmine_eventually) for
[Jasmine](http://jasmine.github.io/).

## Example karma.conf.js

All that's required is that `jasmine-eventually` appears after `jasmine` in your `frameworks` config.

```javascript
module.exports = function(config) {

  config.set({

    frameworks: [
      'jasmine',
      'jasmine-eventually'
    ],

    files: [
      'spec/**/*.spec.js'
    ],

    preprocessors: {
      'src/**/*.js': ['coverage']
    },

    reporters: [
      'progress',
      'coverage'
    ],

    coverageReporter: {
      type: 'html',
      dir: 'build/coverage/'
    }

  });

};
```