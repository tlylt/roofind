<frontmatter>
  layout: default.md
  pageNav: 2
  pageNavTitle: "RooFind"
</frontmatter>

<br>

<div class="container text-center">
  <pic src="logo.png"/>
</div>
<br>
<br>

# Problem Statement
> NUS CS3240 Design Task 6: Apartment Hunting (Application)
>
> You and your friends have come together to build an application that provides location
> rankings for people looking to rent an apartment/room both long-term or short-term. You
> are designated as the designer for the team and you are tasked to come up with screens,
> allowing people to ﬁnd apartments based on their needs, and also liaise with the owners.

# Motivation
I chose this task because I have been personally invovled (once in a while) in both the process of renting out a spare room and finding a room to rent. In both cases and in Singapore's context, I find the processes to be tolerable but not ideal. To my knowledge, there is no one good solution to both problems in Singapore. Hence, in this post I am set to design a solution named **"RooFind"** that aims to solve the problem of apartment hunting.

# User Requirements Gathering

To begin with, I would like to define my target group of potential users to be:
- living (or planning to live) in Singapore
- looking for a room to rent both long-term or short-term
- comfortable with digital technology and the use of mobile applications
- young adults of 18-28 years of age

## User Persona

<pic src="roofind_persona.png" alt="User Persona" />

## User Interview
Guiding questions to ask to identify problem and validate assumptions:
- What are the tools and technologies that you use to find a room?
- What are the some of the typical needs on the room you are looking for?
- How long do you expect to take to find a room?
- How do you usually liaise with the owners of the room you are looking for?
- What are your thoughts on the process of finding a room?

## User Findings
### Pain points
- Existing applications have too much advertisements that makes it difficult to look at the relevant information posted by home owners.
- Not sure of the type and status of the other tenants in the flat (if any).
- Want to know about the convenience of the flat (e.g. nearby shops, restaurants, etc.)
- Want to know about the pricing and payment options.

### Some exising applications/tools for finding room
- propertyguru
- wechat/whatsapp/telegram groups
- online forums

### Most wanted features
- a way to bookmark rooms and organize them into lists
- a way to check available and timing of room tours
- a way to easily procure related services such as house moving, house cleaning, etc.

## Primary User Goals
From the interviews and the initial research, the three primary user goals my product should achieve are:
- Help users take control of the apartment hunting process
- Expedite the process of finding a room
- Secure the most suitable room for the user

# Prototyping
During wireframing, I realized that there are some complexities that need to be addressed. In particular, the "search parameters", or the critical information about a room, can be quite complicated. Below I listed out a few of the key parameters that I would like to include in the search/room information display. To aid the design process, I also listed out some user flows that the application should support.

## Search parameters
- Price
- Location
  - MRT
  - School
  - Town
  - Offices
- Type of room
  - Shared room
  - Single bedroom
  - Master bedroom
  - Studio
  - Entire flat
- Type of rental
  - Long-term
  - Short-term
- Time of posting
- Type of amenities
  - Aircon
  - Washing Machine
  - TV
  - Table
  - Wifi
  - Wardrobe
- Type of facilities(nearby)
  - Swimming pool
  - Supermarket
  - Stadium
  - Shopping mall
- Restrictions
  - Pets
  - Cooking
  - Visitor
  - Others

## User Flows

<panel type="seamless" header="### First time user" expanded>

- Visits the login screen
  - Sign up
    - Click on the "Sign up" button
    - Key in the phone number
    - Receives the validation code
    - Click on the "Confirm" button
    - Sign up is successful and redirects to the home screen
  - Login
    - Prompt to sign up
  - Browse as a visitor
    - Redirects to the search screen
</panel>

<panel type="seamless" header="### Second/long time user" expanded>

- Visits the home screen
  - freely navigate to the rest of the screens via the bottom menu
    - Go search
    - Go progress
    - Go saved
    - Go settings
</panel>

<panel type="seamless" header="### Task based" expanded>

"I want to quickly find rooms nearby because of an emergency need to move out"
1. Download the app
2. Click on browse as a visitor -> search screen
   1. Select filter: Rooms nearby, OR
   2. Search the postal code
3. Browse the list of search results
4. Tab on one of the rooms to see the details
</panel>

## Wireframes

<tabs>
  <tab header="Wireframe 1">

