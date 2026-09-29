
node {
    def PYTHON = 'C:\\Users\\HP\\AppData\\Local\\Microsoft\\WindowsApps\\python.exe'

    try {
        stage('Checkout') {
            checkout scm
        }

        stage('Extract Data') {
            bat "${PYTHON} extract.py"
        }

    } catch (err) {
        echo "Pipeline failed: ${err}"
        currentBuild.result = 'FAILURE'
    } finally {
        echo 'Pipeline completed.'
    }
}
