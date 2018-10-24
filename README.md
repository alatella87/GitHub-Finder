# Github-Finder

This is a foundation project that helped me build up my skills in Vanilla JavaScript.

## Getting Started

Download the directory and open the index.html file to start the application.

### Elements Learned

* DOM Manipulation & Events
* Keyboard & Input Events
* ES6 Features
* Constructors
* Asynchronous Programming
* async await
* External API Authentication
* Fetch API
* Arrow functions
* Template literal/strings


```
    async getUser(user) {

        // Profile (api.github.com/users/wlixw, i.e.) and
        // Repo (api.github.users/wlixw/repos)

        const profileResponse = await fetch(`https://api.github.com/users/${user}?client_id=${this.client_id}&client_secret=${this.client_secret}`);

        const repoResponse = await fetch(`https://api.github.com/users/${user}/repos?per_page=${this.repos_count}&sort=${this.repos_sort}&client_id=${this.client_id}&client_secret=${this.client_secret}`);

        const profile = await profileResponse.json();
        const repos = await repoResponse.json();

        // We are returning an object (here is why using asynchronous operations)
        return {

            profile,
            repos
        }
    }
```
