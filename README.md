This gem is intended to be installed locally.

## Installation

```zsh
./rails_app $ mkdir -p ./gems
./rails_app $ cd ./gems
./rails_app/gems $ git clone https://github.com/amrani/common_testing.git
```

Bundle and remove git.

```zsh
./host_app/gems $ cd ./common_testing
./host_app/gems/common_testing $ rm -rf .git
./host_app/gems/common_testing $ bundle install
```

For adding it to a rails engine:

```ruby
# engines/my_engine/Gemfile

group :development, :test do
  gem "common_testing", path: "../../gems/common_testing"
end
```

```ruby
# engines/my_engine/my_engine.gemspec
spec.add_development_dependency "common_testing"
```
