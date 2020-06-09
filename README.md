# HNGi7-team-sentry-docker_task
 A dockerized micro-service for managing static, external pages

## The task
**Create A dockerized micro-service for managing static, external pages**

 * add_page
 * retrieve_page_html
 * set_page_markdown
 * list_pages

### Model
    * id will be autogenerated by database
    *title(page url) required,string
    *content( the html of the page in string form) string

### End-points

 * */add_page ==== GET

    expecting the url of the page and the content (page source)t though option
 * */retrieve_page_html/:id === POST
    route params:id -the id of the page to retrieve
 * */set_page_markup/:id* =====PATCH
    route params:id -the id of the page to set the markup
    expecting req.body ={ title:the already save url,content:the html to save in string form} 

 * */list_pages* ====GET

    returns all the pages and their markups
