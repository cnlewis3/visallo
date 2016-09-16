# Visallo Quick Start

After reviewing the required [devleopment dependencies](dependencies.md)
there are just three steps to get Visallo running locally:

1. Clone the open source repository from GitHub:
```bash
        git clone https://github.com/v5analytics/visallo.git
```

1. Change into the new directory:
```bash
        cd visallo
```

1. Run the web application with embedded H2 and Elasticsearch datastores:
```bash
        mvn -am -pl dev/jetty-server -P dev-jetty-run compile
```

Browse to [https://localhost:8889](https://localhost:8889) and log in
with any username (the `web-auth-username-only` authentication plugin
is configured by default).

See how to use the Visallo user interface with documentation hosted
withing the web application by clicking on `? Help` in the lower
left corner of the Visallo web page.