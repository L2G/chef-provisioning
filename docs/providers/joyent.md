# Joyent provider (via Fog driver)

CHEF_DRIVER must be set to `"fog:Joyent:https://<region>.api.joyentcloud.com"`, where `<region>` is "us-sw-1", "us-east-1",
or any of Joyent's regions.

## compute_options
- `:joyent_keyfile`
- `:joyent_keyname`
- `:joyent_username`
- `:joyent_version` (optional) -- request a particular version of the Joyent API (note that this must be set to `~7.0`
  in order to use certain features, particularly the `:networks` bootstrap option described below)

## bootstrap_options

- `:image` **(required)** -- UUID of the Joyent image to use to create the new instance
- `:networks` (optional) -- array of UUIDs of Joyent networks to attach to the new instance
- `:package` **(required)** --
