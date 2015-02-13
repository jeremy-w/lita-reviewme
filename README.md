# lita-reviewme

A [lita](https://www.lita.io/) handler that helps with [code review](http://en.wikipedia.org/wiki/Code_review)
without getting in the way.

The handler rotates, in order, through a list of names to provider a "reviewer"
for some unit of work.

## Installation

Add lita-reviewme to your Lita instance's Gemfile:

``` ruby
gem "lita-reviewme", github: "iamvery/lita-reviewme"
```

## Configuration

Environment variable needed for Github integration:

```
ENV["GITHUB_BOT_ACCESS_TOKEN"]
```

## Usage

### See who is in the review rotation.

> **Jay H.** Lita: reviewers
>
> **Lita** @iamvery, @zacstewart, ...

### Add a name to the review rotation

> **Jay H.** Lita: add @kyfast to reviews
>
> **Lita** added @kyfast to reviews

### Remove a name from the review rotation

> **Jay H.** Lita: remove @kyfast from reviews
>
> **Lita** removed @kyfast from reviews

### Fetch the next reviewer

> **Jay H.** Lita: review me
>
> **Lita** @iamvery

### Comment on a Github pull request or issue
This will post a comment mentioning the next reviewer on the referenced Github
pull request or issue. In order for this to work, @wolfbrain must have access
to the repository.

> **Jay H.** Lita: review https://github.com/iamvery/lita-reviewme/issues/7
>
> **Lita** @iamvery should be on it...

## License

[MIT](http://opensource.org/licenses/MIT)