Time for the real design work! I have created a wireframe of the application in Figma and the very basic lofi prototype is viewable at this [link](https://www.figma.com/proto/jU0RMaV81UIymjc8D3qTu3/RooFind-W1?page-id=0%3A1&node-id=9%3A525&viewport=241%2C48%2C0.17&scaling=scale-down&starting-point-node-id=9%3A525). I have also embedded the wireframe below. Note that I did not link up all the buttons and the text fields as I intended to make this just enough for the very first round of user interviews.

<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="800" height="450" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Fproto%2FjU0RMaV81UIymjc8D3qTu3%2FRooFind-W1%3Fpage-id%3D0%253A1%26node-id%3D9%253A525%26viewport%3D241%252C48%252C0.17%26scaling%3Dscale-down%26starting-point-node-id%3D9%253A525" allowfullscreen></iframe>

With the basic wireframe W1, I decided to conduct a formative evaluation to ensure that the application is going towards the right direction. The first interview is done with a protential user over a Zoom meeting, in which she manipulated the prototype to achieve the task of finding a room. Below are some of the pointers taken during the testing.

- On the **search** screen, the user clicked on a room in the search results and found the popup near the bottom of the screen to be small and difficult to interact with. The user was confused with the star icon on the left corner and did not understand it to be the button to save a room. The user wondered about the wording "2 hrs ago" that was displayed on top. The user thought that the information about time that the room was posted was not relevant/important.
  - Action Items: 
    - The popup could be centered and make the other information less distracting so that the user can focus on that particular room.
    - Have a tooltip or use a more relevant icon for the "save room" functionality.
    - Reorganize information displayed on the popup to make it more relevant.
- On the **room full-details** screen, the user was not sure whether the photos can be enlarged or scrollable. The user also was unsure why there is a "copy contact" button, which seems less useful than the rest of the options. The user clicked on the chat button and wondered if the chat functionality could be natively supported by the application.
  - Action Items:
    - The photos could be displayed in a carousel or include a scroll bar.
    - Consider removing the "copy contact" button.
    - Consider adding a chat interface.
- On the **home** screen, the user was confused by the text "feed" on the top left. The user was not sure how to manipulate the pinning of search keywords.
  - Action Items:
    - Find a better placement of the text.
    - Make the search interface more intuitive.
- On the **saved** screen, the user questioned that why only saved rooms can be compared. The user was wondering what if she wants to compare the rooms back in the search screen.The user was also confused about the purpose of the saved screen since it mainly does comparison. However, the user was pleased that the comparison feature exists and commented that other applications do not have such feature.
  - Action Items:
    - Make "compare" available on other screens.
    - Make the saved feature more functional.
    - Consider moving the saved rooms to a better location, maybe as part of settings
- On the **progress** screen, the user was not sure if she needs to be told about which stage she was in. The user found the screen irrevelant.
  - Action Items:
    - Re-consider the usefulness of the progress screen.

  </tab>
  <tab header="Wireframe 2">

The second wireframe is a slight modification of W1. The wireframe screens can be seen in this [figma link](https://www.figma.com/file/5Lc3nKcD3GDYNlsQ7EaGUP/RooFind-W2?node-id=0%3A1). To gather more thoughts, I have interviewed one more potential user and noted down some observations/feedback as follows:

- In general, the functionalies of the application were satisfactory.
- In the login screen, the user was unsure about the login method and questioned about why there was no Email login option.
  - Action Items:
    - Consider adding an Email login option.
    - Consider making it clearer that the default login is via mobile number.
- In the home screen, the user was not sure the category of the rooms displayed (whether it's All, or a specific category).
  - Action Items:
    - Make sure the category selected is obvious.
- In terms of search, the user wondered if there is a way to group rooms based on the MRT stations nearby. The user also wondered if she can sort different categories.
  - Action Items:
    - Consider adding a filter to group rooms based on MRT.
    - Consider adding per category sorting.
- In the progress screen, the user was not sure about the different stages and what they mean. For example, what is the "enter needs" stage and how to enter needs. The user also suggested about including helpful materials under each stage. These will serve as a guide for users who may not be familiar with the renting proceess in Singapore. 
  - Action Items:
    - Re-consider the meaning of the stages.
    - Re-consider the layout of the progress screen.
    - Re-consider the functionalities of each stage.
    - Consider adding helpful materials.
- In the search screen, it was not clear how the user could enter the room details page.
  - Action Items:
    - Make a button for navigating to the room details.
- In the room details page, the user was not sure the communication would be done with an agent who posted the room details or the landlord. The user was not sure if a room can allow price negotiation.
  - Action Items:
    - Make sure it is clear who posted the room.
    - Indicate whether the room allows price negotiation.
- The user suggested exploring the idea of having reviews on rooms.
  </tab>
</tabs>


## Interactive Prototypes

<tabs>
  <tab header="Prototype 1">

With all the feedback collected, I have created a prototype of the application in Figma to put all the elements into place.

<iframe style="border: 1px solid rgba(0, 0, 0, 0.1);" width="800" height="450" src="https://www.figma.com/embed?embed_host=share&url=https%3A%2F%2Fwww.figma.com%2Fproto%2FqWGltpJxENsU5GSw30wO0r%2FRooFind-P1%3Fpage-id%3D1%253A1250%26node-id%3D1%253A4546%26viewport%3D241%252C48%252C0.24%26scaling%3Dscale-down%26starting-point-node-id%3D1%253A4546" allowfullscreen></iframe>

  </tab>
  <tab header="Prototype 2">
  </tab>
</tabs>

# Conclusion

In summary, this exploratory design exercise has provided me with a good opportunity to practice interaction design.