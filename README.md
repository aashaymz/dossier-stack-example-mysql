An example that uses Dossier Stack with a MySQL backend.

This setup uses
[`docker-compose`](https://docs.docker.com/compose/)
to manage the interaction between the `mysql` and `dossier-stack` containers.
`docker-compose` can be installed with `pip install docker-compose`.

To bring the `mysql` and `dossier-stack` containers up, just clone this repo
and run `docker-compose up -d`:

```bash
git clone git://github.com/dossier/dossier-stack-example-mysql
cd dossier-stack-example-mysql
docker-compose up -d
docker-compose logs -f dossier
```

Once the container is running,
[install the SortingDesk browser extension](https://chrome.google.com/webstore/detail/sorting-desk/ikcaehokdafneaiojndpmfbimilmlnid?hl=en-US).
Go to the extension's "Options" and select the "local" Active URL (which should
be `http://localhost:8080`). By default, the containers are configured to
server on `8080`, but this can be changed by editing the `command` and `ports`
directives in `docker-compose.yml`.
