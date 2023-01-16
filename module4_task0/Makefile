.PHONY: build
build: ## Generate the website from the markdown and configuration files in the directory dist/.
	@hugo
	@touch awesome-api

.PHONY: clean
clean: ## Cleanup the content of the directory dist
	@rm -rf dist

.PHONY: post
post: ## Create a new blog post whose filename and title come from the environment variables POST_TITLE and POST_NAME
	@rm -Rf content/posts/$(POST_NAME).md
	@hugo new posts/$(POST_NAME).md
	@sed -i '0,/title/s/.*title.*/title: "$(POST_TITLE)"/' content/posts/$(POST_NAME).md
	@sed -i 's/draft:.*/draft: "false"/' content/posts/$(POST_NAME).md

.PHONY: package
package: ## create a file named awesome-website.zip
	@make build
	@zip awesome-website.zip dist/ -r

.PHONY: unit-tests
unit-tests: ## ERROR: No comments found for target unit tests in ./Makefile
	@touch coverage-units.out

.PHONY: integration-tests
integration-tests: ## ERROR: No comment found for target integration-tests in ./Makefilei
	@touch coverage-integrations.out

.PHONY:validate
validate: ## ERROR: No comment found for target validate in ./Makefile

.PHONY: lint
lint: ## Check markdown files for any syntax mistable
	@markdownlint README.md DEPLOY.md

.PHONY: help
help: ## Prints out the list of targets and their usage
	@echo "Usage: make <command>"
	@echo "-----"
	@@fgrep -h "##" $(MAKEFILE_LIST) | fgrep -v fgrep | sed -e 's/\\$$//' | sed -e 's/##//'
