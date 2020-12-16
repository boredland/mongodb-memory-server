## [7.0.0-beta.12](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.11...v7.0.0-beta.12) (2020-12-16)


### ⚠ BREAKING CHANGES

* **MongoInstance:** remove function "MongoInstance.getPid", replace with "MongoInstance.childProcess?.pid"

### Features

* **MongoInstance:** remove function "getPid" ([f40da9a](https://github.com/nodkz/mongodb-memory-server/commit/f40da9ac167ba0da65459687c5cfcc990d07a9b0))


### Fixes

* **MongoMemoryReplSet:** remove unnecessary default to empty array ([2035845](https://github.com/nodkz/mongodb-memory-server/commit/203584526ff4b76f7998dfa12a182b50a206bf28))


### Style

* **MongoMemoryReplSet:** remove commented-out case ([8e3ae46](https://github.com/nodkz/mongodb-memory-server/commit/8e3ae46b8f13aaea1ac0e1eac0c1c6f25e484e38))
* **MongoMemoryReplSet:** remove TODO ([5645a87](https://github.com/nodkz/mongodb-memory-server/commit/5645a8750d0da6cb31425820616d43e234eb4c37)), closes [#392](https://github.com/nodkz/mongodb-memory-server/issues/392)


### Refactor

* **MongoBinary:** getSystemPath: return "undefined" instead of empty string ([10039f9](https://github.com/nodkz/mongodb-memory-server/commit/10039f99ceea0321ddfa8a42e5039059cfeba6c4))
* **MongoBinary:** remove unused interface "MongoBinaryCache" ([025df2e](https://github.com/nodkz/mongodb-memory-server/commit/025df2ea32b0b4233c6d2be57646570311c21139))

## [7.0.0-beta.11](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.10...v7.0.0-beta.11) (2020-11-11)


### Features

* remove cross-spawn ([c67ee8f](https://github.com/nodkz/mongodb-memory-server/commit/c67ee8f9330ade069dd00f9d49dd0f132f908048))


### Style

* **MongoInstance:** _launchKiller: remove commented-out code ([132917f](https://github.com/nodkz/mongodb-memory-server/commit/132917fac63745b351dfd73eb30f7f54962ddf37))

## [7.0.0-beta.10](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.9...v7.0.0-beta.10) (2020-11-06)


### ⚠ BREAKING CHANGES

* **MongoBinary:** remove function "MongoBinary.getCachePath", replace with "MongoBinary.cache.get"
* **MongoBinaryDownload:** remove "MongoBinaryDownload.locationExists", replace with "utils.pathExists"
* **MongoBinary:** remove value "LATEST_VERSION" in favor of using resolveConfig Value "VERSION"
* **resolveConfig:** removing alias "reInitializePackageJson", replace with "findPackageJson"

### Features

* **MongoBinary:** remove function "getCachePath" ([af164c1](https://github.com/nodkz/mongodb-memory-server/commit/af164c19007699ec79a9077d9ac7409e79c6f651))
* **MongoBinary:** remove value "LATEST_VERSION" ([22c6dfd](https://github.com/nodkz/mongodb-memory-server/commit/22c6dfd1a710cda5cf465c590f4947c916de46c0))
* **MongoBinaryDownload:** remove function "locationExists" ([0ba071a](https://github.com/nodkz/mongodb-memory-server/commit/0ba071abfac93d4abe016ad0ed7c9e3a5235a28f))
* **MongoBinaryDownload:** startDownload: add check that the downloadDir has sufficient permissions ([310cdae](https://github.com/nodkz/mongodb-memory-server/commit/310cdae9299b505b32cd9f2d633ab72119480022))
* **MongoInstance:** run: add check that the mongoBinary has sufficient permissions ([d9c1019](https://github.com/nodkz/mongodb-memory-server/commit/d9c101937bd3ad1af99ec32c0a3375246df3cafc))
* **resolveConfig:** add enum for all resolveConfig Variables ([7bd9160](https://github.com/nodkz/mongodb-memory-server/commit/7bd91609393f8151529b6827ef8c2f1a5be2fadb))
* **resolveConfig:** remove alias "reInitializePackageJson" ([acc4b0a](https://github.com/nodkz/mongodb-memory-server/commit/acc4b0a41f70cee240a4c062140cd14e694414ab))
* **utils:** add function "pathExists" ([4114d27](https://github.com/nodkz/mongodb-memory-server/commit/4114d27d73a6b34a7b59edc1b86d22723061ec89))


### Refactor

* **getos:** replace "promisify" with "fs.promises" ([60e184b](https://github.com/nodkz/mongodb-memory-server/commit/60e184bb294031e151a40cf668ebff2fd09734ed))
* **MongoBinary:** replace "promisify" with "fs.promises" ([5a769f3](https://github.com/nodkz/mongodb-memory-server/commit/5a769f3fbd32b1be3e6b1413d07362047838f995))
* **MongoBinaryDownload:** replace "existsSync" with "utils.pathExists" ([d8de1cc](https://github.com/nodkz/mongodb-memory-server/commit/d8de1cc8d0601f48146d7ae34a00af058a87e5db))
* **MongoBinaryDownload:** replace "promisify" with "fs.promises" ([911a922](https://github.com/nodkz/mongodb-memory-server/commit/911a922c92e8cf177604f33813adfb6fb98c694c))
* **resolveConfig:** remove unnecessary optional chain ([1c6578d](https://github.com/nodkz/mongodb-memory-server/commit/1c6578d22a311c686ba49eec2ad8afb856eca4a4))
* **utils:** assertion: remove error code from default error ([bbad7c4](https://github.com/nodkz/mongodb-memory-server/commit/bbad7c4d7036aa608262b7ee2fd41d1dedd4e6dc))


### Fixes

* **getos:** replace "not undefined" with "envToBool" ([7fde8be](https://github.com/nodkz/mongodb-memory-server/commit/7fde8beec831edf5d5f6cb2c03646ab182a7ccbe))
* **MongoBinary:** getSystemPath: also check for execute permission ([a501842](https://github.com/nodkz/mongodb-memory-server/commit/a501842e6c64575542cf976628f66a775a3c7d39))


### Style

* **README:** environment variables: add legend for booleans ([17b1937](https://github.com/nodkz/mongodb-memory-server/commit/17b193714870427878058da2ee353808179545c0))
* rename import "promises" (from fs) to "fspromises" everywhere ([f876670](https://github.com/nodkz/mongodb-memory-server/commit/f876670aaecc3b74ca4a85a80d804c137a40d572))
* **eslintrc:** add environment "node" ([8f3ed19](https://github.com/nodkz/mongodb-memory-server/commit/8f3ed194f0a2a19c551be076c99ff2af763fe9f5))
* **eslintrc:** add rule "padding-line-between-statements" for "function" & "class" ([6a0ebd4](https://github.com/nodkz/mongodb-memory-server/commit/6a0ebd43d63785c3457487d2d9834950adf08b30))
* **eslintrc:** add rule "padding-line-between-statements" for "if" ([3efdb47](https://github.com/nodkz/mongodb-memory-server/commit/3efdb4770b27b996ad75f6b645d99369ebb672f4))
* **eslintrc:** add rule "padding-line-between-statements" for "import" ([3bfc4ef](https://github.com/nodkz/mongodb-memory-server/commit/3bfc4ef8783557b2e451093f95be8b03c5d1696a))
* **eslintrc:** add rule "padding-line-between-statements" for "return" ([05b02d2](https://github.com/nodkz/mongodb-memory-server/commit/05b02d231eb70d77e87005943632539a7ddeec49))
* **eslintrc:** comma-dangle: change "functions" to "never" ([0bf9c3e](https://github.com/nodkz/mongodb-memory-server/commit/0bf9c3e5935ef493877110607ca2e4904942df9e))
* **eslintrc:** set rule "no-else-return" to "warn" ([cb242e9](https://github.com/nodkz/mongodb-memory-server/commit/cb242e97e738652aba493e80850dfd39059c2dd8))
* **eslintrc:** set rule "no-unused-expressions" to warn ([d08b293](https://github.com/nodkz/mongodb-memory-server/commit/d08b293f9be929fe159951427a72c030c0e776c1))
* **MongoBinaryDownload:** makeMD5check: add more tsdoc ([911a09a](https://github.com/nodkz/mongodb-memory-server/commit/911a09a141143bf4fa6190b3b52dc47594ac2af3))
* **README:** fix missing "MONGOMS_" on "SKIP_OS_RELEASE" ([e352495](https://github.com/nodkz/mongodb-memory-server/commit/e35249523a275fe7b83a31420aa3c0210349cb60))
* **utils:** add more tsdoc to "statPath" & "pathExists" ([3b36143](https://github.com/nodkz/mongodb-memory-server/commit/3b36143c243497118d4f4fc757bf42305bd36b79))

## [7.0.0-beta.9](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.8...v7.0.0-beta.9) (2020-11-02)


### Dependencies

* upgrade subdependencies (yarn upgrade) ([b7030ae](https://github.com/nodkz/mongodb-memory-server/commit/b7030ae4bdabb7ce64a816c8afe95b0807a44dbe))
* **eslint-config-prettier:** upgrade to 6.15.0 ([7bbcc33](https://github.com/nodkz/mongodb-memory-server/commit/7bbcc3355f441549f98f7560a308f78e9ba603de))
* **lint-staged:** upgrade to 10.5.1 ([6339aaa](https://github.com/nodkz/mongodb-memory-server/commit/6339aaa375a37a3c70830f69acd361e625a17859))
* **semantic-release:** upgrade to 17.2.2 ([1cb1fec](https://github.com/nodkz/mongodb-memory-server/commit/1cb1fecb0a8c3a37e4287df53d2b1db6bd67c565))
* allow "^" range for all type packages ([37c01d8](https://github.com/nodkz/mongodb-memory-server/commit/37c01d8bf7d0bf7668e56bdfe4f8e9d46e308d8d))
* pin all non-types devDependencies ([b647153](https://github.com/nodkz/mongodb-memory-server/commit/b647153a1a05295b55eddc5576ab9c52ba92ad0e))
* remove devDependency "mongodb" ([dbd82a7](https://github.com/nodkz/mongodb-memory-server/commit/dbd82a7d4b7ca831c4c4e4292b2a239e54b112da))

## [7.0.0-beta.8](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.7...v7.0.0-beta.8) (2020-11-01)


### Features

* **MongoBinaryDownloadUrl:** allow overwrite of archiveName ([c19d216](https://github.com/nodkz/mongodb-memory-server/commit/c19d2167a88977a67c886f651bf0a70dcf51a806)), closes [#295](https://github.com/nodkz/mongodb-memory-server/issues/295)


### Style

* **README:** update "packages/*/README.md" to new bages ([3acd086](https://github.com/nodkz/mongodb-memory-server/commit/3acd0866831ddff5f1c3deb5e96a7cc97be56ace))


### Fixes

* **MongoBinaryDownloadUrl:** add case for Linux Mint 20 ([01a6bc6](https://github.com/nodkz/mongodb-memory-server/commit/01a6bc63f0e13a4528ee39ccae64390a8de48582))
* **MongoBinaryDownloadUrl:** detect "linuxmint" and "linux mint" as linux mint ([fda4f72](https://github.com/nodkz/mongodb-memory-server/commit/fda4f7224d156680ac68c743c5a5a963070171dd)), closes [#403](https://github.com/nodkz/mongodb-memory-server/issues/403)
* **MongoBinaryDownloadUrl:** fix win32 download generation ([d62b489](https://github.com/nodkz/mongodb-memory-server/commit/d62b4891a01fe40b5f00c21ee02f08b24a55d80c)), closes [#399](https://github.com/nodkz/mongodb-memory-server/issues/399)
* **MongoBinaryDownloadUrl:** getArchiveName: throw error if platform is unknown ([9fc358b](https://github.com/nodkz/mongodb-memory-server/commit/9fc358b9b2997333b2121eabff16e91e543f3897))
* **MongoInstance:** handle code "12" on windows ([718aed7](https://github.com/nodkz/mongodb-memory-server/commit/718aed7281c25c7198ea068a87b06924d77de8ba)), closes [#411](https://github.com/nodkz/mongodb-memory-server/issues/411)


### Refactor

* **MongoBinaryDownloadUrl:** minify "getUbuntuVersionString" ([04b0ee9](https://github.com/nodkz/mongodb-memory-server/commit/04b0ee9c5685107a1db67a6edc19bb3b2762bbc4))
* **MongoBinaryDownloadUrl:** remove "async" where not needed ([7970fbb](https://github.com/nodkz/mongodb-memory-server/commit/7970fbbaa8a32979a9634765f726419a00bd385c))
* **MongoBinaryDownloadUrl:** translatePlatform: change default error ([61685e0](https://github.com/nodkz/mongodb-memory-server/commit/61685e04c14a45c410a8c258be58f2ed7962820a))
* **MongoMemoryReplSet:** rename "MongoMemoryReplSetEventEnum" to "MongoMemoryReplSetEvents" ([bfd5441](https://github.com/nodkz/mongodb-memory-server/commit/bfd5441f0e18a38e324e8c49a4adaa05adfdf3ec))
* **MongoMemoryReplSet:** rename "MongoMemoryReplSetStateEnum" to "MongoMemoryReplSetStates" ([c02e21d](https://github.com/nodkz/mongodb-memory-server/commit/c02e21d36be0439bc1ea19f2c9cd6733b4fd1074))
* **MongoMemoryReplSet:** setup proper events ([644a335](https://github.com/nodkz/mongodb-memory-server/commit/644a335089cf6a078a055a6780f4cf48630e6506))
* **MongoMemoryServer:** rename "MongoMemoryServerEventEnum" to "MongoMemoryServerEvents" ([251c7ed](https://github.com/nodkz/mongodb-memory-server/commit/251c7ede0dd56e7ac0f98f75c278066ea5333272))
* **MongoMemoryServer:** rename "MongoMemoryServerStateEnum" to "MongoMemoryServerStates" ([139d3fd](https://github.com/nodkz/mongodb-memory-server/commit/139d3fd9c1175c0abc66cc1b0c7c49738f231658))

## [7.0.0-beta.7](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.6...v7.0.0-beta.7) (2020-10-27)


### Fixes

* broken build (Cannot find module 'mongodb-memory-server') ([3c7d102](https://github.com/nodkz/mongodb-memory-server/commit/3c7d1027137257913b4648525a51703a95f07ac4))

## [7.0.0-beta.6](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.5...v7.0.0-beta.6) (2020-10-27)


### ⚠ BREAKING CHANGES

* **MongoMemoryReplSet:** not resetting "servers" after calling "stop" on an replSet can be breaking for some cases
* **MongoMemoryServer:** allow the re-use of instances & dbPath's meant to change some things internally, which could be breaking

### Features

* **db_util:** rename function "getUriBase" to "uriTemplate" ([c888b95](https://github.com/nodkz/mongodb-memory-server/commit/c888b952891fc6e5e54d8ac29994fb8e679b9f59)), closes [#404](https://github.com/nodkz/mongodb-memory-server/issues/404)
* **MongoMemoryReplSet:** add basic "createAuth" support ([6c118a9](https://github.com/nodkz/mongodb-memory-server/commit/6c118a900d9daf272898d0f39134f7919499f299))
* **MongoMemoryReplSet:** allow re-use of instances & dbPath ([3d64705](https://github.com/nodkz/mongodb-memory-server/commit/3d64705c7406a0eb7e0ef7f1b9dbeb7685050494))
* **MongoMemoryReplSet:** getUri: allow executing while state is "init" ([b3ebac2](https://github.com/nodkz/mongodb-memory-server/commit/b3ebac256006a5339d578f23d70f5f00d2be57d0))
* **MongoMemoryServer:** add (protected) function "getNewPort" ([662a69b](https://github.com/nodkz/mongodb-memory-server/commit/662a69b9b60b0c29a76cb1ee6f24eade095eb7a7))
* **MongoMemoryServer:** add ability to automatically create auth ([d5bf77a](https://github.com/nodkz/mongodb-memory-server/commit/d5bf77a16fe8cf4ca43383c5c371e218a487f314)), closes [#299](https://github.com/nodkz/mongodb-memory-server/issues/299)
* **MongoMemoryServer:** add ability to force same port on restart ([18c77e2](https://github.com/nodkz/mongodb-memory-server/commit/18c77e27cb4ed80514a3c4e893711a933c9bfe8a))
* **MongoMemoryServer:** add function "getStartOptions" ([f057ea7](https://github.com/nodkz/mongodb-memory-server/commit/f057ea765785f4acf094f7df2f799fb11acee9fd))
* **MongoMemoryServer:** allow re-use of instances & dbPath ([e2ae879](https://github.com/nodkz/mongodb-memory-server/commit/e2ae87961fa817e1d885487c9edc8ed89ac82260))


### Fixes

* **MongoInstance:** kill: ensure only error ignored is the actual error to be ignored ([5e377fa](https://github.com/nodkz/mongodb-memory-server/commit/5e377fad20604a4fde89c3aee717b3e19123092b))
* **MongoInstance:** run: reset all booleans on ([188d333](https://github.com/nodkz/mongodb-memory-server/commit/188d3330fead506e66250d761dd9c53326b97f92))
* **MongoMemoryReplSet:** _waitForPrimary: check if instance is already primary ([8f65696](https://github.com/nodkz/mongodb-memory-server/commit/8f6569646cf8a8953a3db00f2488244b86152403))
* **MongoMemoryReplSet:** initAllServers: execute "stateChange" with "init" ([28bcf5b](https://github.com/nodkz/mongodb-memory-server/commit/28bcf5bd26b7950a14fd4c5f17688320038b38f9))
* **utils:** killProcess: check if the childProcess PID is still alive ([96c30de](https://github.com/nodkz/mongodb-memory-server/commit/96c30deee12e295738b93e28fad056e24ccaf40e))


### Refactor

* **MongoMemoryReplSet:** _initReplSet: reassign "adminDb" ([19ae688](https://github.com/nodkz/mongodb-memory-server/commit/19ae688d9ccc623ac42d032fada381268c10df93))
* **MongoMemoryServer:** ensureInstance: move "return instanceInfo" into case "running" ([4214aa5](https://github.com/nodkz/mongodb-memory-server/commit/4214aa56362d5cad139acf2c134f410ddb765aba))
* **MongoMemoryServer:** remove destructuring of "promises" ([a828506](https://github.com/nodkz/mongodb-memory-server/commit/a828506ec749ebb9b0d081a77cff0036d97e5e41))
* **MongoMemoryServer:** start: check "state" instead of "instanceInfo" ([4fd1ede](https://github.com/nodkz/mongodb-memory-server/commit/4fd1ede502acb67be052957b3907eb1f5a57212f))
* remove file "types.ts" ([23cdc65](https://github.com/nodkz/mongodb-memory-server/commit/23cdc656562e662780ae5b314d2da3243116e800)), closes [#406](https://github.com/nodkz/mongodb-memory-server/issues/406)
* rename "-test.ts" to ".test.ts" ([deb0098](https://github.com/nodkz/mongodb-memory-server/commit/deb00984281d3e7e7e37fb7bd0358390176d6a79))
* rename file "db_util" to "utils" ([f3df9c8](https://github.com/nodkz/mongodb-memory-server/commit/f3df9c81b4b614ff6cac15579051fd11921c09ce))
* rename file "postinstall-helper" to "postinstallHelper" ([fdf2d09](https://github.com/nodkz/mongodb-memory-server/commit/fdf2d09a33a3d8ed893f0ba01e0022814f3b2089))
* rename file "resolve-config" to "resolveConfig" ([7ee646c](https://github.com/nodkz/mongodb-memory-server/commit/7ee646c2479e8237c0c14096a8ac026d45a8c96e))
* **db_util:** uriTemplate: change "query" to be an string-array ([8dffa64](https://github.com/nodkz/mongodb-memory-server/commit/8dffa64ee4d56523cefd993b1158d2a9e224cd8a))
* unify interface names (remove "T") ([78a78cd](https://github.com/nodkz/mongodb-memory-server/commit/78a78cdc8c1d67d780aaca064169b8324d04d0c3)), closes [#395](https://github.com/nodkz/mongodb-memory-server/issues/395)
* **MongoBinary:** change "cache" to be an Map ([74d30a0](https://github.com/nodkz/mongodb-memory-server/commit/74d30a0244f1d4797129dc9b577ef50d5aae8d41)), closes [#374](https://github.com/nodkz/mongodb-memory-server/issues/374)


### Style

* **MongoBinaryDownload:** rename interface "DownloadProgress" to "MongoBinaryDownloadProgress" ([2bad87c](https://github.com/nodkz/mongodb-memory-server/commit/2bad87c18ab1bf4fc2c6a723af5893fa57de747f))
* **MongoInstance:** add TODO comments ([5e320ca](https://github.com/nodkz/mongodb-memory-server/commit/5e320cad6cd277e0e87da7beb4dd35d3bb92e5c5))
* **MongoMemoryReplSet:** _initReplSet: change logs to be more clear ([561c883](https://github.com/nodkz/mongodb-memory-server/commit/561c8832c5504382d6b70b9a8ff3fa581cbc46e8))
* **MongoMemoryReplSet:** _initReplSet: remove "await" from non-Promise functions ([846f969](https://github.com/nodkz/mongodb-memory-server/commit/846f969893586050476383622cbed412608d69e9))

## [7.0.0-beta.5](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.4...v7.0.0-beta.5) (2020-10-12)


### ⚠ BREAKING CHANGES

* **MongoMemoryReplSet:** change "getUri" to be sync (dosnt wait until running anymore)
* **MongoMemoryReplSet:** remove option "oplogSize", replace with ".replSetOpts.args.push('--oplogSize', '1')"
* **MongoMemoryReplSet:** remove function "getDbName", replace with ".opts.replSet.dbName"
* **MongoMemoryReplSet:** removing function "getConnectionString" could break some code
* **MongoMemoryReplSet:** removing "async" / modifing return type "Promise<string>" can break code

### Features

* change package "mongodb" to be non-optional ([2b14552](https://github.com/nodkz/mongodb-memory-server/commit/2b14552beb5f2bdb1dd1978c8cf391d25adba4b1))
* **db_util:** add function "ensureAsync" ([971b02d](https://github.com/nodkz/mongodb-memory-server/commit/971b02d07453b46dd37dace8d91efd74b20c3575))
* **MongoInstance:** add value "isReplSet" ([3ba31e2](https://github.com/nodkz/mongodb-memory-server/commit/3ba31e249c6ea4cd883979a1a5799863bf9ae971))
* **MongoInstance:** graceful ReplSet shutdown ([017239c](https://github.com/nodkz/mongodb-memory-server/commit/017239c953fd44018855a55d417bfc4573c9f684))
* **MongoMemoryReplSet:** add error if replSet count is 0 or lower ([0202e8f](https://github.com/nodkz/mongodb-memory-server/commit/0202e8fefb835fb256e8c1bd4573e15f8ac5c6f5))
* **MongoMemoryReplSet:** add getter "state" ([65135a8](https://github.com/nodkz/mongodb-memory-server/commit/65135a83a27a932937fe3989e1c56f8c33ea5f5c))
* **MongoMemoryReplSet:** remove function "getConnectionString" ([dbe844e](https://github.com/nodkz/mongodb-memory-server/commit/dbe844e8f972925391ba9edd983fc3043bc39efa))
* **MongoMemoryReplSet:** remove function "getDbName" ([6ebafbd](https://github.com/nodkz/mongodb-memory-server/commit/6ebafbd762c208f60bc9132773edfee07e6d2821))
* **MongoMemoryReplSet:** remove option "autoStart" ([90ed578](https://github.com/nodkz/mongodb-memory-server/commit/90ed57865db4f629d0efd00df5ac0ccbf1fda65a))
* **MongoMemoryReplSet:** remove option "oplogSize" ([07937e2](https://github.com/nodkz/mongodb-memory-server/commit/07937e2fd8ebce9759f4a837a6b013574488b7eb))
* **MongoMemoryReplSet:** rename "opts.*" to "*Opts" & add getters & setters ([c701f09](https://github.com/nodkz/mongodb-memory-server/commit/c701f0980762b21761361ef485b6282569b9741a))
* **MongoMemoryServer:** add function "create" ([6dcb12a](https://github.com/nodkz/mongodb-memory-server/commit/6dcb12ad4a7f96739b0e11e13e3fb9c473633b11))


### Style

* **MongoMemoryReplSet:** add more tsdoc ([6b60a71](https://github.com/nodkz/mongodb-memory-server/commit/6b60a71e0c9c81197f2a42b59e8b6f96660cf410))
* remove "uri" value when only used once ([150494e](https://github.com/nodkz/mongodb-memory-server/commit/150494e8d736d1cb61fc5fdd9306215a599f0b1d))
* **db_util:** add link on why "ensureAsync" is needed ([412e615](https://github.com/nodkz/mongodb-memory-server/commit/412e61589077b8f2ebcc7d046466ffc652a4fe32))
* **MongoMemoryReplSet:** add log to "stop" ([d3dff26](https://github.com/nodkz/mongodb-memory-server/commit/d3dff2605ee0837a3d655a0f31096edc5e33cb7c))
* **MongoMemoryReplSet:** add more logs ([a3a911f](https://github.com/nodkz/mongodb-memory-server/commit/a3a911fda1e083cd4964e57ae34dbe74b7f3a721))
* **MongoMemoryReplSet:** replace templating string with normal ([9add2bc](https://github.com/nodkz/mongodb-memory-server/commit/9add2bcf983e2b7c7c981753c9ca447db49ea2eb))


### Dependencies

* **uuid:** add "^" ([e12396e](https://github.com/nodkz/mongodb-memory-server/commit/e12396eb8368358c69d2d8c23e7d787a42b669db))


### Refactor

* **MongoMemoryReplSet:** _initReplSet: directly use db "admin" ([a335500](https://github.com/nodkz/mongodb-memory-server/commit/a33550022244b023c21d16e667c5c8697b1c22b8))
* **MongoMemoryReplSet:** _initReplSet: remove redundant object assignment ([8e6e312](https://github.com/nodkz/mongodb-memory-server/commit/8e6e312dfc2b9e430854f9868ee68f9cfdfdb8d8))
* **MongoMemoryReplSet:** _initReplSet: rename "conn" to "con" ([335780e](https://github.com/nodkz/mongodb-memory-server/commit/335780e295f0abe7f6d0d7f67aaf1f2e8f0ac8ba))
* **MongoMemoryReplSet:** _waitForPrimary: remove value "timeoutPromise" ([18b9a58](https://github.com/nodkz/mongodb-memory-server/commit/18b9a587b2f6b1185d6253f549abda380f018dec))
* **MongoMemoryReplSet:** add function "stateChange" ([3c3d6fb](https://github.com/nodkz/mongodb-memory-server/commit/3c3d6fb6abe094ecf26bb55af1140041134eed27))
* **MongoMemoryReplSet:** change "_initReplSet" to be "protected" ([f46d113](https://github.com/nodkz/mongodb-memory-server/commit/f46d113497ea0c8685439abae7e3467b25ff8498))
* **MongoMemoryReplSet:** change "_initServer" to be "protected" ([4c32f45](https://github.com/nodkz/mongodb-memory-server/commit/4c32f458bb2957a6a33e783c990eaffe4b77637e))
* **MongoMemoryReplSet:** change "_state" to be "protected" ([415fc8f](https://github.com/nodkz/mongodb-memory-server/commit/415fc8fce60b8ca12dc1d352eddfa304ce77a70b))
* **MongoMemoryReplSet:** change "_waitForPrimary" to be "protected" ([d0d62e2](https://github.com/nodkz/mongodb-memory-server/commit/d0d62e2b9c4824ac6b238d97889d9bab96057bf6))
* **MongoMemoryReplSet:** change "getInstanceOpts" to be "protected" ([e954806](https://github.com/nodkz/mongodb-memory-server/commit/e9548062793340c78ff160afb41c7e3c9229a2d9))
* **MongoMemoryReplSet:** change "getUri" to be sync ([13f3f1d](https://github.com/nodkz/mongodb-memory-server/commit/13f3f1d3ee636b20005f233cb6f50530885659fc))
* **MongoMemoryReplSet:** change "if not state 'stopped'" to switch ([df1af0c](https://github.com/nodkz/mongodb-memory-server/commit/df1af0cac6690ccf5ac3d8b946a13f75d581ca62))
* **MongoMemoryReplSet:** change if-error to "assertion" ([179bdbb](https://github.com/nodkz/mongodb-memory-server/commit/179bdbb417548ce42b02d31c1e545c96595f0a56))
* **MongoMemoryReplSet:** improve "start" ([c2311cb](https://github.com/nodkz/mongodb-memory-server/commit/c2311cb4601404f08175f166d4c5114bca3f1d35))
* **MongoMemoryReplSet:** refactor "_state" into an enum ([e3d4678](https://github.com/nodkz/mongodb-memory-server/commit/e3d4678d34d7165a9726866234a1e25b898dd338))
* **MongoMemoryReplSet:** refactor multiple "if" into one switch ([8b8a609](https://github.com/nodkz/mongodb-memory-server/commit/8b8a6095f415f4daa5761f25c998bd594b0e3f4d))
* **MongoMemoryReplSet:** remove "?" from "MongoMemoryReplSetOptsT" ([138e21d](https://github.com/nodkz/mongodb-memory-server/commit/138e21d6433bfb431243ed9c0c83cef6ec71adfd))
* **MongoMemoryReplSet:** remove "async" from "getDbName" ([2775b4f](https://github.com/nodkz/mongodb-memory-server/commit/2775b4fcc6afcaab99414faf7100021f4047629e))
* **MongoMemoryReplSet:** remove commented out HACK ([1ad5bdc](https://github.com/nodkz/mongodb-memory-server/commit/1ad5bdc879a8f90620ba572e9ec9ab5ca686744c))
* **MongoMemoryReplSet:** remove dynamic import "mongodb" ([fb958ae](https://github.com/nodkz/mongodb-memory-server/commit/fb958aef5a604f636956c2d8656a45ade9595895))
* **MongoMemoryReplSet:** shorten constructor ([e17762d](https://github.com/nodkz/mongodb-memory-server/commit/e17762db2ffbbfa77aef0de24ba6752c0326401a))
* **MongoMemoryReplSet:** small improvements ([9b17925](https://github.com/nodkz/mongodb-memory-server/commit/9b179254099f3d07607f3fbb97b627ea0c323b5f))
* **MongoMemoryReplSet:** waitUntilRunning: shorten function ([0fc27d6](https://github.com/nodkz/mongodb-memory-server/commit/0fc27d6b308a34ab27ae71e113872999549d098c))
* **replset-single:** shorten "state errors" ([2559117](https://github.com/nodkz/mongodb-memory-server/commit/2559117b69c0476b9835b87e1f1cbd702f69e863))


### Fixes

* **MongoMemoryReplSet:** _initReplSet: throw error if "this.servers.length" is "<= 0" ([019b118](https://github.com/nodkz/mongodb-memory-server/commit/019b1188b8f77bcbf47aced7e07aba67336ec3f4))
* **MongoMemoryReplSet:** "getUri" now uses "waitUntilRunning" ([18428d5](https://github.com/nodkz/mongodb-memory-server/commit/18428d5a7f46fdf47f88154f833fcf896d4c3bb5))
* **MongoMemoryReplSet:** change "_waitForPrimary" timout message to be an error ([89c8af6](https://github.com/nodkz/mongodb-memory-server/commit/89c8af6399b81a42bf38a14418aee967d4559d9c))
* **MongoMemoryReplSet:** ensure "start" is async ([765b5b1](https://github.com/nodkz/mongodb-memory-server/commit/765b5b13ded44c68d109552391d0581bbbdddf84))
* **MongoMemoryReplSet:** move "removeListener" before "_state" check ([60646eb](https://github.com/nodkz/mongodb-memory-server/commit/60646eb4829b0c09bf6b88ade4a55f010f8bca6f))
* **MongoMemoryReplSet:** register listener for event "beforeExit" inside "start" ([7859d6c](https://github.com/nodkz/mongodb-memory-server/commit/7859d6c60e47b6f1bbfb2a0c3a39ce417f200470))
* **MongoMemoryReplSet:** throw error if state is not "running" or "init" ([27f6215](https://github.com/nodkz/mongodb-memory-server/commit/27f62155c219ed4a8685c360dfa9bf822d62b38d))

## [7.0.0-beta.4](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.3...v7.0.0-beta.4) (2020-10-12)


### Fixes

* **-global:** change "mongodb_version" to latest patch version ([adcbdcf](https://github.com/nodkz/mongodb-memory-server/commit/adcbdcfa3240f4182466a70b8c731d0d97fa5287))
* **MongoBinary:** change "LATEST_VERSION" to latest patch version "4.0.20" ([23e6eaa](https://github.com/nodkz/mongodb-memory-server/commit/23e6eaa89c82efeb27fe71fd012cf438b54b006a))
* **MongoMemoryReplSet:** _initReplSet: check if there is already an PRIMARY ([a1c9264](https://github.com/nodkz/mongodb-memory-server/commit/a1c92648c8e3ac114b211e86c31b310d00c1c140))


### Refactor

* **postinstall:** rename function "postInstall" to "postInstallEnsureBinary" ([aca8262](https://github.com/nodkz/mongodb-memory-server/commit/aca826211351e73458c56e6d0dce99d068e05941))
* apply suggested changes ([2a9aab7](https://github.com/nodkz/mongodb-memory-server/commit/2a9aab7738e6512ce0e03135f4c8a8d217d62816))
* ***index:** use "tslib.__exportStar" ([2e9faec](https://github.com/nodkz/mongodb-memory-server/commit/2e9faec7a27a13652378d4cdd4d5bd632dc0fa8c))
* **postinstall:** change all packages to depend on "core" ([de41060](https://github.com/nodkz/mongodb-memory-server/commit/de41060cae7e4fcc1af286d18b90d473bca5864e)), closes [#378](https://github.com/nodkz/mongodb-memory-server/issues/378) [#174](https://github.com/nodkz/mongodb-memory-server/issues/174)

## [7.0.0-beta.3](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.2...v7.0.0-beta.3) (2020-10-08)


### ⚠ BREAKING CHANGES

* **MongoMemoryServer:** remove function "getDbName", can be replaced with "instanceInfo.dbName"
* **MongoMemoryServer:** remove function "getDbPath", can be replaced with "instanceInfo.dbPath"
* **MongoMemoryServer:** remove function "getPort", can be replaced with "instanceInfo.port"
* **MongoInstance:** change "start" to not reset "port" to "undefined"
* **MongoInstance:** change "instanceOpts" to be readonly and Readonly
change "binaryOpts" to be readonly and Readonly
change "spawnOpts" to be readonly and Readonly
* **MongoMemoryServer:** removing ".uri" because of function "getUri"
* **MongoMemoryServer:** removing ".childProcess" because it is an alias for ".instance.childProcess"
* **MongoMemoryServer:** remove option "autoStart"
change "MongoMemoryServer.create" to always call "MongoMemoryServer.start"
* **MongoMemoryServer:** change "MongoMemoryServer.getInstanceInfo" to return "undefined" instead of "false"
* **MongoMemoryServer:** change "MongoMemoryServer.getUri" to be sync
* **MongoMemoryServer:** remove deprecated function "getConnectionString" (replace with "getUri")
* **MongoMemoryServer:** change "MongoMemoryServer.getDbName" to be sync
* **MongoMemoryServer:** change "MongoMemoryServer.getDbPath" to be sync
* **MongoMemoryServer:** change "MongoMemoryServer.getPort" to be sync
* **MongoMemoryServer:** change "MongoMemoryServer.runningInstance" to be "undefined" instead of "null"
change "MongoMemoryServer.instanceInfoSync" to be "undefined" instead of "null"

### Features

* **MongoInstance:** change options to be readonly ([e599372](https://github.com/nodkz/mongodb-memory-server/commit/e5993727c618e08e1196b61d1d768bee34657738))
* **MongoMemoryServer:** add getter function "state" ([c19493f](https://github.com/nodkz/mongodb-memory-server/commit/c19493fd5243e66dc9afee7052178ee921d11369))
* **MongoMemoryServer:** extend EventEmitter ([04ca3d7](https://github.com/nodkz/mongodb-memory-server/commit/04ca3d750b83174400409c073d709e7642dc819e))
* **MongoMemoryServer:** remove "MongoInstanceDataT.childProcess" ([c71d8d4](https://github.com/nodkz/mongodb-memory-server/commit/c71d8d46ad52dbecc37470ccd182829b1afbc61e))
* **MongoMemoryServer:** remove "StartupInstanceData.uri" ([dec17a4](https://github.com/nodkz/mongodb-memory-server/commit/dec17a4379c54aab99a881faec2d6e88c949969b))
* **MongoMemoryServer:** remove deprecated function "getConnectionString" ([198f4c0](https://github.com/nodkz/mongodb-memory-server/commit/198f4c032ba0746c7b03ca509b16d8cd772ac875))
* **MongoMemoryServer:** remove function "getDbName" ([e2fc23f](https://github.com/nodkz/mongodb-memory-server/commit/e2fc23f62797aeb4e61a21924e7413621e767da8))
* **MongoMemoryServer:** remove function "getDbPath" ([2343771](https://github.com/nodkz/mongodb-memory-server/commit/2343771c9c7f1c780889cfea94e3f3947550edcd))
* **MongoMemoryServer:** remove function "getPort" ([5eb7017](https://github.com/nodkz/mongodb-memory-server/commit/5eb701741d6f650b72cfbda5394b4ccfab030766))
* **MongoMemoryServer:** remove option "autoStart" ([347085f](https://github.com/nodkz/mongodb-memory-server/commit/347085f890be05a28dc2b01c6ddb5011744f12dc))
* **MongoMemoryServer:** rename function "getInstanceInfo" into "get instanceInfo" ([ae8a9f8](https://github.com/nodkz/mongodb-memory-server/commit/ae8a9f82743df91a13716ab954bac510c30832af))


### Reverts

* "chore: remove unused file "tsconfig.test"" ([cc053c7](https://github.com/nodkz/mongodb-memory-server/commit/cc053c7f78ff29f67aabae30d180376c26ca96d8))


### Style

* **MongoMemoryServer:** remove comment & change log ([b098941](https://github.com/nodkz/mongodb-memory-server/commit/b0989411f39fe1397cecb8423e93bdf3245af0ea))


### Fixes

* **db_util:** killProcess: fix "SIGINT"-"SIGKILL" warn condition ([4113d94](https://github.com/nodkz/mongodb-memory-server/commit/4113d9457874c660b550e4ce5929582091f19d0a))
* **MongoInstance:** remove resetting "port" inside "start" ([7861a6f](https://github.com/nodkz/mongodb-memory-server/commit/7861a6faaf9fbdf229cd5792e7f515931f5a64b8)), closes [#393](https://github.com/nodkz/mongodb-memory-server/issues/393)


### Refactor

* **MongoMemoryReplSet:** stop: reset "servers" after stopping them ([0aa2293](https://github.com/nodkz/mongodb-memory-server/commit/0aa2293168b8081fcf2e1391c6096d30e31e0c38))
* **MongoMemoryServer:** add sanity check to "stop" ([8aff4ef](https://github.com/nodkz/mongodb-memory-server/commit/8aff4efe4356c12fcbe6153d8f33c03779b0626f))
* **MongoMemoryServer:** always reset "port" to "undefined" ([8ca0729](https://github.com/nodkz/mongodb-memory-server/commit/8ca0729cade0f1dd82c0eaefd81a5d2bf2b8fd6c))
* **MongoMemoryServer:** change "_state" to be "protected" ([b716c2c](https://github.com/nodkz/mongodb-memory-server/commit/b716c2cef8b6b74e90930ae08f2390abd3775206))
* **MongoMemoryServer:** change "getDbName" to be sync ([85a97e0](https://github.com/nodkz/mongodb-memory-server/commit/85a97e056c2d407a2d949e94b872403231c164d1))
* **MongoMemoryServer:** change "getDbPath" to be sync ([281fa1c](https://github.com/nodkz/mongodb-memory-server/commit/281fa1c716704f0142b022c7e0555f13c0b63b4f))
* **MongoMemoryServer:** change "getInstanceInfo" to return undefined ([27349a3](https://github.com/nodkz/mongodb-memory-server/commit/27349a3ddabd956038165d94932b5df4d9c0941f))
* **MongoMemoryServer:** change "getPort" to be sync ([e849f2c](https://github.com/nodkz/mongodb-memory-server/commit/e849f2caa5b2c84cb2901269162b8d92351be944))
* **MongoMemoryServer:** change "getUri" to be sync ([5b53f03](https://github.com/nodkz/mongodb-memory-server/commit/5b53f03f25be9946df236977cfb65c7fb72ba4c6))
* **MongoMemoryServer:** change "instanceInfo" to be "protected" ([7390eee](https://github.com/nodkz/mongodb-memory-server/commit/7390eee23bf5edb23b29ddeb33fb1ebf962eae53))
* **MongoMemoryServer:** merge "runningInstance" and "instanceInfoSync" into "instanceInfo" ([7642c75](https://github.com/nodkz/mongodb-memory-server/commit/7642c754f25a20ebee99fe974a008b522be75c0a))
* **MongoMemoryServer:** refactor "start" to be more readable ([7fb31c1](https://github.com/nodkz/mongodb-memory-server/commit/7fb31c151081ef1ada4062966a85eb9aaaace214))
* **MongoMemoryServer:** remove "await" from "getUriBase" call ([ca536b6](https://github.com/nodkz/mongodb-memory-server/commit/ca536b6a3c1059132b0a767653f70e7441b687bd))
* **MongoMemoryServer:** remove "null" use "undefined" ([086abef](https://github.com/nodkz/mongodb-memory-server/commit/086abef19eefb9fd8ac2e6e3304ea2cbafab9e0a))
* **MongoMemoryServer:** remove call to "ensureInstance" inside "stop" ([57801cf](https://github.com/nodkz/mongodb-memory-server/commit/57801cf3e08e95084a73a5e0b8ef3258c098c83b))
* **MongoMemoryServer:** rename "instanceInfo" to "_instanceInfo" ([d3ddcb4](https://github.com/nodkz/mongodb-memory-server/commit/d3ddcb41a55aeb012aeb92c2303eec7b2472cda7))
* **MongoMemoryServer:** rename function "assertionInstanceInfoSync" to "assertionInstanceInfo" ([03c8343](https://github.com/nodkz/mongodb-memory-server/commit/03c834379c306464ede6667a53916f4dfbbe5b39))
* **MongoMemoryServer:** shorten "getUri" ([f1024e5](https://github.com/nodkz/mongodb-memory-server/commit/f1024e551b594783e580a8d6b13dd243c25240dc))
* **MongoMemoryServer:** start: remove first ".catch" ([fafaa29](https://github.com/nodkz/mongodb-memory-server/commit/fafaa29116683c2ce08d027eef8cdcae4c50c991))

# [7.0.0-beta.2](https://github.com/nodkz/mongodb-memory-server/compare/v7.0.0-beta.1...v7.0.0-beta.2) (2020-10-07)


### Bug Fixes

* **types:** remove alias "SpawnOptions" ([8b963c5](https://github.com/nodkz/mongodb-memory-server/commit/8b963c52da9b1acf901a8e5c52074c9c7778aff4))
* **types:** remove unused types ([ab2944b](https://github.com/nodkz/mongodb-memory-server/commit/ab2944b76c9fc5ffa33b15cbfad822ab77a19301))
* remove unused file "deprecate" ([bb3e0f4](https://github.com/nodkz/mongodb-memory-server/commit/bb3e0f4e1c2564632516bf069c25c2bbd1a9e67a))

# [7.0.0-beta.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.9.0...v7.0.0-beta.1) (2020-10-01)


### Bug Fixes

* **MongoInstance:** reset "childProcess" and "killerProcess" after "kill" ([49c710d](https://github.com/nodkz/mongodb-memory-server/commit/49c710df5b2fcaba1163c2d86b81e4eb1728bdff))


### Code Refactoring

* **MongoInstance:** change "null" to "undefined" for "childProcess" & "killerProcess" ([232b812](https://github.com/nodkz/mongodb-memory-server/commit/232b812c7799da392955f6e4d4e49f67b8e10597))
* **MongoInstance:** move "debug" into an private function ([3d23d5b](https://github.com/nodkz/mongodb-memory-server/commit/3d23d5b6d6dbac3c7b365bad3bc9bb03021ddfc6))
* **MongoInstance:** replace "instanceReady" and "instanceFailed" with events ([6925c45](https://github.com/nodkz/mongodb-memory-server/commit/6925c45a15d4ab14d4bd134ebcad1e96c6349580))
* **MongoMemoryReplSet:** "_waitForPrimary" use new events ([ed4b9e9](https://github.com/nodkz/mongodb-memory-server/commit/ed4b9e9c448435ff05cd504ed4e8a1a0e515b649))


### Features

* **db_util:** add function "assertion" ([c059500](https://github.com/nodkz/mongodb-memory-server/commit/c059500f946fa248260b686ec4ffaaa58c942a74))
* **MongoInstance:** change root values of "MongodOpts" to be required ([9779721](https://github.com/nodkz/mongodb-memory-server/commit/97797210bddbb117bfabb28f5b0be898a543bb3e))
* **MongoInstance:** extend EventEmitter ([10965c7](https://github.com/nodkz/mongodb-memory-server/commit/10965c7ac5c6a0877561221608f80d508cbfe30a)), closes [#365](https://github.com/nodkz/mongodb-memory-server/issues/365)
* **MongoInstance:** make "port" and "dbPath" required ([749c3e3](https://github.com/nodkz/mongodb-memory-server/commit/749c3e3dc9bc93d1506e034bf24a74b4420a4139))
* **MongoInstance:** outsource "MongodOpts.instance" ([d9dd6f8](https://github.com/nodkz/mongodb-memory-server/commit/d9dd6f81f84a69b412cdb5198baaabbdfaa156f7))
* **MongoInstance:** remove function "waitPrimaryReady" ([1536dc2](https://github.com/nodkz/mongodb-memory-server/commit/1536dc26f8548e95abc3baa0dba4b9b333b9e140))
* **MongoInstance:** rename interface "MongodOps" to "MongodOpts" ([edd4d39](https://github.com/nodkz/mongodb-memory-server/commit/edd4d39e0f8c0d1ed9c21f95f462e7bb8f42737f))


### BREAKING CHANGES

* **MongoInstance:** changing "null" to "undefined" can break some code
* **MongoInstance:** throwing an error if 2 values are now undefined/null can break some code
* **MongoInstance:** removing the possibility to overwrite 2 functions this can break some use-cases
* **MongoInstance:** removing an function can break some use-cases
* **MongoMemoryReplSet:** "_waitForPrimary" now uses events instead of calling function "waitPrimaryReady"
* **MongoInstance:** because of changing values to "required" this can break some use-cases
* **MongoInstance:** removing the "dynamic" part can break some code with custom debug-logging
* **MongoInstance:** because of the rename it can break some use-cases


## [6.9.2](https://github.com/nodkz/mongodb-memory-server/compare/v6.9.1...v6.9.2) (2020-10-09)


### Bug Fixes

* **MongoBinaryDownloadUrl:** add case for Linux Mint 20 ([01a6bc6](https://github.com/nodkz/mongodb-memory-server/commit/01a6bc63f0e13a4528ee39ccae64390a8de48582))
* **MongoBinaryDownloadUrl:** detect "linuxmint" and "linux mint" as linux mint ([fda4f72](https://github.com/nodkz/mongodb-memory-server/commit/fda4f7224d156680ac68c743c5a5a963070171dd)), closes [#403](https://github.com/nodkz/mongodb-memory-server/issues/403)

## [6.9.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.9.0...v6.9.1) (2020-10-07)


### Bug Fixes

* **MongoBinaryDownloadUrl:** fix win32 download generation ([d62b489](https://github.com/nodkz/mongodb-memory-server/commit/d62b4891a01fe40b5f00c21ee02f08b24a55d80c)), closes [#399](https://github.com/nodkz/mongodb-memory-server/issues/399)

# [6.9.0](https://github.com/nodkz/mongodb-memory-server/compare/v6.8.1...v6.9.0) (2020-09-30)


### Bug Fixes

* **MongoInstance:** try "SIGKILL" after timeout ([f2a06bc](https://github.com/nodkz/mongodb-memory-server/commit/f2a06bcd08922dccd11a8ade9d637cb2efcd157f))
* **MongoMemoryReplSet:** change "process.on" to "process.once" for "beforeExit" ([0e07953](https://github.com/nodkz/mongodb-memory-server/commit/0e0795341ff914b4aca059317aa7cd41bae6db68))
* **MongoMemoryReplSet:** remove "beforeExit" listener inside "stop" ([c7328c9](https://github.com/nodkz/mongodb-memory-server/commit/c7328c9a1a2f68da5463a4fd2cb6a7e588aef6dc))
* **MongoMemoryServer:** remove double check ([b99f3a4](https://github.com/nodkz/mongodb-memory-server/commit/b99f3a4b855e5630ff1b26285dae4942601c0735))


### Features

* **MongoInstance:** warn if nodejs version is below "10.15.0" ([8693b46](https://github.com/nodkz/mongodb-memory-server/commit/8693b4613e3cac078b611f1c581f268a37a38680)), closes [#379](https://github.com/nodkz/mongodb-memory-server/issues/379)
* **MongoMemoryReplSet:** deprecate "getConnectionString" ([b088af2](https://github.com/nodkz/mongodb-memory-server/commit/b088af2fad9660a685b15efdffeb03b16ce58579))
* **MongoMemoryServer:** deprecate "getConnectionString" ([9abf04f](https://github.com/nodkz/mongodb-memory-server/commit/9abf04f23188e1ad4eb47b0797c33e8210b8056b))

# [6.9.0-beta.2](https://github.com/nodkz/mongodb-memory-server/compare/v6.9.0-beta.1...v6.9.0-beta.2) (2020-09-30)


### Features

* **MongoMemoryReplSet:** deprecate "getConnectionString" ([b088af2](https://github.com/nodkz/mongodb-memory-server/commit/b088af2fad9660a685b15efdffeb03b16ce58579))
* **MongoMemoryServer:** deprecate "getConnectionString" ([9abf04f](https://github.com/nodkz/mongodb-memory-server/commit/9abf04f23188e1ad4eb47b0797c33e8210b8056b))

# [6.9.0-beta.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.8.1...v6.9.0-beta.1) (2020-09-29)


### Bug Fixes

* **MongoInstance:** try "SIGKILL" after timeout ([f2a06bc](https://github.com/nodkz/mongodb-memory-server/commit/f2a06bcd08922dccd11a8ade9d637cb2efcd157f))
* **MongoMemoryReplSet:** change "process.on" to "process.once" for "beforeExit" ([0e07953](https://github.com/nodkz/mongodb-memory-server/commit/0e0795341ff914b4aca059317aa7cd41bae6db68))
* **MongoMemoryReplSet:** remove "beforeExit" listener inside "stop" ([c7328c9](https://github.com/nodkz/mongodb-memory-server/commit/c7328c9a1a2f68da5463a4fd2cb6a7e588aef6dc))
* **MongoMemoryServer:** remove double check ([b99f3a4](https://github.com/nodkz/mongodb-memory-server/commit/b99f3a4b855e5630ff1b26285dae4942601c0735))


### Features

* **MongoInstance:** warn if nodejs version is below "10.15.0" ([8693b46](https://github.com/nodkz/mongodb-memory-server/commit/8693b4613e3cac078b611f1c581f268a37a38680)), closes [#379](https://github.com/nodkz/mongodb-memory-server/issues/379)

## [6.8.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.8.0...v6.8.1) (2020-09-28)


### Bug Fixes

* explicitly re-export "default" ([d3a1f6e](https://github.com/nodkz/mongodb-memory-server/commit/d3a1f6e624399ffcdbe2c8ffb8f174692d007169)), closes [nodkz/mongodb-memory-server#386](https://github.com/nodkz/mongodb-memory-server/issues/386)
* **MongoInstance:** add call to "instanceFailed" to "closeHandler" ([c6010f4](https://github.com/nodkz/mongodb-memory-server/commit/c6010f411d5c72f100e55d0b918b7c252e47a5ec)), closes [#385](https://github.com/nodkz/mongodb-memory-server/issues/385)
* **MongoInstance:** fix log in "run" ([38b2f0d](https://github.com/nodkz/mongodb-memory-server/commit/38b2f0dd9737299fd9b0f750be0594779b5df0ac))

## [6.8.1-beta.2](https://github.com/nodkz/mongodb-memory-server/compare/v6.8.1-beta.1...v6.8.1-beta.2) (2020-09-28)


### Bug Fixes

* explicitly re-export "default" ([d3a1f6e](https://github.com/nodkz/mongodb-memory-server/commit/d3a1f6e624399ffcdbe2c8ffb8f174692d007169)), closes [nodkz/mongodb-memory-server#386](https://github.com/nodkz/mongodb-memory-server/issues/386)

## [6.8.1-beta.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.8.0...v6.8.1-beta.1) (2020-09-26)


### Bug Fixes

* **MongoInstance:** add call to "instanceFailed" to "closeHandler" ([c6010f4](https://github.com/nodkz/mongodb-memory-server/commit/c6010f411d5c72f100e55d0b918b7c252e47a5ec)), closes [#385](https://github.com/nodkz/mongodb-memory-server/issues/385)
* **MongoInstance:** fix log in "run" ([38b2f0d](https://github.com/nodkz/mongodb-memory-server/commit/38b2f0dd9737299fd9b0f750be0594779b5df0ac))

# [6.8.0](https://github.com/nodkz/mongodb-memory-server/compare/v6.7.6...v6.8.0) (2020-09-21)


### Features

* skip binary download when binary tar exists ([31ac64c](https://github.com/nodkz/mongodb-memory-server/commit/31ac64c1db82118d76c9defd42597daf1031f7c6))

## [6.7.6](https://github.com/nodkz/mongodb-memory-server/compare/v6.7.5...v6.7.6) (2020-09-16)


### Bug Fixes

* **MongoBinary:** change "LockFile.unlock" to be async ([87c7b33](https://github.com/nodkz/mongodb-memory-server/commit/87c7b33b28de18c6e0701f4b2540c4b0518ee17b))
* **MongoBinary:** improve code ([39ca575](https://github.com/nodkz/mongodb-memory-server/commit/39ca5754acdb26e822262d56189c2ddc203857a8))
* **resolve-config:** improve code ([22d765d](https://github.com/nodkz/mongodb-memory-server/commit/22d765da9f61ffd3abe0bbf37796c562dec80755))

## [6.7.5](https://github.com/nodkz/mongodb-memory-server/compare/v6.7.4...v6.7.5) (2020-09-12)


### Bug Fixes

* **postinstall:** skip postinstall if "SYSTEM_BINARY" is set ([34b1f1f](https://github.com/nodkz/mongodb-memory-server/commit/34b1f1f052c628bf8b434e2d07e801643dc5ad14)), closes [#370](https://github.com/nodkz/mongodb-memory-server/issues/370)

## [6.7.4](https://github.com/nodkz/mongodb-memory-server/compare/v6.7.3...v6.7.4) (2020-09-11)


### Bug Fixes

* **MongoMemoryReplSet:** comment-out older hack ([c9679d8](https://github.com/nodkz/mongodb-memory-server/commit/c9679d8129b2e4c0afec980f78a5b5e91f5a9f3b)), closes [#366](https://github.com/nodkz/mongodb-memory-server/issues/366)

## [6.7.3](https://github.com/nodkz/mongodb-memory-server/compare/v6.7.2...v6.7.3) (2020-09-11)


### Bug Fixes

* **Dependencies:** update mongodb version ([fe53081](https://github.com/nodkz/mongodb-memory-server/commit/fe5308180afb8b0600596cf3d5b7fe3219777967)), closes [#349](https://github.com/nodkz/mongodb-memory-server/issues/349)

## [6.7.2](https://github.com/nodkz/mongodb-memory-server/compare/v6.7.1...v6.7.2) (2020-09-10)


### Bug Fixes

* **MongoBinaryDownload:** extend 404 error ([4a034f0](https://github.com/nodkz/mongodb-memory-server/commit/4a034f069278e052ca305e409363408ff5cf53cc))
* **MongoInstance:** modify "kill"'s debug logs ([d00a96e](https://github.com/nodkz/mongodb-memory-server/commit/d00a96edd4d1c3feddb7dbc302729ae905df8b62))
* use "db_util.isNullOrUndefined" ([83ce9fe](https://github.com/nodkz/mongodb-memory-server/commit/83ce9fed76ce68eaccb87a9ee72f97339f62ae5c))
* **MongoMemoryReplSet:** remove unused variable ([d32aec1](https://github.com/nodkz/mongodb-memory-server/commit/d32aec165e5fb8db6861cf4443d2f1006dfcae3c))

## [6.7.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.7.0...v6.7.1) (2020-09-09)


### Bug Fixes

* **MongoBinaryDownload:** print used URL in 404 Error ([788c12d](https://github.com/nodkz/mongodb-memory-server/commit/788c12d38dc5308f58a4379e7496960dbb454c08))

# [6.7.0](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.9...v6.7.0) (2020-09-08)


### Features

* add packages `mongodb-memory-server-global-4.2`, `mongodb-memory-server-global-4.4` ([7c97997](https://github.com/nodkz/mongodb-memory-server/commit/7c9799723e35b65f1a37204bdbc637fb0a7f622c))


## [6.6.9](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.8...v6.6.9) (2020-09-08)


### Bug Fixes

* **mongo_killer:** refactor mongo_killer to make more sense ([2dd1fae](https://github.com/nodkz/mongodb-memory-server/commit/2dd1fae2dc87468d3b1e32d0baf2f74543edfe4c))
* **MongoInstance:** de-duplicate killer code & actually log output from "mongo_killer" ([76889a6](https://github.com/nodkz/mongodb-memory-server/commit/76889a6eb678a3b3994315bfc0cbee916a622564))
* **MongoInstance:** use environment variable "NODE" before "argv[0]" ([611f227](https://github.com/nodkz/mongodb-memory-server/commit/611f2274cca178bd8cca5fb48bc1b2a23bd16d88)), closes [#177](https://github.com/nodkz/mongodb-memory-server/issues/177)





## [6.6.8](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.7...v6.6.8) (2020-09-08)


### Bug Fixes

* **package:** move non-exposed [@types](https://github.com/types) to devDependencies ([6ff2e8e](https://github.com/nodkz/mongodb-memory-server/commit/6ff2e8e57d59203d2400339a27398f0eb2ed169a)), closes [#286](https://github.com/nodkz/mongodb-memory-server/issues/286)





## [6.6.7](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.6...v6.6.7) (2020-08-29)


### Bug Fixes

* resolve "Invalid Semver version" problem [#345](https://github.com/nodkz/mongodb-memory-server/issues/345) [#335](https://github.com/nodkz/mongodb-memory-server/issues/335) ([#346](https://github.com/nodkz/mongodb-memory-server/issues/346)) ([3cb858b](https://github.com/nodkz/mongodb-memory-server/commit/3cb858ba6fbd2bba64e27d59a5db18fa99e91978))





## [6.6.6](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.5...v6.6.6) (2020-08-25)


### Bug Fixes

* return back `checkMD5` config option which `false` by default ([#342](https://github.com/nodkz/mongodb-memory-server/issues/342)) ([d2c6cc0](https://github.com/nodkz/mongodb-memory-server/commit/d2c6cc0bee8fb03201ea3b138821235028b47971))





## [6.6.5](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.4...v6.6.5) (2020-08-24)


### Bug Fixes

* change mongodb version tests to use semver ([31183dd](https://github.com/nodkz/mongodb-memory-server/commit/31183ddcb3f75e3270d1cd15157636aa167b8035)), closes [nodkz/mongodb-memory-server#340](https://github.com/nodkz/mongodb-memory-server/issues/340) [nodkz/mongodb-memory-server#318](https://github.com/nodkz/mongodb-memory-server/issues/318)





## [6.6.4](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.3...v6.6.4) (2020-08-17)


### Bug Fixes

* URL generation for MongoDB 4.4 ([#329](https://github.com/nodkz/mongodb-memory-server/issues/329)) ([9cd80f9](https://github.com/nodkz/mongodb-memory-server/commit/9cd80f9ec82a7f05f99f2551bccbdd7485dafae8))





## [6.6.3](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.2...v6.6.3) (2020-07-28)


### Bug Fixes

* remove stub package "@types/get-port" ([#328](https://github.com/nodkz/mongodb-memory-server/issues/328)) ([c49c582](https://github.com/nodkz/mongodb-memory-server/commit/c49c5821b2d7704d47532753e9ae37dcab4179c1)), closes [nodkz/mongodb-memory-server#298](https://github.com/nodkz/mongodb-memory-server/issues/298)
* **MongoBinaryDownload:** add debug log for url ([#327](https://github.com/nodkz/mongodb-memory-server/issues/327)) ([d4c9edb](https://github.com/nodkz/mongodb-memory-server/commit/d4c9edb61c59026fe0e49cb2d3de47e3e8f34f8e))





## [6.6.2](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.1...v6.6.2) (2020-07-27)


### Bug Fixes

* lint ([218b057](https://github.com/nodkz/mongodb-memory-server/commit/218b057425eafa2463d8167fe1ba29a0a4590476))
* update Dependencies (audit problems) ([2782166](https://github.com/nodkz/mongodb-memory-server/commit/278216667929379c43c70314b437cc34db6f07fa))





## [6.6.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.6.0...v6.6.1) (2020-05-20)


### Bug Fixes

* read strict-ssl from npm config ([#310](https://github.com/nodkz/mongodb-memory-server/issues/310)) ([3ede8d1](https://github.com/nodkz/mongodb-memory-server/commit/3ede8d1)), closes [#308](https://github.com/nodkz/mongodb-memory-server/issues/308)





# [6.6.0](https://github.com/nodkz/mongodb-memory-server/compare/v6.5.2...v6.6.0) (2020-05-11)


### Features

* read strict-ssl from npm config ([#306](https://github.com/nodkz/mongodb-memory-server/issues/306)) ([6e3dbc8](https://github.com/nodkz/mongodb-memory-server/commit/6e3dbc8)), closes [#162](https://github.com/nodkz/mongodb-memory-server/issues/162)





## [6.5.2](https://github.com/nodkz/mongodb-memory-server/compare/v6.5.1...v6.5.2) (2020-04-05)


### Bug Fixes

* insensitive the regexp when a primary is elected ([#294](https://github.com/nodkz/mongodb-memory-server/issues/294)) ([746ccb1](https://github.com/nodkz/mongodb-memory-server/commit/746ccb1)), closes [#292](https://github.com/nodkz/mongodb-memory-server/issues/292)





## [6.5.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.5.0...v6.5.1) (2020-04-02)


### Bug Fixes

* change "waiting for connections on port" to "waiting for connections"  ([02228c3](https://github.com/nodkz/mongodb-memory-server/commit/02228c3))





# [6.5.0](https://github.com/nodkz/mongodb-memory-server/compare/v6.4.1...v6.5.0) (2020-03-24)


### Features

* add support for rhel & coreos 8 ([#288](https://github.com/nodkz/mongodb-memory-server/issues/288)) ([2d15e6a](https://github.com/nodkz/mongodb-memory-server/commit/2d15e6a))





## [6.4.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.4.0...v6.4.1) (2020-03-19)


### Bug Fixes

* **MongoBinaryDownload:** Resolve in extractTarGz ([58faef2](https://github.com/nodkz/mongodb-memory-server/commit/58faef2))





# [6.4.0](https://github.com/nodkz/mongodb-memory-server/compare/v6.3.3...v6.4.0) (2020-03-19)


### Bug Fixes

* set timeout per test ([b3f9a10](https://github.com/nodkz/mongodb-memory-server/commit/b3f9a10))


### Features

* add try/catch for reinit of repl set ([ab7f5f6](https://github.com/nodkz/mongodb-memory-server/commit/ab7f5f6))





## [6.3.3](https://github.com/nodkz/mongodb-memory-server/compare/v6.3.2...v6.3.3) (2020-03-11)


### Bug Fixes

* update Dependencies ([#281](https://github.com/nodkz/mongodb-memory-server/issues/281)) ([054cbe5](https://github.com/nodkz/mongodb-memory-server/commit/054cbe5)), closes [#280](https://github.com/nodkz/mongodb-memory-server/issues/280)





## [6.3.2](https://github.com/nodkz/mongodb-memory-server/compare/v6.3.1...v6.3.2) (2020-03-03)


### Bug Fixes

* **MongoBinaryDownload:** handle Status Codes other than 200 ([#273](https://github.com/nodkz/mongodb-memory-server/issues/273)) ([3d68233](https://github.com/nodkz/mongodb-memory-server/commit/3d68233)), closes [#226](https://github.com/nodkz/mongodb-memory-server/issues/226)





## [6.3.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.3.0...v6.3.1) (2020-02-28)

**Note:** Version bump only for package lerna-monorepo





# [6.3.0](https://github.com/nodkz/mongodb-memory-server/compare/v6.2.4...v6.3.0) (2020-02-28)


### Features

* rewrite Logging via debug package under `DEBUG=MongoMS:*` key ([#270](https://github.com/nodkz/mongodb-memory-server/issues/270)) ([f2885c0](https://github.com/nodkz/mongodb-memory-server/commit/f2885c0))





## [6.2.4](https://github.com/nodkz/mongodb-memory-server/compare/v6.2.3...v6.2.4) (2020-01-27)


### Bug Fixes

* add @types/tmp to dependencies ([#266](https://github.com/nodkz/mongodb-memory-server/issues/266)) ([ffbf1ea](https://github.com/nodkz/mongodb-memory-server/commit/ffbf1ea))





## [6.2.3](https://github.com/nodkz/mongodb-memory-server/compare/v6.2.2...v6.2.3) (2020-01-20)


### Bug Fixes

* change import for `tmp` package ([4477b9b](https://github.com/nodkz/mongodb-memory-server/commit/4477b9b))





## [6.2.2](https://github.com/nodkz/mongodb-memory-server/compare/v6.2.1...v6.2.2) (2020-01-15)


### Bug Fixes

* add TSDoc to MongoInstance; code refactoring ([#261](https://github.com/nodkz/mongodb-memory-server/issues/261)) ([6865520](https://github.com/nodkz/mongodb-memory-server/commit/6865520))





## [6.2.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.2.0...v6.2.1) (2019-12-30)


### Bug Fixes

* **ArchLinux:** binary not downloaded when no release file is found. Plus other code fixes and cleanups (tnx [@hasezoey](https://github.com/hasezoey)) ([8723187](https://github.com/nodkz/mongodb-memory-server/commit/8723187)), closes [#248](https://github.com/nodkz/mongodb-memory-server/issues/248) [#255](https://github.com/nodkz/mongodb-memory-server/issues/255)





# [6.2.0](https://github.com/nodkz/mongodb-memory-server/compare/v6.1.1...v6.2.0) (2019-12-26)


### Features

* add static async `MongoMemoryServer.create()`; improve Example code & add TSDoc (tnx [@hasezoey](https://github.com/hasezoey)) ([a2b0fc4](https://github.com/nodkz/mongodb-memory-server/commit/a2b0fc4)), closes [#211](https://github.com/nodkz/mongodb-memory-server/issues/211) [/github.com/nodkz/mongodb-memory-server/issues/184#issuecomment-568782496](https://github.com//github.com/nodkz/mongodb-memory-server/issues/184/issues/issuecomment-568782496)





## [6.1.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.1.0...v6.1.1) (2019-12-20)

**Note:** Version bump only for package lerna-monorepo





# [6.1.0](https://github.com/nodkz/mongodb-memory-server/compare/v6.0.2...v6.1.0) (2019-12-20)


### Features

* add support for Linux Mint (tnx [@hasezoey](https://github.com/hasezoey)) ([92a9381](https://github.com/nodkz/mongodb-memory-server/commit/92a9381))





## [6.0.2](https://github.com/nodkz/mongodb-memory-server/compare/v6.0.1...v6.0.2) (2019-12-03)


### Bug Fixes

* compatibility with debian 10 (works for Mongo >= v4.2.1) ([837d98e](https://github.com/nodkz/mongodb-memory-server/commit/837d98e))





## [6.0.1](https://github.com/nodkz/mongodb-memory-server/compare/v6.0.0...v6.0.1) (2019-10-22)


### Bug Fixes

* **MongoMemoryServer:** add `?` character to the connection string (uri) by default (hotfix for v6.0.0) ([505b7c2](https://github.com/nodkz/mongodb-memory-server/commit/505b7c2))





# [6.0.0](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.11...v6.0.0) (2019-10-22)


### Bug Fixes

* **MongoMemoryReplSet:** `getConnectionString()` now returns uri with `?replicaSet=` option. ([401441c](https://github.com/nodkz/mongodb-memory-server/commit/401441c))


### chore

* update cross-spawn ([c99fda8](https://github.com/nodkz/mongodb-memory-server/commit/c99fda8))


### BREAKING CHANGES

* drop support for Node.js < 8
* **MongoMemoryReplSet:** `getConnectionString()` now returns uri with `?replicaSet=` option.





## [5.2.11](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.10...v5.2.11) (2019-10-22)


### Bug Fixes

* upgrade https-proxy-agent till 3.0.0 ([c554faa](https://github.com/nodkz/mongodb-memory-server/commit/c554faa))





## [5.2.10](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.9...v5.2.10) (2019-10-22)


### Bug Fixes

* **ReplSet:** add HACK for "Maximum call stack size exceeded" in MongoClient topology ([470f094](https://github.com/nodkz/mongodb-memory-server/commit/470f094)), closes [#221](https://github.com/nodkz/mongodb-memory-server/issues/221)





## [5.2.9](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.8...v5.2.9) (2019-10-22)


### Bug Fixes

* upgrade `https-proxy-agent` package due high sev. vulnerability ([f44ebe4](https://github.com/nodkz/mongodb-memory-server/commit/f44ebe4))





## [5.2.8](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.7...v5.2.8) (2019-10-09)


### Bug Fixes

* revert add debian v10 downloads ([ffa95cd](https://github.com/nodkz/mongodb-memory-server/commit/ffa95cd))





## [5.2.7](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.6...v5.2.7) (2019-10-08)


### Bug Fixes

* add debian v10 downloads ([012d652](https://github.com/nodkz/mongodb-memory-server/commit/012d652)), closes [#204](https://github.com/nodkz/mongodb-memory-server/issues/204)





## [5.2.6](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.5...v5.2.6) (2019-09-30)


### Bug Fixes

* using "useUnifiedTopology" to avoid deprecation msg ([00e022d](https://github.com/nodkz/mongodb-memory-server/commit/00e022d))





## [5.2.5](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.4...v5.2.5) (2019-09-23)


### Bug Fixes

* **ReplSet:** typescript definitions ReplSetOpts.dbName is optional ([d1e4b53](https://github.com/nodkz/mongodb-memory-server/commit/d1e4b53))





## [5.2.4](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.3...v5.2.4) (2019-09-23)

**Note:** Version bump only for package lerna-monorepo





## [5.2.3](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.2...v5.2.3) (2019-09-11)


### Bug Fixes

* clearTimeout when waiting for primary ([08aa26f](https://github.com/nodkz/mongodb-memory-server/commit/08aa26f))





## [5.2.2](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.1...v5.2.2) (2019-09-09)


### Bug Fixes

* download url exception for win32 & v4.2.0 ([bf8ff9e](https://github.com/nodkz/mongodb-memory-server/commit/bf8ff9e))





## [5.2.1](https://github.com/nodkz/mongodb-memory-server/compare/v5.2.0...v5.2.1) (2019-09-04)


### Bug Fixes

* URL for macos change for 4.2.0 ([0452cbd](https://github.com/nodkz/mongodb-memory-server/commit/0452cbd))





# [5.2.0](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.10...v5.2.0) (2019-08-10)


### Features

* add MONGOMS_DOWNLOAD_URL env variable for downloading binary from url ([8b31ff5](https://github.com/nodkz/mongodb-memory-server/commit/8b31ff5))





## [5.1.10](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.9...v5.1.10) (2019-08-02)


### Bug Fixes

* **ReplicaSet:** detect primary from stdout instead of admin call ([c081ece](https://github.com/nodkz/mongodb-memory-server/commit/c081ece))





## [5.1.9](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.8...v5.1.9) (2019-07-24)


### Bug Fixes

* add fail message when mongod cannot find CURL_OPENSSL_3 ([2ba4ae5](https://github.com/nodkz/mongodb-memory-server/commit/2ba4ae5))
* avoid infinite loop when waiting Primary ([b19c4bf](https://github.com/nodkz/mongodb-memory-server/commit/b19c4bf))





## [5.1.8](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.7...v5.1.8) (2019-07-23)


### Bug Fixes

* wait until primary is transitioned from secondary for replicaSet ([596fed8](https://github.com/nodkz/mongodb-memory-server/commit/596fed8))





## [5.1.7](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.6...v5.1.7) (2019-07-19)

**Note:** Version bump only for package lerna-monorepo





## [5.1.6](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.5...v5.1.6) (2019-07-16)


### Bug Fixes

* global-3.4, global-3.6, global-4.0 now properly set default mongod version ([5fc1652](https://github.com/nodkz/mongodb-memory-server/commit/5fc1652))





## [5.1.5](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.4...v5.1.5) (2019-06-18)


### Bug Fixes

* re-initialise configuration using INIT_CWD in postinstall.js ([9641bf4](https://github.com/nodkz/mongodb-memory-server/commit/9641bf4))





## [5.1.4](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.3...v5.1.4) (2019-06-11)


### Bug Fixes

* simplify postinstall path check for Windows' users ([0b010bf](https://github.com/nodkz/mongodb-memory-server/commit/0b010bf))





## [5.1.3](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.2...v5.1.3) (2019-06-06)


### Bug Fixes

* resolve to config from closest package.json ([34b6e27](https://github.com/nodkz/mongodb-memory-server/commit/34b6e27))
* use cross-spawn to help with Windows issues ([efad669](https://github.com/nodkz/mongodb-memory-server/commit/efad669))





## [5.1.2](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.1...v5.1.2) (2019-05-16)

**Note:** Version bump only for package lerna-monorepo





## [5.1.1](https://github.com/nodkz/mongodb-memory-server/compare/v5.1.0...v5.1.1) (2019-05-09)


### Bug Fixes

* fallback on ubuntu 18 binaries for newest versions ([#183](https://github.com/nodkz/mongodb-memory-server/issues/183)) ([d5a1bfc](https://github.com/nodkz/mongodb-memory-server/commit/d5a1bfc))





# [5.1.0](https://github.com/nodkz/mongodb-memory-server/compare/v5.0.4...v5.1.0) (2019-04-21)


### Features

* configure installation from package.json ([c8dbbb9](https://github.com/nodkz/mongodb-memory-server/commit/c8dbbb9))





## [5.0.4](https://github.com/nodkz/mongodb-memory-server/compare/v5.0.3...v5.0.4) (2019-04-15)

**Note:** Version bump only for package lerna-monorepo





## [5.0.3](https://github.com/nodkz/mongodb-memory-server/compare/v5.0.2...v5.0.3) (2019-04-14)


### Bug Fixes

* **downloadUrl:** elementaryOS support fixed for versions up to 0.3 ([232c33f](https://github.com/nodkz/mongodb-memory-server/commit/232c33f))





## [5.0.2](https://github.com/nodkz/mongodb-memory-server/compare/v5.0.1...v5.0.2) (2019-04-11)


### Bug Fixes

* **MongoBinary:** unwrap deeply nested cache directory ([dcb9c9c](https://github.com/nodkz/mongodb-memory-server/commit/dcb9c9c)), closes [#168](https://github.com/nodkz/mongodb-memory-server/issues/168)





## [5.0.1](https://github.com/nodkz/mongodb-memory-server/compare/v5.0.0...v5.0.1) (2019-04-10)

**Note:** Version bump only for package lerna-monorepo





# [5.0.0](https://github.com/nodkz/mongodb-memory-server/compare/v4.2.2...v5.0.0) (2019-04-10)


### Code Refactoring

* using Lerna multiple packages ([e80e0f2](https://github.com/nodkz/mongodb-memory-server/commit/e80e0f2)), closes [/github.com/nodkz/mongodb-memory-server/issues/159#issuecomment-474398550](https://github.com//github.com/nodkz/mongodb-memory-server/issues/159/issues/issuecomment-474398550)


### Features

* add additional packages with specific default configs ([9cca8f6](https://github.com/nodkz/mongodb-memory-server/commit/9cca8f6))


### BREAKING CHANGES

* Remove `MomgoMemoryServer.getInstanceData()` method. Use `MomgoMemoryServer.ensureInstance()` instead.





# Change Log

## 0.0.0-semantically-released (May 11, 2017)

This package publishing automated by [semantic-release](https://github.com/semantic-release/semantic-release).
[Changelog](https://github.com/nodkz/mongodb-memory-server/releases) is generated automatically and can be found here: https://github.com/nodkz/mongodb-memory-server/releases

## 0.0.1 (May 11, 2017)

- First commit
