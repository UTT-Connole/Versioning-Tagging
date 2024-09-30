# Versioning and Tagging

## Assignment

For this assignment, you will make changes to this repo and tag them with correct semantic version tags.

You are starting in a repo that has a 1.0.0 tag to start, and you'll be making changes to the `calculate` function in the `calculate.py` file. After each change, commit your changes and use `git tag` to record the changes that you made.

For more information on semantic versioning, see [Semantic Versioning](https://semver.org/).


### PATCH

Update the calculate endpoint to handle the divide by 0 error. After you commit the changes, make a new 1.0.1 git tag. 

### MINOR

Add a new non-breaking change to your calculate function and tag the commit with a new 1.1.0 git tag. Here are some ideas for non-breaking changes:

- **Add Logging**: Implement logging to track the inputs and outputs of the `calculate` function.
- **Input Validation**: Add validation to ensure that inputs are of the correct type and within an acceptable range.
- **Performance Improvement**: Optimize the `calculate` function to improve its performance without changing its external behavior.
- **New Operation**: Add a new operation to the endpoint.

After implementing one of these changes, commit your changes and create a new 1.1.0 git tag.

### MAJOR
Update the `calculate` function to change its signature or behavior in a way that is not backward compatible. For example, you could change the function's parameters or modify its return type. After making this breaking change, commit your changes and create a new 2.0.0 git tag.

Examples of breaking changes:

- **Change Function Signature**: Modify the parameters of the `calculate` function, such as changing their types or adding/removing parameters.
- **Alter Return Type**: Change the return type of the `calculate` function.
- **Remove Functionality**: Remove an existing operation from the `calculate` function.

After implementing one of these changes, commit your changes and create a new 2.0.0 git tag.


### Additional Changes

Continue making these changes until you have a 3.2.0 version of the calculate function.



## Submitting

Submit your changes by pushing your code **AND THE TAGS** to github and sharing a URL to them via the assignment in canvas.

You will need to use the following to push the tags:

```sh
git push --tags
```

### How to Use Git Tag

Git tags are used to mark specific points in a repository’s history. Typically, they are used to mark release points (e.g., 1.0.0).

#### Creating a Tag

To create a new tag, use the following command:

```sh
git tag <tagname>
```

For example, to create a tag named `1.0.0`:

```sh
git tag 1.0.0
```

#### Listing Tags

To list all tags in your repository, use:

```sh
git tag
```

#### Pushing Tags to Remote

By default, tags are not pushed to remote repositories. To push a specific tag, use:

```sh
git push origin <tagname>
```

To push all tags, use:

```sh
git push --tags
```

#### Deleting a Tag

To delete a tag locally, use:

```sh
git tag -d <tagname>
```

To delete a tag from the remote repository, use:

```sh
git push origin --delete <tagname>
```

#### Annotated Tags

Annotated tags store extra metadata such as the tagger name, email, and date. To create an annotated tag, use:

```sh
git tag -a <tagname> -m "Tag message"
```

For example:

```sh
git tag -a 1.0.0 -m "Initial release"
```

#### Viewing Tag Details

To view details of an annotated tag, use:

```sh
git show <tagname>
```

For example:

```sh
git show 1.0.0
```

This will display the tag message, the tagger information, and the commit the tag points to.