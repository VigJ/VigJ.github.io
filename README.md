Vignesh Jagathese's Academic Webpage 
====================================

This repository contains code for my personal academic webpage, forked from  https://academicpages.github.io/ with some custom [catpuccin](catpuccin.com) theming. 


Installing My Catpuccin Theme
--------------------------
If you use the academicpages template and would like to copy this theme for your own use, you will need to put the following files into your `_sass/theme/` folder:

`_sass/theme/_catpuccin_dark.scss` (Frappe theme)

`_sass/theme/_catpuccindarker_dark.scss` (Macchiato theme)

`_sass/theme/_catpuccindarkest_dark.scss` (Mocha theme)

And the "light mode" theme files, which are all the Catpuccin Latte theme.

`_sass/theme/_catpuccin_light.scss`

`_sass/theme/_catpuccindarker_light.scss`

`_sass/theme/_catpuccindarkest_light.scss`

Two disclaimers: First, these theme files were all created using AI; I gave AI an existing theme file and a link to catpuccin's color palette then said "format the file". I really should stress that no creativity or thought was required to make these templates. Second, the weird filenames are due to how academicpages sets the theme. To that end, after you put these files in the correct folder, go into your `_config.yml` file and set the theme to any of "catpuccin", "catpuccindarker", or "catpuccindarkest" depending on preference. Remember to "re-serve" the site (ctrl+C then `bundle exec jekyll serve` again) to see the changes on your localhost. 

To theme highlighting and your footer, also add 

`_sass/catpuccin_overrides.scss`

to your `_sass/` folder then add `"catpuccin_overrides"` (possibly followed by a comma) to your `assets/css/main.scss` file inside `@ imports {...}`. 

If you want to use my fun buttons, add the file 

`_sass/catpuccin_buttons.scss`

to your `_sass` folder and add `"catpuccin_buttons"` (possibly followed by a comma) to your `assets/css/main.scss` file inside `@ imports {...}`. To use the buttons, the classes are called `btn--ctp-___`, for "___" any of "blue", "green", "pink", and "peach". 

I stole these buttons directly from the catpuccin.com homepage. I am colorblind and did not trust myself to pick my own colors. These buttons are compatible with the persistent sidebar, as you see on my website. Take a look at my `_includes/author-profile.html` file for how I did this. Note that I only implemented the buttons for the things in the profile that I myself use alongside ORCiD and LinkedIn, which I removed later in this website's development (because who needs those?). Buttons work for intra-site and web links, and can be used in your HTML like below: 

```
<a href="/files/2023_PerfectoidSpacesNotes.pdf"
   class="btn btn--ctp-green"
   style="text-decoration: none;"
   target="_blank">
(Fall '23) Perfectoid Spaces (Mini-Course)
</a>
```

If you want your titles to "pop" with the rainbow pastel effect like in my landing page, add 

`_sass/catpuccin_titles.scss`

to your `_sass` folder and add `"catpuccin_titles` (possibly followed by a comma) to your `assets/css/main.scss` file inside `@ imports {...}`. Note, the gradient was forced to "start late" so that the rainbow wouldn't appear on my shorter titles but would appear on the landing page title. This was to do two things; to get the rainbow portion only show up on the "welcome to my webpage" text and for the rainbow to only go on the landing page. This is a bit of a hack and I would love to know a better solution for this.  
