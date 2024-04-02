# How to run services with runit on NeoTerm

1. Install neoterm-services with `pkg install neoterm-services`
2. Restart your shell so that the service-daemon is started
3. Enable a service by running `sv-enable <service>`, or just start it with `sv up <service>`
4. Check the log content of `$PREFIX/var/log/sv/<service>/current` in case there are problems

You can also stop services with `sv down <service>`, or disable them with `sv-disable <service>`
A service is disabled if `$PREFIX/var/service/<service>/down` exists, so the `sv-enable` and `sv-disable` scripts touches, or removes, this file.
