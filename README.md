## CSSLint
A minimal CSSLint image.

## Usage

```bash
docker run -it --rm -v /path/to/code:/app millerrs/csslint
```

## Usage in Jenkins Pipeline

```groovy
stage('Run CSSLint') {
    agent {
        docker {
            image 'millerrs/csslint'
        }
    }
    steps {
        sh 'csslint path/to/code'
    }
}
```