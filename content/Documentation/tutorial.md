# Tutorial
Build Your First Shitty Site

## Install SSSG

1. [Install the go toolchain](https://go.dev/doc/install) if you don't have it already.
2. Clone the repository:
```bash
git clone https://github.com/ajr-cabbage/sssg.git
```
3. Install sssg in your default go path:
```bash
cd src/ && go build -o ~/go/bin/sssg
```

## Start a new site project

1. Create a new directory for your site:
```bash
mkdir shitty-example && cd shitty-example
```
2. Get things started with ```sssg init```. This will create the necessary directories and a 'config.json' with default values. Take a look in the 'config.json'. Change the site name, modify the directories to suit your use case, make some new themes and change them. If you make changes, you can remove any or all of the generated directories and ```sssg init``` again. The project directory will match your specifications in 'config.json'.
3. With the default configuration, the 'content' directory is where you will build create your markdown documents. Be sure to start with an 'index.md' in the 'content' directory. This will become the index.html in the target directory that gets served. Try the example 'index.md' below for starters:

```markdown
## My First Shitty Site

Welcome to the world wide web Tim Berners-Lee dreamed of.
We have strayed from the path, but it's not too late to turn it around.
```

4. Generate your html:
```bash
sssg build
```
5. Serve your new website:
```bash
sssg serve
```
You have your very own site served on localhost! Bask in the glory.

## What to do next?

- This is the bare minimum to get you started on the path of tinkering on the web. The CSS theme and HTML template provided is terrible, so start there if it's too hard to look at.
- Have a pile of markdown documents an llm spit out? Turn those into something a little easier to read and share.
- Serve it on the local network for your household or serve it on the web. [Tailscale](https://tailscale.com/) is an easy way to serve the site to your friends and family or out on the web for anyone to stumble on. Buy a domain and hook it up to [Caddy](https://caddyserver.com/) to get it out there with your domain.
- Crack open the source code and make it a better site generator.
- Go nuts, have fun.
