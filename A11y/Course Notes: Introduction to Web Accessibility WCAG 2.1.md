# Introduction to Web Accessibility WCAG 2.1 

https://evercommerce.udemy.com/course/introduction-to-web-accessibility-wcag21/ 

Author suggests downloading the following tool(s):
https://www.tpgi.com/color-contrast-checker/ 

Brea recommends https://www.tpgi.com/color-contrast-checker/ 

Section 1: Welcome to the CourseNo notes here 



Section 2: Web Accessibility Overview 

WCAG versions
* WCAG 1 set priorities for accessibility 
* WCAG 2 set 12 guidelines for how web content should be built using the POUR principles 
    * Also outlines conformance ratings. A, AA, AAA
* WCAG 2.1 adds additional guidelines for specific disabilities and is backwards compatible 
    * EU requires WCAG2.1 Level AA

POUR Principles
* Perceivable
* Operable
* Understandable 
* Robust

3 Levels of Conformance - Degrees of difficulty to implement1
* A
* AA
* AAA

Assess A11y
* Many success criteria have failure techniques which describe the steps for a failure to be recorded. Even though in browser tools can be used to test, it is strongly recommended to familiarise yourself with manual testing first before automating the process.
* Where no failure technique exist for a success criteria, use the test within the sufficient technique you have chosen. This test determines if the sufficient technique has been applied correctly, as the sufficient technique is an identified way of passing a guideline.

Types of Sufficient Techniques (Common Ones)
* G - General techniques
    * Technology Neutral
    * Often paired with a technology specific technique 
* C - CSS techniques 
* H - HTML techniques
* ARIA - Aria techniques
* SCR - Clientside Script techniques 
* There are also less common techniques (not listed here)
* The Number following the Letter is just an identifier. 
    * H25


Section 3: Building the Structure of a Page

Create Descriptive Page titles
* Use <title> element
* Be descriptive and concise 
* Multistep pages should include the step number in title
* Pages can be enhanced by providing the website name either before or after the title text

Set the Page Language
* A language code set the the lang attribute on the <html> element will affect the whole page content as its applied globally.
* The lang attribute can be applied to chunks of text where the language is different from the webpages primary language
* The lang attribute value is a two character ISO country code
* Region code can also be added for variations. American English vs UK English
	
Bypass Repeating Content
* Skip links or bypass blocks are a mechanism which allows a user to avoid or bypass repeating page content easily. 
* Limit skip links to 3 or less
* Must have as a minimum a linked named “skip to main content”

Create Logical Headings
* Outline for a website
* 6 levels
* H1 is the page title
* Page should only have one h1
* Each level denotes a subsection of content from the previous parent
* Do not skip levels
* An h3 must be a subsection of an h2
* An h4 must be a subsection of an h3
* Heading elements must be in sequence 
* Page headings should be logical and sequential. Logical in that the heading is used to break up content which requires it and sequential with each level following in the correct sequence and not being skipped.
* Page headings should be applied when new content is being introduced. If the content feels it needs to be broken up into a new section, or you're going into more detail that’s a great time to step down into a lower heading level.

Landmark Regions
* Areas can be marked up consistently
* Exposed to screen readers
* Only provide benefit for screen reader users
* Not natively displayed in browsers - they are structural elements only unless marked up visually. 
* Not a replacement for skip links
* Landmark regions provide a mechanism for screen reader users to navigate to different sections of the page. They can also be used to group common page elements together into a named region, however this is only helpful when reading the code and provides little benefit other than improving code readability.
* Act as containers for content
    * <header>
    * <footer>
    * <main>
    * <article>
    * <nav>
* <header> contains logo / company branding
* <footer> contains non-primary navigation links
* <header> and <footer> can be added to anywhere its appropriate, including modal dialogs and within sections
* <main> describes the part of the page which has prominent content
    * Can not be nested inside an <article> region
    * Only one per page. 
    * Most appropriate for content which could be syndicated
    * Can include <header> and <footer>
    * Can nest many sub <article> elements
    * Can be nested in other landmark regions (?)
    * A landmark region marked as <main> describes the main content of the page, the part of the webpage which has prominent text describing the topic of the page. There must only be one main region per page.
