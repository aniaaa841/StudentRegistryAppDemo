pipeline
{
    agent any

    stages
    {
        stage('Checkout')
        {
            steps
            {
                git branch: 'main', url: 'https://github.com/aniaaa841/StudentRegistryAppDemo'
            }
        }

        stage('Install dependencies')
        {
            steps
            {
                script
                {
                    bat 'npm install'
                }
            }
        }
        stage('Start application')
        {
            steps
            {
                script
                {
                    bat 'start /b npm start'
                }
                
            }
                        
        }
        stage('run tests')
        {
            steps
            {
                script
                {
                    bat 'npm test'                    
                }
            }
        }
    }       
    post
    {
        always
        {
            echo "CI pipeline completed"
        }
    }
}