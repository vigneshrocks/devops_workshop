//test comment
node('master') {
    stage('Git Clone') {
        git branch: 'master', changelog: true, url: 'https://github.com/vigneshrocks/devops_workshop.git'
        sh "ls"
    }

    stage('Project Name') {
        def projects = readJSON file: "${env.WORKSPACE}/input.json"

        echo "current workspace is ${env.WORKSPACE}"
        echo "Project name is ${projects.projects.project[0].name}"
        echo "project nmae is ${projects.projects.project[1].name}"
        echo "project nmae is ${projects.projects.project[1].solution}"         
    }
    
    stage('RUN Python Script') {
        sh "chmod 777 hello-world.py" 
        sh "./hello-world.py"
    }

}