* <nav> groups “major navigation link” together
    * Table of contents
    * Links to different pages
    * Prev and next links

Avoiding an Artificial Tabindex
* An incorrect tab index can adversely affect keyboard navigation
* Hide content from the keyboard tab sequence using a value -1
* Introduce content into the regular keyboard sequence using value 0
* Don’t use positive tab index values
* Tab key press advances the screen focus on position to the right, then moves down in a Z pattern
* Links and form controls have an implied focus in the order laid out on the screen
* tabindex=0 will allow a component to become focusable. It won’t change anything to ordinarily focusable elements
* Elements with a tabindex=1 or higher take focus precedence when the tab key is pressed\
* Adding tabindex=-1 to any element removes it from the documents tab order and renders it unfocusable from the keyboard.
* Tabindex=0 will allow a component to become focusable and part of the documents natural tab sequence. Native HTML elements have this behaviour as standard and the attribute isn't required to be added to those elements.
* Elements with a tabindex=1 and above take precedence when the tab key is pressed, and have an elevated priority to be focused first. Interactive elements laid out visually will have a tab order that is different to how they are laid out when a positive tabindex value is used.


Section 4: Adding Page Level Content

Choose Accessible Colors
* Poor color contrast can affect users with color vision impairments
* Content viewed in low light or high contrast environments can be difficult to see
* Good color contrast benefits everyone
* Use the color contrast tool (link at the top of the notes)
* Wcag 2.1AA color contrast success criteria is confusing
* A pass for large and regular text will mean if a variable font size is implemented into pages, as the font becomes smaller the colour contrast is still acceptable for passing accessibility requirements.

Decorative & Descriptive Images
* Ensure every image has an ALT attribute
* If an image has no ALT attribute the screen reader will announce “image”
    * The user is aware an image is there, it may be relevant or it may not, there is no way to tell
* What is the image describing, why is it relevant, what does it show? 
    * Apply a richness to the description when adding ALT test
    * Short sentence is fine. Avoid overly large amounts of text
* Use Null ALT text means the screen reader will ignore the image 
    * alt=“”
    * Use for decorative images
* Decorative images don’t require ALT text for a screen reader to announce them. However, they do require an ALT attribute and the value needs to be null (an empty string).
* Too little ALT text describing an image is as frustrating as too much. Use enough of a description to convey what the image is showing and why it is relevant, but be succinct as much as possible.
* All images added via the IMG element require an ALT attribute. If the image is decorative the ALT attribute value can be set to null as it indicates to the screen reader to ignore the image.

Use Semantic Elements
* Semantic elements provide structure to content and makes it easier for assistive technology users to understand
* Most common semantic elements 
    * H1, h2, h3, h4, h5, h6
    * <ol> and <ul>
    * <blockquote> and <em>
    * <header>, <footer>, <main>, <article>, <nav>
    * <time>
* Lists group related items
    * Screen reader announces the total number of items followed by each item
* Unordered lists <ul> will announce “bullet item” followed by the item
    * “Bullet Item one”
* Ordered lists announce the position of the item in the list followed by the item
    * “One item one”
* <blockquote> for long quotation
* Cite attribute is used to identify the source of the quote
* <cite> element can be used within a blockquote
* <em> used to stress emphasis on a word or phrase
* <time> element which displays date/time or duration 
    * Mandatory attribute of date time
    * Format must match text description
* Using semantic elements may trigger the screen reader to announce the content differently. In essence semantic elements are meta data which triggers assistive technology to do extra things for free, for example announcing the number of items in a list.
* Heading elements structure the page and provide a clear hierarchy which screen reader and assistive technology users can use to navigate and understand how a page is composed. The heading level should never be chosen based on how the browser will render it as any styling requirements can be changed with CSS. A heading structure is the skeleton of a page.
* Related items need to be grouped together using the ordered and unordered list elements. These elements trigger the screen reader to announce the number of items in the list, and in the case of the ordered list announce the position in the list of each item. DIV elements are non-semantic and provide no information to the screen reader, additionally visual grouping cannot be inferred by the screen reader as it relies on structural markup for understanding.

