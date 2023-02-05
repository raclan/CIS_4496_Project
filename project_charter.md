## Project Description
**What is the data science problem to be solved and why is it important?**

* The data science problem to be solved is providing product recommendatiosn to H&M customers.
* Online stores are available to make shopping easier and faster for consumers. Since there are so many choices on the sites, it might be difficult for customers to quickly find what they are looking for. 
* Developing product recommendations will help buyers see the items that they are more likely to purchase. 
* This is important because it could promote sustainability by reducing returns which in turn lessens transportation emissions. 
* By building an effective program, customers could be more likely to shop again at H&M.

## Project Scope
**What data science solutions are we trying to build? What will we deliver, and how will it be used by the client/user?**

* We will be implementing multiple modes of machine learning to create a recommender system for H&M shoppers
  * Standard recommender system techniques
    * Content-based filtering using the article metadata
    * Collaborative filtering using the customer metadata
  * Natural language processing techniques using the provided descriptions of the articles 
  * Image processing techniques using the provided images of the articles
* Using the metrics described below, our recommender system will output 12 recommendations per customer to be evaluated


## Metrics
**How will we quantify the success of the project? What are the common metrics used by others working in the domain?**

* The submissions for this project are evaluated using the Mean Average Precision @ 12.
![image](https://user-images.githubusercontent.com/77793451/216850661-1d05b53e-e55d-452c-ac8c-e039e1e29986.png)
* Using each customer ID in our training data, we will make up to 12 predictions for each one. 
  * These predicted items are for the next 7-day period after the training time period. 
* We will be making predictions for all Customer IDs in our dataset, even if they did not make purchases in the training data. 
* The customers that did not make purchases during the testing period will not be included in the scoring. 
* We will still make 12 predictions for those who ordered less than 12 items, since there is no penalty for doing so.

## Architecture
**What is the nature of the data? What do we expect and how will it be stored/operated on? On what platform would the client/user access any deliverable services (e.g. dashboard) from the project?**

* Data
  * Article metadata
    * All columns of nominal data
  * Customer metadata
    * Mostly columns of nominal data
    * One column of quantitative data (age)
  * Transaction history
    * One row = one transaction
    * One customer has many rows
    * Unit of price isn’t of any specific current/unit
  * Article image data
    * Not all articles have images
* Tools
  * Compute GPU (High-Performance Computing)
  * VS Code
    * Python
* Dashboard/Presentation
  * Website

## Plan
**Phases (milestones), timeline, short description of what we'll do in each phase. You may consider the phases and deliverables in the course timeline when proposing the plan.**

* Phase 1: Data preprocessing/cleaning and data exploration
  * 1.5 weeks: February 6 - February 15
  * Data preprocessing and exploration will be conducted on the customer attributes, product attributes, and purchase history. The only data that will be excluded from this phase are the descriptions and images of the individual items. The data for item descriptions and images will be processed in a later phase.
* Phase 2: Create a baseline collaborative filtering program and a baseline content-based filtering program 
  * 2.5 weeks: February 16 - March 3
  * **February 22: Phase 1 Project Demo**
  * In this phase, we will implement basic collaborative and content-based filtering programs. The collaborative filtering method will use customer metadata to identify like-minded users so that items can be recommended to users with similar tastes. The content-based filtering method will use product metadata to recommend items. The mean average precision will be calculated in this phase to get an idea of how much we need to improve our model based on the current leadership board on Kaggle.
* Phase 3: Feature extraction for product descriptions and product images
  * 2.5 weeks: March 13 - March 29
  * **March 29: Phase 2 Project Demo**
  * Feature extraction will be performed on the product descriptions and the product images so that useful information can be obtained from the raw data. 
* Phase 4: Incorporate product description features and product image features into models
  * 3 weeks: March 30 - April 19
  * The features that were extracted in phase 2 will be incorporated into the collaborative filtering program and the content-based filtering program. These features should improve the performance of the model and other steps can be taken to improve the performance of the models during this phase. 
* Phase 5: Data Visualization
  * 1.5 weeks: April 20 - April 30
  * An interactive dashboard will be created in this phase to provide visuals of insights gained from the data. 
  * **May 1: Phase 3 Project + Interactive Dashboard Demo**

## Personnel
**Who will be working on this project and in what capacities?**

* Team Members
  * Ryan Aclan
  * Salma Hasan
  * Clare Schwarzenberg
* All team members will work on programming, writing reports, and preparing for presentations.


## Communication
**How (platforms, tools, etc.) will we organize communication around the project?**

* Trello
  * Tasks that need to be completed will be added to Trello along with a description of the task under the to do section. Tasks will be tagged as either related to programming, writing reports, or preparing for demos. Different team members will be assigned to each task on Trello. Once tasks are completed they will be moved to the done section. Questions and ideas can also be posted on Trello.
* Weekly Meetings
  * Every Thursday during the lab sessions there is time dedicated to completing project work. During these sessions, team members will update each other on work that has been completed in the last week along with plans for work to be completed for the next week. 
* Group Chat
  * If any meetings outside of class times are needed, they can be scheduled through texting other team members in a group chat. The group chat can also be used for any quick questions or reminders. 
* GitHub
  * Our project will be maintained and collaborated on via GitHub for coding and version control. Files can also be shared on this platform.



