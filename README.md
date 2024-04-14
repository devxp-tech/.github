# .github
## GitHub Template Repo

This repository store the DevXP-Tech workflow templates.
## 🚦 Pipeline Workflow

```mermaid
graph TD;
    main-->Setup-Environment;
    main--docker-compose-->Test-Application;
    main--code-quality-->SonarQube-Scan;    
    Setup-Environment-->Build-and-Push;
    Test-Application-->Build-and-Push;
    SonarQube-Scan-->Build-and-Push;    
    Build-and-Push--security-gateway-->Trivy-Scan;
    Trivy-Scan-->GitOps-Deploy;
    GitOps-Deploy--notify-->Slack;
```

## feature tests 
## release build-and-push, deploy
## hotfix tests , build-and-push, deploy
## main promote
