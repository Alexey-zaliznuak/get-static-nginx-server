
# Simple Static Server

A simple server for getting static, integrated with
[Yandex.Disk](https://disk.yandex.ru) by [WebDAV](http://www.webdav.org/specs/rfc4918.html)


## API Reference
All requests URI changes on

```http
  https://webdav.yandex.ru/$BASE_PATH/path/to/file
```

#### Get file
```http
  GET /path/to/file
```

#### PUT file
```http
  PUT /path/to/file
```

## Environment Variables

See .env [exmaple](.env.template)


You will need to add the following environment variables to your .env file

`YANDEX_DISK_AUTH_TOKEN` - OAuth token for [Yandex.Disk API](https://yandex.ru/dev/disk/)

[Guide to creating an API key](https://yandex.ru/dev/disk/doc/ru/concepts/quickstart#quickstart__oauth)

`SERVER_TOKEN` - Token for mutations methods(PUT, DELETE)

`BASE_PATH` - configurable base path for your files on Yandex.Disk. It is used as the root path for all files.


## Deployment

Pull repo:
```sh
git clone https://github.com/Portal-AI-Service/static-service
```

Add
[environment variables](#environment-variables)
and run:

```sh
  docker compose up
```


## Authors

- [@AlexeyZaliznuak](https://github.com/Alexey-zaliznuak)
