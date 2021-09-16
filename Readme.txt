Ao Iniciar qualquer projeto deve-se dar um nome e criar o arquivo package.json:
yarn -y init ou npm init -yarn

Exemplo:
PS F:\Ignite\Aulas\github-explorer> yarn -y init
yarn init v1.19.1
warning The yes flag has been set. This will automatically answer yes to all questions, which may have security implications.
success Saved package.json
Done in 0.08s.
1.19.1
PS F:\Ignite\Aulas\github-explorer> npm -v
6.14.15
PS F:\Ignite\Aulas\github-explorer> yarn -v
1.19.1
PS F:\Ignite\Aulas\github-explorer> yarn add react 
yarn add v1.19.1
info No lockfile found.
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Building fresh packages...
success Saved lockfile.
success Saved 4 new dependencies.
info Direct dependencies
└─ react@17.0.2
info All dependencies
├─ js-tokens@4.0.0
├─ loose-envify@1.4.0
├─ object-assign@4.1.1
└─ react@17.0.2
Done in 1.16s.

Agora vamos incluir as bibliotecas no projeto, para isto: yarn add react. 
Exemplo:
PS F:\Ignite\Aulas\github-explorer> yarn add react-dom
yarn add v1.19.1
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Building fresh packages...
success Saved lockfile.
success Saved 2 new dependencies.
info Direct dependencies
└─ react-dom@17.0.2
info All dependencies
├─ react-dom@17.0.2
└─ scheduler@0.20.2
Done in 1.32s.

Com isso foram criados os arquivos package.json e a pasta node_modules, como também um arquivoyarn.lock.
Agora incluímos o react-dom, que é a arvore com todos os elementos da aplicação.
yarn add react-dom

Exemplo:
PS F:\Ignite\Aulas\github-explorer> yarn add react-dom
yarn add v1.19.1
[1/4] Resolving packages...
[2/4] Fetching packages...
[3/4] Linking dependencies...
[4/4] Building fresh packages...
success Saved lockfile.
success Saved 2 new dependencies.
info Direct dependencies
└─ react-dom@17.0.2
info All dependencies
├─ react-dom@17.0.2
└─ scheduler@0.20.2
Done in 1.32s.

Agora vamos criar a estrutura de pastas com todo o cógigo criado na aplicação, como:
arquivos públicos, src. Dentro da pasta public ficará os arquivos públicos incluímos 
a página index.html, a favicon, os arquivos Robot.txt (indica para os buscadores).
Na pasta src ficará todo o código criado para a aplicação, principalmente o javascript.

Agora vamos configurar o Babel, possui a função de auxiliar para que todos os códigos possam
ser interpretado em toda a estrutura do projeto, assim converte o código para uma estrutura legivel
para todos os navegadores.
https://babeljs.io/
Utilizamos o comando: yarn add @babel/core @babel/cli @babel/preset-env -D , todos como dependencia de 
desenvolvimento (usamos -D) assim este recurso somente será utiliza na produção e não será utilizado 
quando estiver on-line.

