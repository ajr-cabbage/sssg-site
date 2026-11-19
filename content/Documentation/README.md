# README
# SSSG 💩
The Small, Shitty, (static) Site Generator

## Motivation
There are a bunch of wonderful site generators out there, but I want one that makes writing and publishing the focus. No fluff, no features, just a way to take your thoughts and push it to your very own website. It was the dream of the internet when I was young, and it would be nice to capture that creativity without any crap coming with it. Those sites I made as a kid were shitty. This site generator is also shitty, and I love it dearly. This was created with my kids in mind. When they are old enough to write, they can make their own sites. As they learn more, they can accomplish more.

## Quick Start
- Requirements:
  - go 1.26+
  - goldmark - ```go get github.com/yuin/goldmark```
- Clone the repo and ```go build .```
- See 'Configuration' for first time setup

## Usage
```sssg <command> -<options> <parameters>```
- ```sssg init```
  - initialize a site project in the current directory with application default configuration
- ```sssg build```
  - no flags - build all markdown in the content directory
  - ```-f <filename.md>``` - build only the specified markdown file
- ```sssg config```
  - ```set <key> <value>``` - modify config.json through via cli
  - ```get <key>``` - print config value to the console
- ```sssg serve```
  - no flags - serve your target directory over http on the port specified in config.json
  - ```-p <port-num>``` - override the default port
  - ```-d``` - start server deteched from current shell session
- ```ssssg theme```
  - <theme-name.css> - change themes live - no server restart requried
- ```sssg help <command>```
  - no params - list available commands with description
  - ```<command>``` - show command usage

## Configuration
config.json - modify directly or edit single values via cli. See "config" command.
- "source_path" - the source directory for your markdown files
- "target_path" - the destination directory for generated html
- "assets_path" - directory for images and other content
- "template_path" - directory for html templates
- "theme_path" - css directory to use
- "theme" - css file
- "port" - default http port

## Contributing
- Glad to take contributions. Please fork and sumbit a pull request on the main branch.
- This was made with learning in mind. For that reason, no LLM contributions.
  - If you wish to extend with LLMs, no judgement, just please fork. 
- If it helps you or your children learn something, it will have been successful.
