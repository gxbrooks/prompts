
1. Configuration files for loading Elasticsearch objects, such as templates, dataviews, watchers,lifecycle managmenet, etc. must use the naming convention: <br>
    >&lt;common-name>.&lt;object-type&gt;.json

    Where: <br>
    1. &lt;common-name&gt; is the common name of a set of interrelated objects (e.g. templates and dataview)
    2. &lt;object-type&gt; is the name of the type of Elasticsearch (or Kibana) object to be created
    3. A '.' is used to seperate the &lt;common-name&gt; from the &lt;object-type&gt;
1. 
