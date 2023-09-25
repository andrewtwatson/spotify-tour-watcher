# spotify-tour-watcher
I want to make bot that will watch for tour announcements of artists I like so I don't have to.

Some initial research: 
- I can use the spotify api to get the artists on a playlist
- I can scrape the spotify webpage for the instagram
  - `curl "https://open.spotify.com/artist/<artist_id>" | grep -i "href=\"https:\/\/instagram.com\/(<get_ig_handle>)"
- I can scrape an instagram post for a caption
  - `curl "https://www.instagram.com/p/<post_id>/?__a=1&__d=dis"` --> convert it to json --> `[0]["caption"]["text"]`

So this is doable. Not easy, but doable. Watch for when any artist on the list posts, scrape the caption for "tour" things like that, send an email.
