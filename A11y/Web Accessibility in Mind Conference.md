# Web Accessibility in Mind Conference
#WebAIMConf

## Accessfuturism: Digital Accessibility in 2032
Opening Keynote: Crystal Preston-Watson

Interesting note: The author described the first slide. She described what she looked like and what content was on the page. 

- Explore disability in a futuristic way

What will we see in 2032..
- Caption and Transcript Integration
	- Potential for error - Makes videos accessible. Auto generated captions cause many errors. Hope is that this fixed over time. 
- AI Generated Code - Github copilot auto codes
	- Potential for error - Errors can popup when it comes to a11y. Semantic means may get lost. 
	- Death of the overlay - Tools like accessibe are shortcuts and not solutions.
	- AI generated code could make overlays obsolete. 
- The Modular Internet
	- allow the user to build their own experience
	- users will have more control over their experience
	- Potential for error - This may only work for a set user base. Limited customization. May exclude those with disabilities.  
- Mobile First ( and only mobile )
	- has become the main access to information and technology for users. 
	- Potential for error - cost could hinder use. 
- Rise of Wearable Technology
	- Smart watches, smart headsets etc
	- Potential for error - Devices may not be accessible. Accessiblity may not be thought out
- Put a chip in it. 
	- Potential - modify brain structure

Back to 2022


## Designing for people who use a mouse
Henny Swan

- We think of users as either a mouse or keyboard user
- Those with physical disabilites will also use a mouse. Its very rare to only use a keyboard. People use a combination of devices
- With the exception of those who are blind or have major physical disabililtes, most people will use a mouse
- Consider the situations your users may be in
- click point drag hover 
- need dexterity and useful vision
- Inclusive Design Principles - https://inclusivedesignprinciples.org/
- dont rely on the hand hover state - difficult for low vision
- avoid inconsistent link pattern. ie a row of logos but not all are links
	- mega menus only on some nav items
	- provide consistent hover and focus styling
- touch target size 44px x 44px for AAA
	- increase touch target size for popular links or high traffic links, difficult to reach, part of sequential task, or not easily undone. 
- put space between interactive controls
- content on hover - this is difficult for those with fine motor skill issues. 
- unwanted content on hover - items that load and push down other content
- Drag and Drop
	- bad interaction for accessibility
- Scroll
	- some users have issues using the scroll wheel. Provide an alternative
	- controls to change layout
	- add filters to reduce amt of content
	- filters, grids, lists, sort-by. 
	- provide alternative ways to complete task
- Be consistant with both hover and focus states. Use the same design for both. Users will use mouse and keyboard together.  
- Good a11y is innotative


## How (and why) to 'shift-left' your accessibility testing
Sheri Byrne-Haber

What does "shift left" mean
- prevent something from happening
- find and fix it before the customer finds it
- progress over perfection
- better to find bugs as early as possbile. 
- most accessibiity testing is done in testing and production. this should be done earlier in design
	- reduces time, cost and risk
- Myths
	- a11y is a technical thing. leave it to the techie. 
		- truth - everyone has a role in a11y. have everybody talk about a11y
	- all that is required is to learn how to use assistive technology. 
		- truth - you need testers with disabilities
- Things you can do
	- discovery phase
		- do your personas have disabilities? start with color blindnes especially in male dominated industries
		- Has the product owner consulted with people with disability?
		- will the product have any functionality that requires device manipulation? drag & drop, haptics, tilting etc
		- is a11y part of "DONE?"
	- feasibility phase
		- do you have people with disabilities in you user research pool?
		- accessible prototypes?
		- Has the product owner consulted with people with disability?
	- design phase
		- Are design sessions accessible? 
		- Are the design tools accessbile? Involve designers with disabilities
		- is an accessible design component library/system being used?
		- use accessibility checklists
		- is there an accessibility brief? for the developers. outline headings etc
	- dev phase
		- is there a a11y automated test in your deployment pipeline
			- this rejects bad code that prevents accessible behavior
			- if its not accessible provide an alternative
				- common issues with progress bars and data visualization
	- testing phase
		- if testing was done in dev, you can focus on manual testing
		- have a11y and functional tickets in the same backlog
		- perform random sampling - if you have thousands of pages you test a random number of pages.
		- focused testing of high traffic pages
		- never overlap functional and a11y testing by 25%
	- deployment
		- do you have accessible customer support
		- do you test content changes in prod? 
		- make sure third parties now how to check for a11y before pushign updates
		- test changes in staging


## From Projects to Programs: Accessibility in Digital Strategy
WebAIM Workshop by Rob Carr


## The Intended Consequence of Inaccessible Digital Ads
Panel moderated by Mike Paciello, featuring Jonathan Day (Centrus Digital), Joe Dolson (Accessible Web Design), and Gerard Cohen (Twitter).

Joe Dolson is a lead contributor for WP. 

Growing accessibiilty Market
- by 2023 the number of people with disabilites will trill due to ai and assistive tech

What are the a11y and usability issues facing digital ads?
- ads that are not accessilble means that a user may not be able to click thru and purchase

What solutions do you recommend? 
- force ad companies to require a11y

## A designer's guide to documenting accessibility & user interactions
Stéphanie Walter

- a11y tends to fall to the developer to implement. 
- This should be done by the designer with guidelines and documentation
- annotations directly at the page level with different styling from the site design
- what documention method does the team prefer?
- Docs
	- color palatte and contrast
	- contrast grid to define colors
	- interactive states
	- focus states
	- form inputs
	- error cases for forms
	- interaction flows
	- how interactive elements work
	- provide alternatives for complex guestures
	- document zoom behavior
	- reduced animation behaviou
	- user flow
	- html title
	- focus order
	- html flow vs visual order
	- links for external resources
- Developers can document 
- map who can document what


## Accessible Roots Grow A Healthy Framework
Shell Little

What is a design system? 
- How do you bake in a11y? 
	-include an a11y designer

Grow Healthy Roots
- product needs to be accessible to be consumed
- context is everything for a11y
- standards are changing
- each change should be checked for a11y

Documentation
- component specs
- code samples
- demo videos
- dont assume the team will remember it. Turnover exists

Transparency
- a11y is a part of the process not a bottle neck
- add it to the process
- spread the work across teams

Education
- have training
- open hours
- presentations
- working examples
- api pages
- functional pattern libraries

Component Tracking and Planning

Feature requests via ticket

Cross functional review

Design Sprint

Talk about failure

Documentation is you biggest ally



## Quick Start for Evaluating and Testing Web Accessibility
WebAIM Workshop by Jared Smith and Jonathan Whiting

W's of a11y evaluation
- who does it impact
- what is the problem
- when does it occur
- where does it occur
- where in the page
- where in the code
- why did it happen
- how to fix?

Tools
- screen reader
- wave tool
- devtools
- 