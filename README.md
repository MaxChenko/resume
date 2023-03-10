# How to host a Markdown Resume on Github Pages

## **Purpose**

The purpose of this README is to demonstrate how to correctly host a *markdown* format resume on *Github pages*.

---------

## **Prerequisites**

> The following are some prerequisites required prior to
> starting on the instruction set.

1. Create a Github account on [Github.com](www.github.com)
2. Install [Git](https://git-scm.com/) onto your computer
3. Download the [VSCode code editor](https://code.visualstudio.com/)
4. Resume formatted in Markdown.

If you are unfamiliar with markdown [here is a helpful resource for learning it.](https://www.markdowntutorial.com/)

---------

## **Instructions**

### **The General Process**

According to Etter's principals hosting a resume should follow the below process

    1. a
    2. b
    3. c
    4. d
    5. e

### **Using Github Pages**

The below instruction set will demonstrate how to host your markdown resume on Github Pages.

    1. Open up github.com and sign into your account

    2. Create a new repository that will be used to store and host your markdown resume, you may call it whatever you would like. Be sure to check the 'include readme' option.

    3. Once your repository is created open up it's webpage. Copy the URL address in the address bar I.E. https://github.com/MaxChenko/resume.

    4. On your computer, open up a terminal window and redirect to your desired directory, then type the following command: 
            > git clone the-url-address-you-copied
        This will clone the repository onto your computer.

    5. Open up VSCode and select the 'Open Folder' option. Navigate to the cloned repository and open it up in VSCode.

    6. Create a new folder in the root directory called '_includes', this can be done within VSCode

    7. Drag or copy your markdown formatted resume into the '_includes' folder.

    8. Create TWO more files that will be stored inside the root directory, the following are the file names and their content.

            _config.yml
                    title: YOUR-NAME
                    description: YOUR-DESCRIPTION

                    # Sets the jekyll pre-exisitng theme
                    theme: jekyll-theme-cayman

                    # Excludes read me file
                    exclude:
                    - README.md
                
            index.html 
                    ---
                    layout: default
                    ---
                    {% capture resume_content %}{% include resume.md %}{% endcapture %}
                    {{ resume_content | markdownify }}

        You may of course replace "YOUR-NAME" and "YOUR-DESCRIPTION" fields in _config.yml, with your desired input. Along with replacing "resume.md" with the file name of the resume you copied into the "_includes" folder.

    9. Hit the 'Source control' tab on the left side of your VSCode. 

    10. Click the upper '+' in the tab that is labeled as 'Stage all changes'. 

    11. Write a short commit message in the topmost prompt bar. 

    12. Select the 'Commit' dropdown and click 'Commit and Push'.

    13. Go back to the Github repository webpage. And click the rightmost settings option.

    14. Click on the 'Pages' option the settings.

    15. Select 'Github Actions' as the source.

    16. Choose the 'Configure' option on the Jekyll card.

    17. Commit the added file to your repository.

    18. Navigate back to the Settings->Pages and press the 'Visit Site' button near the top

    19. Congratualations! You have successfully published an online resume!

---------

## **Authors and Acknowledgements**

README written by *Maxim Omelchenko*


---------

## **FAQs**
