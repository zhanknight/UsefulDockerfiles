## Linguist ##
This dockerfile runs an alpine ruby image and installs and executes GitHub's **Linguist** with the `--breakdown` argument. 
Linguist will analyze the language content of a git repo.

### Usage ###
1. Build the image: `docker build -t linguist:latest .` in the directory where the Dockerfile is located.
2. Run the container: `docker run --rm -v absolute_path_to_git_repo_directory:/home -w /home -t linguist:latest`
    - `--rm` will remove the image after running and `-v` will allow volume mounting so the container can read the git repo you'd like linguist to analyze.
