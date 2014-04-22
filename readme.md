*This repository is a mirror of the [component](http://component.io) module [anthonyshort/raf-queue](http://github.com/anthonyshort/raf-queue). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/anthonyshort-raf-queue`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# raf-queue

Batch jobs to fire in the next frame using requestAnimationFrame.

## Installation

with component:

```
component install anthonyshort/raf-queue
```

with browserify and friends:

```
npm install raf-queue
```

## Usage

```js
var frame = require('raf-queue');

// Add jobs to the job, returns an id
var job = frame.add(increment);

// Remove jobs from the queue
frame.remove(job);

// Fires after the jobs from the next frame are done
frame.defer(function(){
  console.log('job done!');
});
```