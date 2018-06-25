---
title: Ufo Current
---

## service

There's a handy way to shorten ufo commands by setting the current service.  Example:

    ufo current --service hi-web
    ufo ship hi-web # typical usage
    ufo ship # does the same thing as ufo ship hi-web

To view the current settings run `ufo current` with no options.

    $ ufo current
    Current env_extra: 1
    Current service: hi-web

The current service helps shorten other commands also.

    ufo cancel
    ufo deploy
    ufo destroy
    ufo ps
    ufo releases
    ufo resources
    ufo rollback VERSION
    ufo scale COUNT
    ufo ship

## UFO_ENV_EXTRA

The UFO_ENV_EXTRA env variable allows you create multiple same services.  More info about is is detailed at [ufo-env-extra]({% link _docs/ufo-env-extra.md %}).  You can also set a current UFO_ENV_EXTRA with the `--env-extra` option.

    ufo current --env-extra 1

## services

The `ufo ships` commands builds one Docker image and deploys them to multiple ECS services, so it usually takes a list of services like so:

    ufo ships hi-web hi-worker hi-clock

This can be shorten with with current also.

    ufo current --services hi-web hi-worker hi-clock
    ufo ships

<a id="prev" class="btn btn-basic" href="{% link _docs/params.md %}">Back</a>
<a id="next" class="btn btn-primary" href="{% link _docs/variables.md %}">Next Step</a>
<p class="keyboard-tip">Pro tip: Use the <- and -> arrow keys to move back and forward.</p>