Add Keyboard and mouse focus
* A good suggestion is to use a border as a focus effect.
* Navigating a website via the keyboard becomes difficult without a clear focus style
* All Keyboard accessible elements on a page must have distinct focus effect when they receive keyboard focus
* Focus effect consistency - must be the same when navigating from the mouse and keyboard
* :focus is applied to the keyboard tab event when a user is tabbing through the page.
* Not including every form control (input, select, textarea and button) in your CSS rules will mean a focus effect is applied inconsistently to only some of the controls.
* Only link elements and form controls are natively focusable.
* 

Write clear link text
* When the link is read individually the destination of the link is understandable 
* Users can see a full list of all links on a page. 
* Unclear link text can make it difficult for screen reader users navigating a website
* Use clear link text
* The best way o determine if the link text chosen is clear is by reading it aloud
* All interactive elements on a page are focusable by a screen reader, clear link text helps a vision impaired user understand the link destination alone without having to rely on surrounding content.
* Unclear link text is text which cannot be understood unless it is combined with surrounding text and/or relies on its placement on the page to be understood. Link text should be understandable when read on its own outside of the webpage and accompanying text.
* The following are bad examples of link text
    * Click here
    * Read more
    * More information
    * Learn more
* A screen reader can list all page links separately in a separate window. All link text is arranged alphabetically, when there are several links with begin with click here a vision impaired user must listen to every click here link to understand the important information which is after the text click here. There is no way for the user to navigate easily a list of click here links.

Group Related Links
* Screen Reader users navigate websites in a non visual way
* Links arranged visually need to be marked up to induce the screen reader to provide extra helpful information
* The meaning of what these links mean can become confusing without this screen reader hint
* Ul and OL elements can be used to trigger the screen reader to announce 
    * Type of list (ordered/unordered)
    * Number of items in the list
    * If the list is bulleted or numbered
* Use carefully and apply only when necessary
* Announcements adds the audible overhead a user has to understand
* It can get tiring to listen to.
* Although it does make a page hierarchy easier to navigate, and a visual grouping identifiable these are only useful helpers. Using the UL and OL list elements gives the screen reader the ability to announce the number of items in a list.
* Using the OL element triggers the screen reader to announce each item when the list receives focus to announce the position in the list it is in. Announcing the number of items in the list is behaviour which is standard for both ordered and unordered list elements.
* Whilst the expected behaviour of how a screen reader should interpret a list is universal, the implementation in a screen reader may not be up to date with current standards which means the number of items in a list won't be announced, or the list position won't be announced. It is entirely dependent on the screen reader and browser combination in how the behaviour is announced.

Use data tables for tabular data
* Tables must be marked up for a programmatic association to be made
* Column headers are created using the <th> element and scope=col attribute
* Table description is provided using the <caption> element
* The caption element is the correct way to provide a description for a datatable. Although some assistive technology may support the summary attribute, this is becoming deprecated and no longer used. Although the contents of a table can be used to understand the type of data, the contents alone are in no way an alternative to providing a clear and succinct table description.
* The scope attribute identifies any header cell and indicates whether it is a header for a row, column or group of rows of columns. The attribute isn't required for valid HTML as it use is predominantly for complex tables although simple tables can benefit.
* The scope attribute identifies header elements and whether they are columns or row headers and as such are added onto the TH element only. Adding the scope attribute onto TD or TR elements will have no effect.	



Section 5: Structuring a Web form

Navigation in a form

Add Labels to Controls
*  The FOR attribute value of the label element uses the ID of the form control
* This creates a connection between the label and the input that can be used by a screen reader when in focus
* When focused the screen reader will announce the text label describing the type of input required for the control
* “First name input type and text”
* Following controls require a label
    * Input type=text
    * Input type=checkbox
    * Input type=radio
    * Input type=file
    * Input type=password
    * Textarea
    * Select