Exemplo:
PS F:\Ignite\Aulas\github-explorer> yarn add @babel/core @babel/cli @babel/preset-env -D
yarn add v1.19.1
[1/4] Resolving packages...
warning @babel/cli > @nicolo-ribaudo/chokidar-2 > braces > snapdragon > source-map-resolve > resolve-url@0.2.1: https://github.com/lydell/resolve-url#deprecated
warning @babel/cli > @nicolo-ribaudo/chokidar-2 > braces > snapdragon > source-map-resolve > urix@0.1.0: Please see https://github.com/lydell/urix#deprecated
[2/4] Fetching packages...
info fsevents@2.3.2: The platform "win32" is incompatible with this module.
info "fsevents@2.3.2" is an optional dependency and failed compatibility check. Excluding it from installation.
[3/4] Linking dependencies...
[4/4] Building fresh packages...
success Saved lockfile.
success Saved 190 new dependencies.
info Direct dependencies
├─ @babel/cli@7.15.4
├─ @babel/core@7.15.5
└─ @babel/preset-env@7.15.6
info All dependencies
├─ @babel/cli@7.15.4
├─ @babel/compat-data@7.15.0
├─ @babel/core@7.15.5
├─ @babel/helper-builder-binary-assignment-operator-visitor@7.15.4
├─ @babel/helper-compilation-targets@7.15.4
├─ @babel/helper-explode-assignable-expression@7.15.4
├─ @babel/helper-get-function-arity@7.15.4
├─ @babel/helper-module-imports@7.15.4
├─ @babel/helper-plugin-utils@7.14.5
├─ @babel/helper-remap-async-to-generator@7.15.4
├─ @babel/helper-wrap-function@7.15.4
├─ @babel/helpers@7.15.4
├─ @babel/highlight@7.14.5
├─ @babel/plugin-bugfix-v8-spread-parameters-in-optional-chaining@7.15.4
├─ @babel/plugin-proposal-async-generator-functions@7.15.4
├─ @babel/plugin-proposal-class-properties@7.14.5
├─ @babel/plugin-proposal-class-static-block@7.15.4
├─ @babel/plugin-proposal-dynamic-import@7.14.5
├─ @babel/plugin-proposal-export-namespace-from@7.14.5
├─ @babel/plugin-proposal-json-strings@7.14.5
├─ @babel/plugin-proposal-logical-assignment-operators@7.14.5
├─ @babel/plugin-proposal-nullish-coalescing-operator@7.14.5
├─ @babel/plugin-proposal-numeric-separator@7.14.5
├─ @babel/plugin-proposal-object-rest-spread@7.15.6
├─ @babel/plugin-proposal-optional-catch-binding@7.14.5
├─ @babel/plugin-proposal-private-methods@7.14.5
├─ @babel/plugin-proposal-private-property-in-object@7.15.4
├─ @babel/plugin-proposal-unicode-property-regex@7.14.5
├─ @babel/plugin-syntax-class-properties@7.12.13
├─ @babel/plugin-syntax-top-level-await@7.14.5
├─ @babel/plugin-transform-arrow-functions@7.14.5
├─ @babel/plugin-transform-async-to-generator@7.14.5
├─ @babel/plugin-transform-block-scoped-functions@7.14.5
├─ @babel/plugin-transform-block-scoping@7.15.3
├─ @babel/plugin-transform-classes@7.15.4
├─ @babel/plugin-transform-computed-properties@7.14.5
├─ @babel/plugin-transform-destructuring@7.14.7
├─ @babel/plugin-transform-dotall-regex@7.14.5
├─ @babel/plugin-transform-duplicate-keys@7.14.5
├─ @babel/plugin-transform-exponentiation-operator@7.14.5
├─ @babel/plugin-transform-for-of@7.15.4
├─ @babel/plugin-transform-function-name@7.14.5
├─ @babel/plugin-transform-literals@7.14.5
├─ @babel/plugin-transform-member-expression-literals@7.14.5
├─ @babel/plugin-transform-modules-amd@7.14.5
├─ @babel/plugin-transform-modules-commonjs@7.15.4
├─ @babel/plugin-transform-modules-systemjs@7.15.4
├─ @babel/plugin-transform-modules-umd@7.14.5
├─ @babel/plugin-transform-named-capturing-groups-regex@7.14.9
├─ @babel/plugin-transform-new-target@7.14.5
├─ @babel/plugin-transform-object-super@7.14.5
├─ @babel/plugin-transform-property-literals@7.14.5
├─ @babel/plugin-transform-regenerator@7.14.5
├─ @babel/plugin-transform-reserved-words@7.14.5
├─ @babel/plugin-transform-shorthand-properties@7.14.5
├─ @babel/plugin-transform-spread@7.14.6
├─ @babel/plugin-transform-sticky-regex@7.14.5
├─ @babel/plugin-transform-template-literals@7.14.5
├─ @babel/plugin-transform-typeof-symbol@7.14.5
├─ @babel/plugin-transform-unicode-escapes@7.14.5
├─ @babel/plugin-transform-unicode-regex@7.14.5
├─ @babel/preset-env@7.15.6
├─ @babel/preset-modules@0.1.4
├─ @babel/runtime@7.15.4
├─ @nicolo-ribaudo/chokidar-2@2.1.8-no-fsevents.2
├─ ansi-styles@3.2.1
├─ anymatch@2.0.0
├─ arr-flatten@1.1.0
├─ assign-symbols@1.0.0
├─ async-each@1.0.3
├─ atob@2.1.2
├─ babel-plugin-polyfill-corejs2@0.2.2
├─ babel-plugin-polyfill-corejs3@0.2.4
├─ babel-plugin-polyfill-regenerator@0.2.2
├─ balanced-match@1.0.2
├─ base@0.11.2
├─ binary-extensions@1.13.1
├─ brace-expansion@1.1.11
├─ braces@2.3.2
├─ browserslist@4.17.0
├─ cache-base@1.0.1
├─ call-bind@1.0.2
├─ caniuse-lite@1.0.30001257
├─ chalk@2.4.2
├─ chokidar@3.5.2
├─ class-utils@0.3.6
├─ collection-visit@1.0.0
├─ color-convert@1.9.3
├─ color-name@1.1.3
├─ colorette@1.4.0
├─ commander@4.1.1
├─ concat-map@0.0.1
├─ convert-source-map@1.8.0
├─ copy-descriptor@0.1.1
├─ core-js-compat@3.17.3
├─ core-util-is@1.0.3
├─ debug@4.3.2
├─ decode-uri-component@0.2.0
├─ define-properties@1.1.3
├─ electron-to-chromium@1.3.840
├─ escalade@3.1.1
├─ escape-string-regexp@1.0.5
├─ esutils@2.0.3
├─ expand-brackets@2.1.4
├─ extglob@2.0.4
├─ fill-range@4.0.0
├─ for-in@1.0.2
├─ fs-readdir-recursive@1.1.0
├─ fs.realpath@1.0.0
├─ gensync@1.0.0-beta.2
├─ get-intrinsic@1.1.1
├─ glob-parent@5.1.2
├─ glob@7.1.7
├─ graceful-fs@4.2.8
├─ has-flag@3.0.0
├─ has-value@1.0.0
├─ inflight@1.0.6
├─ inherits@2.0.4
├─ is-accessor-descriptor@1.0.0
├─ is-binary-path@1.0.1
├─ is-core-module@2.6.0
├─ is-data-descriptor@1.0.0
├─ is-descriptor@1.0.2
├─ is-extglob@2.1.1
├─ is-glob@4.0.1
├─ is-plain-object@2.0.4
├─ is-windows@1.0.2
├─ isarray@1.0.0
├─ jsesc@2.5.2
├─ json5@2.2.0
├─ kind-of@3.2.2
├─ lodash.debounce@4.0.8
├─ make-dir@2.1.0
├─ map-visit@1.0.0
├─ micromatch@3.1.10
├─ minimatch@3.0.4
├─ minimist@1.2.5
├─ mixin-deep@1.3.2
├─ ms@2.1.2
├─ nanomatch@1.2.13
├─ node-releases@1.1.75
├─ object-copy@0.1.0
├─ object-keys@1.1.1
├─ object.assign@4.1.2
├─ pascalcase@0.1.1
├─ path-is-absolute@1.0.1
├─ path-parse@1.0.7
├─ picomatch@2.3.0
├─ pify@4.0.1
├─ posix-character-classes@0.1.1
├─ process-nextick-args@2.0.1
├─ readable-stream@2.3.7
├─ readdirp@2.2.1
├─ regenerate-unicode-properties@9.0.0
├─ regenerator-runtime@0.13.9
├─ regenerator-transform@0.14.5
├─ regexpu-core@4.8.0
├─ regjsgen@0.5.2
├─ regjsparser@0.7.0
├─ remove-trailing-separator@1.1.0
├─ repeat-element@1.1.4
├─ resolve-url@0.2.1
├─ resolve@1.20.0
├─ ret@0.1.15
├─ safe-buffer@5.1.2
├─ semver@6.3.0
├─ set-value@2.0.1
├─ slash@2.0.0
├─ snapdragon-node@2.1.1
├─ snapdragon-util@3.0.1
├─ source-map-resolve@0.5.3
├─ source-map-url@0.4.1
├─ source-map@0.5.7
├─ split-string@3.1.0
├─ static-extend@0.1.2
├─ string_decoder@1.1.1
├─ supports-color@5.5.0
├─ to-fast-properties@2.0.0
├─ to-object-path@0.3.0
├─ to-regex-range@2.1.1
├─ unicode-canonical-property-names-ecmascript@2.0.0
├─ unicode-match-property-ecmascript@2.0.0
├─ unicode-match-property-value-ecmascript@2.0.0
├─ unicode-property-aliases-ecmascript@2.0.0
├─ union-value@1.0.1
├─ unset-value@1.0.0
├─ upath@1.2.0
├─ urix@0.1.0
├─ use@3.1.1
└─ util-deprecate@1.0.2
Done in 29.84s.

