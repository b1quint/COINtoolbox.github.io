
  # How to collaborate to the COIN WebPage
  
  ## Page Structure
  
  The current webpage contains a lot of information and, up to now, I did not 
  find what can actually be deleted or has to be maintained to keep it safe and
  sound. Because of that, you may find yourself lost in a huge amount of folders
  and files. This section is intended to make it easier to find the important 
  files that need to be edited.
  
  ### _config.yml
  
  This is the main configuration file. You may want to keep most of the 
  parameters as they are but here are some of the important ones that you 
  can edit freely:
  
  1. **title**: The website title.
  
  2. **description**: A really short description about the page.
  
  3. **url**: This is important. At the moment, it is pointing to my personal 
  repository, i.e. `https://b1quint.github.io`. That means that it will look for 
  the sources within my own repository. When we do the merge, we need to change
  this to `https://COINtoolbox.github.io`.
  
  4. **repository**: This parameter is important for particular projects. In 
  other words, for pages to repositories within the user/institution. Since 
  this webpage will be the actuall one for the COIN Toolbox as an GitHub 
  institute, it should be commented when the merge is done.
  
  ### _pages
  
  Here is where all the important pages are. You may find the following 
  tree:
  
  ```
  |- _pages  
  |    |- crp1  
  |    |    |- main.md
  |    |- crp2  
  |    |    |- main.md
  |    |- crp3  
  |    |    |- main.md
  |    |- crp4   
  |    |    |- main.md
  |    |- pprojects  
  |    |    |- AGNgmm.md
  |    |    |- AGNLogit.md
  |    |    |- amada.md
  |    |    |- cosmoabc.md
  |    |    |- dracula.md
  |    |    |- glm_i.md
  |    |    |- glm_ii.md
  |    |    |- glm_iii.md
  |    |    |- teddy_happy.md
  |    |- 404.md
  |    |- about.md
  |    |- home.md
  |    |- people.md
  |    |- programs.md
  ```
  
  You will notice that every file starts with some header separated by the 
  rest of the markdown context by a leading and a trailing `---`. This is what 
  the Jekyll call the [Front Matter](https://jekyllrb.com/docs/frontmatter/). 
  
  The most important parameters to be edited are:
  
  1. **layout**: The page layout. In our case, I set most pages to `archive`. I 
   simply did not go through all the layouts so let me know if you find another 
   one more interesting.
   
  2. **title**: The main head and the title of the page.
  
  3. **permalink**: This is the address relative to the `url` and the 
   `repository`. You may notice that, for example, we do not have a `index.html`
   file. That's because I set the `permalink` inside the `_pages/home.md` file 
   to `/`. The `about.md` file has `permalink: /about`. That means that Jekyll 
   will put the content of this file on 
   `https://b1quint.github.io/COINtoolbox.io/about/`.
   
   
   ## _data/navigation.yml
    
   This file can be edited to change the main bar at the top (`main`) or the
    sidebars in the COIN Residence Programs (`sidebar_programs`) or in the 
    Projects (`sidebar_projects`). 
    
   At the moment, these sidebars have to be manually activated in every page 
   you want to add them by adding the following the following lines to the 
   file Front Matter:
   
   ```
   sidebar:
     nav: name_of_the_sidebar
   ``` 