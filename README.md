# vue-typescript-vim-test

Exec `node_modules/.bin/tsserver` and input following for open src/app.vue.
```
{"seq":null,"arguments":{"file":"<full path of src/app.vue>"},"type":"request","command":"open"}
```

tsserver returns with no error.
```
{"seq":0,"type":"event","event":"configFileDiag","body":{"triggerFile":"<full path of src/app.vue>","configFile":"/home/ryo/devel/src/github.com/ryo7000/vue-typescript-vim-test/tsconfig.json","diagnostics":[]}}
```

But open src/app2.vue with following.
```
{"seq":null,"arguments":{"file":"<full path of src/app2.vue>"},"type":"request","command":"open"}
```
tsserver returns error TS1219.

```
{"seq":0,"type":"event","event":"semanticDiag","body":{"file":"<full path of src/app2.vue>","diagnostics":[{"start":{"line":11,"offset":22},"end":{"line":11,"offset":26},"text":"Experimental support for decorators is a feature that is subject to change in a future release. Set the 'experimentalDecorators' option to remove this warning.","code":1219,"category":"error"}]}}
```
