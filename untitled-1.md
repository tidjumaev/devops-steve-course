# 6 of my favorite Jenkins plugins - Level Up

Jenkins is extendable via plug-in modules, and currently, there are 1500+ plugins to choose from. Anything that you can think of about Jenkins, such as PHP support, JIRA and Docker integrations can all be done through Jenkins plugins.  In our [Jenkins course](https://www.level-up.one/courses/), we have covered several useful plugins such as [build pipeline plugin](https://wiki.jenkins.io/display/JENKINS/Build+Pipeline+Plugin) and [copy artifact plugin,](https://wiki.jenkins.io/display/JENKINS/Copy+Artifact+Plugin) etc. In this post, I will introduce another 6 of my favorite Jenkins plugins.

## Server monitoring

### plugin: [Disk Usage plugin](https://wiki.jenkins-ci.org/display/JENKINS/Disk+Usage+Plugin)

Being a continuous integration server, monitoring the server is very important. This certainly is helpful for avoiding issues related to the server. Disk Usage Plugin is very simple and useful plugin. It helps you monitor the master and slaves. The disk space might not be a big issue but checking and monitoring it is a must. The Plugin has its own monitoring page which will allow you to see the overall metrics of your server. While this plugin is quite popular, another server monitoring plugin which is known as Monitoring Plugin has also proved its worth. So anyone of these can certainly be used.

![](https://www.level-up.one/wp-content/uploads/2017/09/Picture1-1-300x187.png)

## Dashboard and Views

### Plugin: [Build Monitor Plugin](https://wiki.jenkins.io/display/JENKINS/Build+Monitor+Plugin)

This build monitor plugin is actually a treat! With all your busy development schedule and tasks related to Jenkins, this plugin will allow you to work in a nice dashboard environment. The plugin is all about customizing your dashboard, displaying the status of your important jobs, and feeling happy while working! Not just this, the plugin is also helpful for identifying critical parts of the build process. It can then be used to pinpoint the issues related to it.

![](https://www.level-up.one/wp-content/uploads/2017/09/Screen-Shot-2017-09-22-at-9.54.08-PM-300x176.png)

### Plugin: [Nested View Plugin](https://wiki.jenkins.io/display/JENKINS/Nested+View+Plugin)

Organizing your jobs into separate views helps keep your Jenkins organized. In a bigger company you usually share Jenkins with other teams, therefore serval other jobs exist on the same Jenkins server. So you want your own structured view. Nested views plugin allows you to group relevant views together under a parent view, creating comfortably traversed view trees which can improve clarity and transparency.

![](https://www.level-up.one/wp-content/uploads/2017/09/nested_view1-300x153.png)

## Job Configuration

### Plugin: [Job Configuration History Plugin](https://wiki.jenkins.io/display/JENKINS/JobConfigHistory+Plugin)

We all know that Jenkins has many jobs. The JobConfigHistory Plugin saves the copy of all these jobs. Not just this, it also takes care of the system configurations. This plugin is simple and easy to use. The plugin displays a list of the jobs, provides backup and also keeps a track of the changes that have been made to any particular job. The plugin is quite useful for lengthy and big projects where the number of jobs is more.

![](https://www.level-up.one/wp-content/uploads/2017/09/diff_list2-300x98.png)

## UI Customization

### Plugin: [Green Balls](https://wiki.jenkins-ci.org/display/JENKINS/Green+Balls)

Blue balls are used in Jenkins to mark successful builds [**for a reason.**](https://jenkins.io/blog/2012/03/13/why-does-jenkins-have-blue-balls/) However, there are lots of people who prefer green ball. This green ball plugin changes the ball color and is in the list of top 10 installed plugins.

![](https://www.level-up.one/wp-content/uploads/2017/09/both_balls-300x171.png)

## Pipeline

### Plugin: [Pipeline as Code](https://jenkins.io/solutions/pipeline/)

The Jenkins Pipeline as Code plugin is really a game changer for Jenkins users. users now can implement a project’s entire build/test/deploy pipeline in a Jenkinsfile and store that alongside their code, treating their pipeline as another piece of code checked into source control. The Pipeline plugin makes pipelines scriptable and it is an incredibly powerful way to develop complex, multi-step DevOps pipelines. It allows you to version control your configuration, regenerate your jobs on the fly.We are currently working adding new

We are currently working on adding new lectures in our [Jenkins course](https://www.level-up.one/courses/) to cover Jenkins Pipeline as Code plugin. Stay tuned!

![](https://www.level-up.one/wp-content/uploads/2017/09/Screen-Shot-2016-08-04-at-7.29.54-PM-300x150.png)

## Wrap up

Jenkins is really versatile via the extensibility of plug-in modules. Anything that you can think of about Jenkins can usually be done through Jenkins plugins.

Look for more Jenkins customization? Search in the list of available plugins under the Jenkins plugin manager and you shall find!

