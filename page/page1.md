---
title: Page with menubar
subtitle: Demo page with a menubar
layout: page
show_sidebar: false
---

This is another sample page showing how a page can look with a menubar. 

## Displaying a menubar

The menubar gets its content from a data file in your site's `_data` directory. Simply set the name of your data file in the page's menubar setting in the frontmatter. 

```yml
title: Page with menubar
subtitle: Demo page with a menubar
layout: page
show_sidebar: false
menubar: example_menu
```


<div id="ldavis_example"></div>


You will probably want to disable the show_sidebar otherwise there will be little room for the page's content. 

## Creating a menubar data file

Create a data file in the _data directory and use the following format (if using yml)

```yml
- label: Example Menu
  items:
    - name: Home
      link: /
    - name: Pages
      link: #
      items:
        - name: Page With Sidebar 
          link: /page-1/
        - name: Page Without Sidebar
          link: /page-2/
        - name: Page With Menubar
          link: /page-3/
    - name: Blog
      link: /blog/
```

### Multiple menus

You may make multiple menus in the same file, separated by the label

```yml
- label: Menu Label
  items:
    - name: Example item
      link: /example-item/
- label: Second Menu Label
  items:
    - name: Parent Item
      link: /parent-item/
      items:
        - name: Sublink 
          link: /sublink/
        - name: Sublink 2
          link: /sublink2/
- label: Third Menu Label
  items:
    - name: Another example item
      link: /another-example-item/
```


<script src="https://code.jquery.com/jquery-3.5.1.min.js" integrity="sha256-9/aliU8dGd2tb6OSsuzixeV4y/faTqgFtohetphbbj0=" crossorigin="anonymous"></script>
<script type="text/javascript">
      $(document).ready(function(){
         $("#ldavis_example").load("https://github.com/kes185/kes185.github.io/blob/master/LDA_Visualization.html")
      });
</script>
