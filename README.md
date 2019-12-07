# WindowsContainerBuildImage
Docker files and scripts for creating a Windows Server Core image with builds tools and Azure Pipelines build agent


docker build -f .\Dockerfile . -t win-vsts-agent


```powershell

docker run -d -m 2GB --name $name `
--restart=always `
--storage-opt size=10GB `
-e TFS_URL=$tfs_url `
-e TFS_PAT=$pat `
-e TFS_POOL_NAME=$pool_name `
-e TFS_AGENT_NAME=$agent_name `
-v //./pipe/docker_engine://./pipe/docker_engine `
win-vsts-agent
```