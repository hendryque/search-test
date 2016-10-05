Steps to reproduce:

1. Start up a new Jekyll site: `jekyll new search-test`
2. Add plugin to the `Gemfile`:

  ```
  group :jekyll_plugins do
    gem "jekyll_pages_api_search"
  end
  ```

3. Run `bundle install`
4. Add configuration to `_config.yml`:

  ```
  jekyll_pages_api_search:
    index_fields:
      title:
        boost: 10
  ```

5. Run `bundle exec jekyll build`

Result:

```
Configuration file: /home/jf/search-test/_config.yml
            Source: /home/jf/search-test
       Destination: /home/jf/search-test/_site
 Incremental build: disabled. Enable with --incremental
      Generating...
jekyll_pages_api_search: checking for Node.js: v6.7.0
  Liquid Exception: undefined method `start_with?' for nil:NilClass in index.html
jekyll 3.2.1 | Error:  undefined method `start_with?' for nil:NilClass
```
