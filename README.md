# Urchin Tracking Module

Add google analytics params to your URLs.

## Installation

Add this line to your application's Gemfile:

    gem 'utm'

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install utm

## Usage

    require 'utm'

    UTM("http://example.com/#/welcome",
      utm_source: "newsletter_de",
      utm_medium: "email",
      utm_term:   "fashion+leather",
      utm_content: "Could be the subject line of your email",
      utm_campaign: "winter_2013" )
    => "http://example.com/?utm_source=newsletter_de&utm_medium=email&utm_term=fashion+leather&utm_content=Could+be+the+subject+line+of+your+email&utm_campaign=winter_2013#/welcome"

## Contributing

Your thought's/improvements are welcome :)

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## TODOs

  * remove dependency to Rails
  * remove bonusbox specific `src` param or make this kind of
  additions configurable.
  * `Utm.configure {|c| c[:utm_source] => nil }` would generate
  invalid params. It should pick up defaults instead.
  * `Utm.configure {|c| c[:utm_source] => 'my_app' }` could have a
  configuration object instead of a hash, to become
  `Utm.configure {|c| c.utm_source = 'my_app' }`

## Code status

* [![Build Status](https://api.travis-ci.org/bonusboxme/urchin_tracking_module.png)](https://travis-ci.org/bonusboxme/urchin_tracking_module)

## License

This `urchin_tracking_module` project is released under the [MIT License](http://www.opensource.org/licenses/MIT).