Agora criamos o arquivo .gitignore, assim todas as pastas e arquivos dentro dele serão
ignorados quando fizermos o upload no github, assim não serão commitados no rastreamento.
Um arquivo .gitignore é um arquivo de texto plano no qual cada linha especifica um padrão
de arquivos ou diretórios a ignorar, geralmente se coloca no diretório raiz de um repositório,
mas é possível colocá-lo em outro lugar (mas não recomendado).
Exemplo: 
yarn.lock
yarn-error.log
*.txt - qualquer arquivo co extensão txt
*.log - todos os arquivos .log
*.lock - todos aos arquivos .lock
node_modules/* - vai ignorar a pasta completa 

Para clonar uma pasta utilizamos o comando (git clone e o endereço da pasta no github com .git),
para isto é importante que a pasta esteja vazia, como é em todo projeto. Exemplo:

PS F:\Aulas Ignite> git clone https://github.com/Aldo2019/Aulas-Ignite.git
Cloning into 'Aulas-Ignite'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), 625 bytes | 41.00 KiB/s, done.


Agora efetuamos um teste de conversão com o comando: yarn babel src/index.js --out-file dist/bundle.js
para isto usa-se a Cli (interface de linha de comado) do babel, a pasta de destino é a dist (distribuição)
para um arquivo bundle.js ( um tipo de arquivo padrão do babel).





