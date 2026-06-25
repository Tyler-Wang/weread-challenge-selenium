## 保持与原仓库同步

### merge方式
1. 拉取上游更新
git fetch upstream

2. 合并主项目最新的 main 到你的 main
git checkout main
git merge upstream/main

3. 推送到你的 fork
git push origin main

### rebase方式
如果你希望同步主项目更新时不出现很多 merge commit，可使用 rebase
git fetch upstream
git rebase upstream/main
git push -f origin main


## scp复制
在当前项目根目录执行
scp -r ./src/ ./Dockerfile ./package-lock.json ./package.json root@服务器IP:/root/weread-challenge/DockerBuild
