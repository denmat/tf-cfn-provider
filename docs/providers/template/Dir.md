# Terraform::Template::Dir

Renders a directory containing templates into a separate directory of
corresponding rendered files.

`template_dir` is similar to [`template_file`](../d/file.html) but it walks
a given source directory and treats every file it encounters as a template,
rendering it to a corresponding file in the destination directory.

~> **Note** When working with local files, Terraform will detect the resource
as having been deleted each time a configuration is applied on a new machine
where the destination dir is not present and will generate a diff to create
it. This may cause "noise" in diffs in environments where configurations are
routinely applied by many different users or within automation systems.

## Return Values

### Fn::GetAtt

Fn::GetAtt returns a value for a specified attribute of this type. The following are the available attributes and sample return values.

## See Also

* [template_dir](https://www.terraform.io/docs/providers/template/r/dir.html) in the _Terraform Provider Documentation_