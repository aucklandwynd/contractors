# Local Development
To develop this site locally:

1. Install Ruby: https://www.ruby-lang.org/en/documentation/installation/

2. Install Jekyll:
```bash
gem install bundler jekyll
```

3. Create a Gemfile in the project root:
```bash
touch Gemfile
```
```ruby
# ./Gemfile
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
```

4. Install dependencies:
```bash
bundle install
```

5. Run the site:
```bash
bundle exec jekyll serve
```

6. Visit `http://localhost:4000/contractors/` in your browser

## Prerequisites
* bundler
* jekyll
* ruby

## Recommended VS Code Extensions
* Jekyll Run (by Dedsec727) - This extension can simply Run your Jekyll site locally and opens your site in browser.
* Liquid (by panoply) - VS Code support for [Liquid](https://shopify.github.io/liquid/).
* Jekyll Syntax Support (by Ed Heltzel) - Jekyll specific syntax highlighting.
* Live Server (by Ritwick Dey) - Launch a local development server with live reload feature for static & dynamic pages.

### Install Ruby
For the latest guidance see https://www.ruby-lang.org/en/documentation/installation/.

#### Windows
Download and install Ruby+Devkit from [RubyInstaller](https://rubyinstaller.org/). After installation, run:
```bash
ridk install
```
#### macOS:
```bash
brew install ruby
echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

#### Linux (Ubuntu/Debian)
```bash
sudo apt-get update
sudo apt-get install ruby-full build-essential zlib1g-dev
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

### Install Jekyll & Bundler
```bash
gem install jekyll bundler
```

## 1. Create a Gemfile
Create this file in your project root:
```bash
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
```

### Windows-specific Gems
```bash
gem "wdm", "~> 0.1.1", :platforms => [:mingw, :x64_mingw, :mswin]
gem "webrick", "~> 1.7"
```
Gemfile
## 2. Install Dependencies
```bash
bundle install
```

## 3. Run the Site
### Option 1: Using VS Code Tasks
Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on macOS), type "Run Task", and select "Serve Jekyll Site"

### Option 2: Using Terminal
```bash
bundle exec jekyll serve --livereload
```

### Option 3: Using the Debug Panel
Press **F5** or go to **Run** → **Start Debugging**

## 4. View Site
Open a web browser and navigate to:

http://localhost:4000

The `--livereload` flag will automatically refresh your browser when changes are made.

## Useful Commands
### Serve site with live reload:
```bash
bundle exec jekyll serve --livereload
```
### Serve site with drafts:
```bash
bundle exec jekyll serve --livereload --drafts
```
### Build only (no server):
```bash
bundle exec jekyll build
```
### Clean generated files:
```bash
bundle exec jekyll clean
```
### Update GitHub Pages Gem:
```bash
bundle update github-pages
```