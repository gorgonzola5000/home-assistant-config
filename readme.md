# My Home Assistant Configuration

## YAML configs
All of the .yaml configs are split into their respective .yaml files and are kept in directory `/config/yaml-configs`. `configuration.yaml` then uses `!include` to read them. All of this is benefitial because you don't have to work with a one huge file now. Neat.

The only thing that this breaks, unfortunately, is editing automations using the GUI. Home Assistant can only edit automations that are kept in `/config/automations.yaml`. This can be easily fixed by creating a symlink: `ln -s ~/config/automations.yaml ~/config/yaml-configs/automations.yaml`. Now you can have your yaml configs in a separate directory and still edit automations using the GUI.
Same goes with scripts: `ln -s ~/config/scripts.yaml ~/config/yaml-configs/scripts.yaml`.

### Future reference
To push changes to GitHub: `git push`, username: <github_username>, password: <regenerated_fine_grained_token> (https://github.com/settings/tokens?type=beta)