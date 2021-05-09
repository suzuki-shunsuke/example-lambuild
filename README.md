# example-lambuild

Example of [lambuild](https://github.com/suzuki-shunsuke/lambuild)

This is a [template repository](https://docs.github.com/en/github/creating-cloning-and-archiving-repositories/creating-a-repository-from-a-template).
Please create your repository from this repository and try `lambuild`.

## Prepare

Plaese set up lambuild according to [Getting Started](https://github.com/suzuki-shunsuke/lambuild/blob/main/docs/getting-started.md).

## Try lambuild

In this repository, there are two Go application [foo](foo) and [bar](bar) and lambuild configuration file [lambuild.yaml](lambuild.yaml).
In `lambuild.yaml`, two builds are defined, `foo_test` and `bar_test`.
`foo_test` is run only when files under `foo` directory is updated in the associated pull request,
and `bar_test` is run only when files under `bar` directory is updated in the associated pull request.

Let's update [foo/main.go](foo/main.go) and create a pull request.

```go
	fmt.Println("foo !!!")
```

Then please confirm only `foo_test` is run.

Let's update [bar/main.go](bar/main.go) as well.

```go
	fmt.Println("bar !!!")
```

Then please confirm both `foo_test` and `bar_test` are run.

## LICENSE

[MIT](LICENSE)
