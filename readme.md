
Task base path calculation fault.

To reproduce on Windows 10

1. Clone VSCODE_TEST project - install typescript if required: npm install.
2. Double Click the VSCODE_TEST.code-workspace file from Windows Explorer.

3A. Observe - Menu: Terminal > Run Task... will produce a task list comparable to that seen in the attached "Dbl Click code-workspace.png"
3B. Observe - Using "Run Task..." will result in a warning dialog lower right... "There are task errors. See the output for details"

4. Switch to Debug mode in VSCode - 

4A. Observe: Running the "Launch Program (VSCODE_TEST)" launch task will result in an error "could not find the task buildTask". 
4B. Observe: same warning dialog as 3B.

5. Close workspace.
6. Open VSCODE_TEST.code-workspace using Menu: File > Open Workspace...

7A. Observe - Menu: Terminal > Run Task... will produce a task list comparable to that seen in the attached "File Open Workspace.png"
7B. Observe - no task errors are reported.

8. Switch to Debug mode in VSCode - 

9A. Observe: Running the "Launch Program (VSCODE_TEST)" launch task will result in no errors.
9B. Observe: preLaunchTask task runs - compiles using TSC
9C. Observve: program runs on internal terminal

