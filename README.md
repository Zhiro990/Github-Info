<h1 align="center"> { Github-Info } </h1>

A simple project that can help you in using the GitHub API.

## Table of Contents
> * [Installing](#installing)
> * [Importing](#importing)
> * [Usage](#usage)
> * [GitHubInfo](#githubinfo)
>   * [Properties](#properties)
>     * [token](#token--string--null)
>   * [Methods](#methods)
>     * [getAuthenticatedUser()](#getauthenticateduser--promiseuser--null)
>     * [searchRepo()](#searchrepo--promiserepository)
>     * [getRepo()](#getrepo--promiserepository)
>     * [getRepoContents()](#getrepocontents--promisecontent)
>     * [getRepoContributors()](#getrepocontributors--promisecontributor)
>     * [getRepoBranches()](#getrepobranches--promisebranch)
>     * [getRepoTags()](#getrepotags--promisetag)
>     * [getRepoLanguages()](#getrepolanguages--promiselanguage)
>     * [searchUser()](#searchuser--promiseuser)
>     * [getUser()](#getuser--promiseuser)
>     * [getUserRepos()](#getuserrepos--promiserepository)
>     * [getUserStarredRepos()](#getuserstarredrepos--promiserepository)
>     * [getUserSocialAccounts()](#getusersocialaccounts--promisesocialaccount)
>     * [getRateLimit()](#getratelimit--promiseobject)
> * [Data Structures](#data-structures)
>   * [Repository](#repository)
>   * [Owner](#owner)
>   * [User](#user)
>   * [Contributor](#contributor)
>   * [Branch](#branch)
>   * [Tag](#tag)
>   * [Content](#content)
>   * [Language](#language)
>   * [SocialAccount](#socialaccount)
> * [Types](#types)
>   * [Owner/User/Contributor Types](#ownerusercontributor-types)
>   * [Visibility Types](#visibility-types)
>   * [Content Types](#content-types)

## Installing

```bash
npm install Zhiro990/Github-Info
```

## Importing

```js
const GitHubInfo = require("Github-Info");
```

## Usage

```js
let githubinfo = new GitHubInfo("YOUR_GITHUB_TOKEN");
```

## GitHubInfo

### Properties

#### token : [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null)
> Your GitHub personal access token.

### Methods

#### getAuthenticatedUser() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[User](#user) | [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null)\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |

#### searchRepo() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[Repository](#repository)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `name` | The repository name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |
| `max` | The maximum amount of data. (between 1-100) | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) | Yes | `30` |

#### getRepo() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[Repository](#repository)\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `owner` | The repository owner username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |
| `name` | The repository name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### getRepoContents() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[Content](#content)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `owner` | The repository owner username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |
| `name` | The repository name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### getRepoContributors() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[Contributor](#contributor)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `owner` | The repository owner username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |
| `name` | The repository name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### getRepoBranches() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[Branch](#branch)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `owner` | The repository owner username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |
| `name` | The repository name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### getRepoTags() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[Tag](#tag)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `owner` | The repository owner username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |
| `name` | The repository name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### getRepoLanguages() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[Language](#language)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `owner` | The repository owner username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |
| `name` | The repository name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### searchUser() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[User](#user)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `name` | The user username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |
| `max` | The maximum amount of data. (between 1-100) | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) | Yes | `30` |

#### getUser() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[User](#user)\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `name` | The user username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### getUserRepos() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[Repository](#repository)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `name` | The user username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### getUserStarredRepos() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[Repository](#repository)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `name` | The user username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### getUserSocialAccounts() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[SocialAccount](#socialaccount)\[\]\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |
| `name` | The user username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) | No | None |

#### getRateLimit() : [Promise](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)\<[object](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Object)\>

| Parameter | Description | Type | Optional | Default |
| :-: | :-: | :-: | :-: | :-: |

## Data Structures

### Repository

| Property | Description | Type |
| :-: | :-: | :-: |
| `name` | The repository name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `fullName` | The repository full name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `description` | The repository description. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `url` | The repository url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `owner` | The repository owner. | [Owner](#owner) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `private` | Is the repository private? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `visibility` | The repository [visibility](#visibility-types). | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `fork` | Is the repository forked from other repository? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `defaultBranch` | The repository default branch. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `language` | The repository language. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `createdAt` | The repository created time. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `updatedAt` | The repository updated time. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `pushedAt` | The repository pushed time. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `stargazers` | The repository stargazers count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `watchers` | The repository watchers count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `openIssues` | The repository open issues count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `forks` | The repository forks count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `networks` | The repository networks count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `subscribers` | The repository subscribers count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `topics` | The repository topics. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String)\[\] |
| `homepage` | The repository homepage url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `gitUrl` | The repository git url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `sshUrl` | The repository ssh url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `cloneUrl` | The repository clone url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `allowForking` | Can i fork the repository? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `isTemplate` | Is the repository a template repository? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `hasIssues` | Is the repository has issues? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `hasProjects` | Is the repository has projects? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `hasDownloads` | Is the repository has downloads? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `hasWiki` | Is the repository has wiki? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `hasPages` | Is the repository has pages? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `hasDiscussions` | Is the repository has discussions? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `archived` | Is the repository archived? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `disabled` | Is the repository disabled? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |
| `size` | The repository size. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) |
| `license` | The repository license name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |

### Owner

| Property | Description | Type |
| :-: | :-: | :-: |
| `username` | The repository owner username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `avatar` | The repository owner avatar url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `url` | The repository owner profile url.| [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `type` | The repository [owner type](#ownerusercontributor-types). | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `siteAdmin` | Is the repository owner a site admin? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |

### User

| Property | Description | Type |
| :-: | :-: | :-: |
| `username` | The user username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `name` | The user name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `avatar` | The user avatar url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `url` | The user profile url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `bio` | The user bio. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `publicRepos` | The user public repos count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `followers` | The user followers count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `following` | The user following count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `twitterUsername` | The user twitter username.| [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `company` | The user company. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `location` | The user location. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `createdAt` | The user account created time. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) | 
| `updatedAt` | The user account updated time. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `blog` | The user blog. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `email` | The user email. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `hireable` | Is the user hireable? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `type` | The [user type](#ownerusercontributor-types). | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `siteAdmin` | Is the user a site admin? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |

### Contributor

| Property | Description | Type |
| :-: | :-: | :-: |
| `username` | The contributor username. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `avatar` | The contributor avatar url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `url` | The contributor profile url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `contributions` | The contributor contributions count. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) |
| `type` | The [contributor type](#ownerusercontributor-types). | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `siteAdmin` | Is the contributor a site admin? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |

### Branch

| Property | Description | Type |
| :-: | :-: | :-: |
| `name` | The branch name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `commit` | The branch last commit sha. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `protected` | Is the branch protected? | [boolean](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Boolean) |

### Tag

| Property | Description | Type |
| :-: | :-: | :-: |
| `name` | The tag name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `commit` | The tag last commit sha. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |

### Content

| Property | Description | Type |
| :-: | :-: | :-: |
| `name` | The content name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `path` | The content path. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `url` | The content url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) \| [null](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/null) |
| `type` | The [content type](#content-types). | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `sha` | The content last commit sha. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `size` | The content size. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) |

### Language

| Property | Description | Type |
| :-: | :-: | :-: |
| `name` | The language name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `size` | The language size. | [number](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number) |

### SocialAccount

| Property | Description | Type |
| :-: | :-: | :-: |
| `provider` | The social media name. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |
| `url` | The social account url. | [string](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String) |

## Types

### Owner/User/Contributor Types

> * `User`
> * `Organization`

### Visibility Types

> * `public`
> * `private`

### Content Types

> * `file`
> * `dir`
