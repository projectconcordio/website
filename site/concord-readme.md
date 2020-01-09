# Config 

* make sitewide configurations in `_config.yaml` to change content such as the footer links, or generic urls & content.
* note that you must recompile / rebuild for config changes to take if you are doing a jekyll livereload on your local machine.

# Pages 

Each page is in the root directory of the site and gets compiled to the `_site` directory by Jeckyll. the .html files represents each static page.

| File Name | Page |
| ---- | ----- |
| index.html | Home |
| about.html | About |
| blog.html | Blog landing page |
| community.html | Community page |
| developer.html | Developer page |
| news_events.html | News & Events page |

## Home 

All of the relevant content is stored in front-matter at the top of index.html, with the exception of the blog posts at the bottom of the page and the features displayed in the left-right orientation in the middle of the page (called Features on the front end but stored as Case Studies in the site).

### Adding or Updating Home Page Features / Case Studies

* Find the `_casestudies` directory
* Edit the file as required.
* Each tile supports a title, icon, subtitle and link
* The content below the front matter appears in the feature's tile next to the icon.
* To add a new feature, copy / paste an existing and update the content. The loop on the front-end will automatically add it to the list. 
* Be sure to update the number prefix on the file name to set the order.
* To change the order of an item, update the number prefix on the file name.

## About 

This page does not have much front matter, but accepts standard html for the body content.

## Developer 

The page is divided into Downloads (top) and Papers (bottom), defined as separate front-matter lists.

### Downloads:

* Title - Appears above the descripton
* Description - Small text below the image. 
* URL - URL the user will go to when clicking download. Optional.
* Image - Path (relative or absolute) to icon

### Papers:

* Title - The title of the document or paper.
* URL - URL the user will go to when clicking the title

## Community 

Each link is constructed using front matter data called Links. Edit each line as required:


### Links:

* title: the title of the network.
* description: text that appears before the URL.
* url: URL that appears after description.
* label: Text that appears in the URL hyperlink
* notes: optional text that appears below the url / link.
* image: Path to icon.


## News / Events

The site supports news and events, but since Jekyll is completely static, the site does not automatically mark events as future or past, or discern between a news item and events. Thus, this is simply two separate lists that render on different parts of the page. 

### News / Events

Each news / events item supports:
* date: The date of the event. Use `YYYY-DD-MM` format. Optional
* label: Label that appears next to date. 
* url: Optional URL that will wrap the label and date in a hyperlink.

To move a future event into the past, remove it from the `future` list and paste it into the `past` list.

# Adding new blog posts

* Add new posts into the `_posts` directory.
* We recommend copying existing post and changing the file name and relevant data inside the post itself.
* Prefix the filename with the date you wish to appear on the front-end:
 * e.g, `2019-07-01` = July 1st, 2019
 * By prefixing the filename with the date, your posts will remain in the correct order throughout the site.
* Posts are markdown formatted, but have Yaml "Front matter" at the top to define various fields (Title, image, etc).

## Post Front Matter

| Name | Notes |
| ---- | ----- |
| title | The title of the post. |
| date | Can override the date set in the file name. Recommend leaving this commented this out |
| image | Thumbnail for the post. Dimensions: 300x137 |
| excerpt | Preview of the post. Appears on tile views such as on home page. |
| author_name | Name of author. |
| author_url | URL for author. `/tags/Albert Chiang/` |
| author_avatar | URL for author's avatar. This avatar image must be square / 1:1 ratio | 
| categories | Built-in array. Not used. Formatted in square brackets, e.g `[
'topic one', 'topic 2']` | 
| external | use "external" if you only want to drive users to a different blog post that lives outside this site. |
| tags | Tag should match author to drive author pages, eg, `['Albert Chiang']`