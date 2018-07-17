# WelcomeApp

Client for talking to WelcomeApp, currently it can only check if a user is registered.

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'welcome_app'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install welcome_app

## Usage

```ruby
# Configure
WelcomeApp.configure do |config|
  config.base_uri = 'https://welcomeapp.example.com'
  config.client_key = 'secretkey'
end

# Check if user exists in WelcomeApp's database
welcome = WelcomeApp::Client.new
welcome.user_exists?(email: 'jane.doe@example.com')
# => false
```

## Development

After checking out the repo, run `bin/setup` to install dependencies. Then, run `rake spec` to run the tests. You can also run `bin/console` for an interactive prompt that will allow you to experiment.

## Contributing

Bug reports and pull requests are welcome on GitHub at https://github.com/buren/welcome_app.


## License

The gem is available as open source under the terms of the [MIT License](http://opensource.org/licenses/MIT).