* Following controls dent require a label
    * Submit and reset buttons with the value attribute doesn’t require a label as its provided by value attribute
        * <input type=submit value=“submit”>
    * Image buttons include the alt attribute
        * <input type=image alt=“search”>
    * Hidden inputs
        * <input type=hidden>
    * Button element with text description 
    * <button type=button>Add to Basket</button>
    * 
* Whilst physical placement and bold text may convey to the user there is a relationship, this is only seen visually. A screen reader user won't be able to discern the change in visual presentation and has to rely on other ways to understand relationships.
* Submit, reset, image, hidden and buttons don’t require a label as a text description is provided by the value attribute of the control, the ALT attribute or content within the element. Hidden form fields don’t require a visible label as the control is hidden and is not expected to be interacted with by the user.
* A larger clickable area makes it easier to select form controls. The label increases the clickable area of a control, which makes it particularly convenient for users of smaller screen devices. Rather than clicking inside the control to activate it, the activation can now occur from either the label or the control which is helpful for users with dexterity problems.

Identify Data Format
* Screen Reader users may not see form validation errors. 
* Label the constraint. The label followed by the constraint will be announced
* “First name twenty character maximum”
*  Describe all constraints. Provide the expected data formats int e label
* Don’t add too much information in the constraints
* Formatting and constraint information can be added to enhance the input control label
* Providing constraint information within the label of the control will trigger the screen reader to announce it when the label is announced.
* Constraint information contained in the label element is announced whenever the control receives focus.
* Although text input controls do have a maximum length attribute, this isn't conveyed to the screen reader when the limit has been reached. adding the constraint information into a span element will not announce this to a screen reader as the SPAN element is not programmatically associated to the label.

Highlight Required Input
*  A red asterisk is the popular choice but this can be difficult to understand for users who may be unfamiliar with online forms
* The convention requires explanation before a user encounters it
* The explanation is typically rendered as non interactive text, doesnt receive keyboard focus and isn’t announced by the screen reader
* Identify items by color may impact users with color vision impairment 
* Better approach is to include the text “required” in the label
* Don’t mark controls as “optional” 
* Using colour or a <span> element to indicate a control is required to be completed relies on the visual presentation for a user to understand. A screen reader user requires a programmatically associated label element for each control to understand if there is further information to be completed. Additionally, relying on colour alone to indicate importance will make it difficult for users with a colour vision impairment.
* A screen reader user understands and navigates a page audibly. Hearing all onscreen text announced can be a difficult cognitive task. Indicating only the required form controls makes it easier for the user to know what controls are relevant and which controls can be ignored.

Group Related controls
* To identify related controls use the fieldset and legend elements for the whole group
* The legend element is the first element within a the fields, this is announced by the screen reader
* Better grouping - when each control receives focus, the legend text will be announced first followed by the control label
* Best suited to use for checkboxes and radio buttons where the individual label for each control may be insufficient
* Controls which are grouped using the fieldset and legend elements trigger the screen reader to announce the legend text when each control in the group receives focus.
* Controls grouped together using the fieldset and legend elements convey the legend text to a screen reader when each control in the group has focus. Additionally, users with a cognitive impairment can benefit from the greater context being provided around the controls.
* Grouping should only be applied when the relationship between related controls may be unclear or difficult to understand. The fieldset and legend elements trigger the screen reader to announce the legend text, and overuse can become a frustrating experience with verbose descriptions for controls.

Handle Errors

Use Inline Error Message
* An accessible inline error message is contained within the label element and is announced as part of the label text
* The addition of the inline error message is extending the accessibility support the control already has to now include an error message
    * Place the error message in a span element inside the label element
    * When error occurs unhide the span element with the error msg
* The technique does announce the error message to a screen reader
    * It is only announced as part of the label which is only announced when focused
* The inline error message shouldn’t be the only way to describe a control in error
* Inline error messages are only ever used when combined with other techniques as a complementary way of providing error feedback
* An inline error must be contained within the label element of the in-error control. When the control receives focus the error message will be announced as it is part of the controls label which is programmatically associated.
* An inline error message added into the label text is only announced when the control gains focus. A programmatic relationship is established using the FOR and ID attributes on the label, and the inline error message text is combined to the existing control label text.
* Inline error messages are a complementary way of displaying errors only, they must be combined with other error handling techniques and cannot be relied upon as the sole way of proving error feedback.

