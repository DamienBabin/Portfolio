## Running the Documentation Site

### Using Docker (Recommended)

The documentation site can be built and served using Docker, which ensures consistency across different development environments.

1. **Prerequisites**
   - Docker
   - Docker Compose

2. **Start the Documentation Server**
   ```bash
   docker-compose up
   ```
   The site will be available at http://localhost:4000

3. **Rebuild the Container** (if dependencies change)
   ```bash
   docker-compose build
   ```

### Local Development (Alternative)

If you prefer to run without Docker, you'll need:
- Ruby 3.2+
- Bundler

1. **Install Dependencies**
   ```bash
   bundle install
   ```

2. **Start the Documentation Server**
   ```bash
   bundle exec jekyll serve
   ```
   The site will be available at http://localhost:4000