node {
    stage 'Build'
        git url: 'https://github.com/jsureshsg/maventest.git'

    stage 'Artifactory configuration'
        echo "artifactory config"

    stage 'Exec Maven'
        rtMaven.run pom: 'maven-example/pom.xml', goals: 'clean install', buildInfo: buildInfo

    stage 'Publish build info'
        server.publishBuildInfo buildInfo
}
