# maven-repo

mvn install:install-file -Dfile=${path}/${artifactId}.jar -DgroupId=com.github.supaide -DartifactId=testlib -Dversion=1.0.0 -Dpackaging=jar

git add -f com/github/supaide/${artifactId}

allprojects {
    repositories {
        jcenter()
            maven{
                url 'https://raw.githubusercontent.com/supaide/maven-repo/master'
            }
    }
}

compile 'com.github.supaide:testlib:1.0.0'
