## …or create a new repository on the command line
```git
echo "# sample_git" >> README.md
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/nanumhn/sample_git.git
git push -u origin main
```

## …or push an existing repository from the command line
```git
git remote add origin https://github.com/nanumhn/sample_git.git
git branch -M main
git push -u origin main
```


## pull 명령 실행시 refusing to merge unrelated histories 
```git
git pull origin 브런치명 --allow-unrelated-histories
```

```git
C:\Users\gitProject>git push origin master
To https://github.com/userId/userProject.git
 ! [rejected]        master -> master (non-fast-forward)
error: failed to push some refs to 'https://github.com/userId/userProject.git'
hint: Updates were rejected because the tip of your current branch is behind
hint: its remote counterpart. Integrate the remote changes (e.g.
hint: 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```
## push 전에 먼저 pull을 해서 프로젝트를 병합
```git
refusing to merge unrelated histories
```

--allow-unrelated-histories   이 명령 옵션은 이미 존재하는 두 프로젝트의 기록(history)을 저장하는 드문 상황에 사용된다고 한다. 즉, git에서는 서로 관련 기록이 없는 이질적인 두 프로젝트를 병합할 때 기본적으로 거부하는데, 이것을 허용해 주는 것이다.
