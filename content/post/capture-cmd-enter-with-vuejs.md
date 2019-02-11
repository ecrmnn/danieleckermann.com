+++
title = "Capture cmd/command + enter events with Vue.js"
description = "Capture cmd/command + enter events with Vue.js"
date = "2016-03-01"
+++

> <a href="https://github.com/ecrmnn/meta-ctrl-enter" target="_blank">This post is getting old. Please use my Vue package to achieve this.</a>

Unlike Shift/Alt/Ctrl, Mac/Apple key is not considered as a modifier key.

If you try to capture this with ``@keyup`` in ``Vue`` it won't work.

But, if we change that to ``@keydown`` it does!

#### This won't work
```html
<div class="form-group">
	<strong>Title</strong>
	<input type="text" class="form-control" v-model="title"
		@keyup="save($event)">
</div>
```

#### This works!
```html
<div class="form-group">
	<strong>Title</strong>
	<input type="text" class="form-control" v-model="title"
		@keydown="save($event)">
</div>
```

Personally tested and implemented in ``Vue`` 1.0.24