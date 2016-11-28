# Writing Chrome Extensions


[Resources](https://developer.chrome.com/extensions/devguide)
[Getting started](https://developer.chrome.com/extensions/getstarted)



## Overview:

	### Tech:

		*	HTML, CSS: View;
		*	JavaScript: Logic/Control and GCE Framework API access.
		*	JSON: Manifest (info about extension, version for update, etc).

	### Packaging:

		*	An extension is a CRX file.
		*	A CRX file is a ZIP of the folder containing the extension files.
		*	Extension files consist of HTML, CSS, JavaScript, images, etc.
		*	Extensions are sandboxed but can communicate through messages.


	### Minimum Viable Extension:

		*	Files:

			*	popup.html: View. (what the user sees)
			*	script.js: Controller in MVC (app logic)
			*	manifest.json: (extension metadata: version, permissions, etc)
			*	icon.[png]/[ico]: 


			*	`manifest.json`:
				```json
					{
						"manifest_version": 1,
						"name": "MinViaEx",
						"description": "The most awesome extension ever",
						"version": "1",
						"browser_action": {
							"default_title": "YouKnowMyName",
							"default_icon": "icon.png",
							"default_popup": "popup.html"
						}
					}
				```

	### Extensions API	
		*	Can't *see* other extensions (sandboxed).
		*	Can *communicate* with other extensions messages.

## Getting Personal:

	### Interacting with extensions:

		*	Browser action
		*	Page action
		*	Context-Menu
		*	Omnibox
		*	Content UI.
		*	Shortcut

	### Script Types (different scopes):
	
		*	Event scripts
		*	Popup scripts
		*	Content scripts



## Mini goals:
	
	*	[DONE] Load extension that does nothing.
	*	Return current tab url:
		*	Needs tabs permissions in manifest.json
	*	Return current tabs urls (list).
	*	Send list or url to server.
	*	Display response from server.
	*	XMPP.
	*	WebRTC (communicate with another peer)