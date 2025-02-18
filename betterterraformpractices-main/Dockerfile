# Use Ruby 3.2 as base image
FROM ruby:3.2-slim

# Install essential Linux packages
RUN apt-get update && apt-get install -y \
    build-essential \
    git \
    && rm -rf /var/lib/apt/lists/*

# Set working directory
WORKDIR /site

# Copy Gemfile and Gemfile.lock
COPY Gemfile Gemfile.lock ./

# Install bundler and gems
RUN bundle install

# Copy the rest of the site
COPY . .

# Expose port 4000
EXPOSE 4000

# Command to serve the site
CMD ["bundle", "exec", "jekyll", "serve", "--host", "0.0.0.0"]