pipeline {
    agent any

    parameters {
        string(name: 'VAR', defaultValue: 'true', description: 'Enter true or false')
    }

    environment {
        // Utiliser le paramètre directement sans besoin de le réassigner
        VAR = "${params.VAR}"
    }

    stages {
        stage("Display param") {
            steps {
                script {
                    // Utilisation de VAR en tant que chaîne de caractères pour la comparaison
                    if(VAR == 'true') {
                        echo "my value is true"
                    } else if(VAR == 'false') {
                        echo "my value is false"
                    } else {
                        echo "VAR contains an unexpected value"
                    }
                }
            }
        }
    }
}
