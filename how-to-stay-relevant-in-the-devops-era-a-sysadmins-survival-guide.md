# How to stay relevant in the DevOps era: A SysAdmin's survival guide

The merging of development and operations to speed product delivery, or DevOps, is all about agility, automation and information sharing. In DevOps, servers are often treated like cattle”that can be easily replaced, rather than individual pets”to be nurtured.

System administrators that built their careers configuring and troubleshooting individual servers still have a role to play in [this new world](https://www.reddit.com/r/sysadmin/comments/3ry602/is_devops_andor_sre_becoming_the_new_sysadmin/). But they must learn to apply their skills to entire [IT infrastructures described and managed by code](http://techbeacon.com/why-you-should-embrace-software-defined-data-center). They must learn to [manage cloud services](http://techbeacon.com/cloud-operations-security-developers-survival-guide) and use [automated deployment tools](http://techbeacon.com/running-gauntlet-setting-your-first-deployment-pipeline) and code repositories—and to share their expertise with others.  

_\[ Continuous delivery and release automation \(CDRA\) demands speed and quality. Find out how in_ [_TechBeacon's guide to CDRA_](https://content.microfocus.com/l/continuous-delivery-release-automation-tb?utm_source=techbeacon&utm_medium=techbeacon&utm_campaign=00134846)_. Plus: Get the_ [_Forrester Wave on CDRA_](https://content.microfocus.com/continuous-delivery-release-automation-tb/forrester-wave-cdra-q418?lx=-DC2cJ&utm_source=techbeacon&utm_medium=techbeacon&utm_campaign=00134846)_.  \]_

#### **Debugging at scale**

A system administrator's debugging skills still matter in DevOps, says [Nathen Harvey](https://twitter.com/nathenharvey), vice president of community development at Chef.  

> “You cannot automate what you can’t understand.”

What changes, Harvey says, is the scale, complexity, and the need to turn a properly tuned server into code, "a recipe I can execute in a machine, and lay down those changes in a consistent, repeatable way \[for new server deployments.\]” 

In DevOps, system administrators also must learn to focus on the infrastructure they can control \(often from the operating system on up\) because in the cloud they usually won’t have access to, or information about, the underlying hardware, storage, or networks.  

[Chris Gervais](https://twitter.com/cgervais), vice president of engineering at Threat Stack, says: “At the OS level, you can see if you have a runaway process that’s consuming too much system memory." But you can’t do some of the kernel tuning you used to do on a Linux container in a private cloud, he says.

#### **How resources affect decisions**

In DevOps, if a system fails or suffers [performance problems](http://techbeacon.com/why-performance-engineering-essential-business-success), it is often automatically removed and replaced with a healthy one, rather than going to the trouble of debugging it. If the same system image runs fine when redeployed, the problem may have been with the cloud hardware or a corrupted system image, says Gervais. “If the same problem persists when the server is brought back up, you then begin your root cause analysis.”

One area where system administrators will see fewer changes to their jobs is in supporting legacy applications that are too expensive or difficult to move to the cloud, says [Brian Day](https://twitter.com/logicalis_bday), senior director of cloud services at Logicalis. That means they still need individual configuration and troubleshooting.

[Eric Turnquist](https://www.linkedin.com/in/erictq), senior director of IT at Ipswitch, says legacy systems will always require hands-on experience, creating demand for long-serving system administrators.

> “There’s usually tribal knowledge around legacy systems—people that know the old systems because they were here when they were built—that is tough to replace."

In addition, in-depth knowledge of system administrators will always be critical when new servers need to be configured, new tasks automated, or unexpected problems solved, says [Ashley Mathew](https://www.linkedin.com/in/ashley-mathew-8b535658), team lead at SmartFile.

_\[ Learn_ [_the secrets of successful DevOps initiatives_](https://content.microfocus.com/l/optimize-devops-tb?utm_source=techbeacon&utm_medium=techbeacon&utm_campaign=00134846) _in TechBeacon’s Guide. Plus: Get the_ [_Optimizing DevOps Initiatives: Both Sides of the DevOps Divide_](https://content.microfocus.com/optimize-devops-tb/optimizing-devops-EMA-report?lx=vm26kZ&utm_source=techbeacon&utm_medium=techbeacon&utm_campaign=00134846) _report \]_

#### **Needed: New technical skills**

For system administrators to use their configuration, monitoring and debugging skills in DevOps, they must build on existing skills and learn new tools.

**Languages**

Most, for example, already use shell scripts to automate repetitive or error-prone tasks, which is a key practice in DevOps, says Mathew. But she adds that learning a programming language such as Python or Perl will help them create more robust scripts far more quickly.

**Cloud services**

Since most DevOps systems run in the cloud, learning the management interfaces to Infrastructure as a Service offerings such as Amazon Web Services \(AWS\) or Microsoft Azure is valuable, says Day.  [Bobby Smith](https://github.com/denodaeus), director of research and development at QASymphony, says, “Anyone with basic shell scripting experience can pick \(them\) up pretty easily."

**Configuration management**

A [knowledge of configuration management tools, ](http://techbeacon.com/which-developer-skills-should-you-master-next-puppet-pops-out-hiring-lists)such[ ](http://techbeacon.com/which-developer-skills-should-you-master-next-puppet-pops-out-hiring-lists)as[ ](http://techbeacon.com/which-developer-skills-should-you-master-next-puppet-pops-out-hiring-lists)Puppet[ ](http://techbeacon.com/which-developer-skills-should-you-master-next-puppet-pops-out-hiring-lists)and Chef, can help system administrators automate the large-scale system provisioning that is central to DevOps, says Smith. Understanding the languages on which such tools are built, such as Ruby, makes it easier to extend their use to an organization’s specific needs.

**Other tools**

Inventory management tools such as PuppetDB help system administrators identify the resources they need to manage in fast-changing cloud environments, says Smith. For performance monitoring, he recommends tools such Nagios or Amazon CloudWatch, along with log aggregation products such as Logstash and Flume. Combined with a cloud service, he says, it’s possible to create systems of metrics to understand how your infrastructure is doing. That is very more important at scale, Smith says.

> "It's really  difficult to play 'whack a mole' and identify why an individual server failed."

The next step, Smith says, is combining build management tools, such as Gradle and Maven, with continuous integration platforms, such as Jenkins. This helps system administrators provide the agility promised by DevOps. He also recommends learning version control systems, such as Github, that hold the code that describes enterprise infrastructures.

#### **Time for an attitude adjustment**

Along with product and technology skills, system administrators need to make the mental leap from being experts in one vendor’s product to serving as generalists that work with others to fix problems. In DevOps, systems administrators must share their knowledge, not hoard it as a way of keeping their status or their jobs. For example, at Logicalis, software engineers write Chef configuration and policy cookbooks, and infrastructure engineers help software engineers instrument code for better monitoring and health checks, says Day.

“The conversation has changed from the old world,” where developers created applications without much knowledge of the infrastructure on which they must run, says Gervais. “Now, your value is not just what I can do, but how I help others, and how can I help align with the organization’s goals and objectives.”

> “The focus is not running IT infrastructure, but valuable business services.”

For system administrators that can make the leap, says Harvey, DevOps doesn’t make their specialized skills obsolete. Rather, he says, it can give them “super powers” to make those skills even more important to the business.

[https://techbeacon.com/devops/how-stay-relevant-devops-era-sysadmins-survival-guide](https://techbeacon.com/devops/how-stay-relevant-devops-era-sysadmins-survival-guide)

