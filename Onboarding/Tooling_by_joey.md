# Tooling by Joey Tuong

### Link: https://drive.google.com/file/d/1E_onbqzzdlCpwnEAR3jRb6B5Mpage1Ik/view

### Ticketing on Phabricator
- Ticketing system is called MANIPHEST
- Person assigned to it is the person responsible
- Priority - needs triage initially, and then will be changed by respective person
- Subscribers - people who get notified about changes

### Workboard (Like Trello)
- Tickets start at first column and then go through the right

### Code hosting
- Code / repo hosted on phabricator
- Once you cloned the code bases and have got a ticket assigned, its time to start coding

## Development
### Backend
- FLI manages development instances

### Frontend
- Just locally, point to shared development env
- Frontend Stack: AngularJS + Typescript + RxJS
- Two building blocks: Datastore and Bits

#### Datastore
- Like react's redux - a centralised state management system
- All frontend component will be only talking to one guy - the datastore
- All data model stored in datastore
- You don't manipulate it directly, all frontend component will trigger action and its event driven, so when event happens, operation happens within
- This is one-way communication (ONE WAY DATA BINDING), not two-way, because you trigger -> make decision -> and then react to what the model says
- One way data binding is safer
- Datastore will also wrap up all backend API for developers, and you just have to talk to you datastore

#### Bits
- Component library -> like google material
- Not only the look and feel, but also the dynamic (with angular behind)
- We dont need to think about the nitty gritty details of a button, all of this is centralised and managed by Bits
- CSS has been made very simple - ALL YOU NEED TO KNOW IS FLEXBOX
- We try to make the developer experience as simple as possible

### Version Control
- Use GIT, connected to phabricator, integrated by Arcanist
- Normal workflow: Commit to the code base in a branch, the branch stay local (we usually dont push the branches, you can do whatever with it), and you use:
`arc diff`
- Arc diff will also check for structure ETC.
- In the summary of arc diff, go ham on details
- There is also test plan - how you test your changes and how it should be run (this is mandatory)
- Reviewers (code reviewer) is your team lead
- Once you submit it, it will go on Phabricator

### Review Process
- Allow for comments and checklists

### Documentation
- Ideally, all public interfaces, whether it be classes/files/modules - they should contain docstring (""" Comment """)
- In phabricator, it immediately makes a manual
- If we make changes to the API, must change the API documentation

## CI 
- Jenkins is CI tool, builds the apps, runs linters and checks to see if everything is okay, runs testing, does uploading assets. 
- Rocket Chat -> most things are reported here
- rollback time = time before old services die (so if the new services go wrong, we can quickly change it back)

## Database Access
- Our database is MySQL, so most people use either SQL Datagrip or MySQL WorkBench
- Brains powered by redash which we can see other people's query? 

## Bug Report Template
- What are you trying to do? Please include steps
- What was your expected outcome?
- What was the actual outcome?
- Which account did you use?
- Which platform (main website, ios, android, etc) and browser did you use?
- Attach screenshots if you have some

## Post Mortems
- What went wrong etc etc: Happens on Tuesdays!

