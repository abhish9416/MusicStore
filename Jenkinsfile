pipeline{
    agent(label 'AGENT'){
        stages{
            stage('Version control system'){
                steps{
                    git url: 'https://github.com/abhish9416/MusicStore.git',
                        branch: 'declarative'
                }
            }
            stage('Build the application'){
                steps{
                    sh 'dotnet build MusicStore.sln'
                }

           }    
        }
    }
}