# Simplycop

Provides standard shared rubocop configuration for Simply Business applications. No more copying `.rubocop.yml`, no more out-of-sync configuration files. Yay!

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'simplycop', git: 'git@github.com:simplybusiness/simplycop.git'

```

Then install gems by executing:

    $ bundle install

Put following lines at the beginning of your `rubocop.yml` file:

```yaml
inherit_gem:
  simplycop: .rubocop.yml

AllCops:
  Exclude:
    - 'vendor/**/*'
```

## Usage

Run Rubocop as you would usually do, i.e.

    $ bundle exec rubocop

or from your continuous integration tool.

## Guidances

* If you are implementing this in a non-rails project, you probably don't want or need the rails cops. In case they cause problems, you can exclude them using:
```yaml
Rails:
  Enabled: false
```
* When adding rubocop and simplycop to a legacy project, you might want to initially disable some of the rules.
