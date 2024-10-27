Started by user Aditya M

[Pipeline] Start of Pipeline
[Pipeline] node
Running on Jenkins
 in C:\ProgramData\Jenkins\.jenkins\workspace\IBMTest
[Pipeline] {
[Pipeline] stage
[Pipeline] { (Checkout)
[Pipeline] git
The recommended git tool is: NONE
No credentials specified
Cloning the remote Git repository
Cloning repository https://github.com/THEOTNER/junkinsibm.git
 > git.exe init C:\ProgramData\Jenkins\.jenkins\workspace\IBMTest # timeout=10
Fetching upstream changes from https://github.com/THEOTNER/junkinsibm.git
 > git.exe --version # timeout=10
 > git --version # 'git version 2.47.0.windows.1'
 > git.exe fetch --tags --force --progress -- https://github.com/THEOTNER/junkinsibm.git +refs/heads/*:refs/remotes/origin/* # timeout=10
 > git.exe config remote.origin.url https://github.com/THEOTNER/junkinsibm.git # timeout=10
 > git.exe config --add remote.origin.fetch +refs/heads/*:refs/remotes/origin/* # timeout=10
Avoid second fetch
 > git.exe rev-parse "refs/remotes/origin/main^{commit}" # timeout=10
Checking out Revision 5e24de25f0cb8ccfa463380ce0e2a4ceced816da (refs/remotes/origin/main)
 > git.exe config core.sparsecheckout # timeout=10
 > git.exe checkout -f 5e24de25f0cb8ccfa463380ce0e2a4ceced816da # timeout=10
 > git.exe branch -a -v --no-abbrev # timeout=10
 > git.exe checkout -b main 5e24de25f0cb8ccfa463380ce0e2a4ceced816da # timeout=10
Commit message: "Initial commit"
First time build. Skipping changelog.
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Build)
[Pipeline] echo
Building the application...
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Test)
[Pipeline] echo
Running tests...
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Deploy)
[Pipeline] echo
Deploying the application...
[Pipeline] }
[Pipeline] // stage
[Pipeline] stage
[Pipeline] { (Declarative: Post Actions)
[Pipeline] echo
Pipeline succeeded!
[Pipeline] }
[Pipeline] // stage
[Pipeline] }
[Pipeline] // node
[Pipeline] End of Pipeline
Finished: SUCCESS
