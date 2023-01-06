#Awesome Inc. Website Docs
Welcome to our site!!

## Prerequisites
- Hugo v0.80+ must be used.
- Use the theme “ananke” for the website
- The website title should be “Awesome Inc.”
- All of the website’s source code is stored under a directory named module1_task2
- GNU Make version 3.81 or 4.0 must be used
- Makefile present
- There are no Git Submodules

## Lifecycle
- **POST**: Generate the website from the markdown and configuration files in the directory `dist/`.
- **BUILD** : Cleanup the content of the directory `dist/`
- **CLEAN** : Create a new blog post whose filename and title come from the environment variables `POST_TITLE` and `POST_NAME`.
- **HELP** : Shows a short help description about Makefile usage.
