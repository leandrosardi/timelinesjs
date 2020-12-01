# Timelines.Js
The **Timelines.Js** is a little HTML widget to show a timeline with notes, and some other features like:
1. add/remove notes at the client side using JavaScript;
2. show buttons on each note for edition, copying and removing it;
3. overload callback functions for custom code when the user clicks either the edition, copy or delete buttons.

You can find a [live example](https://expandedventure.com/timelinesjs/index.html) of **Timelines.Js** here: [https://expandedventure.com/timelinesjs/index.html](https://expandedventure.com/timelinesjs/index.html)


# Getting Started
Get started in 3 simple steps.

1. Download the required libraries and stylesheets.
All these files are included in this project. You can download them from this page.

2. Include them in the <header> section of your HTML page.

```html
<script src="./javascripts/commons-1.0.3.js" type="text/javascript"></script>
<script src="./javascripts/jquery-3.5.1.min.js" type="text/javascript"></script>
<script src="./javascripts/1.3.0/adminflare-demo-init.min.js" type="text/javascript"></script>
<link href="https://fonts.googleapis.com/css?family=Open+Sans:300italic,400italic,600italic,700italic,400,300,600,700" rel="stylesheet" type="text/css">	
<link href="./css/1.3.0/black-blue/bootstrap.min.css" media="all" rel="stylesheet" type="text/css" id="bootstrap-css">
<link href="./css/1.3.0/black-blue/adminflare.min.css" media="all" rel="stylesheet" type="text/css" id="adminflare-css">
<link href="./css/commons.css" media="all" rel="stylesheet" type="text/css" id="commons-css">
```

3. Create a nice timeline.

```html
<link rel="stylesheet" href="./timelines.css">
<script src="./timelines.min.js" type="text/javascript"></script>

<h1>The French Revolution's Timeline</h1>
<div id='myTimeline'> <!-- draw timeline here --> </div>

<script>
	ctx = $('#myTimeline');

	$(document).ready(function() {
		timelinesJs.draw( ctx );

		// 1789
		timelinesJs.addDot( ctx, {
			id: '1789-dot',
			left: true,
		});

		timelinesJs.addNote( ctx, '1789-dot', {
			id: '1789',
			html: '<b>July 14, 1789:</b> Parisian mobs storm the Bastille, and the French Revolution begins.',
		});

		// 1793
		timelinesJs.addDot( ctx, {
			id: '1793-dot',
			left: false,
		});

		timelinesJs.addNote( ctx, '1793-dot', {
			id: '1793',
			html: '<b>September 5, 1793:</b>  The Reign of Terror, the most radical period of the French Revolution, begins. At least 300,000 suspects are arrested; 17,000 are executed, and perhaps 10,000 die in prison or without trial.',
		});

		// 1795
		timelinesJs.addDot( ctx, {
			id: '1795-dot',
			left: true,
		});

		timelinesJs.addNote( ctx, '1795-dot', {
			id: '1795',
			html: '<b>SAugust 22–October 5, 1795::</b> The Convention of the French Republic creates a new constitution, establishing the Directory (a five-member committee) as the leaders of the French government. On October 5, in support of the Directory, Napoleon fires into a crowd of Royalists and defeats the anti-Republican forces that threaten the new government.',
		});

	});
	$('#remove').click(function() {
		timelinesJs.removeNote( ctx, 'invitation-messages', 'ABF1-guid');		
	});
</script>
```

# Features in Version 1.0.1
Here are listed each one of the features provided by **Timelines.Js**.

## Adding more than one note per dot.
Notes will be added one under the other.

```javascript
// 1789
timelinesJs.addDot( ctx, {
	id: '1789-dot',
	left: true,
});

timelinesJs.addNote( ctx, '1789-dot', {
	id: '1789',
	html: '<b>July 14, 1789:</b> Parisian mobs storm the Bastille, and the French Revolution begins.',
});

timelinesJs.addNote( ctx, '1789-dot', {
	id: '1789-2',
	html: 'Prison symbolizing power of Old Regime.',
});
```

## Placing notes in either the left or right side of the timeline.
Set the `left` parameter as `false` to show the dot's notes in the right side.

```javascript
// 1793
timelinesJs.addDot( ctx, {
	id: '1793-dot',
	left: false,
});
```

## Showing an 'add note' button.

## Adding a note.

## Removing a note.

## HTML vs Plain-Text notes.

## Adding an 'edit' button to a note.

## Adding a 'copy' button to a note.

## Adding a 'delete' button to a note.


# Functions in Version 1.0.1
Here are listed each one of the features provided by **Timelines.Js**.

## timelinesJs.version()
Returns the version of this **Templates.Js** library.



# Deployment 
The **Timelines.Js** requires the [**Commons.JS 1.0.3**](https://github.com/leandrosardi/commonsjs/), [**JQuery 3.5.1**](https://jquery.com/download/) and the ***AdminFlare 1.0.3** library used internally at [**ExpandedVenture**](https://expandedventure.com/expandedventure).

All the libraries are already included in this repository.

# Additional Notes
The **Timelines.Js** is used at [**ExpandedVenture**](https://expandedventure.com/expandedventure) to develop different UI/UX features.

The **Timelines.Js** library is just starting on Nov-2020, and more functions will be added as needed.

The **Timelines.Js** library has been written following the [**W3C JavaScript Best Practices**](https://www.w3.org/community/webed/wiki/JavaScript_best_practices).

# Disclaimer
Use at your own risk. The use of the software and scripts downloaded on this site is done at your own discretion and risk and with agreement that you will be solely responsible for any damage to any computer system or loss of data that results from such activities.

# Maintainer
Leandro Daniel Sardi <leandro((dot))sardi((@))expandedventure.com>