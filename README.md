# gh-repos
AngularJS 1 Directive for displaying GitHub repositories of an user

## Dependencies

This module requires `ngResource` to run.

## Usage

### Controller Setup

You will need to add the Dependency `ghRepositories` to the module containing your Controller

```javascript
angular.module("main", ['ghRepositories'])

.controller("MainController", function () {

});
```

### HTML

```html
<body ng-app="main">
	<div ng-controller="MainController">
		<github-repos user="error418"></github-repos>
	</div>
</body>
```

Change the value of the attribute `user` to the GitHub user name you want to display the repositories for.


### Functional Behavior

The directive will only display non-forked Repositories by default. You can modify `partials/repositories.html` to change that behaviour.

## Styling

The default template for displaying the repositories can be found in the file `partials/repositories.html`.

Following css classes are used:

### repo-list

Is the container class wrapping all repositories

### repo

Is the container class wrapping a repository

### repo-name

Is the repository name, a `span` wrapping a link to the repository

### repo-description

Is the repository description, also a `span` containing plain text.