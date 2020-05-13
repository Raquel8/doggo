<!DOCTYPE html>
<html>

<head>
    <!--Required Meta Tags-->
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">
    <title>Home Page</title>
    <!--CSS File-->
    <link rel="stylesheet" href="resume.css">
    <link rel="stylesheet" href="resume.css">
    <!--Bootstrap Stylesheet-->
    <link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/css/bootstrap.min.css"
        integrity="sha384-Vkoo8x4CGsO3+Hhxv8T/Q5PaXtkKtu6ug5TOeNV6gBiFeWPGFN9MuhOf23Q9Ifjh" crossorigin="anonymous">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/animate.css/3.5.2/animate.min.css">
    <!-- FontAwesome -->
    <script src="https://kit.fontawesome.com/938a18ead6.js" crossorigin="anonymous"></script>
    <!--w3 schools-->
    <link rel="stylesheet" href="https://www.w3schools.com/w3css/4/w3.css">

    <link rel="apple-touch-icon" sizes="180x180" href="/apple-touch-icon.png">
    <link rel="icon" type="image/png" sizes="32x32" href="/favicon-32x32.png">
    <link rel="icon" type="image/png" sizes="16x16" href="/favicon-16x16.png">
    <link rel="manifest" href="/site.webmanifest">

</head>

<body id="toTop" data-spy="scroll" data-target="#toTop" data-offset="50">
    <!-- BS navbar -->
    <nav class="navbar navbar-expand-lg customNavBg">
        <a class="navbar-brand" href="index.html"><b>RELG</b></a>
        <button class="navbar-toggler" type="button" data-toggle="collapse" data-target="#customNavBg"
            aria-controls="navbarsExample09" aria-expanded="false" aria-label="Toggle navigation">
            <span class="navbar-toggler-icon">
                <svg aria-hidden="true" focusable="false" data-prefix="far" data-icon="bars" role="img"
                    xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"
                    class="svg-inline--fa fa-cheeseburger fa-w-16 fa-fw fa-lg">
                    <path fill="currentColor"
                        d="M352 176a16 16 0 1 0-16-16 16 16 0 0 0 16 16zm-96-32a16 16 0 1 0-16-16 16 16 0 0 0 16 16zm-96 32a16 16 0 1 0-16-16 16 16 0 0 0 16 16zm352 112a79.33 79.33 0 0 0-28.1-60.4 8.78 8.78 0 0 0 1.2-1.5 72.49 72.49 0 0 0 .6-75.4C442.3 78.7 352.19 32.1 256 32c-96.1.1-186.31 46.7-229.71 118.7a72.45 72.45 0 0 0 .6 75.4 15.76 15.76 0 0 0 1.2 1.5 79.35 79.35 0 0 0-9.3 111.8 78.09 78.09 0 0 0 15 13.7c-.7 2.8-1.7 5.5-1.7 8.5v34.7a83.73 83.73 0 0 0 83.7 83.7h280.6a83.8 83.8 0 0 0 83.71-83.7v-34.7c0-3-1.1-5.7-1.7-8.5A80 80 0 0 0 512 288zM67.37 175.5c34.9-57.9 109-95.4 188.61-95.5 79.71.1 153.81 37.6 188.72 95.5a24.51 24.51 0 0 1-.2 25.2c-2.9 4.7-7.41 7.4-12.21 7.4H79.67c-4.8 0-9.3-2.7-12.2-7.4a24.73 24.73 0 0 1-.1-25.2zM432 396.3a35.72 35.72 0 0 1-35.7 35.7H115.67A35.72 35.72 0 0 1 80 396.3v-25.6h352zm0-76.3H80a32 32 0 0 1 0-64h144l96 48 96-48h16a32 32 0 1 1 0 64z"
                        class="words"></path>
                </svg>
            </span>
        </button>
        <div class="collapse navbar-collapse" id="customNavBg">
            <ul class="navbar-nav mr-auto">
                <li class="nav-item">
                    <a class="nav-link" href="index.html">Home</a>
                </li>
                <li class="nav-item active">
                    <a class="nav-link" href="resume.html">Resume</a>
                </li>
                <li class="nav-item dropdown">
                    <a class="nav-link dropdown-toggle" href="#" data-toggle="dropdown" aria-haspopup="true"
                        aria-expanded="false">Contact</a>
                    <div class="dropdown-menu">
                        <a class="dropdown-item" href="mailto: lariosr29@hotmail.com">Email</a>
                        <a class="dropdown-item" href="https://github.com/raquel8" target="_blank">Github page</a>
                        <a class="dropdown-item" href="https://raquel8.github.io" target="_blank">VCD 5d website</a>
                    </div>
                </li>
            </ul>
            <form class="form-inline my-2 my-md-0">
                <input class="form-control" type="text" placeholder="Search" aria-label="Search">
            </form>
        </div>
    </nav>

    <!-- fixed footer -->
    <a href="index.html">
        <footer>
            <p>This is sticky footer</p>
        </footer>
    </a>


    <!--Resumae-->
   
</style>
<script id="applicationScript">
///////////////////////////////////////
// INITIALIZATION
///////////////////////////////////////

/**
 * Functionality for scaling, showing by media query, and navigation between multiple pages on a single page. 
 * Code subject to change.
 **/

if (window.console==null) { window["console"] = { log : function() {} } }; // some browsers do not set console

