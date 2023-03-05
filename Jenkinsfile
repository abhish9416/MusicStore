pipeline{
    agent{label 'AGENT'}
    triggers {pollSCM('* * * * *') }
    stages{
        stage('VCS'){
            steps{
                git url: 'https://github.com/abhish9416/MusicStore.git',
                branch: 'declarative'
            }
        }
        stage('Build'){
            steps{
                sh 'dotnet restore ./MusicStore/MusicStore.csproj && dotnet build ./MusicStore/MusicStore.csproj'
            }
        }
        stage('Test'){
            steps{
                sh 'dotnet test ./MusicStoreTest/MusicStoreTest.csproj'
            }
        }
    }
}