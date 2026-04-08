# Meddbase API Documentation Site

View site here: <https://meddbase.github.io/meddbase-apis/>

## Intro
Welcome to the Meddbase API's documentation site.

Here you will find details of all of the publicly available API endpoints for the Meddbase application.

Issues can be raised here <https://github.com/meddbase/meddbase-apis/issues>. Issues can be used to ask questions around use cases as well as seek technical assistance on ways of using the API documentation.
When posting issues, please do not share client or patient specific information, or any PII.

## Local Development
If you wish to contribute to these docs or preview changes locally, follow these steps:

### Prerequisites
Ruby 3.3.x

Install bundler 
```Bash
gem install bundler -v 2.5.9 
```

### Setup & Preview

Install dependencies
```Bash
bundle install
```

Build and serve the site

```Bash
bundle exec jekyll serve
```

View the site: Open your browser to http://127.0.0.1:4000.