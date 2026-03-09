Claude, carefully examine the repository at https://github.com/mpesce/mrs-server/

It describes a Mixed Reality Service (MRS) server.
The first public instance of an MRS server - is live at owen.iz.net

Now need to generate a mobile HTML5 app to access that server.

We will give it the geolocation of the mobile device (and yes that will require HTTPS, that is understood), and it will use those coordinates to query the MRS server at owen.iz.net (documentation at owen.iz.net/docs).

If the server returns a ‘hit’ - that is, there is something at those coordinates - the URL for that hit should be displayed in the bottom half of the screen, while the top half should show the JSON response to the query.

That's the ultimate source of truth.

You will code this in HTML and Javascript.
You are not to use any frameworks.
This should all be in a single, monolithic HTML file so that it can be installed quickly on any server with TLS.

Do you have any questions?