var Application = function() {
	// event constants
	this.NAVIGATION_CHANGE = "viewChange";
	this.VIEW_NOT_FOUND = "viewNotFound";
	this.VIEW_CHANGE = "viewChange";
	this.STATE_NOT_FOUND = "stateNotFound";
	this.APPLICATION_COMPLETE = "applicationComplete";
	this.APPLICATION_RESIZE = "applicationResize";
	this.SIZE_STATE_NAME = "data-is-view-scaled";

	this.lastView = null;
	this.lastState = null;
	this.lastOverlay = null;
	this.currentView = null;
	this.currentState = null;
	this.currentOverlay = null;
	this.currentQuery = {index: 0, rule: null, mediaText: null, id: null};
	this.inclusionQuery = "(min-width: 0px)";
	this.exclusionQuery = "none and (min-width: 99999px)";
	this.LastModifiedDateLabelName = "LastModifiedDateLabel";
	this.viewScaleSliderId = "ViewScaleSliderInput";
	this.pageRefreshedName = "showPageRefreshedNotification";
	this.prefix = "--web-";
	this.applicationStylesheet = null;
	this.mediaQueryDictionary = {};
	this.viewsDictionary = {};
	this.addedViews = [];
	this.views = {};
	this.viewIds = [];
	this.viewIds = [];
	this.viewQueries = {};
	this.overlays = {};
	this.overlayIds = [];
	this.numberOfViews = 0;
	this.verticalPadding = 0;
	this.horizontalPadding = 0;
	this.stateName = null;
	this.viewScale = 1;
	this.viewLeft = 0;
	this.viewTop = 0;

	// view settings
	this.showUpdateNotification = false;
	this.showNavigationControls = false;
	this.scaleViewsToFit = false;
	this.scaleToFitOnDoubleClick = false;
	this.actualSizeOnDoubleClick = false;
	this.scaleViewsOnResize = false;
	this.navigationOnKeypress = false;
	this.showViewName = false;
	this.enableDeepLinking = true;
	this.refreshPageForChanges = false;
	this.showRefreshNotifications = true;

	// view controls
	this.scaleViewSlider = null;
	this.lastModifiedLabel = null;
	this.supportsPopState = false; // window.history.pushState!=null;
	this.initialized = false;

	// refresh properties
	this.refreshDuration = 250;
	this.lastModifiedDate = null;
	this.refreshRequest = null;
	this.refreshInterval = null;
	this.refreshContent = null;
	this.refreshContentSize = null;
	this.refreshCheckContent = false;
	this.refreshCheckContentSize = false;

	var self = this;

	self.initialize = function(event) {
		var view = self.getVisibleView();
		if (view==null) view = self.getInitialView();
		self.collectViews();
		self.collectOverlays();
		self.collectMediaQueries();
		self.setViewOptions(view);
		self.setViewVariables(view);

		// sometimes the body size is 0 so we call this now and again later
		if (self.initialized) {
			window.addEventListener(self.NAVIGATION_CHANGE, self.viewChangeHandler);
			window.addEventListener("keyup", self.keypressHandler);
			window.addEventListener("keypress", self.keypressHandler);
			window.addEventListener("resize", self.resizeHandler);
			window.document.addEventListener("dblclick", self.doubleClickHandler);

			if (self.supportsPopState) {
				window.addEventListener('popstate', self.popStateHandler);
			}
			else {
				window.addEventListener('hashchange', self.hashChangeHandler);
			}

			// we are ready to go
			window.dispatchEvent(new Event(self.APPLICATION_COMPLETE));
		}

		if (self.initialized==false) {
			if (self.showNavigationControls || (self.singlePageApplication && self.showByMediaQuery==false)) {
				self.syncronizeViewToURL();
			}
	
			if (self.refreshPageForChanges) {
				self.setupRefreshForChanges();
			}
	
			self.initialized = true;
		}
		
		if (self.scaleViewsToFit) {
			self.viewScale = self.scaleViewToFit(view);
			
			if (self.viewScale<0) {
				setTimeout(self.scaleViewToFit, 500, view);
			}
		}
		else if (view) {
			self.viewScale = self.getViewScaleValue(view);
			self.centerView(view);
			self.updateSliderValue(self.viewScale);
		}
		else {
			// no view found
		}
	
		if (self.showUpdateNotification) {
			self.showNotification();
		}
	
		//"addEventListener" in window ? null : window.addEventListener = window.attachEvent;
		//"addEventListener" in document ? null : document.addEventListener = document.attachEvent;
	}


	///////////////////////////////////////
	// AUTO REFRESH 
	///////////////////////////////////////

	self.setupRefreshForChanges = function() {
		self.refreshRequest = new XMLHttpRequest();

		if (!self.refreshRequest) {
			return false;
		}

		// get document start values immediately
		self.requestRefreshUpdate();
	}

	/**
	 * Attempt to check the last modified date by the headers 
	 * or the last modified property from the byte array (experimental)
	 **/
	self.requestRefreshUpdate = function() {
		var url = document.location.href;
		var protocol = window.location.protocol;
		var method;
		
		try {

			if (self.refreshCheckContentSize) {
				self.refreshRequest.open('HEAD', url, true);
			}
			else if (self.refreshCheckContent) {
				self.refreshContent = document.documentElement.outerHTML;
				self.refreshRequest.open('GET', url, true);
				self.refreshRequest.responseType = "text";
			}
			else {

				// get page last modified date for the first call to compare to later
				if (self.lastModifiedDate==null) {

					// File system does not send headers in FF so get blob if possible
					if (protocol=="file:") {
						self.refreshRequest.open("GET", url, true);
						self.refreshRequest.responseType = "blob";
					}
					else {
						self.refreshRequest.open("HEAD", url, true);
						self.refreshRequest.responseType = "blob";
					}

					self.refreshRequest.onload = self.refreshOnLoadOnceHandler;

					// In some browsers (Chrome & Safari) this error occurs at send: 
					// 
					// Chrome - Access to XMLHttpRequest at 'file:///index.html' from origin 'null' 
					// has been blocked by CORS policy: 
					// Cross origin requests are only supported for protocol schemes: 
					// http, data, chrome, chrome-extension, https.
					// 
					// Safari - XMLHttpRequest cannot load file:///Users/user/Public/index.html. Cross origin requests are only supported for HTTP.
					// 
					// Solution is to run a local server, set local permissions or test in another browser
					self.refreshRequest.send(null);

					// In MS browsers the following behavior occurs possibly due to an AJAX call to check last modified date: 
					// 
					// DOM7011: The code on this page disabled back and forward caching.

					// In Brave (Chrome) error when on the server
					// index.js:221 HEAD https://www.example.com/ net::ERR_INSUFFICIENT_RESOURCES
					// self.refreshRequest.send(null);

				}
				else {
					self.refreshRequest = new XMLHttpRequest();
					self.refreshRequest.onreadystatechange = self.refreshHandler;
					self.refreshRequest.ontimeout = function() {
						self.log("Couldn't find page to check for updates");
					}
					
					var method;
					if (protocol=="file:") {
						method = "GET";
					}
					else {
						method = "HEAD";
					}

					//refreshRequest.open('HEAD', url, true);
					self.refreshRequest.open(method, url, true);
					self.refreshRequest.responseType = "blob";
					self.refreshRequest.send(null);
				}
			}
		}
		catch (error) {
			self.log("Refresh failed for the following reason:")
			self.log(error);
		}
	}

	self.refreshHandler = function() {
		var contentSize;

		try {

			if (self.refreshRequest.readyState === XMLHttpRequest.DONE) {
				
				if (self.refreshRequest.status === 2 || 
					self.refreshRequest.status === 200) {
					var pageChanged = false;

					self.updateLastModifiedLabel();

					if (self.refreshCheckContentSize) {
						var lastModifiedHeader = self.refreshRequest.getResponseHeader("Last-Modified");
						contentSize = self.refreshRequest.getResponseHeader("Content-Length");
						//lastModifiedDate = refreshRequest.getResponseHeader("Last-Modified");
						var headers = self.refreshRequest.getAllResponseHeaders();
						var hasContentHeader = headers.indexOf("Content-Length")!=-1;
						
						if (hasContentHeader) {
							contentSize = self.refreshRequest.getResponseHeader("Content-Length");

							// size has not been set yet
							if (self.refreshContentSize==null) {
								self.refreshContentSize = contentSize;
								// exit and let interval call this method again
								return;
							}

							if (contentSize!=self.refreshContentSize) {
								pageChanged = true;
							}
						}
					}
					else if (self.refreshCheckContent) {

						if (self.refreshRequest.responseText!=self.refreshContent) {
							pageChanged = true;
						}
					}
					else {
						lastModifiedHeader = self.getLastModified(self.refreshRequest);

						if (self.lastModifiedDate!=lastModifiedHeader) {
							self.log("lastModifiedDate:" + self.lastModifiedDate + ",lastModifiedHeader:" +lastModifiedHeader);
							pageChanged = true;
						}

					}

					
					if (pageChanged) {
						clearInterval(self.refreshInterval);
						self.refreshUpdatedPage();
						return;
					}

				}
				else {
					self.log('There was a problem with the request.');
				}

			}
		}
		catch( error ) {
			//console.log('Caught Exception: ' + error);
		}
	}

	self.refreshOnLoadOnceHandler = function(event) {

		// get the last modified date
		if (self.refreshRequest.response) {
			self.lastModifiedDate = self.getLastModified(self.refreshRequest);

			if (self.lastModifiedDate!=null) {

				if (self.refreshInterval==null) {
					self.refreshInterval = setInterval(self.requestRefreshUpdate, self.refreshDuration);
				}
			}
			else {
				self.log("Could not get last modified date from the server");
			}
		}
	}

	self.refreshUpdatedPage = function() {
		if (self.showRefreshNotifications) {
			var date = new Date().setTime((new Date().getTime()+10000));
			document.cookie = encodeURIComponent(self.pageRefreshedName) + "=true" + "; max-age=6000;" + " path=/";
		}

		document.location.reload(true);
	}

	self.showNotification = function(duration) {
		var notificationID = self.pageRefreshedName+"ID";
		var notification = document.getElementById(notificationID);
		if (duration==null) duration = 4000;

		if (notification!=null) {return;}

		notification = document.createElement("div");
		notification.id = notificationID;
		notification.textContent = "PAGE UPDATED";
		var styleRule = ""
		styleRule = "position: fixed; padding: 7px 16px 6px 16px; font-family: Arial, sans-serif; font-size: 10px; font-weight: bold; left: 50%;";
		styleRule += "top: 20px; background-color: rgba(0,0,0,.5); border-radius: 12px; color:rgb(235, 235, 235); transition: all 2s linear;";
		styleRule += "transform: translateX(-50%); letter-spacing: .5px; filter: drop-shadow(2px 2px 6px rgba(0, 0, 0, .1))";
		notification.setAttribute("style", styleRule);

		notification.className= "PageRefreshedClass";
		
		document.body.appendChild(notification);

		setTimeout(function() {
			notification.style.opacity = "0";
			notification.style.filter = "drop-shadow( 0px 0px 0px rgba(0,0,0, .5))";
			setTimeout(function() {
				notification.parentNode.removeChild(notification);
			}, duration)
		}, duration);

		document.cookie = encodeURIComponent(self.pageRefreshedName) + "=; max-age=1; path=/";
	}

	/**
	 * Get the last modified date from the header 
	 * or file object after request has been received
	 **/
	self.getLastModified = function(request) {
		var date;

		// file protocol - FILE object with last modified property
		if (request.response && request.response.lastModified) {
			date = request.response.lastModified;
		}
		
		// http protocol - check headers
		if (date==null) {
			date = request.getResponseHeader("Last-Modified");
		}

		return date;
	}

	self.updateLastModifiedLabel = function() {
		var labelValue = "";
		
		if (self.lastModifiedLabel==null) {
			self.lastModifiedLabel = document.getElementById("LastModifiedLabel");
		}

		if (self.lastModifiedLabel) {
			var seconds = parseInt(((new Date().getTime() - Date.parse(document.lastModified)) / 1000 / 60) * 100 + "");
			var minutes = 0;
			var hours = 0;

			if (seconds < 60) {
				seconds = Math.floor(seconds/10)*10;
				labelValue = seconds + " seconds";
			}
			else {
				minutes = parseInt((seconds/60) + "");

				if (minutes>60) {
					hours = parseInt((seconds/60/60) +"");
					labelValue += hours==1 ? " hour" : " hours";
				}
				else {
					labelValue = minutes+"";
					labelValue += minutes==1 ? " minute" : " minutes";
				}
			}
			
			if (seconds<10) {
				labelValue = "Updated now";
			}
			else {
				labelValue = "Updated " + labelValue + " ago";
			}

			if (self.lastModifiedLabel.firstElementChild) {
				self.lastModifiedLabel.firstElementChild.textContent = labelValue;

			}
			else if ("textContent" in self.lastModifiedLabel) {
				self.lastModifiedLabel.textContent = labelValue;
			}
		}
	}

	self.getShortString = function(string, length) {
		if (length==null) length = 30;
		string = string!=null ? string.substr(0, length).replace(/\n/g, "") : "[String is null]";
		return string;
	}

	self.getShortNumber = function(value, places) {
		if (places==null || places<1) places = 4;
		value = Math.round(value * Math.pow(10,places)) / Math.pow(10, places);
		return value;
	}

	///////////////////////////////////////
	// NAVIGATION CONTROLS
	///////////////////////////////////////

	self.updateViewLabel = function() {
		var viewNavigationLabel = document.getElementById("ViewNavigationLabel");
		var view = self.getVisibleView();
		var viewIndex = view ? self.getViewIndex(view) : -1;
		var viewName = view ? self.getViewPreferenceValue(view, self.prefix + "view-name") : null;
		var viewId = view ? view.id : null;

		if (viewNavigationLabel && view) {
			if (viewName && viewName.indexOf('"')!=-1) {
				viewName = viewName.replace(/"/g, "");
			}

			if (self.showViewName) {
				viewNavigationLabel.textContent = viewName;
				self.setTooltip(viewNavigationLabel, viewIndex + 1 + " of " + self.numberOfViews);
			}
			else {
				viewNavigationLabel.textContent = viewIndex + 1 + " of " + self.numberOfViews;
				self.setTooltip(viewNavigationLabel, viewName);
			}

		}
	}

	self.updateURL = function(view) {
		view = view == null ? self.getVisibleView() : view;
		var viewId = view ? view.id : null
		var viewFragment = view ? "#"+ viewId : null;

		if (viewId && self.viewIds.length>1 && self.enableDeepLinking) {

			if (self.supportsPopState==false) {
				self.setFragment(viewId);
			}
			else {
				if (viewFragment!=window.location.hash) {

					if (window.location.hash==null) {
						window.history.replaceState({name:viewId}, null, viewFragment);
					}
					else {
						window.history.pushState({name:viewId}, null, viewFragment);
					}
				}
			}
		}
	}

	self.setFragment = function(value) {
		window.location.hash = "#" + value;
	}

	self.setTooltip = function(element, value) {
		// setting the tooltip in edge causes a page crash on hover
		if (/Edge/.test(navigator.userAgent)) { return; }

		if ("title" in element) {
			element.title = value;
		}
	}

	self.getStylesheetRules = function(styleSheet) {
		try {
			if (styleSheet) return styleSheet.cssRules || styleSheet.rules;
	
			return document.styleSheets[0]["cssRules"] || document.styleSheets[0]["rules"];
		}
		catch (error) {
			// ERRORS:
			// SecurityError: The operation is insecure.
			// Errors happen when script loads before stylesheet or loading an external css locally

			// InvalidAccessError: A parameter or an operation is not supported by the underlying object
			// Place script after stylesheet

			console.log(error);
			if (error.toString().indexOf("The operation is insecure")!=-1) {
				console.log("Load the stylesheet before the script or load the stylesheet inline until it can be loaded on a server")
			}
			return [];
		}
	}

	/**
	 * If single page application hide all of the views. 
	 * @param {Number} selectedIndex if provided shows the view at index provided
	 **/
	self.hideViews = function(selectedIndex, animation) {
		var rules = self.getStylesheetRules();
		var queryIndex = 0;
		var numberOfRules = rules!=null ? rules.length : 0;

		// loop through rules and hide media queries except selected
		for (var i=0;i<numberOfRules;i++) {
			var rule = rules[i];

			if (rule.media!=null) {

				if (queryIndex==selectedIndex) {
					self.currentQuery.mediaText = rule.conditionText;
					self.currentQuery.index = selectedIndex;
					self.currentQuery.rule = rule;
					self.enableMediaQuery(rule);
				}
				else {
					if (animation) {
						self.fadeOut(rule)
					}
					else {
						self.disableMediaQuery(rule);
					}
				}
				
				queryIndex++;
			}
		}

		self.numberOfViews = queryIndex;
		self.updateViewLabel();
		self.updateURL();

		self.dispatchViewChange();

		var view = self.getVisibleView();
		var viewIndex = view ? self.getViewIndex(view) : -1;

		return viewIndex==selectedIndex ? view : null;
	}

	/**
	 * Hide view
	 * @param {Object} view element to hide
	 **/
	self.hideView = function(view) {
		var rule = view ? self.mediaQueryDictionary[view.id] : null;

		if (rule) {
			self.disableMediaQuery(rule);
		}
	}

	/**
	 * Hide overlay
	 * @param {Object} overlay element to hide
	 **/
	self.hideOverlay = function(overlay) {
		var rule = overlay ? self.mediaQueryDictionary[overlay.id] : null;

		if (rule) {
			self.disableMediaQuery(rule);

			//if (self.showByMediaQuery) {
				overlay.style.display = "none";
			//}
		}
	}

	/**
	 * Show the view by media query. Does not hide current views
	 * Sets view options by default
	 * @param {Object} view element to show
	 * @param {Boolean} setViewOptions sets view options if null or true
	 */
	self.showViewByMediaQuery = function(view, setViewOptions) {
		var id = view ? view.id : null;
		var query = id ? self.mediaQueryDictionary[id] : null;
		var display = null;
		setViewOptions = setViewOptions==null ? true : setViewOptions;

		if (query) {
			self.enableMediaQuery(query);
			if (view && setViewOptions) self.setViewOptions(view);
			if (view && setViewOptions) self.setViewVariables(view);
		}
	}

	/**
	 * Show the view. Does not hide current views
	 */
	self.showView = function(view, setViewOptions) {
		var id = view ? view.id : null;
		var query = id ? self.mediaQueryDictionary[id] : null;
		var display = null;
		setViewOptions = setViewOptions==null ? true : setViewOptions;

		if (query) {
			self.enableMediaQuery(query);
			if (view==null) view =self.getVisibleView();
			if (view && setViewOptions) self.setViewOptions(view);
		}
		else if (id) {
			display = window.getComputedStyle(view).getPropertyValue("display");
			if (display=="" || display=="none") {
				view.style.display = "block";
			}
		}

		if (view) {
			if (self.currentView!=null) {
				self.lastView = self.currentView;
			}

			self.currentView = view;
		}
	}

	self.showViewById = function(id, setViewOptions) {
		var view = id ? self.getViewById(id) : null;

		if (view) {
			self.showView(view);
			return;
		}

		self.log("View not found '" + id + "'");
	}

	/**
	 * Show overlay over view
	 * @param {String} id id of view or view reference
	 * @param {Number} x x location
	 * @param {Number} y y location
	 * @param {Event | HTMLElement} event event or html element with styles applied
	 */
	self.showOverlay = function(id, x, y, event) {
		var overlay = id && typeof id === 'string' ? self.getViewById(id) : id ? id : null;
		var query = overlay ? self.mediaQueryDictionary[overlay.id] : null;
		var centerHorizontally = false;
		var centerVertically = false;
		var display = null;

		// get enter animation - event target must have css variables declared
		if (event) {
			var button = event.currentTarget || event; // can be event or htmlelement
			var buttonComputedStyles = getComputedStyle(button);
			var actionTargetValue = buttonComputedStyles.getPropertyValue(self.prefix+"action-target").trim();
			var animation = buttonComputedStyles.getPropertyValue(self.prefix+"animation").trim();
			var targetType = buttonComputedStyles.getPropertyValue(self.prefix+"action-type").trim();
			var actionTarget = self.application ? null : self.getElement(actionTargetValue);
			var actionTargetStyles = actionTarget ? actionTarget.style : null;

			if (actionTargetStyles) {
				actionTargetStyles.setProperty("animation", animation);
			}

			if ("stopImmediatePropagation" in event) {
				event.stopImmediatePropagation();
			}
		}
		
		if (self.application==false || targetType=="page") {
			document.location.href = "./" + actionTargetValue;
			return;
		}

		// remove any current overlays
		if (self.currentOverlay) {
			self.removeOverlay();
		}

		if (query) {
			//self.setElementAnimation(overlay, null);
			//overlay.style.animation = animation;
			self.enableMediaQuery(query);
			
			var display = overlay && overlay.style.display;
			
			if (overlay && display=="" || display=="none") {
				overlay.style.display = "block";
				self.setViewOptions(overlay);
			}

			// add animation defined in event target style declaration
			if (animation && self.supportAnimations) {
				self.fadeIn(overlay, false, animation);
			}
		}
		else if (id) {
			if (overlay==null || overlay==false) {
				self.log("Overlay not found, '"+ id + "'");
				return;
			}

			display = window.getComputedStyle(overlay).getPropertyValue("display");

			if (display=="" || display=="none") {
				overlay.style.display = "block";
			}

			// add animation defined in event target style declaration
			if (animation && self.supportAnimations) {
				self.fadeIn(overlay, false, animation);
			}
		}

		// do not set x or y position if centering
		centerHorizontally = self.getViewPreferenceBoolean(overlay, self.prefix + "center-horizontally", false);
		centerVertically = self.getViewPreferenceBoolean(overlay, self.prefix + "center-vertically", false);

		if (overlay && centerHorizontally==false) {
			overlay.style.left = x + "px";
		}
		
		if (overlay && centerVertically==false) {
			overlay.style.top = y + "px";
		}

		self.currentOverlay = overlay;
	}

	self.goBack = function() {
		if (self.currentOverlay) {
			self.removeOverlay();
		}
		else if (self.lastView) {
			self.goToView(self.lastView.id);
		}
	}

	self.removeOverlay = function(animate) {
		var overlay = self.currentOverlay;
		animate = animate===false ? false : true;

		if (overlay) {
			var style = overlay.style;
			
			if (style.animation && self.supportAnimations && animate) {
				self.reverseAnimation(overlay, true);

				var duration = self.getAnimationDuration(style.animation, true);
		
				setTimeout(function() {
					self.setElementAnimation(overlay, null);
					self.hideOverlay(overlay);
				}, duration);
			}
			else {
				self.setElementAnimation(overlay, null);
				self.hideOverlay(overlay);
			}
		}
	}

	/**
	 * Reverse the animation and hide after
	 * @param {Object} target element with animation
	 * @param {Boolean} hide hide after animation ends
	 */
	self.reverseAnimation = function(target, hide) {
		var lastAnimation = null;
		var style = target.style;

		style.animationPlayState = "paused";
		lastAnimation = style.animation;
		style.animation = null;
		style.animationPlayState = "paused";

		if (hide) {
			//target.addEventListener("animationend", self.animationEndHideHandler);
	
			var duration = self.getAnimationDuration(lastAnimation, true);
			var isOverlay = self.isOverlay(target);
	
			setTimeout(function() {
				self.setElementAnimation(target, null);

				if (isOverlay) {
					self.hideOverlay(target);
				}
				else {
					self.hideView(target);
				}
			}, duration);
		}

		setTimeout(function() {
			style.animation = lastAnimation;
			style.animationPlayState = "paused";
			style.animationDirection = "reverse";
			style.animationPlayState = "running";
		}, 30);
	}

	self.animationEndHandler = function(event) {
		var target = event.currentTarget;
		self.dispatchEvent(new Event(event.type));
	}

	self.isOverlay = function(view) {
		var result = view ? self.getViewPreferenceBoolean(view, self.prefix + "is-overlay") : false;

		return result;
	}

	self.animationEndHideHandler = function(event) {
		var target = event.currentTarget;
		self.setViewVariables(null, target);
		self.hideView(target);
		target.removeEventListener("animationend", self.animationEndHideHandler);
	}

	self.animationEndShowHandler = function(event) {
		var target = event.currentTarget;
		target.removeEventListener("animationend", self.animationEndShowHandler);
	}

	self.setViewOptions = function(view) {

		if (view) {
			self.minimumScale = self.getViewPreferenceValue(view, self.prefix + "minimum-scale");
			self.maximumScale = self.getViewPreferenceValue(view, self.prefix + "maximum-scale");
			self.scaleViewsToFit = self.getViewPreferenceBoolean(view, self.prefix + "scale-to-fit");
			self.scaleToFitType = self.getViewPreferenceValue(view, self.prefix + "scale-to-fit-type");
			self.scaleToFitOnDoubleClick = self.getViewPreferenceBoolean(view, self.prefix + "scale-on-double-click");
			self.actualSizeOnDoubleClick = self.getViewPreferenceBoolean(view, self.prefix + "actual-size-on-double-click");
			self.scaleViewsOnResize = self.getViewPreferenceBoolean(view, self.prefix + "scale-on-resize");
			self.enableScaleUp = self.getViewPreferenceBoolean(view, self.prefix + "enable-scale-up");
			self.centerHorizontally = self.getViewPreferenceBoolean(view, self.prefix + "center-horizontally");
			self.centerVertically = self.getViewPreferenceBoolean(view, self.prefix + "center-vertically");
			self.navigationOnKeypress = self.getViewPreferenceBoolean(view, self.prefix + "navigate-on-keypress");
			self.showViewName = self.getViewPreferenceBoolean(view, self.prefix + "show-view-name");
			self.refreshPageForChanges = self.getViewPreferenceBoolean(view, self.prefix + "refresh-for-changes");
			self.refreshPageForChangesInterval = self.getViewPreferenceValue(view, self.prefix + "refresh-interval");
			self.showNavigationControls = self.getViewPreferenceBoolean(view, self.prefix + "show-navigation-controls");
			self.scaleViewSlider = self.getViewPreferenceBoolean(view, self.prefix + "show-scale-controls");
			self.enableDeepLinking = self.getViewPreferenceBoolean(view, self.prefix + "enable-deep-linking");
			self.singlePageApplication = self.getViewPreferenceBoolean(view, self.prefix + "application");
			self.showByMediaQuery = self.getViewPreferenceBoolean(view, self.prefix + "show-by-media-query");
			self.showUpdateNotification = document.cookie!="" ? document.cookie.indexOf(self.pageRefreshedName)!=-1 : false;
			self.imageComparisonDuration = self.getViewPreferenceValue(view, self.prefix + "image-comparison-duration");
			self.supportAnimations = self.getViewPreferenceBoolean(view, self.prefix + "enable-animations", true);

			if (self.scaleViewsToFit) {
				var newScaleValue = self.scaleViewToFit(view);
				
				if (newScaleValue<0) {
					setTimeout(self.scaleViewToFit, 500, view);
				}
			}
			else {
				self.viewScale = self.getViewScaleValue(view);
				self.viewToFitWidthScale = self.getViewFitToViewportWidthScale(view, self.enableScaleUp)
				self.viewToFitHeightScale = self.getViewFitToViewportScale(view, self.enableScaleUp);
				self.updateSliderValue(self.viewScale);
			}

			if (self.imageComparisonDuration!=null) {
				// todo
			}

			if (self.refreshPageForChangesInterval!=null) {
				self.refreshDuration = Number(self.refreshPageForChangesInterval);
			}
		}
	}

	self.previousView = function(event) {
		var rules = self.getStylesheetRules();
		var view = self.getVisibleView()
		var index = view ? self.getViewIndex(view) : -1;
		var prevQueryIndex = index!=-1 ? index-1 : self.currentQuery.index-1;
		var queryIndex = 0;
		var numberOfRules = rules!=null ? rules.length : 0;

		if (event) {
			event.stopImmediatePropagation();
		}

		if (prevQueryIndex<0) {
			return;
		}

		// loop through rules and hide media queries except selected
		for (var i=0;i<numberOfRules;i++) {
			var rule = rules[i];
			
			if (rule.media!=null) {

				if (queryIndex==prevQueryIndex) {
					self.currentQuery.mediaText = rule.conditionText;
					self.currentQuery.index = prevQueryIndex;
					self.currentQuery.rule = rule;
					self.enableMediaQuery(rule);
					self.updateViewLabel();
					self.updateURL();
					self.dispatchViewChange();
				}
				else {
					self.disableMediaQuery(rule);
				}

				queryIndex++;
			}
		}
	}

	self.nextView = function(event) {
		var rules = self.getStylesheetRules();
		var view = self.getVisibleView();
		var index = view ? self.getViewIndex(view) : -1;
		var nextQueryIndex = index!=-1 ? index+1 : self.currentQuery.index+1;
		var queryIndex = 0;
		var numberOfRules = rules!=null ? rules.length : 0;
		var numberOfMediaQueries = self.getNumberOfMediaRules();

		if (event) {
			event.stopImmediatePropagation();
		}

		if (nextQueryIndex>=numberOfMediaQueries) {
			return;
		}

		// loop through rules and hide media queries except selected
		for (var i=0;i<numberOfRules;i++) {
			var rule = rules[i];
			
			if (rule.media!=null) {

				if (queryIndex==nextQueryIndex) {
					self.currentQuery.mediaText = rule.conditionText;
					self.currentQuery.index = nextQueryIndex;
					self.currentQuery.rule = rule;
					self.enableMediaQuery(rule);
					self.updateViewLabel();
					self.updateURL();
					self.dispatchViewChange();
				}
				else {
					self.disableMediaQuery(rule);
				}

				queryIndex++;
			}
		}
	}

	/**
	 * Enables a view via media query
	 */
	self.enableMediaQuery = function(rule) {

		try {
			rule.media.mediaText = self.inclusionQuery;
		}
		catch(error) {
			//self.log(error);
			rule.conditionText = self.inclusionQuery;
		}
	}

	self.disableMediaQuery = function(rule) {

		try {
			rule.media.mediaText = self.exclusionQuery;
		}
		catch(error) {
			rule.conditionText = self.exclusionQuery;
		}
	}

	self.dispatchViewChange = function() {
		try {
			var event = new Event(self.NAVIGATION_CHANGE);
			window.dispatchEvent(event);
		}
		catch (error) {
			// In IE 11: Object doesn't support this action
		}
	}

	self.getNumberOfMediaRules = function() {
		var rules = self.getStylesheetRules();
		var numberOfRules = rules ? rules.length : 0;
		var numberOfQueries = 0;

		for (var i=0;i<numberOfRules;i++) {
			if (rules[i].media!=null) { numberOfQueries++; }
		}
		
		return numberOfQueries;
	}

	/////////////////////////////////////////
	// VIEW SCALE 
	/////////////////////////////////////////

	self.sliderChangeHandler = function(event) {
		var value = self.getShortNumber(event.currentTarget.value/100);
		var view = self.getVisibleView();
		self.setViewScaleValue(view, false, value, true);
	}

	self.updateSliderValue = function(scale) {
		var slider = document.getElementById(self.viewScaleSliderId);
		var tooltip = parseInt(scale * 100 + "") + "%";
		var inputType;
		var inputValue;
		
		if (slider) {
			inputValue = self.getShortNumber(scale * 100);
			if (inputValue!=slider["value"]) {
				slider["value"] = inputValue;
			}
			inputType = slider.getAttributeNS(null, "type");

			if (inputType!="range") {
				// input range is not supported
				slider.style.display = "none";
			}

			self.setTooltip(slider, tooltip);
		}
	}

	self.viewChangeHandler = function(event) {
		var view = self.getVisibleView();
		var matrix = view ? getComputedStyle(view).transform : null;
		
		if (matrix) {
			self.viewScale = self.getViewScaleValue(view);
			
			var scaleNeededToFit = self.getViewFitToViewportScale(view);
			var isViewLargerThanViewport = scaleNeededToFit<1;
			
			// scale large view to fit if scale to fit is enabled
			if (self.scaleViewsToFit) {
				self.scaleViewToFit(view);
			}
			else {
				self.updateSliderValue(self.viewScale);
			}
		}
	}

	self.getViewScaleValue = function(view) {
		var matrix = getComputedStyle(view).transform;

		if (matrix) {
			var matrixArray = matrix.replace("matrix(", "").split(",");
			var scaleX = parseFloat(matrixArray[0]);
			var scaleY = parseFloat(matrixArray[3]);
			var scale = Math.min(scaleX, scaleY);
		}

		return scale;
	}

	/**
	 * Scales view to scale. 
	 * @param {Object} view view to scale. views are in views array
	 * @param {Boolean} scaleToFit set to true to scale to fit. set false to use desired scale value
	 * @param {Number} desiredScale scale to define. not used if scale to fit is false
	 * @param {Boolean} isSliderChange indicates if slider is callee
	 */
	self.setViewScaleValue = function(view, scaleToFit, desiredScale, isSliderChange) {
		var enableScaleUp = self.enableScaleUp;
		var scaleToFitType = self.scaleToFitType;
		var minimumScale = self.minimumScale;
		var maximumScale = self.maximumScale;
		var hasMinimumScale = !isNaN(minimumScale) && minimumScale!="";
		var hasMaximumScale = !isNaN(maximumScale) && maximumScale!="";
		var scaleNeededToFit = self.getViewFitToViewportScale(view, enableScaleUp);
		var scaleNeededToFitWidth = self.getViewFitToViewportWidthScale(view, enableScaleUp);
		var scaleNeededToFitHeight = self.getViewFitToViewportHeightScale(view, enableScaleUp);
		var scaleToFitFull = self.getViewFitToViewportScale(view, true);
		var scaleToFitFullWidth = self.getViewFitToViewportWidthScale(view, true);
		var scaleToFitFullHeight = self.getViewFitToViewportHeightScale(view, true);
		var scaleToWidth = scaleToFitType=="width";
		var scaleToHeight = scaleToFitType=="height";
		var shrunkToFit = false;
		var topPosition = null;
		var leftPosition = null;
		var translateY = null;
		var translateX = null;
		var transformValue = "";
		var canCenterVertically = true;
		var canCenterHorizontally = true;

		if (scaleToFit && isSliderChange!=true) {
			if (scaleToFitType=="fit" || scaleToFitType=="") {
				desiredScale = scaleNeededToFit;
			}
			else if (scaleToFitType=="width") {
				desiredScale = scaleNeededToFitWidth;
			}
			else if (scaleToFitType=="height") {
				desiredScale = scaleNeededToFitHeight;
			}
		}
		else {
			if (isNaN(desiredScale)) {
				desiredScale = 1;
			}
		}

		self.updateSliderValue(desiredScale);
		
		// scale to fit width
		if (scaleToWidth && scaleToHeight==false) {
			canCenterVertically = scaleNeededToFitHeight>=scaleNeededToFitWidth;
			canCenterHorizontally = scaleNeededToFitWidth>=1 && enableScaleUp==false;

			if (isSliderChange) {
				canCenterHorizontally = desiredScale<scaleToFitFullWidth;
			}
			else if (scaleToFit) {
				desiredScale = scaleNeededToFitWidth;
			}

			if (hasMinimumScale) {
				desiredScale = Math.max(desiredScale, Number(minimumScale));
			}

			if (hasMaximumScale) {
				desiredScale = Math.min(desiredScale, Number(maximumScale));
			}

			desiredScale = self.getShortNumber(desiredScale);

			canCenterHorizontally = self.canCenterHorizontally(view, "width", enableScaleUp, desiredScale, minimumScale, maximumScale);
			canCenterVertically = self.canCenterVertically(view, "width", enableScaleUp, desiredScale, minimumScale, maximumScale);

			if (desiredScale>1 && (enableScaleUp || isSliderChange)) {
				transformValue = "scale(" + desiredScale + ")";
			}
			else if (desiredScale>=1 && enableScaleUp==false) {
				transformValue = "scale(" + 1 + ")";
			}
			else {
				transformValue = "scale(" + desiredScale + ")";
			}

			if (self.centerVertically) {
				if (canCenterVertically) {
					translateY = "-50%";
					topPosition = "50%";
				}
				else {
					translateY = "0";
					topPosition = "0";
				}
				
				if (view.style.top != topPosition) {
					view.style.top = topPosition + "";
				}

				if (canCenterVertically) {
					transformValue += " translateY(" + translateY+ ")";
				}
			}

			if (self.centerHorizontally) {
				if (canCenterHorizontally) {
					translateX = "-50%";
					leftPosition = "50%";
				}
				else {
					translateX = "0";
					leftPosition = "0";
				}

				if (view.style.left != leftPosition) {
					view.style.left = leftPosition + "";
				}

				if (canCenterHorizontally) {
					transformValue += " translateX(" + translateX+ ")";
				}
			}

			view.style.transformOrigin = "0 0";
			view.style.transform = transformValue;

			self.viewScale = desiredScale;
			self.viewToFitWidthScale = scaleNeededToFitWidth;
			self.viewToFitHeightScale = scaleNeededToFitHeight;
			self.viewLeft = leftPosition;
			self.viewTop = topPosition;

			return desiredScale;
		}

		// scale to fit height
		if (scaleToHeight && scaleToWidth==false) {
			//canCenterVertically = scaleNeededToFitHeight>=scaleNeededToFitWidth;
			//canCenterHorizontally = scaleNeededToFitHeight<=scaleNeededToFitWidth && enableScaleUp==false;
			canCenterVertically = scaleNeededToFitHeight>=scaleNeededToFitWidth;
			canCenterHorizontally = scaleNeededToFitWidth>=1 && enableScaleUp==false;
			
			if (isSliderChange) {
				canCenterHorizontally = desiredScale<scaleToFitFullHeight;
			}
			else if (scaleToFit) {
				desiredScale = scaleNeededToFitHeight;
			}

			if (hasMinimumScale) {
				desiredScale = Math.max(desiredScale, Number(minimumScale));
			}

			if (hasMaximumScale) {
				desiredScale = Math.min(desiredScale, Number(maximumScale));
				//canCenterVertically = desiredScale>=scaleNeededToFitHeight && enableScaleUp==false;
			}

			desiredScale = self.getShortNumber(desiredScale);

			canCenterHorizontally = self.canCenterHorizontally(view, "height", enableScaleUp, desiredScale, minimumScale, maximumScale);
			canCenterVertically = self.canCenterVertically(view, "height", enableScaleUp, desiredScale, minimumScale, maximumScale);

			if (desiredScale>1 && (enableScaleUp || isSliderChange)) {
				transformValue = "scale(" + desiredScale + ")";
			}
			else if (desiredScale>=1 && enableScaleUp==false) {
				transformValue = "scale(" + 1 + ")";
			}
			else {
				transformValue = "scale(" + desiredScale + ")";
			}

			if (self.centerHorizontally) {
				if (canCenterHorizontally) {
					translateX = "-50%";
					leftPosition = "50%";
				}
				else {
					translateX = "0";
					leftPosition = "0";
				}

				if (view.style.left != leftPosition) {
					view.style.left = leftPosition + "";
				}

				if (canCenterHorizontally) {
					transformValue += " translateX(" + translateX+ ")";
				}
			}

			if (self.centerVertically) {
				if (canCenterVertically) {
					translateY = "-50%";
					topPosition = "50%";
				}
				else {
					translateY = "0";
					topPosition = "0";
				}
				
				if (view.style.top != topPosition) {
					view.style.top = topPosition + "";
				}

				if (canCenterVertically) {
					transformValue += " translateY(" + translateY+ ")";
				}
			}

			view.style.transformOrigin = "0 0";
			view.style.transform = transformValue;

			self.viewScale = desiredScale;
			self.viewToFitWidthScale = scaleNeededToFitWidth;
			self.viewToFitHeightScale = scaleNeededToFitHeight;
			self.viewLeft = leftPosition;
			self.viewTop = topPosition;

			return scaleNeededToFitHeight;
		}

		if (scaleToFitType=="fit") {
			//canCenterVertically = scaleNeededToFitHeight>=scaleNeededToFitWidth;
			//canCenterHorizontally = scaleNeededToFitWidth>=scaleNeededToFitHeight;
			canCenterVertically = scaleNeededToFitHeight>=scaleNeededToFit;
			canCenterHorizontally = scaleNeededToFitWidth>=scaleNeededToFit;

			if (hasMinimumScale) {
				desiredScale = Math.max(desiredScale, Number(minimumScale));
			}

			desiredScale = self.getShortNumber(desiredScale);

			if (isSliderChange || scaleToFit==false) {
				canCenterVertically = scaleToFitFullHeight>=desiredScale;
				canCenterHorizontally = desiredScale<scaleToFitFullWidth;
			}
			else if (scaleToFit) {
				desiredScale = scaleNeededToFit;
			}

			transformValue = "scale(" + desiredScale + ")";

			//canCenterHorizontally = self.canCenterHorizontally(view, "fit", false, desiredScale);
			//canCenterVertically = self.canCenterVertically(view, "fit", false, desiredScale);
			
			if (self.centerVertically) {
				if (canCenterVertically) {
					translateY = "-50%";
					topPosition = "50%";
				}
				else {
					translateY = "0";
					topPosition = "0";
				}
				
				if (view.style.top != topPosition) {
					view.style.top = topPosition + "";
				}

				if (canCenterVertically) {
					transformValue += " translateY(" + translateY+ ")";
				}
			}

			if (self.centerHorizontally) {
				if (canCenterHorizontally) {
					translateX = "-50%";
					leftPosition = "50%";
				}
				else {
					translateX = "0";
					leftPosition = "0";
				}

				if (view.style.left != leftPosition) {
					view.style.left = leftPosition + "";
				}

				if (canCenterHorizontally) {
					transformValue += " translateX(" + translateX+ ")";
				}
			}

			view.style.transformOrigin = "0 0";
			view.style.transform = transformValue;

			self.viewScale = desiredScale;
			self.viewToFitWidthScale = scaleNeededToFitWidth;
			self.viewToFitHeightScale = scaleNeededToFitHeight;
			self.viewLeft = leftPosition;
			self.viewTop = topPosition;

			self.updateSliderValue(desiredScale);
			
			return desiredScale;
		}

		if (scaleToFitType=="default" || scaleToFitType=="") {
			desiredScale = 1;

			if (hasMinimumScale) {
				desiredScale = Math.max(desiredScale, Number(minimumScale));
			}
			if (hasMaximumScale) {
				desiredScale = Math.min(desiredScale, Number(maximumScale));
			}

			canCenterHorizontally = self.canCenterHorizontally(view, "none", false, desiredScale, minimumScale, maximumScale);
			canCenterVertically = self.canCenterVertically(view, "none", false, desiredScale, minimumScale, maximumScale);

			if (self.centerVertically) {
				if (canCenterVertically) {
					translateY = "-50%";
					topPosition = "50%";
				}
				else {
					translateY = "0";
					topPosition = "0";
				}
				
				if (view.style.top != topPosition) {
					view.style.top = topPosition + "";
				}

				if (canCenterVertically) {
					transformValue += " translateY(" + translateY+ ")";
				}
			}

			if (self.centerHorizontally) {
				if (canCenterHorizontally) {
					translateX = "-50%";
					leftPosition = "50%";
				}
				else {
					translateX = "0";
					leftPosition = "0";
				}

				if (view.style.left != leftPosition) {
					view.style.left = leftPosition + "";
				}

				if (canCenterHorizontally) {
					transformValue += " translateX(" + translateX+ ")";
				}
				else {
					transformValue += " translateX(" + 0 + ")";
				}
			}

			view.style.transformOrigin = "0 0";
			view.style.transform = transformValue;


			self.viewScale = desiredScale;
			self.viewToFitWidthScale = scaleNeededToFitWidth;
			self.viewToFitHeightScale = scaleNeededToFitHeight;
			self.viewLeft = leftPosition;
			self.viewTop = topPosition;

			self.updateSliderValue(desiredScale);
			
			return desiredScale;
		}
	}

	/**
	 * Returns true if view can be centered horizontally
	 * @param {HTMLElement} view view
	 * @param {String} type type of scaling - width, height, all, none
	 * @param {Boolean} scaleUp if scale up enabled 
	 * @param {Number} scale target scale value 
	 */
	self.canCenterHorizontally = function(view, type, scaleUp, scale, minimumScale, maximumScale) {
		var scaleNeededToFit = self.getViewFitToViewportScale(view, scaleUp);
		var scaleNeededToFitHeight = self.getViewFitToViewportHeightScale(view, scaleUp);
		var scaleNeededToFitWidth = self.getViewFitToViewportWidthScale(view, scaleUp);
		var canCenter = false;
		var minScale;

		type = type==null ? "none" : type;
		scale = scale==null ? scale : scaleNeededToFitWidth;
		scaleUp = scaleUp == null ? false : scaleUp;

		if (type=="width") {
	
			if (scaleUp && maximumScale==null) {
				canCenter = false;
			}
			else if (scaleNeededToFitWidth>=1) {
				canCenter = true;
			}
		}
		else if (type=="height") {
			minScale = Math.min(1, scaleNeededToFitHeight);
			if (minimumScale!="" && maximumScale!="") {
				minScale = Math.max(minimumScale, Math.min(maximumScale, scaleNeededToFitHeight));
			}
			else {
				if (minimumScale!="") {
					minScale = Math.max(minimumScale, scaleNeededToFitHeight);
				}
				if (maximumScale!="") {
					minScale = Math.max(minimumScale, Math.min(maximumScale, scaleNeededToFitHeight));
				}
			}
	
			if (scaleUp && maximumScale=="") {
				canCenter = false;
			}
			else if (scaleNeededToFitWidth>=minScale) {
				canCenter = true;
			}
		}
		else if (type=="fit") {
			canCenter = scaleNeededToFitWidth>=scaleNeededToFit;
		}
		else {
			if (scaleUp) {
				canCenter = false;
			}
			else if (scaleNeededToFitWidth>=1) {
				canCenter = true;
			}
		}

		self.horizontalScrollbarsNeeded = canCenter;
		
		return canCenter;
	}

	/**
	 * Returns true if view can be centered horizontally
	 * @param {HTMLElement} view view to scale
	 * @param {String} type type of scaling
	 * @param {Boolean} scaleUp if scale up enabled 
	 * @param {Number} scale target scale value 
	 */
	self.canCenterVertically = function(view, type, scaleUp, scale, minimumScale, maximumScale) {
		var scaleNeededToFit = self.getViewFitToViewportScale(view, scaleUp);
		var scaleNeededToFitWidth = self.getViewFitToViewportWidthScale(view, scaleUp);
		var scaleNeededToFitHeight = self.getViewFitToViewportHeightScale(view, scaleUp);
		var canCenter = false;
		var minScale;

		type = type==null ? "none" : type;
		scale = scale==null ? 1 : scale;
		scaleUp = scaleUp == null ? false : scaleUp;
	
		if (type=="width") {
			canCenter = scaleNeededToFitHeight>=scaleNeededToFitWidth;
		}
		else if (type=="height") {
			minScale = Math.max(minimumScale, Math.min(maximumScale, scaleNeededToFit));
			canCenter = scaleNeededToFitHeight>=minScale;
		}
		else if (type=="fit") {
			canCenter = scaleNeededToFitHeight>=scaleNeededToFit;
		}
		else {
			if (scaleUp) {
				canCenter = false;
			}
			else if (scaleNeededToFitHeight>=1) {
				canCenter = true;
			}
		}

		self.verticalScrollbarsNeeded = canCenter;
		
		return canCenter;
	}

	self.getViewFitToViewportScale = function(view, scaleUp) {
		var enableScaleUp = scaleUp;
		var availableWidth = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth;
		var availableHeight = window.innerHeight || document.documentElement.clientHeight || document.body.clientHeight;
		var elementWidth = parseFloat(getComputedStyle(view, "style").width);
		var elementHeight = parseFloat(getComputedStyle(view, "style").height);
		var newScale = 1;

		// if element is not added to the document computed values are NaN
		if (isNaN(elementWidth) || isNaN(elementHeight)) {
			return newScale;
		}

		availableWidth -= self.horizontalPadding;
		availableHeight -= self.verticalPadding;

		if (enableScaleUp) {
			newScale = Math.min(availableHeight/elementHeight, availableWidth/elementWidth);
		}
		else if (elementWidth > availableWidth || elementHeight > availableHeight) {
			newScale = Math.min(availableHeight/elementHeight, availableWidth/elementWidth);
		}
		
		return newScale;
	}

	self.getViewFitToViewportWidthScale = function(view, scaleUp) {
		// need to get browser viewport width when element
		var isParentWindow = view && view.parentNode && view.parentNode===document.body;
		var enableScaleUp = scaleUp;
		var availableWidth = window.innerWidth || document.documentElement.clientWidth || document.body.clientWidth;
		var elementWidth = parseFloat(getComputedStyle(view, "style").width);
		var newScale = 1;

		// if element is not added to the document computed values are NaN
		if (isNaN(elementWidth)) {
			return newScale;
		}

		availableWidth -= self.horizontalPadding;

		if (enableScaleUp) {
			newScale = availableWidth/elementWidth;
		}
		else if (elementWidth > availableWidth) {
			newScale = availableWidth/elementWidth;
		}
		
		return newScale;
	}

	self.getViewFitToViewportHeightScale = function(view, scaleUp) {
		var enableScaleUp = scaleUp;
		var availableHeight = window.innerHeight || document.documentElement.clientHeight || document.body.clientHeight;
		var elementHeight = parseFloat(getComputedStyle(view, "style").height);
		var newScale = 1;

		// if element is not added to the document computed values are NaN
		if (isNaN(elementHeight)) {
			return newScale;
		}

		availableHeight -= self.verticalPadding;

		if (enableScaleUp) {
			newScale = availableHeight/elementHeight;
		}
		else if (elementHeight > availableHeight) {
			newScale = availableHeight/elementHeight;
		}
		
		return newScale;
	}

	self.keypressHandler = function(event) {
		var rightKey = 39;
		var leftKey = 37;
		
		// listen for both events 
		if (event.type=="keypress") {
			window.removeEventListener("keyup", self.keypressHandler);
		}
		else {
			window.removeEventListener("keypress", self.keypressHandler);
		}
		
		if (self.showNavigationControls) {
			if (self.navigationOnKeypress) {
				if (event.keyCode==rightKey) {
					self.nextView();
				}
				if (event.keyCode==leftKey) {
					self.previousView();
				}
			}
		}
		else if (self.navigationOnKeypress) {
			if (event.keyCode==rightKey) {
				self.nextView();
			}
			if (event.keyCode==leftKey) {
				self.previousView();
			}
		}
	}

	///////////////////////////////////
	// GENERAL FUNCTIONS
	///////////////////////////////////

	self.getViewById = function(id) {
		id = id ? id.replace("#", "") : "";
		var view = self.viewIds.indexOf(id)!=-1 && self.getElement(id);
		return view;
	}

	self.getViewIds = function() {
		var viewIds = self.getViewPreferenceValue(document.body, self.prefix + "view-ids");
		var viewId = null;

		viewIds = viewIds!=null && viewIds!="" ? viewIds.split(",") : [];

		if (viewIds.length==0) {
			viewId = self.getViewPreferenceValue(document.body, self.prefix + "view-id");
			viewIds = viewId ? [viewId] : [];
		}

		return viewIds;
	}

	self.getInitialViewId = function() {
		var viewId = self.getViewPreferenceValue(document.body, self.prefix + "view-id");
		return viewId;
	}

	self.getApplicationStylesheet = function() {
		var stylesheetId = self.getViewPreferenceValue(document.body, self.prefix + "stylesheet-id");
		self.applicationStylesheet = document.getElementById("applicationStylesheet");
		return self.applicationStylesheet.sheet;
	}

	self.getVisibleView = function() {
		var viewIds = self.getViewIds();
		
		for (var i=0;i<viewIds.length;i++) {
			var viewId = viewIds[i].replace(/[\#?\.?](.*)/, "$" + "1");
			var view = self.getElement(viewId);
			var postName = "_Class";

			if (view==null && viewId && viewId.lastIndexOf(postName)!=-1) {
				view = self.getElement(viewId.replace(postName, ""));
			}
			
			if (view) {
				var display = getComputedStyle(view).display;
		
				if (display=="block" || display=="flex") {
					return view;
				}
			}
		}

		return null;
	}

	self.getInitialView = function() {
		var viewId = self.getInitialViewId();
		viewId = viewId.replace(/[\#?\.?](.*)/, "$" + "1");
		var view = self.getElement(viewId);
		var postName = "_Class";

		if (view==null && viewId && viewId.lastIndexOf(postName)!=-1) {
			view = self.getElement(viewId.replace(postName, ""));
		}

		return view;
	}

	self.getViewIndex = function(view) {
		var viewIds = self.getViewIds();
		var id = view ? view.id : null;
		var index = id && viewIds ? viewIds.indexOf(id) : -1;

		return index;
	}

	self.syncronizeViewToURL = function() {
		var fragment = window.location.hash;
		var view = self.getViewById(fragment);
		var index = view ? self.getViewIndex(view) : 0;
		if (index==-1) index = 0;
		var currentView = self.hideViews(index);

		if (self.supportsPopState && currentView) {

			if (fragment==null) {
				window.history.replaceState({name:currentView.id}, null, "#"+ currentView.id);
			}
			else {
				window.history.pushState({name:currentView.id}, null, "#"+ currentView.id);
			}
		}
		
		self.setViewVariables(view);
		return view;
	}

	/**
	 * Set the currentView or currentOverlay properties and set the lastView or lastOverlay properties
	 */
	self.setViewVariables = function(view, overlay, parentView) {
		if (view) {
			if (self.currentView) {
				self.lastView = self.currentView;
			}
			self.currentView = view;
		}

		if (overlay) {
			if (self.currentOverlay) {
				self.lastOverlay = self.currentOverlay;
			}
			self.currentOverlay = overlay;
		}
	}

	self.getViewPreferenceBoolean = function(view, property, altValue) {
		var computedStyle = window.getComputedStyle(view);
		var value = computedStyle.getPropertyValue(property);
		var type = typeof value;
		
		if (value=="true" || (type=="string" && value.indexOf("true")!=-1)) {
			return true;
		}
		else if (value=="" && arguments.length==3) {
			return altValue;
		}

		return false;
	}

	self.getViewPreferenceValue = function(view, property, defaultValue) {
		var value = window.getComputedStyle(view).getPropertyValue(property);

		if (value===undefined) {
			return defaultValue;
		}
		
		value = value.replace(/^[\s\"]*/, "");
		value = value.replace(/[\s\"]*$/, "");
		value = value.replace(/^[\s"]*(.*?)[\s"]*$/, function (match, capture) { 
			return capture;
		});

		return value;
	}

	self.getStyleRuleValue = function(cssRule, property) {
		var value = cssRule ? cssRule.style.getPropertyValue(property) : null;

		if (value===undefined) {
			return null;
		}
		
		value = value.replace(/^[\s\"]*/, "");
		value = value.replace(/[\s\"]*$/, "");
		value = value.replace(/^[\s"]*(.*?)[\s"]*$/, function (match, capture) { 
			return capture;
		});

		return value;
	}

	self.getCSSPropertyValueForElement = function(id, property) {
		var styleSheets = document.styleSheets;
		var numOfStylesheets = styleSheets.length;
		var values = [];
		var selectorIDText = "#" + id;
		var selectorClassText = "." + id + "_Class";
		var value;

		for(var i=0;i<numOfStylesheets;i++) {
			var styleSheet = styleSheets[i];
			var cssRules = self.getStylesheetRules(styleSheet);
			var numOfCSSRules = cssRules.length;
			var cssRule;
			
			for (var j=0;j<numOfCSSRules;j++) {
				cssRule = cssRules[j];
				
				if (cssRule.media) {
					var mediaRules = cssRule.cssRules;
					var numOfMediaRules = mediaRules ? mediaRules.length : 0;
					
					for(var k=0;k<numOfMediaRules;k++) {
						var mediaRule = mediaRules[k];
						
						if (mediaRule.selectorText==selectorIDText || mediaRule.selectorText==selectorClassText) {
							
							if (mediaRule.style && property in mediaRule.style) {
								value = mediaRule.style.getPropertyValue(property);
								values.push(value);
							}
						}
					}
				}
				else {

					if (cssRule.selectorText==selectorIDText || cssRule.selectorText==selectorClassText) {
						if (cssRule.style && property in cssRule.style) {
							value = cssRule.style.getPropertyValue(property);
							values.push(value);
						}
					}
				}
			}
		}
		
		return values.pop();
	}

	self.collectViews = function() {
		var viewIds = self.getViewIds();

		for (let index = 0; index < viewIds.length; index++) {
			const id = viewIds[index];
			const view = self.getViewById(id);
			//view && view.addEventListener("animationend", self.animationEndHandler);
			self.views[id] = view;
		}
		
		self.viewIds = viewIds;
	}

	self.collectOverlays = function() {
		var viewIds = self.getViewIds();
		var ids = [];

		for (let index = 0; index < viewIds.length; index++) {
			const id = viewIds[index];
			const view = self.getViewById(id);
			const isOverlay = view && self.isOverlay(view);
			
			if (isOverlay) {
				ids.push(id);
				self.overlays[id] = view;
			}
		}
		
		self.overlayIds = ids;
	}

	self.collectMediaQueries = function() {
		var viewIds = self.getViewIds();
		var styleSheet = self.getApplicationStylesheet();
		var cssRules = self.getStylesheetRules(styleSheet);
		var numOfCSSRules = cssRules ? cssRules.length : 0;
		var cssRule;
		var id = viewIds.length ? viewIds[0]: ""; // single view
		var selectorIDText = "#" + id;
		var selectorClassText = "." + id + "_Class";
		var viewsNotFound = viewIds.slice();
		var viewsFound = [];
		var selectorText = null;
		var property = self.prefix + "view-id";
		
		for (var j=0;j<numOfCSSRules;j++) {
			cssRule = cssRules[j];
			
			if (cssRule.media) {
				var mediaRules = cssRule.cssRules;
				var numOfMediaRules = mediaRules ? mediaRules.length : 0;
				
				for(var k=0;k<numOfMediaRules;k++) {
					var mediaRule = mediaRules[k];
					var mediaId = null;

					selectorText = mediaRule.selectorText;
					
					if (selectorText==".mediaViewInfo") {

						mediaId = self.getStyleRuleValue(mediaRule, property);

						self.addView(mediaId, cssRule);
						viewsFound.push(mediaId);

						if (viewsNotFound.indexOf(mediaId)!=-1) {
							viewsNotFound.splice(viewsNotFound.indexOf(mediaId));
						}

						break;
					}
				}
			}
			else {
				selectorText = cssRule.selectorText.replace(/[#|\s|*]?/g, "");

				if (viewIds.indexOf(selectorText)!=-1) {
					self.addView(selectorText, cssRule);

					if (viewsNotFound.indexOf(selectorText)!=-1) {
						viewsNotFound.splice(viewsNotFound.indexOf(selectorText));
					}

					break;
				}
			}
		}

		if (viewsNotFound.length) {
			console.log("Could not find the following views:" + viewsNotFound.join(",") + "");
			console.log("Views found:" + viewsFound.join(",") + "");
		}
	}

	/**
	 * Adds a view. A view object contains the id of the view and the style rule
	 * Use enableMediaQuery(rule) to enable
	 * An array of view names are in self.views array
	 */
	self.addView = function(name, cssRule, parentId) {
		var state = {name:name, rule:cssRule, id:name, parentId:parentId};
		self.addedViews.push(name);
		self.viewsDictionary[name] = state;
		self.mediaQueryDictionary[name] = cssRule;
	}

	self.hasView = function(name) {

		if (self.addedViews.indexOf(name)!=-1) {
			return true;
		}
		return false;
	}

	/**
	 * Go to view by id. Views are added in addView()
	 * @param {String} name id of view in current
	 * @param {String} parent id of parent view
	 * @param {Boolean} maintainPreviousState if true then do not hide other views
	 */
	self.goToView = function(name, maintainPreviousState, parent) {
		var state = self.viewsDictionary[name];

		if (state) {
			if (maintainPreviousState==false || maintainPreviousState==null) {
				self.hideViews();
			}
			self.enableMediaQuery(state.rule);
			self.updateViewLabel();
			self.updateURL();
		}
		else {
			var event = new Event(self.STATE_NOT_FOUND);
			self.stateName = name;
			window.dispatchEvent(event);
		}
	}

	/**
	 * Go to the view in the event targets CSS variable
	 */
	self.goToTargetView = function(event) {
		var button = event.currentTarget;
		var buttonComputedStyles = getComputedStyle(button);
		var actionTargetValue = buttonComputedStyles.getPropertyValue(self.prefix+"action-target").trim();
		var animation = buttonComputedStyles.getPropertyValue(self.prefix+"animation").trim();
		var targetType = buttonComputedStyles.getPropertyValue(self.prefix+"action-type").trim();
		var targetView = self.application ? null : self.getElement(actionTargetValue);
		var actionTargetStyles = targetView ? targetView.style : null;
		var state = self.viewsDictionary[actionTargetValue];
		
		// navigate to page
		if (self.application==false || targetType=="page") {
			document.location.href = "./" + actionTargetValue;
			return;
		}

		// if view is found
		if (targetView) {

			if (self.currentOverlay) {
				self.removeOverlay(false);
			}

			// add animation set in event target style declaration
			if (animation && self.supportAnimations) {
				self.crossFade(self.currentView, targetView, false, animation);
			}
			else {
				self.setViewVariables(self.currentView);
				self.hideViews();
				self.enableMediaQuery(state.rule);
				self.scaleViewIfNeeded(targetView);
				self.centerView(targetView);
				self.updateViewLabel();
				self.updateURL();
			}
		}
		else {
			var stateEvent = new Event(self.STATE_NOT_FOUND);
			self.stateName = name;
			window.dispatchEvent(stateEvent);
		}

		event.stopImmediatePropagation();
	}

	/**
	 * Cross fade between views
	 **/
	self.crossFade = function(from, to, update, animation) {
		var targetIndex = to.parentNode
		var fromIndex = Array.prototype.slice.call(from.parentElement.children).indexOf(from);
		var toIndex = Array.prototype.slice.call(to.parentElement.children).indexOf(to);

		if (from.parentNode==to.parentNode) {
			var reverse = self.getReverseAnimation(animation);
			var duration = self.getAnimationDuration(animation, true);

			// if target view is above (higher index)
			// then fade in target view 
			// and after fade in then hide previous view instantly
			if (fromIndex<toIndex) {
				self.setElementAnimation(from, null);
				self.setElementAnimation(to, null);
				self.showViewByMediaQuery(to);
				self.fadeIn(to, update, animation);

				setTimeout(function() {
					self.setElementAnimation(to, null);
					self.setElementAnimation(from, null);
					self.hideView(from);
					self.updateURL();
					self.setViewVariables(to);
					self.updateViewLabel();
				}, duration)
			}
			// if target view is on bottom
			// then show target view instantly 
			// and fade out current view
			else if (fromIndex>toIndex) {
				self.setElementAnimation(to, null);
				self.setElementAnimation(from, null);
				self.showViewByMediaQuery(to);
				self.fadeOut(from, update, reverse);

				setTimeout(function() {
					self.setElementAnimation(to, null);
					self.setElementAnimation(from, null);
					self.hideView(from);
					self.updateURL();
					self.setViewVariables(to);
				}, duration)
			}
		}
	}

	self.fadeIn = function(element, update, animation) {
		self.showViewByMediaQuery(element);

		if (update) {
			self.updateURL(element);

			element.addEventListener("animationend", function(event) {
				element.style.animation = null;
				self.setViewVariables(element);
				self.updateViewLabel();
				element.removeEventListener("animationend", arguments.callee);
			});
		}

		self.setElementAnimation(element, null);
		
		element.style.animation = animation;
	}

	self.fadeOutCurrentView = function(animation, update) {
		if (self.currentView) {
			self.fadeOut(self.currentView, update, animation);
		}
		if (self.currentOverlay) {
			self.fadeOut(self.currentOverlay, update, animation);
		}
	}

	self.fadeOut = function(element, update, animation) {
		if (update) {
			element.addEventListener("animationend", function(event) {
				element.style.animation = null;
				self.hideView(element);
				element.removeEventListener("animationend", arguments.callee);
			});
		}

		element.style.animationPlayState = "paused";
		element.style.animation = animation;
		element.style.animationPlayState = "running";
	}

	self.getReverseAnimation = function(animation) {
		if (animation && animation.indexOf("reverse")==-1) {
			animation += " reverse";
		}

		return animation;
	}

	/**
	 * Get duration in animation string
	 * @param {String} animation animation value
	 * @param {Boolean} inMilliseconds length in milliseconds if true
	 */
	self.getAnimationDuration = function(animation, inMilliseconds) {
		var duration = 0;
		var expression = /.+(\d\.\d)s.+/;

		if (animation && animation.match(expression)) {
			duration = parseFloat(animation.replace(expression, "$" + "1"));
			if (duration && inMilliseconds) duration = duration * 1000;
		}

		return duration;
	}

	self.setElementAnimation = function(element, animation, priority) {
		element.style.setProperty("animation", animation, "important");
	}

	self.getElement = function(id) {
		var elementId = id ? id.trim() : id;
		var element = elementId ? document.getElementById(elementId) : null;

		return element;
	}

	self.resizeHandler = function(event) {
		var view = self.getVisibleView();

		if (self.showByMediaQuery && view) {
			self.setViewOptions(view);
			self.setViewVariables(view);
		}
		else {
			self.scaleViewIfNeeded();
		}

		window.dispatchEvent(new Event(self.APPLICATION_RESIZE));
	}

	self.scaleViewIfNeeded = function(view) {

		if (self.scaleViewsOnResize) {
			if (view==null) {
				view = self.getVisibleView();
			}

			var isViewScaled = view.getAttributeNS(null, self.SIZE_STATE_NAME)=="false" ? false : true;

			if (isViewScaled) {
				self.scaleViewToFit(view, true);
			}
			else {
				self.scaleViewToActualSize(view);
			}
		}
		else if (view) {
			self.centerView(view);
		}
	}

	self.centerView = function(view) {

		if (self.scaleToFit) {
			self.scaleViewToFit(view, true);
		}
		else {
			self.scaleViewToActualSize(view);  // for centering support for now
		}
	}

	self.preventDoubleClick = function(event) {
		event.stopImmediatePropagation();
	}

	self.hashChangeHandler = function(event) {
		var fragment = window.location.hash ? window.location.hash.replace("#", "") : "";
		var view = self.getViewById(fragment);

		if (view) {
			self.hideViews();
			self.showView(view);
			self.setViewVariables(view);
			self.updateViewLabel();
			window.dispatchEvent(new Event(self.VIEW_CHANGE));
		}
		else {
			window.dispatchEvent(new Event(self.VIEW_NOT_FOUND));
		}
	}

	self.popStateHandler = function(event) {
		var state = event.state;
		var fragment = state ? state.name : window.location.hash;
		var view = self.getViewById(fragment);

		if (view) {
			self.hideViews();
			self.showView(view);
			self.updateViewLabel();
		}
		else {
			window.dispatchEvent(new Event(self.VIEW_NOT_FOUND));
		}
	}

	self.doubleClickHandler = function(event) {
		var view = self.getVisibleView();
		var scaleValue = view ? self.getViewScaleValue(view) : 1;
		var scaleNeededToFit = view ? self.getViewFitToViewportScale(view) : 1;
		var scaleNeededToFitWidth = view ? self.getViewFitToViewportWidthScale(view) : 1;
		var scaleNeededToFitHeight = view ? self.getViewFitToViewportHeightScale(view) : 1;
		var scaleToFitType = self.scaleToFitType;

		// Three scenarios
		// - scale to fit on double click
		// - set scale to actual size on double click
		// - switch between scale to fit and actual page size

		if (scaleToFitType=="width") {
			scaleNeededToFit = scaleNeededToFitWidth;
		}
		else if (scaleToFitType=="height") {
			scaleNeededToFit = scaleNeededToFitHeight;
		}

		// if scale and actual size enabled then switch between
		if (self.scaleToFitOnDoubleClick && self.actualSizeOnDoubleClick) {
			var isViewScaled = view.getAttributeNS(null, self.SIZE_STATE_NAME);
			var isScaled = false;
			
			// if scale is not 1 then view needs scaling
			if (scaleNeededToFit!=1) {

				// if current scale is at 1 it is at actual size
				// scale it to fit
				if (scaleValue==1) {
					self.scaleViewToFit(view);
					isScaled = true;
				}
				else {
					// scale is not at 1 so switch to actual size
					self.scaleViewToActualSize(view);
					isScaled = false;
				}
			}
			else {
				// view is smaller than viewport 
				// so scale to fit() is scale actual size
				// actual size and scaled size are the same
				// but call scale to fit to retain centering
				self.scaleViewToFit(view);
				isScaled = false;
			}
			
			view.setAttributeNS(null, self.SIZE_STATE_NAME, isScaled+"");
			isViewScaled = view.getAttributeNS(null, self.SIZE_STATE_NAME);
		}
		else if (self.scaleToFitOnDoubleClick) {
			self.scaleViewToFit(view);
		}
		else if (self.actualSizeOnDoubleClick) {
			self.scaleViewToActualSize(view);
		}

	}

	self.scaleViewToFit = function(view) {
		return self.setViewScaleValue(view, true);
	}

	self.scaleViewToActualSize = function(view) {
		self.setViewScaleValue(view, false, 1);
	}

	self.onloadHandler = function(event) {
		self.initialize();
	}

	self.getStackArray = function(error) {
		var value = "";
		
		if (error==null) {
		  try {
			 error = new Error("Stack");
		  }
		  catch (e) {
			 
		  }
		}
		
		if ("stack" in error) {
		  value = error.stack;
		  var methods = value.split(/\n/g);
	 
		  var newArray = methods ? methods.map(function (value, index, array) {
			 value = value.replace(/\@.*/,"");
			 return value;
		  }) : null;
	 
		  if (newArray && newArray[0].includes("getStackTrace")) {
			 newArray.shift();
		  }
		  if (newArray && newArray[0].includes("getStackArray")) {
			 newArray.shift();
		  }
		  if (newArray && newArray[0]=="") {
			 newArray.shift();
		  }
	 
			return newArray;
		}
		
		return null;
	}

	self.log = function(value) {
		console.log.apply(this, [value]);
	}
	
	// initialize on load
	// sometimes the body size is 0 so we call this now and again later
	window.addEventListener("load", self.onloadHandler);
	window.document.addEventListener("DOMContentLoaded", self.onloadHandler);
}

window.application = new Application();
</script>
</head>
<body>
<div id="resume">
	<div id="Group_30">
		<div id="Group_3">
			<div id="Group_1">
				<svg class="Rectangle_1">
					<rect fill="rgba(26,24,24,1)" id="Rectangle_1" rx="0" ry="0" x="0" y="0" width="1044.505" height="1085.464">
					</rect>
				</svg>
			</div>
			<div id="Group_2">
				<svg class="Rectangle_2">
					<rect fill="rgba(0,0,0,0)" stroke="rgba(26,24,24,1)" stroke-width="1px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Rectangle_2" rx="0" ry="0" x="0" y="0" width="1044.505" height="1085.464">
					</rect>
				</svg>
			</div>
		</div>
		<svg class="Rectangle_3">
			<rect fill="rgba(37,83,22,1)" id="Rectangle_3" rx="0" ry="0" x="0" y="0" width="51.633" height="51.633">
			</rect>
		</svg>
		<svg class="Rectangle_4">
			<rect fill="rgba(38,38,38,1)" id="Rectangle_4" rx="0" ry="0" x="0" y="0" width="51.633" height="51.633">
			</rect>
		</svg>
		<svg class="Rectangle_5">
			<rect fill="rgba(110,34,0,1)" id="Rectangle_5" rx="0" ry="0" x="0" y="0" width="51.633" height="51.633">
			</rect>
		</svg>
		<svg class="Rectangle_6">
			<rect fill="rgba(7,16,55,1)" id="Rectangle_6" rx="0" ry="0" x="0" y="0" width="51.633" height="51.633">
			</rect>
		</svg>
		<svg class="Rectangle_7">
			<rect fill="rgba(26,24,24,1)" id="Rectangle_7" rx="0" ry="0" x="0" y="0" width="51.633" height="51.633">
			</rect>
		</svg>
		<svg class="Rectangle_8">
			<rect fill="rgba(26,24,24,1)" id="Rectangle_8" rx="0" ry="0" x="0" y="0" width="51.633" height="51.633">
			</rect>
		</svg>
		<svg class="Rectangle_9_t">
			<linearGradient id="Rectangle_9_t" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#343c86" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#4c8133" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_9_t)" id="Rectangle_9_t" rx="0" ry="0" x="0" y="0" width="397.003" height="144.573">
			</rect>
		</svg>
		<svg class="Rectangle_10">
			<rect fill="rgba(0,38,51,1)" id="Rectangle_10" rx="0" ry="0" x="0" y="0" width="1044.836" height="142.662">
			</rect>
		</svg>
		<svg class="Rectangle_11">
			<rect fill="rgba(0,38,51,1)" id="Rectangle_11" rx="0" ry="0" x="0" y="0" width="1048.111" height="328.815">
			</rect>
		</svg>
		<svg class="Rectangle_12">
			<rect fill="rgba(0,38,51,1)" id="Rectangle_12" rx="0" ry="0" x="0" y="0" width="519.469" height="161.785">
			</rect>
		</svg>
		<svg class="Rectangle_13">
			<rect fill="rgba(0,38,51,1)" id="Rectangle_13" rx="0" ry="0" x="0" y="0" width="506.373" height="161.536">
			</rect>
		</svg>
		<svg class="Rectangle_14">
			<rect fill="rgba(0,38,51,1)" id="Rectangle_14" rx="0" ry="0" x="0" y="0" width="522.071" height="261.279">
			</rect>
		</svg>
		<svg class="Rectangle_15">
			<rect fill="rgba(0,38,51,1)" id="Rectangle_15" rx="0" ry="0" x="0" y="0" width="505.831" height="267.561">
			</rect>
		</svg>
		<div id="NOTETAKER____________Assisted__gp">
			<span>NOTETAKER</span><br><span style="font-family:Helvetica;color:rgba(255,255,255,1);">	</span><br><span style="font-family:Helvetica;font-size:9px;color:rgba(255,255,255,1);">         Assisted disabled students<br/>two and Informed them with their daily homework. Tutored them when they need any help. I also recorded updated, organized, and professional notes and outlines.</span><br>
		</div>
		<div id="Group_5">
			<div id="Group_4">
			<svg style="width:inherit;height:inherit;overflow:visible;">
				<rect fill="url(#Group_4_jn_pattern)" width="100%" height="100%"></rect>
					<pattern elementId="Group_4_jn" id="Group_4_jn_pattern" x="0" y="0" width="100%" height="100%">
						<image x="0" y="0" width="100%" height="100%" href="Group_4_jn_pattern.png" xlink:href="Group_4_jn_pattern.png"></image>
					</pattern>
					</svg>
				</div>
			<svg class="Ellipse_2">
				<ellipse fill="rgba(0,0,0,0)" stroke="rgba(112,112,112,1)" stroke-width="1px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Ellipse_2" rx="72.60044860839844" ry="72.60044860839844" cx="72.60044860839844" cy="72.60044860839844">
				</ellipse>
			</svg>
		</div>
		<svg class="Rectangle_17_">
			<linearGradient id="Rectangle_17_" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_17_)" id="Rectangle_17_" rx="3.685936212539673" ry="3.685936212539673" x="0" y="0" width="27.914" height="7.372">
			</rect>
		</svg>
		<svg class="Rectangle_18_">
			<linearGradient id="Rectangle_18_" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_18_)" id="Rectangle_18_" rx="3.685936212539673" ry="3.685936212539673" x="0" y="0" width="27.914" height="7.372">
			</rect>
		</svg>
		<svg class="Rectangle_19_bb">
			<linearGradient id="Rectangle_19_bb" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_19_bb)" id="Rectangle_19_bb" rx="3.685936212539673" ry="3.685936212539673" x="0" y="0" width="27.914" height="7.372">
			</rect>
		</svg>
		<svg class="Rectangle_20_bd">
			<linearGradient id="Rectangle_20_bd" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_20_bd)" id="Rectangle_20_bd" rx="3.685936212539673" ry="3.685936212539673" x="0" y="0" width="46.667" height="7.372">
			</rect>
		</svg>
		<svg class="Ellipse_3_bf">
			<linearGradient id="Ellipse_3_bf" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<ellipse fill="url(#Ellipse_3_bf)" id="Ellipse_3_bf" rx="3.824693441390991" ry="3.824693441390991" cx="3.824693441390991" cy="3.824693441390991">
			</ellipse>
		</svg>
		<svg class="Ellipse_4_bh">
			<linearGradient id="Ellipse_4_bh" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<ellipse fill="url(#Ellipse_4_bh)" id="Ellipse_4_bh" rx="3.824693441390991" ry="3.824693441390991" cx="3.824693441390991" cy="3.824693441390991">
			</ellipse>
		</svg>
		<svg class="Ellipse_5_bj">
			<linearGradient id="Ellipse_5_bj" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<ellipse fill="url(#Ellipse_5_bj)" id="Ellipse_5_bj" rx="3.824693441390991" ry="3.824693441390991" cx="3.824693441390991" cy="3.824693441390991">
			</ellipse>
		</svg>
		<svg class="Ellipse_6_bl">
			<linearGradient id="Ellipse_6_bl" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<ellipse fill="url(#Ellipse_6_bl)" id="Ellipse_6_bl" rx="3.824693441390991" ry="3.824693441390991" cx="3.824693441390991" cy="3.824693441390991">
			</ellipse>
		</svg>
		<svg class="Rectangle_21_bn">
			<linearGradient id="Rectangle_21_bn" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_21_bn)" id="Rectangle_21_bn" rx="3.685936212539673" ry="3.685936212539673" x="0" y="0" width="53.272" height="7.372">
			</rect>
		</svg>
		<div id="RAQUEL_LARIOS">
			<span>RAQUEL</span><span style="font-family:MyriadPro-Regular;"> </span><span style="font-family:Helvetica-Light;">LARIOS</span>
		</div>
		<div id="Group_8">
			<img id="Rectangle_22" src="Rectangle_22.png" srcset="Rectangle_22.png 1x, Rectangle_22@2x.png 2x">
			<div id="Group_7">
				<div id="Group_6">
					<svg class="Rectangle_23">
						<rect fill="rgba(115,153,122,1)" id="Rectangle_23" rx="0" ry="0" x="0" y="0" width="94.246" height="93.749">
						</rect>
					</svg>
					<svg class="Path_1" viewBox="685.278 -570.845 94.246 93.749">
						<path fill="rgba(141,173,147,1)" id="Path_1" d="M 779.5239868164062 -477.0960083007812 L 685.2780151367188 -477.0960083007812 L 685.2780151367188 -570.844970703125 L 763.7739868164062 -570.844970703125 C 772.4719848632812 -570.844970703125 779.5239868164062 -563.7930297851562 779.5239868164062 -555.093994140625 L 779.5239868164062 -477.0960083007812 Z">
						</path>
					</svg>
					<svg class="Path_2" viewBox="496.786 -570.845 94.246 93.749">
						<path fill="rgba(83,109,87,1)" id="Path_2" d="M 591.031982421875 -477.0960083007812 L 496.7860107421875 -477.0960083007812 L 496.7860107421875 -555.7760009765625 C 496.7860107421875 -564.0980224609375 503.5320129394531 -570.844970703125 511.85400390625 -570.844970703125 L 591.031982421875 -570.844970703125 L 591.031982421875 -477.0960083007812 Z">
						</path>
					</svg>
					<svg class="Path_3" viewBox="496.786 -477.096 282.738 46.875">
						<path fill="rgba(224,224,223,1)" id="Path_3" d="M 763.427978515625 -430.2210083007812 L 512.8809814453125 -430.2210083007812 C 503.9920043945312 -430.2210083007812 496.7860107421875 -437.427001953125 496.7860107421875 -446.3169860839844 L 496.7860107421875 -477.0960083007812 L 779.5239868164062 -477.0960083007812 L 779.5239868164062 -446.3169860839844 C 779.5239868164062 -437.427001953125 772.3179931640625 -430.2210083007812 763.427978515625 -430.2210083007812 Z">
						</path>
					</svg>
					<div id="ID9ABAA4">
						<span>9ABAA4</span>
					</div>
					<div id="_81A98D">
						<span>#81A98D</span>
					</div>
					<div id="_617F6A">
						<span>#617F6A</span>
					</div>
				</div>
			</div>
		</div>
		<div id="Group_11">
			<img id="Rectangle_24" src="Rectangle_24.png" srcset="Rectangle_24.png 1x, Rectangle_24@2x.png 2x">
			<div id="Group_10">
				<div id="Group_9">
					<svg class="Rectangle_25">
						<rect fill="rgba(0,52,70,1)" id="Rectangle_25" rx="0" ry="0" x="0" y="0" width="94.544" height="94.045">
						</rect>
					</svg>
					<svg class="Path_4" viewBox="-147.512 539.867 94.544 94.045">
						<path fill="rgba(39,88,103,1)" id="Path_4" d="M -52.96799850463867 633.9119873046875 L -147.5119934082031 633.9119873046875 L -147.5119934082031 539.8670043945312 L -68.71900177001953 539.8670043945312 C -60.02000045776367 539.8670043945312 -52.96799850463867 546.9190063476562 -52.96799850463867 555.6179809570312 L -52.96799850463867 633.9119873046875 Z">
						</path>
					</svg>
					<svg class="Path_5" viewBox="-336.599 539.867 94.543 94.045">
						<path fill="rgba(0,38,51,1)" id="Path_5" d="M -242.0559997558594 633.9119873046875 L -336.5989990234375 633.9119873046875 L -336.5989990234375 554.9359741210938 C -336.5989990234375 546.614013671875 -329.8529968261719 539.8670043945312 -321.531005859375 539.8670043945312 L -242.0559997558594 539.8670043945312 L -242.0559997558594 633.9119873046875 Z">
						</path>
					</svg>
					<svg class="Path_6" viewBox="-336.599 633.912 283.631 47.023">
						<path fill="rgba(224,224,223,1)" id="Path_6" d="M -68.88200378417969 680.9349975585938 L -320.6860046386719 680.9349975585938 C -329.4750061035156 680.9349975585938 -336.5989990234375 673.8099975585938 -336.5989990234375 665.02197265625 L -336.5989990234375 633.9119873046875 L -52.96799850463867 633.9119873046875 L -52.96799850463867 665.02197265625 C -52.96799850463867 673.8099975585938 -60.09299850463867 680.9349975585938 -68.88200378417969 680.9349975585938 Z">
						</path>
					</svg>
					<div id="_336979">
						<span>#336979</span>
					</div>
					<div id="_004358">
						<span>#004358</span>
					</div>
					<div id="_003242">
						<span>#003242</span>
					</div>
				</div>
			</div>
		</div>
		<div id="Group_17">
			<img id="Rectangle_26" src="Rectangle_26.png" srcset="Rectangle_26.png 1x, Rectangle_26@2x.png 2x">
			<div id="Group_16">
				<div id="Group_15">
					<div id="Group_12">
						<svg class="Rectangle_27">
							<rect fill="rgba(224,224,223,1)" id="Rectangle_27" rx="0" ry="0" x="0" y="0" width="94.95" height="47.225">
							</rect>
						</svg>
						<svg class="Rectangle_28">
							<rect fill="rgba(192,192,191,1)" id="Rectangle_28" rx="0" ry="0" x="0" y="0" width="94.951" height="94.45">
							</rect>
						</svg>
						<div id="_CBCBCB">
							<span>#CBCBCB</span>
						</div>
					</div>
					<div id="Group_13">
						<svg class="Path_7" viewBox="-645.147 636.607 94.95 47.225">
							<path fill="rgba(224,224,223,1)" id="Path_7" d="M -550.197021484375 683.8319702148438 L -629.1019897460938 683.8319702148438 C -637.9630126953125 683.8319702148438 -645.14697265625 676.6480102539062 -645.14697265625 667.7860107421875 L -645.14697265625 636.6069946289062 L -550.197021484375 636.6069946289062 L -550.197021484375 683.8319702148438 Z">
							</path>
						</svg>
						<svg class="Path_8" viewBox="-645.147 542.157 94.951 94.45">
							<path fill="rgba(84,84,84,1)" id="Path_8" d="M -550.1959838867188 636.6069946289062 L -645.14697265625 636.6069946289062 L -645.14697265625 558.4080200195312 C -645.14697265625 549.4329833984375 -637.8709716796875 542.156982421875 -628.89599609375 542.156982421875 L -550.1959838867188 542.156982421875 L -550.1959838867188 636.6069946289062 Z">
							</path>
						</svg>
						<div id="_666666">
							<span>#666666</span>
						</div>
					</div>
					<div id="Group_14">
						<svg class="Path_9" viewBox="-455.246 636.607 94.951 47.225">
							<path fill="rgba(224,224,223,1)" id="Path_9" d="M -376.9960021972656 683.8319702148438 L -455.2460021972656 683.8319702148438 L -455.2460021972656 636.6069946289062 L -360.2950134277344 636.6069946289062 L -360.2950134277344 667.1309814453125 C -360.2950134277344 676.35498046875 -367.7720031738281 683.8319702148438 -376.9960021972656 683.8319702148438 Z">
							</path>
						</svg>
						<svg class="Path_10" viewBox="-455.246 542.157 94.951 94.45">
							<path fill="rgba(255,255,255,1)" id="Path_10" d="M -360.2950134277344 636.6069946289062 L -455.2460021972656 636.6069946289062 L -455.2460021972656 542.156982421875 L -376.3940124511719 542.156982421875 C -367.5029907226562 542.156982421875 -360.2950134277344 549.364990234375 -360.2950134277344 558.2559814453125 L -360.2950134277344 636.6069946289062 Z">
							</path>
						</svg>
						<div id="_FFFFFF">
							<span>#FFFFFF</span>
						</div>
					</div>
				</div>
			</div>
		</div>
		<div id="VISUAL_COMMUNICATION_DESIGNER">
			<span>VISUAL COMMUNICATION DESIGNER</span>
		</div>
		<div id="ABOUT_ME">
			<span>ABOUT ME</span>
		</div>
		<div id="JOB_HISTORY">
			<span>JOB HISTORY</span>
		</div>
		<div id="_EXPERIENCE___PROJECT">
			<span> EXPERIENCE & PROJECT</span>
		</div>
		<div id="_SKILLS">
			<span> SKILLS</span>
		</div>
		<div id="_REFRENCE">
			<span> REFRENCE</span>
		</div>
		<div id="_EDUCATION">
			<span> EDUCATION</span>
		</div>
		<div id="Lorem_ipsum_dolor_sit_amet__co">
			<span>Lorem ipsum dolor sit amet, consectetuer adipiscing elit, sed diam nonummy nibh euismod tincidunt ut laoreet dolore magna aliquam erat volutpat. Ut wisi enim ad minim veniam, quis nostrud exerci tation ullamcorper suscipit lobortis nisl ut </span>
		</div>
		<div id="Group_18">
			<svg class="Rectangle_29">
				<rect fill="rgba(0,0,0,0)" stroke="rgba(165,165,165,1)" stroke-width="2px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Rectangle_29" rx="6.002915382385254" ry="6.002915382385254" x="0" y="0" width="24.436" height="23.976">
				</rect>
			</svg>
			<svg class="Path_11" viewBox="358.205 172.535 22.776 13.206">
				<path fill="rgba(0,0,0,0)" stroke="rgba(165,165,165,1)" stroke-width="2px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Path_11" d="M 380.9809875488281 172.5350036621094 L 370.9490051269531 184.9799957275391 C 370.1300048828125 185.9949951171875 369.0549926757812 185.9949951171875 368.2359924316406 184.9799957275391 L 358.2049865722656 172.5350036621094">
				</path>
			</svg>
		</div>
		<div id="Group_20">
			<svg class="Ellipse_7">
				<ellipse fill="rgba(0,0,0,0)" stroke="rgba(165,165,165,1)" stroke-width="2px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Ellipse_7" rx="12.733057975769043" ry="12.14912223815918" cx="12.733057975769043" cy="12.14912223815918">
				</ellipse>
			</svg>
			<div id="Group_19">
				<svg class="Path_12" viewBox="485.713 214.343 11.157 10.739">
					<path fill="rgba(165,165,165,1)" id="Path_12" d="M 485.9769897460938 222.77099609375 C 487.2969970703125 225.5839996337891 494.7219848632812 226.0749969482422 496.4849853515625 222.8699951171875 C 497.9309997558594 220.2409973144531 495.0719909667969 214.85400390625 491.8720092773438 214.3869934082031 C 489.9960021972656 214.1139984130859 488.4440002441406 215.14599609375 487.1690063476562 216.8849945068359 C 485.8940124511719 218.6230010986328 485.343994140625 221.4219970703125 485.9769897460938 222.77099609375 Z">
					</path>
				</svg>
				<svg class="Ellipse_8">
					<ellipse fill="rgba(165,165,165,1)" id="Ellipse_8" rx="4.255010604858398" ry="4.255010604858398" cx="4.255010604858398" cy="4.255010604858398">
					</ellipse>
				</svg>
			</div>
		</div>
		<svg class="Ellipse_9">
			<ellipse fill="rgba(0,0,0,0)" stroke="rgba(165,165,165,1)" stroke-width="2px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Ellipse_9" rx="12.908926010131836" ry="12.908926010131836" cx="12.908926010131836" cy="12.908926010131836">
			</ellipse>
		</svg>
		<div id="Group_23">
			<div id="Group_21">
				<svg class="Path_13" viewBox="487.167 173.448 10.183 9.179">
					<path fill="rgba(165,165,165,1)" id="Path_13" d="M 492.2579956054688 173.447998046875 C 489.4460144042969 173.447998046875 487.1669921875 175.5030059814453 487.1669921875 178.0379943847656 C 487.1669921875 178.6219940185547 487.2869873046875 179.1799926757812 487.5079956054688 179.6940002441406 C 488.2449951171875 181.4100036621094 490.093994140625 182.6269989013672 492.2579956054688 182.6269989013672 C 495.0700073242188 182.6269989013672 497.3500061035156 180.572998046875 497.3500061035156 178.0379943847656 C 497.3500061035156 175.5030059814453 495.0700073242188 173.447998046875 492.2579956054688 173.447998046875 Z">
					</path>
				</svg>
			</div>
			<div id="Group_22">
				<svg class="Path_14" viewBox="487.167 173.448 10.183 9.179">
					<path fill="rgba(0,0,0,0)" stroke="rgba(165,165,165,1)" stroke-width="1px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Path_14" d="M 492.2579956054688 173.447998046875 C 489.4460144042969 173.447998046875 487.1669921875 175.5030059814453 487.1669921875 178.0379943847656 C 487.1669921875 178.6219940185547 487.2869873046875 179.1799926757812 487.5079956054688 179.6940002441406 C 488.2449951171875 181.4100036621094 490.093994140625 182.6269989013672 492.2579956054688 182.6269989013672 C 495.0700073242188 182.6269989013672 497.3500061035156 180.572998046875 497.3500061035156 178.0379943847656 C 497.3500061035156 175.5030059814453 495.0700073242188 173.447998046875 492.2579956054688 173.447998046875 Z">
					</path>
				</svg>
			</div>
		</div>
		<div id="Group_26">
			<div id="Group_24">
				<svg class="Path_15" viewBox="487.918 177.308 9.084 11.905">
					<path fill="rgba(165,165,165,1)" id="Path_15" d="M 494.9739990234375 177.3079986572266 L 490.4450073242188 177.3079986572266 C 488.5859985351562 177.3079986572266 487.3659973144531 179.1369934082031 488.1700134277344 180.7149963378906 L 492.5039978027344 189.2129974365234 L 496.8269958496094 179.9880065917969 C 497.4190063476562 178.7259979248047 496.43798828125 177.3079986572266 494.9739990234375 177.3079986572266 Z">
					</path>
				</svg>
			</div>
			<div id="Group_25">
				<svg class="Path_16" viewBox="487.918 177.308 9.084 11.905">
					<path fill="rgba(0,0,0,0)" stroke="rgba(165,165,165,1)" stroke-width="1px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Path_16" d="M 494.9739990234375 177.3079986572266 L 490.4450073242188 177.3079986572266 C 488.5859985351562 177.3079986572266 487.3659973144531 179.1369934082031 488.1700134277344 180.7149963378906 L 492.5039978027344 189.2129974365234 L 496.8269958496094 179.9880065917969 C 497.4190063476562 178.7259979248047 496.43798828125 177.3079986572266 494.9739990234375 177.3079986572266 Z">
					</path>
				</svg>
			</div>
		</div>
		<div id="ID16141_Doublegrove__La_Puente">
			<span>16141 Doublegrove, La Puente,<br/>Zip Code 91744</span>
		</div>
		<div id="_626__559_4462">
			<span>(626) 559-4462</span>
		</div>
		<div id="relarios_cpp_com">
			<span>relarios@cpp.com</span>
		</div>
		<div id="oo00ff_">
			<span>oo00ff_</span>
		</div>
		<div id="Group_27">
			<svg class="Rectangle_30">
				<rect fill="rgba(0,0,0,0)" stroke="rgba(165,165,165,1)" stroke-width="2px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Rectangle_30" rx="3.537400245666504" ry="3.537400245666504" x="0" y="0" width="23.739" height="23.739">
				</rect>
			</svg>
			<svg class="Ellipse_10">
				<ellipse fill="rgba(0,0,0,0)" stroke="rgba(150,153,156,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Ellipse_10" rx="4.589632034301758" ry="4.589632034301758" cx="4.589632034301758" cy="4.589632034301758">
				</ellipse>
			</svg>
			<svg class="Ellipse_11">
				<ellipse fill="rgba(150,153,156,1)" id="Ellipse_11" rx="1.2211753129959106" ry="1.2211753129959106" cx="1.2211753129959106" cy="1.2211753129959106">
				</ellipse>
			</svg>
		</div>
		<div id="Group_29">
			<div id="Group_28">
				<svg class="Path_17" viewBox="69.174 357.46 909.248 46.879">
					<path fill="rgba(0,0,0,0)" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Path_17" d="M 978.4219970703125 382.4620056152344 L 922.791015625 357.4599914550781 L 922.791015625 369.5360107421875 L 80.42500305175781 369.5360107421875 C 74.21099853515625 369.5360107421875 69.17400360107422 374.572998046875 69.17400360107422 380.7869873046875 C 69.17400360107422 387.0010070800781 74.21099853515625 392.0379943847656 80.42500305175781 392.0379943847656 L 922.791015625 392.0379943847656 L 922.791015625 404.3389892578125 L 978.4219970703125 382.4620056152344 Z">
					</path>
				</svg>
			</div>
		</div>
		<svg class="Rectangle_31_du">
			<linearGradient id="Rectangle_31_du" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_31_du)" id="Rectangle_31_du" rx="10.481303215026855" ry="10.481303215026855" x="0" y="0" width="92.079" height="20.963">
			</rect>
		</svg>
		<svg class="Rectangle_32_dw">
			<linearGradient id="Rectangle_32_dw" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_32_dw)" id="Rectangle_32_dw" rx="10.481303215026855" ry="10.481303215026855" x="0" y="0" width="92.079" height="20.963">
			</rect>
		</svg>
		<svg class="Rectangle_33_dy">
			<linearGradient id="Rectangle_33_dy" spreadMethod="pad" x1="0" x2="1" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_33_dy)" id="Rectangle_33_dy" rx="10.481303215026855" ry="10.481303215026855" x="0" y="0" width="92.079" height="20.963">
			</rect>
		</svg>
		<svg class="Line_1" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_1" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_2" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_2" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_3" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_3" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_4" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_4" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_5" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_5" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_6" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_6" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_7" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_7" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_8" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_8" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_9" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_9" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_10" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_10" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_11" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_11" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_12" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_12" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_13" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_13" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_14" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_14" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_15" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_15" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_16" viewBox="0 0 0.574 72.775">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_16" d="M 0 0 L 0.5737752914428711 72.77516937255859">
			</path>
		</svg>
		<svg class="Line_17" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_17" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_18" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_18" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_19" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_19" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_20" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_20" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_21" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_21" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_22" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_22" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_23" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_23" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_24" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_24" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_25" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_25" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_26" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_26" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_27" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_27" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_28" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_28" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_29" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_29" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_30" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_30" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_31" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_31" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_32" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_32" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_33" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_33" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_34" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_34" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_35" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_35" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_36" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_36" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_37" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_37" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_38" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_38" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_39" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_39" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_40" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_40" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_41" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_41" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_42" viewBox="0 0 0.173 72.463">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_42" d="M 0 0 L 0.1726047694683075 72.46254730224609">
			</path>
		</svg>
		<svg class="Line_43" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_43" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_44" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_44" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_45" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_45" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_46" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_46" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_47" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_47" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_48" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_48" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_49" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_49" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_50" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_50" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_51" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_51" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_52" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_52" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_53" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_53" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_54" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_54" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_55" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_55" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_56" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_56" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_57" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_57" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_58" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_58" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_59" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_59" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_60" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_60" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_61" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_61" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_62" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_62" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_63" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_63" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_64" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_64" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_65" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_65" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_66" viewBox="0 0 0.425 76.797">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_66" d="M 0 0 L 0.4246059656143188 76.79669952392578">
			</path>
		</svg>
		<svg class="Line_67" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_67" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_68" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_68" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_69" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_69" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_70" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_70" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_71" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_71" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_72" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_72" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_73" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_73" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_74" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_74" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_75" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_75" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_76" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_76" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_77" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_77" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_78" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_78" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_79" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_79" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Line_80" viewBox="0 0 3 22.374">
			<path fill="transparent" stroke="rgba(112,112,112,1)" stroke-width="3px" stroke-linejoin="miter" stroke-linecap="butt" stroke-miterlimit="10" shape-rendering="auto" id="Line_80" d="M 0 0 L 0 22.37445640563965">
			</path>
		</svg>
		<svg class="Rectangle_34">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_34" rx="0" ry="0" x="0" y="0" width="190.515" height="127.649">
			</rect>
		</svg>
		<svg class="Rectangle_35">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_35" rx="0" ry="0" x="0" y="0" width="190.515" height="127.649">
			</rect>
		</svg>
		<svg class="Rectangle_36">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_36" rx="0" ry="0" x="0" y="0" width="190.515" height="123.92">
			</rect>
		</svg>
		<svg class="Path_18" viewBox="221.343 327.48 74.199 28.111">
			<path fill="rgba(141,173,147,1)" id="Path_18" d="M 288.2439880371094 327.4800109863281 L 228.6410064697266 327.4800109863281 C 224.6100006103516 327.4800109863281 221.3430023193359 329.4750061035156 221.3430023193359 331.9360046386719 L 221.3430023193359 339.0549926757812 C 221.3430023193359 341.5150146484375 224.6100006103516 343.510009765625 228.6410064697266 343.510009765625 L 245.6889953613281 343.510009765625 L 257.4909973144531 355.5910034179688 L 270.4540100097656 343.510009765625 L 288.2439880371094 343.510009765625 C 292.2739868164062 343.510009765625 295.5419921875 341.5150146484375 295.5419921875 339.0549926757812 L 295.5419921875 331.9360046386719 C 295.5419921875 329.4750061035156 292.2739868164062 327.4800109863281 288.2439880371094 327.4800109863281 Z">
			</path>
		</svg>
		<div id="ID2016___2017">
			<span>2016 - 2017</span>
		</div>
		<svg class="Path_19" viewBox="461.343 327.48 74.199 28.111">
			<path fill="rgba(141,173,147,1)" id="Path_19" d="M 528.2440185546875 327.4800109863281 L 468.6409912109375 327.4800109863281 C 464.6099853515625 327.4800109863281 461.3429870605469 329.4750061035156 461.3429870605469 331.9360046386719 L 461.3429870605469 339.0549926757812 C 461.3429870605469 341.5150146484375 464.6099853515625 343.510009765625 468.6409912109375 343.510009765625 L 485.6889953613281 343.510009765625 L 497.4909973144531 355.5910034179688 L 510.4540100097656 343.510009765625 L 528.2440185546875 343.510009765625 C 532.2739868164062 343.510009765625 535.5419921875 341.5150146484375 535.5419921875 339.0549926757812 L 535.5419921875 331.9360046386719 C 535.5419921875 329.4750061035156 532.2739868164062 327.4800109863281 528.2440185546875 327.4800109863281 Z">
			</path>
		</svg>
		<div id="ID2018___2019">
			<span>2018 - 2019</span>
		</div>
		<svg class="Path_20" viewBox="691.343 327.48 74.199 28.111">
			<path fill="rgba(141,173,147,1)" id="Path_20" d="M 758.2440185546875 327.4800109863281 L 698.6409912109375 327.4800109863281 C 694.6099853515625 327.4800109863281 691.343017578125 329.4750061035156 691.343017578125 331.9360046386719 L 691.343017578125 339.0549926757812 C 691.343017578125 341.5150146484375 694.6099853515625 343.510009765625 698.6409912109375 343.510009765625 L 715.6890258789062 343.510009765625 L 727.4910278320312 355.5910034179688 L 740.4539794921875 343.510009765625 L 758.2440185546875 343.510009765625 C 762.2739868164062 343.510009765625 765.5419921875 341.5150146484375 765.5419921875 339.0549926757812 L 765.5419921875 331.9360046386719 C 765.5419921875 329.4750061035156 762.2739868164062 327.4800109863281 758.2440185546875 327.4800109863281 Z">
			</path>
		</svg>
		<div id="ID2019___2020">
			<span>2019 - 2020</span>
		</div>
		<svg class="Ellipse_12">
			<ellipse fill="rgba(26,24,24,1)" id="Ellipse_12" rx="3.859055995941162" ry="4.055371284484863" cx="3.859055995941162" cy="4.055371284484863">
			</ellipse>
		</svg>
		<div id="SPANISH">
			<span>SPANISH</span>
		</div>
		<div id="PHOTHOSHOP">
			<span>PHOTHOSHOP</span>
		</div>
		<div id="GITHUB">
			<span>GITHUB</span>
		</div>
		<div id="ADOBE_ILLUTRATOR">
			<span>ADOBE ILLUTRATOR</span>
		</div>
		<div id="ADOBE_XD">
			<span>ADOBE XD</span>
		</div>
		<div id="VISUAL_STUDIO">
			<span>VISUAL STUDIO</span>
		</div>
		<div id="POLAR_PUFF_____Made_ice_cream_">
			<span>POLAR PUFF</span><br><span style="font-family:Helvetica;color:rgba(255,255,255,1);">	</span><br><span style="font-family:Helvetica;font-size:9px;color:rgba(255,255,255,1);">  Made ice cream cones, milkshakes and other orders for customers according to their request. Explained local ingredient sources, the importance of sustainability, and product nutritional information with a focus on gluten-free and dairy-free foods. Also designed their poster on Photoshop.</span>
		</div>
		<div id="SNAK_KING__________Worked_in_a">
			<span>SNAK-KING</span><br><span style="font-family:Helvetica;color:rgba(255,255,255,1);">	</span><br><span style="font-family:Helvetica;font-size:9px;color:rgba(255,255,255,1);">       Worked in a warehouse as packager and made sure lables were on and restoked properly. Made sure that labels and orders are correct.</span>
		</div>
		<div id="NOTETAKER____________Assisted__gp">
			<span>NOTETAKER</span><br><span style="font-family:Helvetica;color:rgba(255,255,255,1);">	</span><br><span style="font-family:Helvetica;font-size:9px;color:rgba(255,255,255,1);">         Assisted disabled students<br/>two and Informed them with their daily homework. Tutored them when they need any help. I also recorded updated, organized, and professional notes and outlines.</span><br>
		</div>
		<div id="Group">
			<div id="MANOJ_J">
				<span>MANOJ J</span>
			</div>
			<div id="AY">
				<span>AY</span>
			</div>
			<div id="AGOD">
				<span>AGOD</span>
			</div>
			<div id="A">
				<span>A</span>
			</div>
		</div>
		<svg class="Rectangle_37_gw">
			<linearGradient id="Rectangle_37_gw" spreadMethod="pad" x1="0.444" x2="18.448" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_37_gw)" id="Rectangle_37_gw" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_38_gy">
			<linearGradient id="Rectangle_38_gy" spreadMethod="pad" x1="-2.461" x2="15.543" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_38_gy)" id="Rectangle_38_gy" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_39_g">
			<linearGradient id="Rectangle_39_g" spreadMethod="pad" x1="-5.366" x2="12.637" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_39_g)" id="Rectangle_39_g" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_40_g">
			<linearGradient id="Rectangle_40_g" spreadMethod="pad" x1="-8.271" x2="9.732" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_40_g)" id="Rectangle_40_g" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_41_g">
			<linearGradient id="Rectangle_41_g" spreadMethod="pad" x1="-11.176" x2="6.827" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_41_g)" id="Rectangle_41_g" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_42_g">
			<linearGradient id="Rectangle_42_g" spreadMethod="pad" x1="-14.081" x2="3.922" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_42_g)" id="Rectangle_42_g" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_43">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_43" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_44">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_44" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_45">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_45" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_46_hb">
			<linearGradient id="Rectangle_46_hb" spreadMethod="pad" x1="0.444" x2="18.448" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_46_hb)" id="Rectangle_46_hb" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_47_hd">
			<linearGradient id="Rectangle_47_hd" spreadMethod="pad" x1="-2.461" x2="15.543" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_47_hd)" id="Rectangle_47_hd" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_48_hf">
			<linearGradient id="Rectangle_48_hf" spreadMethod="pad" x1="-5.366" x2="12.637" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_48_hf)" id="Rectangle_48_hf" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_49_hh">
			<linearGradient id="Rectangle_49_hh" spreadMethod="pad" x1="-8.271" x2="9.732" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_49_hh)" id="Rectangle_49_hh" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_50_hj">
			<linearGradient id="Rectangle_50_hj" spreadMethod="pad" x1="-11.176" x2="6.827" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_50_hj)" id="Rectangle_50_hj" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_51_hl">
			<linearGradient id="Rectangle_51_hl" spreadMethod="pad" x1="-14.081" x2="3.922" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_51_hl)" id="Rectangle_51_hl" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_52_hn">
			<linearGradient id="Rectangle_52_hn" spreadMethod="pad" x1="-16.986" x2="1.017" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_52_hn)" id="Rectangle_52_hn" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_53_hp">
			<linearGradient id="Rectangle_53_hp" spreadMethod="pad" x1="-19.891" x2="-1.888" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_53_hp)" id="Rectangle_53_hp" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_54">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_54" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_55_hs">
			<linearGradient id="Rectangle_55_hs" spreadMethod="pad" x1="0.444" x2="18.448" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_55_hs)" id="Rectangle_55_hs" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_56_hu">
			<linearGradient id="Rectangle_56_hu" spreadMethod="pad" x1="-2.461" x2="15.543" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_56_hu)" id="Rectangle_56_hu" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_57_hw">
			<linearGradient id="Rectangle_57_hw" spreadMethod="pad" x1="-5.366" x2="12.637" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_57_hw)" id="Rectangle_57_hw" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_58">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_58" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_59">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_59" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_60">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_60" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_61">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_61" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_62">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_62" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_63">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_63" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_64_h">
			<linearGradient id="Rectangle_64_h" spreadMethod="pad" x1="0.444" x2="18.448" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_64_h)" id="Rectangle_64_h" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_65_h">
			<linearGradient id="Rectangle_65_h" spreadMethod="pad" x1="-2.461" x2="15.543" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_65_h)" id="Rectangle_65_h" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_66_h">
			<linearGradient id="Rectangle_66_h" spreadMethod="pad" x1="-5.366" x2="12.637" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_66_h)" id="Rectangle_66_h" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_67_ia">
			<linearGradient id="Rectangle_67_ia" spreadMethod="pad" x1="-8.271" x2="9.732" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_67_ia)" id="Rectangle_67_ia" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_68_ic">
			<linearGradient id="Rectangle_68_ic" spreadMethod="pad" x1="-11.176" x2="6.827" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_68_ic)" id="Rectangle_68_ic" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_69_ie">
			<linearGradient id="Rectangle_69_ie" spreadMethod="pad" x1="-14.081" x2="3.922" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_69_ie)" id="Rectangle_69_ie" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_70_ig">
			<linearGradient id="Rectangle_70_ig" spreadMethod="pad" x1="-16.986" x2="1.017" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_70_ig)" id="Rectangle_70_ig" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_71_ii">
			<linearGradient id="Rectangle_71_ii" spreadMethod="pad" x1="-19.891" x2="-1.888" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_71_ii)" id="Rectangle_71_ii" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_72">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_72" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_73_il">
			<linearGradient id="Rectangle_73_il" spreadMethod="pad" x1="0.444" x2="18.448" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_73_il)" id="Rectangle_73_il" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_74_in">
			<linearGradient id="Rectangle_74_in" spreadMethod="pad" x1="-2.461" x2="15.543" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_74_in)" id="Rectangle_74_in" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_75_ip">
			<linearGradient id="Rectangle_75_ip" spreadMethod="pad" x1="-5.366" x2="12.637" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_75_ip)" id="Rectangle_75_ip" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_76_ir">
			<linearGradient id="Rectangle_76_ir" spreadMethod="pad" x1="-8.271" x2="9.732" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_76_ir)" id="Rectangle_76_ir" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_77_it">
			<linearGradient id="Rectangle_77_it" spreadMethod="pad" x1="-11.176" x2="6.827" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_77_it)" id="Rectangle_77_it" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_78_iv">
			<linearGradient id="Rectangle_78_iv" spreadMethod="pad" x1="-14.081" x2="3.922" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_78_iv)" id="Rectangle_78_iv" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_79">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_79" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_80">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_80" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_81">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_81" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_82_i">
			<linearGradient id="Rectangle_82_i" spreadMethod="pad" x1="0.444" x2="18.448" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_82_i)" id="Rectangle_82_i" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_83_i">
			<linearGradient id="Rectangle_83_i" spreadMethod="pad" x1="-2.461" x2="15.543" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_83_i)" id="Rectangle_83_i" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_84_i">
			<linearGradient id="Rectangle_84_i" spreadMethod="pad" x1="-5.366" x2="12.637" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_84_i)" id="Rectangle_84_i" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_85_i">
			<linearGradient id="Rectangle_85_i" spreadMethod="pad" x1="-8.271" x2="9.732" y1="0.5" y2="0.5">
				<stop offset="0" stop-color="#4c8133" stop-opacity="1"></stop>
				<stop offset="1" stop-color="#343c86" stop-opacity="1"></stop>
			</linearGradient>
			<rect fill="url(#Rectangle_85_i)" id="Rectangle_85_i" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_86">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_86" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_87">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_87" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_88">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_88" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_89">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_89" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<svg class="Rectangle_90">
			<rect fill="rgba(0,52,70,1)" id="Rectangle_90" rx="0" ry="0" x="0" y="0" width="3.442" height="11.092">
			</rect>
		</svg>
		<div id="Mt__SAC_Program_Specialist__mj">
			<span>Mt. SAC Program Specialist</span><span style="font-family:Helvetica-Bold;"> </span><br><span>mjayagoda@student.mtsac.edu</span><br>
		</div>
		<div id="Created_a_non_profit_organizat">
			<span>Created a non-profit organization with my partner of a project that consist of rehoming dogs into safer home. The design was created in Adobe XD. Built protypes scrated including logos and the design template of the website. With time sequence </span><br>
		</div>
		<div id="Group_je">
			<div id="NON_PROFIT_WEBSITE">
				<span>NON-PROFIT WEBSITE</span>
			</div>
			<div id="__2020">
				<span> /2020</span>
			</div>
		</div>
		<div id="Assited_on_my_partner_on_the_p">
			<span>Assited on my partner on the preparation of the game design event at Mt.SAC. I was hading out flyers and handing free keychains. Bringing up on invlucreating desiners to participate for this event.     </span>
		</div>
		<div id="Group_ji">
			<div id="GAME_DESIGN_EVENT">
				<span>GAME DESIGN EVENT</span>
			</div>
			<div id="__2018">
				<span> /2018</span>
			</div>
		</div>
		<div id="Mount_San_Antonio_Community_Co">
			<span>Mount San Antonio Community College</span><br><span style="font-family:Helvetica-Light;">- got my associate degree on Studio Art </span>
		</div>
		<div id="Mount_San_Antonio_Community_Co_jm">
			<span>Mount San Antonio Community College</span><br><span style="font-family:Helvetica-Light;">- got my associate degree on Studio Art </span>
		</div>
	</div>
</div>
</body>
</html>
    
    
        <!-- boostrap script -->
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"></script>
        <script src="https://cdn.jsdelivr.net/npm/popper.js@1.16.0/dist/umd/popper.min.js"
            integrity="sha384-Q6E9RHvbIyZFJoft+2mJbHaEWldlvI9IOYy5n3zV9zzTtmI3UksdQRVvoxMfooAo" crossorigin="anonymous">
        </script>
        <script src="https://stackpath.bootstrapcdn.com/bootstrap/4.4.1/js/bootstrap.min.js"
            integrity="sha384-wfSDF2E50Y2D1uUdj0O3uMBJnjuUD4Ih7YwaYd1iqfktj0Uod8GCExl3Og8ifwB6" crossorigin="anonymous">
        </script>
    
        <script>
            $(document).ready(function () {
                $('[data-toggle="tooltip"]').tooltip();
            })
        </script>
    </body>
    
    </html>