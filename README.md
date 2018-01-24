# Radio Nachtlab Bookya Integration

This document explains how to integrate [Bookya](https://bookya.com) public profile to be displayed as part of [Radio Nachtlab](http://radionachtlab.com/) website. in the explanation I will use DJ "**Dimi Angélis**" as an example. You can find the web link for Dimi Angélis in Radio Nachtlab [here](http://radionachtlab.com/index.php/shows/angls-on-air-with-dimi-angelis-deniro/)

## Step 1

To apply Bookya public profile in the website, you need the artist public profile link. Simply go to [bookya.com](https://bookya.com). Login and search for the artist name.
![screen shot 2018-01-24 at 3 06 27 pm](https://user-images.githubusercontent.com/6648552/35318901-730b6820-0118-11e8-883e-b8cde1f08579.png)


Once you find the artist open the profile and click on public profile and copy the link.
![screen shot 2018-01-24 at 3 06 40 pm](https://user-images.githubusercontent.com/6648552/35318902-733b2d1c-0118-11e8-89df-8c7376d0fcae.png)

## Step 2

Allocate the artist bio that contained in the red box in the picture below.

![screen shot 2018-01-24 at 2 35 47 pm](https://user-images.githubusercontent.com/6648552/35318005-74e152ee-0114-11e8-8dc3-835abb86e00c.png)

<br/>

It should look like this:

```html
<div class="qt-card qt-contents qt-showcard">
 <div class="row">
	<div class="col s12 m6 l6 qt-show-tagline">
		<h3 class="qt-title"></h3>
		<h4></h4>
	</div>
	<div class="col s12 m6 l6">
		<h5>Tagged as:</h5>
		<div class="qt-content-readmore">
			<div class="qt-the-content">
			<div>
				<div>
					<p>Dimi Angélis</p>
			    <div class="f24">It might sound like a cliché, but sticking to what you believe in really does pay off in the end. Dimi has been actively involved in the Dutch technoscene since the late nineties, his legendary raves at various locations still speaking to the imagination of many. Technofreaks abroad must know Dimi from his Counterpart and A&amp;S project (w/ Jeroen Search). For their sound they draw inspiration from the classical Detroit minimalists and give it their own contemporary twist. As for Dimi’s dj-sets, he can venture into the deepest of house or the bloodiest of nosebleed techno, but he always stays true to himself and to the music in its purest form.
					</div>
				</div>
			</div>
			</div>
			<hr class="qt-spacer-m">
		</div>
		</div>
	</div>
</div>

```

## Step 3

In Bookya public profile there is two themes **Light** and **Dark** The profile will be displayed in the default theme. here is an example on how to change the profile theme

__Example:__

Theme | URL
---|---
Default | `https://bookya.com/artist/dimi-angelis`
Dark | `https://bookya.com/artist/dimi-angelis?style=dark`
Light | `https://bookya.com/artist/dimi-angelis?style=light`
> _**NOTE:** the default theme is specified by the profile owner (the artist). It can be light or dark._

<br/>

Now replace the HTML code that you fined in the first step with

```html
  <iframe class="qt-showcard" src="https://bookya.com/artist/dimi-angelis"></iframe>
```
<br/>
The result should look like this.

![screen shot 2018-01-24 at 2 39 24 pm](https://user-images.githubusercontent.com/6648552/35318006-751651c4-0114-11e8-9804-9e17cc8c37c7.png)
