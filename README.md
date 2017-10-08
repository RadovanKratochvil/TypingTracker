#### Typing Tracker 

This is a JavaScript object that shows a progress bar indicating how much text has been entered into either an `input` or `textarea` tag. 


![](https://i.imgur.com/vCbWjkm.png)

#### Constructor usage:

	TypingTracker(id, maxCharsLength, event)
	
* id -- the id of either an `input` or `textarea` tag.	
* maxCharsLength -- the maximum number of characters allowed.
* event -- the event to attached the character counter event handler. The default is `keyup`.

#### Example:	

Given an `input` tag with the id of `title` and a `textarea` with the id of `seo-description`:

    let afterDocumentLoaded = () => {
		const MAX_SEO_DESC_LENGTH = 160;
    	const MAX_SEO_TITLE_LENGTH = 70;

		new rp.core.TypingTracker('seo-description', MAX_SEO_DESC_LENGTH)
    	new rp.core.TypingTracker('title', MAX_SEO_TITLE_LENGTH)	
	}

    rp.core.documentReady(afterDocumentLoaded);


#### Notes:

TypingTracker `adds` a `progress` tag and `span` tag immediately after the `input` or `textarea` tag. The `progress` tag shows typing progress with a progress bar and the `span` tag shows the remaining number of characters left. 

TypingTracker should be instanced after the document is fully loaded. You can use the `afterDocumentLoaded` function for this (also in this repository), jQuery's document ready function, or your own way to determine when the document is loaded and ready.

