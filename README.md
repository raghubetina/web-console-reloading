# Web Console Live Reloading Bug Demo

It appears that `web-console` is breaking code live reloading in some instances.

## To reproduce

 1. Clone.
 1. `bundle`
 1. `rails s`
 1. Navigate to [http://localhost:3000/pages/home](http://localhost:3000/pages/home)
 1. You should see "Hi there".
 1. Make a change to the value of `@output` in Line 3 of `app/controllers/pages_controller.rb` and refresh the page. The changes should be reflected. So far so good.
 1. Now do something in the web console at the bottom of the page. Anything should do -- `2 + 3` is enough.
 1. Now go make another change to the value of `@output`. Refresh the page. **The changes might not be reflected.** (I have tested this with several students and the issue seems to be intermittent; it happens about 75% of the time.)
 1. Restart the `rails server`. Refresh. The changes will be reflected.
