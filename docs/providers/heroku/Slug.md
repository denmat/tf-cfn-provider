# Terraform::Heroku::Slug

Provides a [Heroku Slug](https://devcenter.heroku.com/articles/platform-api-reference#slug)
resource.

This resource supports uploading a pre-generated archive file of executable code, making it possible to launch apps directly from a Terraform config. This resource does not itself generate the slug archive. [A guide to creating slug archives](https://devcenter.heroku.com/articles/platform-api-deploying-slugs) is available in the Heroku Dev Center.

## Properties

`App` - (Required) The ID of the Heroku app.

`BuildpackProvidedDescription` - Description of language or app framework, `"Ruby/Rack"`; displayed as the app's language in the Heroku Dashboard.

`Checksum` - Hash of the slug for verifying its integrity, auto-generated from contents of `FilePath` or `FileUrl`, `SHA256:e3b0c44298fc1c149afbf4c8996fb92427ae41e4649b934ca495991b7852b855`.

`Commit` - Identification of the code with your version control system (eg: SHA of the git HEAD), `"60883d9e8947a57e04dc9124f25df004866a2051"`.

`CommitDescription` - Description of the provided commit.

`FilePath` - (Required unless `FileUrl` is set) Local path to a slug archive, `"slugs/current.tgz"`.

`FileUrl` - (Required unless `FilePath` is set) **https** URL to a slug archive, `"https://example.com/slugs/app-v1.tgz"`.

`ProcessTypes` - (Required) Map of [processes to launch on Heroku Dynos](https://devcenter.heroku.com/articles/process-model).

`Stack` - Name or ID of the [Heroku stack](https://devcenter.heroku.com/articles/stack).


## Return Values

### Fn::GetAtt

`Id` - The ID of the slug.

`App` - The ID or unique name of the Heroku app.

`Blob` - Slug archive (compressed tar of executable code).

`Method` - HTTP method to upload the archive.

`Url` - Pre-signed, expiring URL to upload the archive.

`BuildpackProvidedDescription` - Description of language or app framework, `"Ruby/Rack"`.

`Checksum` - Hash of the slug for verifying its integrity, auto-generated from contents of `FilePath` or `FileUrl`.

`Commit` - Identification of the code with your version control system (eg: SHA of the git HEAD), `"60883d9e8947a57e04dc9124f25df004866a2051"`.

`CommitDescription` - Description of the provided commit.

`ProcessTypes` - Map of [processes to launch on Heroku Dynos](https://devcenter.heroku.com/articles/process-model).

`Size` - Slug archive filesize in bytes.

`Stack` - [Heroku stack](https://devcenter.heroku.com/articles/stack) name.

`StackId` - [Heroku stack](https://devcenter.heroku.com/articles/stack) ID.

## See Also

* [heroku_slug](https://www.terraform.io/docs/providers/heroku/r/slug.html) in the _Terraform Provider Documentation_