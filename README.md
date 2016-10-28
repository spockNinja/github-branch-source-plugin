# GitHub Branch Source plugin for Jenkins

#### Initial setup for java/maven
```
$> brew update
$> brew cask install java
$> brew install maven
$> export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk1.8.0_112.jdk/Contents/Home
```

#### Pushing changes after PRs
```
$> mvn package
$> scp target/github-branch-source.hpi aws.JenkinsMaster:~/github-branch-source.hpi
$> ssh aws.JenkinsMaster
>>
>> cd /var/lib/jenkins/plugins
>> mv github-branch-source.hpi github-branch-source.hpi.bak
>> mv ~/github-branch-source.hpi ./
>> touch github-branch-source.hpi.pinned
```