Suggest Corrections
* Inline error messages can be used as a way to suggest what the user can enter to minimize further errors
* Error suggestion provides further assistance. Think of it as further nudges or prompts to the user
* Any specific formatting must be conveyed in the error message 
    * “Incorrect format the required format is dd/mm/yyyy”
    * 
* Describe the data format requirement in the controls label
* Ensure the data format is repeated in the error message
* Explain why the value was reject as well as the the correct format
* Error messages should indicate there has been a problem
* Explain why the problem occurred
* If the situation allows suggest a correction
* "this cannot be blank" is the best example of adopting a tone of language which can be understood by everyone. Using just the word "mandatory" or "required" may confuse users unfamiliar with web forms and can become a problem for users with cognitive impairments.
* Providing more information than just the error message will allow users to understood what went wrong and what they need to do to reduce errors occurring. Rather than simply stating the error, explain why the entered value was rejected (perhaps due to an incorrect format) as well as the correct format.
* Providing a suggested correction which includes the format of the data means the user won't repeat the mistake. They will understand data has to be entered in a particular sequence.

Use a Validation summary
* Summary of all errors on the form
* Complementary way to provide error identification
* A region above the form indicating error have occurred and identifying which controls are in error
* Use a list UL to group errors means the number of items is announced by the screen reader
* Summary includes addition styling to draw focus to the in-error region
    * Prominent color
    * Heading element (h2)
    * Bold text 
    * full or partial border
* Traditional websites send the page to the server to be validated
    * If errors have been identified the page is returned with the validation summary and inline error messages visible 
    * When a page is reset the focus is lost
    * Lost user focus can be fixed by appending the hash character in the returned url
    * <h2 id=“validationsummary”>Error has occurred</h2>
* Without a validation summary a user has to navigate through form controls to determine if any are in error
* Validation summary regions are an additional cue which can help users understand form errors
    * THey provide a convenient central location for grouping all errors together
* Adding errors to an ordered or unordered list means extra features are provided by the screen reader. The UL or OL elements are semantic, they have a structure which allows the screen reader to announce how many error items are contained in the list.
* Hash is used to move focus to the validation summary with the user having to tab to it.
* The colour red can be used to draw attention visually to the validation summary, this is can be complemented by a border around the region to help users with a colour vision impairment and finally a heading of "Validation summary" can be applied to give the errors a defined region and help the user by providing a clear page hierarchy.



Section 6: Conclusion

Be Involved in the conversation online
* Use the hashtag #a11y

Twitter users active in accessibility
* Ross Mullen
* Marcy Sutton
* Heydon Pickering
* Steve Faulkner
* InclusiveDesign24
* Bryan Garaventa
* Andy Ronksley
* Bruce Lawson
* Leonie Watson
* Karl Groves
* Richard Morton

Books to get about A11y
* Inclusive Components
* Inclusive Design Patterns
* Accessibility for Everyone
* Practical Web inclusion and accessibility
* Inclusive design for products
* A Web for Everyone
* The Ability Hacks
* Authentic Inclusion
* Mismatch
* Structured Negotiations
* Diversify

Websites and Blogs to read more
* CANAXESS website
* CANAXESS articles
* CSS tricks
* AlistApart
* Adrian Roselli
* The Paciello Group
* Smashing Magazine
* Caniuse
* HTML5 Doctor

Course Author information
* Twitter
* LinkedIn
* CANAXESS Newsletter signup





—————————————————————————————


Introduction of UX Design for Accessibility and WCAG 2.0

https://evercommerce.udemy.com/course/accessibility_ux/


Section 1: Introduction

No Content here


Section 2: Why Design for accessibility?

Its good business
* 1.3 billon people have disabilities worldwide

