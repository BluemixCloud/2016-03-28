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

  - To follow me on C9: [Chyld's C9](https://ide.c9.io/chyld/bluemix)

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
    - Name the project: backend
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
cd backend
npm install
npm test test/hello.js # this should pass
npm test test/multiply.js # this will fail, please fix
npm test # to run all tests
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
    - Use `manifest.yml` from [Backend](https://hub.jazz.net/project/chyld/backend)
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

#### OpenWhisk
  - Distributed, Event Driven Compute
  - [Notes & Lab](openwhisk.md)
  - To call from other code
    - `Content-Type: application/json`
    - `Authorization: Basic <based64 encoded key>`
    - [Base64 Utility](https://www.base64encode.org/)
    - `POST https://openwhisk.ng.bluemix.net/api/v1/namespaces/{org_space}/actions/{action-name}?blocking=true`

#### NodeRED
  - http://nodered.org/
  - https://console.ng.bluemix.net/catalog/starters/node-red-starter/
  - Additional Nodes & Flows, http://flows.nodered.org/
  - Create basic NodeRED flows, exercise functionality

#### Chrome Plugins
  - [JSON Formatter](https://chrome.google.com/webstore/detail/json-formatter/bcjindcccaagfpapjjmafapmmgkkhgoa)
  - [Angular Inspector](https://chrome.google.com/webstore/detail/ng-inspector-for-angularj/aadgmnobpdmgmigaicncghmmoeflnamj)

#### Front End Technologies
  - Browser
  - Angular, JavaScript MVC Framework, https://angularjs.org/
  - Twitter Bootstrap CSS Framework, http://getbootstrap.com/
  - Highcharts Analytical Charting, http://www.highcharts.com/
  - [Fullstack Template](https://hub.jazz.net/project/chyld/full-stack-template)

#### Project 3
  - Microservice Architecture
  - Prerequisites
    - [NodeRED](https://console.ng.bluemix.net/catalog/starters/node-red-starter/)
    - [OpenWhisk](https://new-console.ng.bluemix.net/openwhisk/)
    - [Twitch](https://api.twitch.tv/kraken/games/top)
  - Fork and Clone the [Fullstack Template](https://hub.jazz.net/project/chyld/full-stack-template)
  - In Angular, create 3 buttons
  - Button 1: Angular -> NodeRed -> OpenWhisk (squares an input number along each step)
  - Button 2: Angular -> Express (factorial of input number)
  - Button 3: Angular -> OpenWhisk (computes volume from three numbers)
  - Button 4: Show a list of top games on Twitch

#### Project 4
  - Twitter Sentiment Analysis
  - Prerequisites
    - [NodeRED](https://console.ng.bluemix.net/catalog/starters/node-red-starter/)
    - [OpenWhisk](https://new-console.ng.bluemix.net/openwhisk/)
    - [SQL Database](https://console.ng.bluemix.net/catalog/services/sql-database/)
  - Fork and Clone the [Fullstack Template](https://hub.jazz.net/project/chyld/full-stack-template)
  - Use NodeRED to create a flow that collects data from Twitter, performs Sentiment Analyis and inserts all that data into a DB2 SQL Database.
  - Create another flow to query the database and send back the result as JSON.
  - Create a button in Angular that will fetch all the data and display the data in a table and graph.

Code that aggregates the tweet + sentiment analysis data; ready for insertion into DB2.

```js
var place;

if(msg.location){
    place = msg.location.place;
}

msg.payload = {
    SCORE: msg.sentiment.score,
    TWEET: msg.tweet.text,
    USERNAME: msg.tweet.user.screen_name,
    LOCATION: place || 'unknown',
    CREATED_AT: 'TIMESTAMP'
};

return msg;
```

Script that creates the table inside DB2. Where the tweet data will be stored.

```sql
create table tweets
(
  id integer not null generated always as identity (start with 1 increment by 1),
  primary key (id),
  score integer,
  tweet varchar(256),
  username varchar(256),
  location varchar(256),
  created_at timestamp
);
```

SQL to collect all the tweet data from DB2.

```sql
select * from tweets;
```

Angular code to draw a chart using Highcharts.

```js
function drawChart(tweets){
  $('#graph').highcharts({
    title: {
      text: 'Tweet Sentiment Analysis'
    },
    xAxis: {
       categories: tweets.map(function(t, i){return i})
    },
    series: [
     {
       data: tweets.map(function(t){return t.SCORE})
     }
    ]
  });
}
```

#### Project 5
  - SMS Famous Movie Quote Service
  - Prerequisites
    - [OpenWhisk](https://new-console.ng.bluemix.net/openwhisk/)
    - [Twilio Credentials](https://www.twilio.com/user/account/messaging/dashboard)
    - [Twilio Phone Numbers](https://www.twilio.com/user/account/messaging/phone-numbers)
    - [Twilio API](http://twilio.github.io/twilio-node/)
    - [Quote Service](https://market.mashape.com/andruxnet/random-famous-quotes)
  - Fork and Clone the [Fullstack Template](https://hub.jazz.net/project/chyld/full-stack-template)
  - A user sends an SMS message to Twilio -> Express -> OpenWhisk -> Quote Service
  - The service returns a famous movie quote to the user's phone

#### Project 6
  - Slack Get Current Weather Forecast
  - Prerequisites
    - [OpenWhisk](https://new-console.ng.bluemix.net/openwhisk/)
    - [Slack Account](https://slack.com/)
    - [Slack Outgoing Webhooks](https://api.slack.com/outgoing-webhooks)
    - [Weather Service](http://openweathermap.org/current)
    - [Weather Service Key](http://home.openweathermap.org/users/sign_up)
  - Fork and Clone the [Fullstack Template](https://hub.jazz.net/project/chyld/full-stack-template)
  - User opens a slack channel, asks for the current weather for their zip code
  - Slack -> Express -> OpenWhisk -> Weather Service
  - The retured weather forcast gets displayed in the slack channel

#### Project 7
  - Camera Image Capture & Watson Analyis
  - Prerequisites
    - [Webcam.js](https://pixlcore.com/read/WebcamJS)
    - [Object Storage](https://console.ng.bluemix.net/catalog/services/object-storage/)
    - [NodeRED](https://console.ng.bluemix.net/catalog/starters/node-red-starter/)
    - [Visual Recognition](https://console.ng.bluemix.net/catalog/services/visual-recognition/)
    - [Cloudant](https://console.ng.bluemix.net/catalog/services/cloudant-nosql-db/)
  - Fork and Clone the [Fullstack Template](https://hub.jazz.net/project/chyld/full-stack-template)
  - User snaps a photo of herself using the laptop's webcam.
  - The photo gets uploaded to Object Storage.
  - Then the photo gets pulled into NodeRED, gets analyzed by Watson Visual Recognition
  - That data gets stored in a Cloudant database
  - A browser will query the Cloudant database and display all the results

#### Project 8
  - Microphone Audio Capture, Speech Translation
  - Prerequisites
    - [Object Storage](https://console.ng.bluemix.net/catalog/services/object-storage/)
    - [NodeRED](https://console.ng.bluemix.net/catalog/starters/node-red-starter/)
    - [Cloudant](https://console.ng.bluemix.net/catalog/services/cloudant-nosql-db/)
    - [Language Translation](https://console.ng.bluemix.net/catalog/services/language-translation/)
    - [Text to Speech](https://console.ng.bluemix.net/catalog/services/text-to-speech/)
    - [Speech to Text](https://console.ng.bluemix.net/catalog/services/speech-to-text/)
  - Fork and Clone the [Fullstack Template](https://hub.jazz.net/project/chyld/full-stack-template)

![Audio](images/audio.png)

![Whiteboard](images/whiteboard.jpg)

Buttons inside HTML

```html
<button ng-click="startRec()">Start</button>
<button ng-click="stopRec()">Stop</button>
```

Place at the bottom of your angular code in index.js

```js
var audio_context;
var recorder;

initAudio();

function startUserMedia(stream) {
  var input = audio_context.createMediaStreamSource(stream);
  recorder = new Recorder(input);
}

function initAudio(){
  try {
    window.AudioContext = window.AudioContext || window.webkitAudioContext;
    navigator.getUserMedia = navigator.getUserMedia || navigator.webkitGetUserMedia || navigator.mozGetUserMedia;
    window.URL = window.URL || window.webkitURL;

    audio_context = new AudioContext;
  } catch (e) {
    alert('No web audio support in this browser!');
  }

  navigator.getUserMedia({audio: true}, startUserMedia, function(e) {
    console.log('No live audio input: ' + e);
  });
}

function uploadAudio(){
  recorder && recorder.exportWAV(function(blob) {
    var formData = new FormData();
    formData.append("voice", blob);
    var request = new XMLHttpRequest();
    request.open("post", "/audio");
    request.send(formData);
  });
}
```

Functions to start and stop recording - also upload to server

```js
 $scope.startRec = function(){
    console.log('Recording: Start');
    recorder && recorder.record();
  };

  $scope.stopRec = function(){
    console.log('Recording: Stop');
    recorder && recorder.stop();
    uploadAudio();
    recorder.clear();
  };
```

REST API Endpoint in Express.js that will upload audio to NodeRED

```js
var os = new ObjectStorage('user_id', 'password', 'project_id', 'container_name', 'access_point_url');
os.setContainerPublicReadable();

app.post('/audio', uploadr.single('voice'), function(req, res){
  var name = 'audio-original-' + uuid.v1() + '.wav';
  os.uploadFileToContainer(name, req.file.mimetype, req.file.buffer, req.file.size)
  .then(function(file){
    var o = {url: 'http://___your_node_red___.mybluemix.net/translate-audio', json: true, method: 'post', body: {url: file}};
    request(o, function(e, r, b){
      res.send({payload: 'success'});
    });
  });
});
```

#### Hackathon
  - http://bluemixathon.devpost.com/
  - https://vimeo.com/137915648
  - http://www.linkedin.com/pulse/so-you-want-run-corporate-hackathon-vinod-ralh
  - Split into groups of 3 or 4
  - Each team build an application using Bluemix services and deploys using DevOps services
  - At the conclusion of the hackathon, each team demos their app to the class

#### Retrospective

#### Feedback
  - https://docs.google.com/a/galvanize.com/forms/d/1jRT3EE_acCe_V8iWA77nU8sdqhbBmIiHUsAiMVQt4Eo/viewform

#### Tour
  - Galvanize
  - Full Stack Classrooms
  - Data Science Classrooms
  - Bluemix Garage
  - Cloudant
  - Startups

#### Happy Hour on Roof

#### Collect Badges

# REFERENCES

### Bluemix Services
  - [SQL Database](https://console.ng.bluemix.net/catalog/services/sql-database/)
  - [Cloudant](https://console.ng.bluemix.net/catalog/services/cloudant-nosql-db/)
  - [Object Storage](https://console.ng.bluemix.net/catalog/services/object-storage/)
  - [Language Translation](https://console.ng.bluemix.net/catalog/services/language-translation/)
  - [Visual Recognition](https://console.ng.bluemix.net/catalog/services/visual-recognition/)
  - [Text to Speech](https://console.ng.bluemix.net/catalog/services/text-to-speech/)
  - [Speech to Text](https://console.ng.bluemix.net/catalog/services/speech-to-text/)

### Books
  - [You Don't Know JS 6-book series](https://github.com/getify/You-Dont-Know-JS)
  - [Eloquent JavaScript](http://eloquentjavascript.net/)
  - [Learning JavaScript Design Patterns](https://addyosmani.com/resources/essentialjsdesignpatterns/book/)
  - [Human JavaScript](http://read.humanjavascript.com/ch04-organizing-your-code.html)
  - [JavaScript Allonge](https://leanpub.com/javascript-allonge/read)
  - [Speaking JavaScript](http://speakingjs.com/es5/)

### Reference Links
  - [DB2 Data Types](https://www-01.ibm.com/support/knowledgecenter/SSEPGG_10.5.0/com.ibm.db2.luw.sql.ref.doc/doc/r0008483.html?cp=SSEPGG_10.5.0%2F2-12-2-3)
