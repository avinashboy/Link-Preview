# Link preview 

Just send the post request to the back-end sevrer. It will
 response has json 
 <br>
 ## It consist of 
  - Url
  - Site
  - Favicon
  - Title
  - Description
  - Image

 ## Api
 
 `const url = "https://abt-link-preview.herokuapp.com";`
 
 ### HTML

```
<input type="text" name="name" value="" id="link">
```
### JS
 ``` 
 $.ajax({
        type: "POST",
        url: url+"/api",
        data: { "Url": link.value },
        success: function (response) {
          console.log(response);
        },
        error: function (err) {
          console.log(err);
        }
      });
 ```

### JSON structure 
```
{
url: "https://github.com", 
site: "github.com", 
favicon: "https://github.githubassets.com/favicons/favicon.svg",
title: "The world’s leading software development platform · GitHub", 
description: "GitHub brings together the world’s largest communi…ll-in-one platform for collaborative development.",
image: "https://github.githubassets.com/images/modules/open_graph/github-logo.png"
}
```
