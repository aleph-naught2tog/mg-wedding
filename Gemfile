source "https://rubygems.org"
git_source(:github) { |repo| "https://github.com/#{repo}.git" }

####
# Welcome to your project's Gemfile, used by Rubygems & Bundler.
#
# To install a plugin, run:
#
#   bundle add new-plugin-name -g bridgetown_plugins
#
# This will ensure the plugin is added to the correct Bundler group.
#
# When you run Bridgetown commands, we recommend using a binstub like so:
#
#   bin/bridgetown start (or console, etc.)
#
# This will help ensure the proper Bridgetown version is running.
####

# If you need to upgrade/switch Bridgetown versions, change the line below
# and then run `bundle update bridgetown`
gem "bridgetown", "~> 2.0.0.beta2"

# Uncomment to add file-based dynamic routing to your project:
# gem "bridgetown-routes", "~> 2.0.0.beta2"

# Puma is the Rack-compatible web server used by Bridgetown
# (you can optionally limit this to the "development" group)
gem "puma", "< 7"

# Uncomment to use the Inspectors API to manipulate the output
# of your HTML or XML resources:
# gem "nokogiri", "~> 1.13"

# Or for faster parsing of HTML-only resources via Inspectors, use Nokolexbor:
# gem "nokolexbor", "~> 0.4"

group :bridgetown_plugins do
  gem "bridgetown-svg-inliner", "~> 2.0"
end

group :development do
  gem "foreman", "~> 0.88.1"
  # This is for formatting, etc. It also lints but honestly I picked it because I
  # needed a formatter and I figured I could TestDouble's setup docs and debugging
  # page to be accurate and indeed I was able to finally get this up and running
  # with VSCode's "Ruby LSP" plugin
  gem "standard", "~> 1.41", ">= 1.41.1"

  # This is the gem that powers the ERB formatting extension
  # NOTE:@MAX: I had to go into the container and run `gem install...` this myself
  gem "htmlbeautifier", "~> 1.4.3"
end
