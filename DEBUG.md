# Debug

When installing the necessary gems with

`$ bundle install`

the following error will occur:

`Retrying fetcher due to error (2/4): Bundler::HTTPError Could not fetch specs from https://rubygems.org/ due to underlying error <Net::OpenTimeout: Failed to open TCP connection to rubygems.org:443 (execution expired) (https://rubygems.org/specs.4.8.gz)>`

Running this solved:
`gem update --system`
`gem install bundler`

There were lots of erros that needed installings to solve.