## Project abstract

<u>Sustainability 3: Selenium automation of energy measurement / accessibility tests for KDE applications</u>  


This project aims to contribute to the KDE community's **Sustainable Software** and **Accessibility** goals by implementing automated testing using the Selenium Webdriver AT-SPI tool. The project focuses on addressing specific issues outlined in the repository, including automating the setup of Selenium Webdriver AT-SPI, creating automated tests for a selection of KDE applications, and updating the KDE Eco Selenium guide to reflect the current setup procedures. The expected outcomes include improved testing processes for KDE applications, enhanced documentation for developers, and potential additions to the project's issue repository.

## Proposal


  
This proposal aims to improve several aspects of "Selenium Webdriver AT-SPI" which is a tool used for automated testing of KDE applications. Here’s a detailed list of improvements that can be expected:

Areas of Improvement :

**_1. Updating User guide and test distributions for missing packages_**

Currently the [User guide](https://invent.kde.org/sdk/selenium-webdriver-at-spi/-/wikis/writing-tests) for installation and usage of `selenium-webdriver-at-spi` is detailed enough for a new developer to set it up and start writing tests. We can use this guide instead of existing [setup guide](https://invent.kde.org/nitintejuja/be4foss/-/blob/selenium-guide/handbook/sections/4_selenium-at-spi.md), this will also cut out extra steps currently required while setup. It just needs a few minor updates. For example:

![image (7)](https://github.com/prady0t/KDE-SoK-proposal/assets/99216956/a1e17798-7de1-4805-89b4-d54724a248d4)

Here `libwayland-dev` and `pip` dependencies are missing from installation on `neon OS`.
Other mentiond suppored Distributions needs to be tested against the guide to find out missing dependencies if any.


**_2.Promote Selenium-AT-SPI tests_**

With inclusion of above packages in the latest release version of `neon` (expected) we would have to promote selenium and make developers aware. Hear's a list of things that can be done:

- **Create a YouTube/Peertube video :** A video for developes and testers to setup `selenium-webdriver-at-spi` and run tests. The video can be detailed enough so that its beginner friendly.

-  **Create a blog post to announce and promote selenium :** A blog talking about newely added packages and promoting `Selenium-AT-SPI` can be published so that users and developers are made aware.

-  **Create a selenium support mechanism :** For newcomers to Selenium a support room would be really helpful. We can create :  a) Matrix room to help selenium beginners, b) A kde discuss room for selenium.


**_3. Write automating tests for apps like Gcompris_**


There are already tests written for some of the activities like Baby Keyboard and  Explore World Music, which can provide a solid foundation for writing several such tests. There are more than 180+ activities hence writing tests for all of them is a lengthy procedure. 

Writing a Selenium test comprises of the following steps:

- Identifying QML elements for that activity.

- Add accessibility code to QML element. Accessibility code is basically a locator which will help selenium identify that element and interact with it. An example can be:

![image (3)](https://github.com/prady0t/KDE-SoK-proposal/assets/99216956/509e142a-aae4-4647-aa85-8a2625950c48)


- Get elements by its locator. Once we are done with the previous step, we can now access those elements. For example, to access the above element:

```py
textedit_element = driver.find_element(by=AppiumBy.NAME, value='textinput')
```


- Perform events on the elements. Once we are able to access the element, we can write code to interact with it. For example we can give input to above TextEdit by:

```py
textedit_element.send_keys('textinput_value')
```



In this way several tests can be written. Aim would be to interact with the QML elements and find ways to test different activities. 


**_4. Addressing the Issues that are present in the repo._**

Over the period new issues could be added to Selenium AT-SPI repo. Goal would be to solve those issues and address previously mentioned ones.


## Timeline

Here’s a detailed expected timeline of events:

***Week 1:***

- Getting to know more about the KDE environment and exploring aspects of applications that can be tested.

- Testing setup on various Distributions.

- Improving Setup documentation.

***Week 2 - Week 3:***

- Create a video explaining latest release and setup process.

- Write a blog post announcing the new selenium package release.

- Create suppoet rooms

***Week 4 - Week 8:***

- Start writing automating tests for selenium.

- Find potential bugs in the process.

- Document everything.

***Week 9 - Week 10:***

- Update documentation about added tests.

- Look into open issues and find ways to solve them.

## Foreseen challenges

Writing tests for all the activities can be a length process. The actual time of completion can only be evaluated based upon writing some initial tests.
To tackle it I can start learning about writing tests beforehand so that I'm able to complete it within the given timeline.

## References / relevant background info

I have a strong foundation in python. I’ve been contributing to several open-source projects some of which include: [PyBaMm](https://github.com/pulls?q=is%3Aopen+is%3Apr+author%3Aprady0t+archived%3Afalse+pybamm) (a python based battery modelling system), [Sympy](https://github.com/pulls?q=is%3Aopen+is%3Apr+author%3Aprady0t+archived%3Afalse+sympy+) (python library for symbolic mathematics), [Mitmproxy](https://github.com/pulls?q=is%3Apr+author%3Aprady0t+archived%3Afalse+mitmproxy+is%3Aclosed) (a TLS capable packet interceptor), [web scrapers](https://github.com/Clueless-Community/scrape-up/pull/253) and many more. I’ve written several automation scripts using [Selenium](https://github.com/prady0t/SOPHOS-Login) (for browser automation).

I also have a background in DevOps and automation. I’ve previously contributed to [Kyverno](https://github.com/pulls?q=is%3Apr+author%3Aprady0t+archived%3Afalse+kyverno+is%3Aclosed) (Kubernetes native policy management.)and have worked on tools such as Jenkins, Github Actions, ArgoCD, AWS EC2, etc to create a fully automated CI/CD pipeline [here](https://github.com/prady0t/CI-CD-pipeline-app).

I would really like to work on this project as it would be a great learning opportunity for me!


## How to reach you
(Element / IRC nickname / email)

Pradyot Ranjan @pradyotranjan:gitter.im

Email : rickprimeranjan@gmail.com

<!-- Do not remove this line and the two below, else your proposal will become public and the team won't be notified of it -->
/confidential
/cc @teams/season-of-kde
