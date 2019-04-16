# {{title}}

Last updated: {{timestamp | date(format="%Y-%m-%d %H:%M")}}

{% for entry in entries %}
  {{loop.index}}. {{entry.title}} - [EPUB]({{entry.path | urlencode}}) ({{entry.epub_size | filesizeformat}}) | [Website]({{entry.url}}) | [Repository]({{entry.repo_url}})  
  Commit: {{entry.commit_sha}} ({{entry.last_modified | date(format="%Y-%m-%d %H:%M")}})
{% endfor %}
