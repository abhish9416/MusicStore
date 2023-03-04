node('AGENT'){
    stage('version control system'){
        git url: 'https://github.com/abhish9416/MusicStore.git',
            branch: 'scripted'
    }
    stage('Build the application'){
        sh 'dotnet build MusicStore.sln'
    }
}