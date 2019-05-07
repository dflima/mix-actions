FROM elixir:1.6.6

LABEL "repository"="https://github.com/dflima/mix-actions"
LABEL "homepage"="https://github.com/dflima/mix-actions"
LABEL "maintainer"="Danilo Lima <danferreiralima@gmail.com>"

LABEL "com.github.actions.name"="Run `mix format`"
LABEL "com.github.actions.description"="An action for running `mix format`"
LABEL "com.github.actions.icon"="code"
LABEL "com.github.actions.color"="orange"

ARG MIX_HOME=/.mix
ENV MIX_HOME=$MIX_HOME

ARG MIX_ENV=dev
ENV MIX_ENV=$MIX_ENV

RUN mix local.rebar --force
RUN mix local.hex --force

COPY entrypoint.sh /entrypoint.sh

ENTRYPOINT ["/entrypoint.sh"]
