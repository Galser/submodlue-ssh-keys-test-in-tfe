# submodlue-ssh-keys-test-in-tfe
Repository with submodule  to test fetching in TFE using SSH keys added specifically to workspace only

# Assumption

I'm trying to setup submodule checkout on my workspace. I followed https://www.terraform.io/docs/cloud/workspaces/ssh-keys.html to create a custom key and assign it to my workspace as well as added Deploy key to the related Github repository.

However I'm getting configuration error. While the very same repo is working great when used with VCS Provider connection with SSH key defined at top level.

Perhaps, SSH keys added at workspace level are ignored due to some bug in the current versions of TFE ( v202101-1 an v202012-1,2 )

During slug ingress we getting errors like : 

```
Load key "/tmp/587399498": invalid format

git@github.com: Permission denied (publickey).
```

