@Library('jenkins-shared-library') _

def configMap = [
    project: "roboshop",
    component: "catalogue"
]
  
echo "Going to execute Jenkins shared library"
// if branch is not equal to main, then run CI pipeline
if ( ! env.BRANCH_NAME.equalsIgnoreCase('main') ){
    //configMap["deploy"] = true
    nodeJSEKSPipeline(configMap)
}
else {
    configMap["jiraProject"] = "ROBO"
    nodeJSEKSMainPipeline(configMap)
}