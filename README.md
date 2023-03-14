# AutoSync Branches
 Keeps a secondary branch perfectly in sync with your main branch. 
 
 I use this to have branch-deploys in CI/CD with different environmental variables.
 
 In my use case, I needed to have an endpoint running production code, but connected to a test database for external users of an API to test their own code against my production code, without affecting their real data.

# Use
Set the following variables in your .env / GitHub actions variables tab:
```sh
AUTOSYNC_FROM=main # The branch you want to use as the source of replication
AUTOSYNC_TO=target_branch # The branch you want to mirror the source branch
```

Then, upload this to your `.github/workflows` folder and let er rip !