Why?
* Its easy
* Removing barriers to improve lives
* Medical Model of disability - society blames the disabled
* Social model of disability - society removes barriers to help disabled
* Improve lives

Section 3: Types of Disability

4 Types of Disabilities 
* Visual
* Deaf and Hard of Hearing
* Cognitive
* Motor
* 4 major disability types are Deaf and Hard of Hearing, Vision Impairment, Cognitive Impairment and Motor Impairment

Vision Impaired
* Fully impaired - unable to see light
* Partially impaired - can see some light
* Color blind 

Deaf and Hard of Hearing
* Deaf: Very little of no hearing - uses sign language
* Hard of hearing: mild to moderate hearing loss. May use sign language 
* “Hearing Impaired” is considered an offensive term
* Tools
    * Captioning
    * Open and Closed
        * Closed captioning is an overlay and can be turned off or change language
        * Open captioning can’t be turned off and is embedded in the media
    * Transcription - example: screenplay of a movie

Cognitive and Learning 
* Clinical Disability - similar to medical model of disability
    * Autism, Down syndrome, ADD, etc 
* Functional Disability - Similar to Social model
    * Ignores medical causes focus on difficulty 
        * memory
        * Problem solving
        * Attention
        * Reading, Linguistic and verbal comprehension
        *  

Physical Disabilities
* Spinal cord injuries
* Lost or damaged limbs
* Diseases and congenital conditions
* Tools
    * Keyboard browsing
    * Eye tracking
    * Voice recognition
    * Joysticks


Section 4: Introduction to WCAG 2.0

See downloads
* Ux Accessibility Toolset 
* WCAG Checklist

WCAG: Web Content Accessibility Guidelines 
* Principles, Guidelines and Techniques

4 Principles POUR
* Perceivable 
* Operable 
* Understandable
* Robust

AA Compliance meets most needs


Section 5: 4 Principles of WCAG 2.0

See Downlaod
* Keyboard cheat sheet

Perceivable 
* Provide appropriate content for all users regardless of disability or accessibility challenges they face
* Screen readers are for those with vision impairments. They can hear the web 
* Use alt attribute, describe image and how it matters to the story
* If the image is decorative or redundant you can leave the alt empty. 
* If no alt attribute exists the SR will read the file name. This is the worst experience
* Captions and transcripts provide the hard of hearing with written text - ideal for videos
* Avoid color alone to convey information
* To test for color print out your website in black and white and see if you understand it. 
    * Set appropriate color contrast ratios
    * 5:1 ratio
    * Use online tools
    * Avoid auto play
* For people with colorblindness reds and greens often present themselves as Mustard color
* 

Operable 
* Can you do everything with a keyboard
* Goals
    * Get thru navigation links and sections
    * Get into and out of search and form fields
    * Navigate forms
* Avoiding Seizures
    * Flashing or blinking content may cause seizures
    * Warnings don’t work
    * Flashing and Blinking is Bad UX and UI
* Give you users plenty of time to complete tasks
    * Try not to use timers

Understandable
* Make sure content is digestible by everyone. Even those with accessibility concerns and especially those with cognitive disabilities 
* Avoid
    * Unusual words
    * Abbreviations
    * Jargon
    * Acronyms
    * If unavoidable then define the reasoning for these. Ie a technical web page 
* Write to a 9th grade reading level
    * Determined to be the best level for cognitive issues and those without
    * Use shorter paragraphs
    * 2-3 sentence paragraphs
    * Each sentence about 15 words
    * Use tools to check
* Forms best practice
    * Page focus is always visible 
    * Identify input error and suggest fixes
    * Avoid color only to indicate errors
    * Clearly label elements and give instructions
    * Labels on top, instructions on bottom 
    * Provide help option
    * 

Robust
* Make sure site works with all user agents (browsers) and assistive technology
* Screen readers present info in a linear fashion
* Content must make sense when it is out of context
    * Avoide links such as “learn more”
* Find balance between real estate, aesthetics and descriptive usability
* Do headers make sense out of context
* Do the first couple sentences in a paragraph make sense
* Are we using familiar items for their intended purpose 




























































