# FixturesDumper

Dump data from development or test database to create fixtures easily.

[![Circle CI](https://circleci.com/gh/bigbinary/fixtures_dumper.png?style=badge)](https://circleci.com/gh/bigbinary/fixtures_dumper)
[![Gem Version](https://badge.fury.io/rb/fixtures_dumper.svg)](http://badge.fury.io/rb/fixtures_dumper)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'fixtures_dumper'
```

And then execute:

```
bundle
```
## Supported Rails Versions

Rails 3.2.x and higher

## Usage

``` ruby
# Dump data in all the tables to fixtures
rake fd:fixtures:dump

# Dump data from table `users` to its fixture file
rake fd:fixtures:dump TABLE=users

# Dump data from test database to fixtures
rake fd:fixtures:dump RAILS_ENV=test
```

## Example

```
$ rake fd:fixtures:dump TABLE=users
$ cat users.yml
user_1:
  id: 1
  email: john@example.com
  encrypted_password: "$2a$10$5jvZFdi7rNvn.pEACqsRtulzLIBHjTp.Fq8V4mEIN9lLRkhdjugjK"
  reset_password_token:
  reset_password_sent_at:
  remember_created_at:
  sign_in_count: 0
  current_sign_in_at:
  last_sign_in_at:
  current_sign_in_ip:
  last_sign_in_ip:
  created_at: 2014-09-08 09:02:15.286126000 Z
  updated_at: 2014-09-08 09:02:15.286126000 Z
  last_name: Smith
  first_name: John
  role: super_admin
  authentication_token: VPsQJyicduFU2GKJbeLz
  profile_image:
```

## Contributing

1. Fork it ( https://github.com/bigbinary/fixtures_dumper/fork )
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

#### Brought to you by

![BigBinary](http://bigbinary.com/assets/common/logo.png)
