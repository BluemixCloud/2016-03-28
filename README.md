# IBM Cloud Advisor 101 Course

![Galvanize](images/galvanize.png)
![Watson](images/watson.gif)
![IBM Bluemix](images/ibm.jpg)

## Cohort 2016-03-28

### Food Schedule
  - Monday: 8am - 5pm (Breakfast and Lunch served)
  - Tuesday - Friday: 9am - 5pm
  - Friday: 5pm (Hosted Happyhour on Rooftop)

### Coding Schedule
  - Monday: Fundamentals, Backend
  - Tuesday: DevOps, Cloud Foundry, OpenWhisk, NodeRED
  - Wednesday: Fullstack Apps with Microservices
  - Thursday: Fullstack Apps with Microservices
  - Friday: Hackathon

### Syllabus

#### Arrive & Setup
  - Meet & Greet + Breakfast
  - Get on Network (g|events -> machinelearning)

#### Introductions
  - Roll Call, Verify Emails
  - Students
  - Instructor
  - About Galvanize, http://www.galvanize.com/
  - Course Overview
  - Distribute Badges

#### Bluemix Garage
  - https://www.ibm.com/cloud-computing/bluemix/garage/
  - Presentation
  - Design Thinking

#### Assessment
  - Technical
  - Cloud
  - Agile

#### Cloud 9 Setup
  - https://c9.io/
  - Create a Custom Ubuntu Workspace
  - Open Terminal

```sh
rm README.md
wget https://raw.githubusercontent.com/chyld/devops/master/c9-setup.sh
chmod +x c9-setup.sh
./c9-setup.sh
rm c9-setup.sh
vi ~/.gitconfig
exit
```

#### Git & JazzHub
  - [Git](http://git-scm.com/)
  - [JazzHub](https://hub.jazz.net/)

#### JazzHub
![JazzHub](images/jazzhub.png)

#### Git Commands
```sh
# To clone an existing repository
git clone https://github.com/BluemixCloud/2016-03-28

# To initialize an empty git repository
git init

# To check the status of your repository
git status

# To see all the local and remote branches
git branch -av

# To check your remote repository
git remote -v

# To see all of your commits
git log

# To push your code up to the remote repository
git add .
git commit -am "enter a commit message here"
git pull
git push
```

#### Modern Programming Fundamentals
  - JavaScript, https://developer.mozilla.org/en-US/docs/Web/JavaScript
  - Node.js, https://nodejs.org/en/
  - Module system
  - Node Package Manager, https://www.npmjs.com/
  - Pair Programming
  - Test Driven Development: [Mocha](https://mochajs.org/) | [Chai](http://chaijs.com/)

#### Project 1
  - This project will be done as a pair
  - Pick a project manager
  - The PM will go here, https://hub.jazz.net/project/chyld/fundamentals
  - PM, click the "Fork Project" button
    - Name the project: fundamentals
    - Check all the boxes
    - Click Create
  - PM, click the "Members" link on the left, add your partner to the repository
  - Both people can now push and pull the repository
  - Both, on the project page, click the "Git URL" link
  - Both, copy that link
  - Both, open C9 terminal
  - Both, make sure you're in the `~/workspace` directory

```sh
git clone <link you copied above>
cd fundamentals
npm install
npm test test/square.js # this should pass
npm test test/add.js # this fails, fix
npm test # to run all tests
```

  - Fix the remaining tests
  - Take turns, with both people fixing the failing tests
  - Push your completed code up the repository

#### Backend
  - HTTP, https://www.w3.org/Protocols/rfc2616/rfc2616.txt
  - [Express.js](http://expressjs.com/)
  - Performance: CPU Bound, Memory Bound, I/O Bound
  - Async programming with callbacks & promises
  - Node.js perf test with Apache Bench
  - Run sequentially `-c 1`, then run in parallel `-c 1000`
  - `ab -n __ -c __ http://0.0.0.0:8080/`
  - Compare perf to Rails app
  - Use `rake routes` and browser to demo REST API
  - Parse a deeply nested JSON structure; [Weather Data](weather.json)

#### Project 2
  - This project will be done as a pair
  - Pick a project manager
  - The PM will go here, https://hub.jazz.net/project/chyld/backend
  - PM, click the "Fork Project" button
    - Name the project: fundamentals
    - Check all the boxes
    - Click Create
  - PM, click the "Members" link on the left, add your partner to the repository
  - Both people can now push and pull the repository
  - Both, on the project page, click the "Git URL" link
  - Both, copy that link
  - Both, open C9 terminal
  - Both, make sure you're in the `~/workspace` directory

```sh
git clone <link you copied above>
cd fundamentals
npm install
npm test # to run all tests
# comment out every failing test except one
```

  - Fix the remaining tests
  - Take turns, with both people fixing the failing tests
  - Push your completed code up the repository

#### DevOps Services
  - https://hub.jazz.net/
  - JazzHub
  - Code Editor
  - Track & Plan
  - Build Pipeline
    - Build a Stage
    - Add Jobs to a Stage
    - Jobs can be re-ordered

#### Cloud Foundry
  - https://www.cloudfoundry.org/
  - `cf api https://api.ng.bluemix.net`
  - `cf login`
  - `cf target`
  - `cf marketplace`
  - `cf apps`
  - `cf services`
  - `cf --help`
