1. Overview of this guide
2. Github and directory structure
    - Repository types
    - Branch structure
    - HTML directory structure
    - Other project structures (grunt, jekyll?)
    - Issue management
    - Licenses and readme
3. Development environment
    - Dependencies
    - Install project dependencies
4. Grunt overview
    - What is grunt
    - Deploying grunt on web app projects
5. Javascript standards
6. HTML standards
7. CSS standards
8. Webmap standards
    - Map engine APIs
    - Level of design
    - 



Now that we are strapped with an awesome toolset it is high time we established a defined and meaningful process. Github is a powerful tool for development but in order to take full advantage of it's capabilities we need some ground rules. Here are some that I propose. Edit these if you have suggestions.

*** 

### Development environment
All developers should have the following dependencies installed on their workstation in order to adequately participate in the development of products.

- Ruby
- Rails
- Node.js

Additional dependencies will be loaded from `gemfile` and `package.json` references in corresponding products.

***

### Branch structure
The primary active version of a project should exist in the `master` directory and should include a readme and license file defining the information about the project.

For web projects the `gh-pages` directory can be used for nightly build updates. However, testing of changes and revisions __should be done locally not__ in `gh-pages`.

#### Branch names
When developing new features or addressing existing issues, a new branch should be created. This branch should be named `test/[your-name]` or `test/[your-name]-[issue-identifier]`. 

_Branches should be deleted when changes are merged to their parent by the project manager._

If the project is moving to a new version, a branch should be created from the existing `master` and named `archive/version-[version #]`. **Only the project manager should create a new version in order to prevent issue and build conflicts.**

#### Project directory structure
Directory structure should be standard across all final web products. The following is a standard web structure:

```text
--html
    |--lib/
    |   |--images/
    |   |--assets/
    |   |   |--[local vendor files js or css]
    |   |--style.min.css (project css minified)
    |   |--build.min.js (project js minified)
    |   |--tools/
    |       |--[other dynamicall loaded js and css]
    |--data/
    |   |--[json, csv, or other data]
    |--license.md
    |--readme.md
    |--index.htm
```

***

### Issue management
Issues can be submitted by project members and for public repos, anyone who is interested in sharing issues. DVRPC repos should have several standard tags to help manage workflow on project issues:

#### Issue type (select all that apply)

- `js`
- `css`
- `bug`
- `enhancement`

#### Status (only one at a time)

- `in progress`
- `testing` 
- `help wanted`

When an issue is registered, project members should assign the appropriate **issue type**. When a project member is working on an issue they should assign the issue to themselves and tag as `in progress`.

If an issue can be addressed by an individual or if the project manager requires help, a staff member can be assigned to the issue and the issue should be tagged with `help wanted`. 

When an issue is addressed by any commit, the commit message should provide some description of what was completed as well as a reference to the issue.

- Fixing an issue: `fixed #12`
- Others?

***

### Licenses and Readme
All projects should include a `license.md` and `readme.md`.

Specs about each file and what should be provided?

***

### Javascript Standards
In order to provide better legibility of products, all projects should adhere to these javascript standards. **As all projects will be linted and compiled before launch, comments should be used liberally when necessary**.
