dokku-ikachan-plugin
====================

A plugin to notify build/deploy via ikachan

## Install

```bash
git clone https://github.com/udzura/dokku-ikachan-plugin.git ikachan
```

You should edit setting `$DOKKU_ROOT/dokkurc` (This may be `/home/dokku/dokkurc` by default) first.

```bash
export IKACHAN_HOST=http://dokku001.example.com:8080
export IKACHAN_CHANNEL='#ikachan'
```

## Usage

Just deploy your app. And then, ikachan will notify to your IRC channel.

```chat
ikachan: ✈︎ Image build for minne-chan started on dokku001.example.com
ikachan: ✈︎ Image build for minne-chan finished on dokku001.example.com
...
```

Hooks are `pre-build,post-build,pre-deploy,post-deploy`.

You cat edit active hooks by setting `$IKACHAN_HOOK_ENABLED`

```bash
export IKACHAN_HOOK_ENABLED="pre-build,post-deploy"
```
