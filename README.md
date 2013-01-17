# jquery.emojify

Converts emoji text into images.

Helps you easily use any of the emoji on the [Emoji Cheat Sheet](http://www.emoji-cheat-sheet.com/) :smile:

## Usage

Simply select the element which contains the emoji text and run `emojify` on it:

```html
<div class="message">Hey check out my smile! :smile:</div>
<script>
	$('div.message').emojify({
		url: 'path/to/emoji'
	});
</script>
```

This will convert the contents of `div.message` to:

```html
Hey check out my smile! <img src="path/to/emoji/smile.png" />
```

You can specify any HTML attribute you like by passing an object as `attr` in the configuration (this just maps to `$().attr`):

```javascript
$('div.message').links({
	url: 'path/to/emoji',
	attr: {
		class: 'emoji'
	}
});
```