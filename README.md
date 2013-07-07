# Actionview::LinkToBlock

[![Gem Version](https://badge.fury.io/rb/actionview-link_to_block.png)](http://badge.fury.io/rb/actionview-link_to_block)
[![Build Status](https://api.travis-ci.org/sanemat/actionview-link_to_block.png?branch=master)](https://travis-ci.org/sanemat/actionview-link_to_block)
[![Code Climate](https://codeclimate.com/github/sanemat/actionview-link_to_block.png)](https://codeclimate.com/github/sanemat/actionview-link_to_block)

Add helper method, `link_to_block`, `link_to_block_if`, `link_to_block_unless`, `link_to_block_unless_current`.
This is symmetrical to `link_to`, `link_to_if`, `link_to_unless`, `link_to_unless_current`.

`link_to_block*` always accepts block.

`link_to` accepts complex html as block, like below:

    <%= link_to user_path(@user) do %>
      <i class="icon-ok icon-white"></i> Do it@
    <% end %>
    # http://stackoverflow.com/questions/9401942/using-link-to-with-embedded-html

But `link_to_if` with block behavior is below:

    <%= link_to_if condition, user_path(@user) do %>
      Appear if condition falsy
    <% end %>

Then use `link_to_block_if` below:

    <%= link_to_block_if condition, user_path(@user) do %>
      <i class="icon-ok icon-white"></i> Do it@
    <% end %>
    
    #=> if condition truthy, then shows html and link, else if condition falsy, then show only html.

## Installation

Add this line to your application's Gemfile:

    gem 'actionview-link_to_block'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install actionview-link_to_block

## Usage

TODO: Write usage instructions here

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
