# Changelog

## [5.1.0](https://github.com/rolehippie/loki/compare/v5.0.0...v5.1.0) (2026-01-05)


### Features

* **minor:** update dependency community.general to >=12.2.0,<12.3.0 ([#90](https://github.com/rolehippie/loki/issues/90)) ([a1e989c](https://github.com/rolehippie/loki/commit/a1e989cd455afb340757f85e4b0c740487f7192d))

## [5.0.0](https://github.com/rolehippie/loki/compare/v4.2.1...v5.0.0) (2025-12-17)


### ⚠ BREAKING CHANGES

* replace boltdb shipper by tsdb
* restructure config and make it full customizable

### Features

* replace boltdb shipper by tsdb ([9432d98](https://github.com/rolehippie/loki/commit/9432d98e4f222cca2dbe7242f6ba188ccb231eac))
* restructure config and make it full customizable ([bd0f97b](https://github.com/rolehippie/loki/commit/bd0f97b67e23ce6acc900439963a8abda560c365))


### Bugfixes

* drop healthcheck, no wget on loki image available ([462b047](https://github.com/rolehippie/loki/commit/462b0478724c5ef368face72b6080dbf45d56684))

## [4.2.1](https://github.com/rolehippie/loki/compare/v4.2.0...v4.2.1) (2025-12-15)


### Bugfixes

* **patch:** update dependency grafana/loki to v3.6.3 ([#87](https://github.com/rolehippie/loki/issues/87)) ([1a89666](https://github.com/rolehippie/loki/commit/1a89666f1ceff27d18b5506d2d9f5f7565274b47))

## [4.2.0](https://github.com/rolehippie/loki/compare/v4.1.1...v4.2.0) (2025-12-08)


### Features

* **minor:** update dependency community.general to >=12.1.0,<12.2.0 ([#82](https://github.com/rolehippie/loki/issues/82)) ([3bb6e81](https://github.com/rolehippie/loki/commit/3bb6e8192050c4c66c64e8b1f67bec746b5b73cb))

## [4.1.1](https://github.com/rolehippie/loki/compare/v4.1.0...v4.1.1) (2025-12-01)


### Bugfixes

* **patch:** update dependency grafana/loki to v3.6.2 ([#81](https://github.com/rolehippie/loki/issues/81)) ([14714fd](https://github.com/rolehippie/loki/commit/14714fda2e3cffccc8fbaa202db764a6fd094252))

## [4.1.0](https://github.com/rolehippie/loki/compare/v4.0.0...v4.1.0) (2025-11-24)


### Features

* **minor:** update dependency grafana/loki to v3.6.0 ([#75](https://github.com/rolehippie/loki/issues/75)) ([3d139ab](https://github.com/rolehippie/loki/commit/3d139abca7f581ad87b3201ea5ff64f435ae6161))


### Bugfixes

* **patch:** update dependency grafana/loki to v3.6.1 ([#78](https://github.com/rolehippie/loki/issues/78)) ([f904ee5](https://github.com/rolehippie/loki/commit/f904ee5ef364f8a0090c53adbcfc205a964806dc))

## [4.0.0](https://github.com/rolehippie/loki/compare/v3.12.3...v4.0.0) (2025-11-17)


### Features

* **major:** update dependency community.docker to v5 ([#68](https://github.com/rolehippie/loki/issues/68)) ([1a42b43](https://github.com/rolehippie/loki/commit/1a42b43a880ac4d0656f75b08c28c0d45ad5d280))
* **major:** update dependency community.general to v12 ([#69](https://github.com/rolehippie/loki/issues/69)) ([1671cde](https://github.com/rolehippie/loki/commit/1671cdebcdb399f0517e88c16a380df0d609d3ce))
* **minor:** update dependency oauth2-proxy/oauth2-proxy to v7.13.0 ([#71](https://github.com/rolehippie/loki/issues/71)) ([96b8cfe](https://github.com/rolehippie/loki/commit/96b8cfed0c3a7e49f1a21caafad629a59ce92846))


### Bugfixes

* **patch:** update dependency grafana/loki to v3.5.8 ([#70](https://github.com/rolehippie/loki/issues/70)) ([1078cde](https://github.com/rolehippie/loki/commit/1078cde9b83f4662dd0f7e781b59f7187c5671d5))

## [3.12.3](https://github.com/rolehippie/loki/compare/v3.12.2...v3.12.3) (2025-10-20)


### Bugfixes

* **patch:** update dependency grafana/loki to v3.5.7 ([#65](https://github.com/rolehippie/loki/issues/65)) ([2869202](https://github.com/rolehippie/loki/commit/2869202441d143c4f62b044333346f7bc4001ab1))

## [3.12.2](https://github.com/rolehippie/loki/compare/v3.12.1...v3.12.2) (2025-10-13)


### Bugfixes

* **patch:** update dependency grafana/loki to v3.5.6 ([#63](https://github.com/rolehippie/loki/issues/63)) ([b319bed](https://github.com/rolehippie/loki/commit/b319bedd4d7c629a06b238e41c3a3b314d015233))

## [3.12.1](https://github.com/rolehippie/loki/compare/v3.12.0...v3.12.1) (2025-09-22)


### Bugfixes

* add noble to supported versions ([4abdaf3](https://github.com/rolehippie/loki/commit/4abdaf353c144d4f557a662932136efe37a7fdbf))

## [3.12.0](https://github.com/rolehippie/loki/compare/v3.11.1...v3.12.0) (2025-09-17)


### Features

* apply new repo structure and update linting ([6d6b06a](https://github.com/rolehippie/loki/commit/6d6b06a3d934b9d790eb19bd15a670a6a34f8124))


### Bugfixes

* define requirements only once ([ae5ed91](https://github.com/rolehippie/loki/commit/ae5ed91ccd0b5aa4d921341f21d26943e3859db9))
* **deps:** update dependency grafana/loki to v3.5.5 ([#58](https://github.com/rolehippie/loki/issues/58)) ([15fd88e](https://github.com/rolehippie/loki/commit/15fd88e940bfe453ac02b08fb5e221c8ecc09a8a))

## [3.11.1](https://github.com/rolehippie/loki/compare/v3.11.0...v3.11.1) (2025-09-08)


### Bugfixes

* **deps:** update dependency grafana/loki to v3.5.4 ([#57](https://github.com/rolehippie/loki/issues/57)) ([2d1f638](https://github.com/rolehippie/loki/commit/2d1f6384d712a74265d7034831bc681e52bf372e))

## [3.11.0](https://github.com/rolehippie/loki/compare/v3.10.0...v3.11.0) (2025-08-19)


### Features

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.12.0 ([#55](https://github.com/rolehippie/loki/issues/55)) ([c30ed0c](https://github.com/rolehippie/loki/commit/c30ed0c9026bfcad4947b89165c05bd72d5cc643))

## [3.10.0](https://github.com/rolehippie/loki/compare/v3.9.1...v3.10.0) (2025-08-11)


### Features

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.11.0 ([#53](https://github.com/rolehippie/loki/issues/53)) ([e7c12ff](https://github.com/rolehippie/loki/commit/e7c12ff75103ab58123bf9a61b13496a82e5b89a))

## [3.9.1](https://github.com/rolehippie/loki/compare/v3.9.0...v3.9.1) (2025-07-28)


### Bugfixes

* **deps:** update dependency grafana/loki to v3.5.3 ([#52](https://github.com/rolehippie/loki/issues/52)) ([6620ceb](https://github.com/rolehippie/loki/commit/6620cebae4a27505dbe071ed06ba9838f2c22a55))

## [3.9.0](https://github.com/rolehippie/loki/compare/v3.8.1...v3.9.0) (2025-07-21)


### Features

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.10.0 ([#51](https://github.com/rolehippie/loki/issues/51)) ([39703c4](https://github.com/rolehippie/loki/commit/39703c4a4bc46dff0c886d7d338a584250996dbb))


### Bugfixes

* **deps:** update dependency grafana/loki to v3.5.2 ([#50](https://github.com/rolehippie/loki/issues/50)) ([7ec8ba3](https://github.com/rolehippie/loki/commit/7ec8ba30dff3666e56ffed38468c14b38939c5b5))

## [3.8.1](https://github.com/rolehippie/loki/compare/v3.8.0...v3.8.1) (2025-05-26)


### Bugfixes

* **deps:** update dependency grafana/loki to v3.5.1 ([#49](https://github.com/rolehippie/loki/issues/49)) ([ebe38c0](https://github.com/rolehippie/loki/commit/ebe38c06acebddc2a7c15fe4cba745c4c2e71def))

## [3.8.0](https://github.com/rolehippie/loki/compare/v3.7.0...v3.8.0) (2025-05-05)


### Features

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.9.0 ([#48](https://github.com/rolehippie/loki/issues/48)) ([fc41acf](https://github.com/rolehippie/loki/commit/fc41acfe6d17c003209cc09e76e00e52c6ab9042))

## [3.7.0](https://github.com/rolehippie/loki/compare/v3.6.2...v3.7.0) (2025-04-28)


### Features

* **deps:** update dependency grafana/loki to v3.5.0 ([#47](https://github.com/rolehippie/loki/issues/47)) ([28755d2](https://github.com/rolehippie/loki/commit/28755d2d7728f2cee8261fe7637384dbe4d4b82d))

## [3.6.2](https://github.com/rolehippie/loki/compare/v3.6.1...v3.6.2) (2025-04-07)


### Bugfixes

* **deps:** update dependency grafana/loki to v3.4.3 ([#46](https://github.com/rolehippie/loki/issues/46)) ([e752bf6](https://github.com/rolehippie/loki/commit/e752bf68a47c1417bd97a7a9988770e53383184b))

## [3.6.1](https://github.com/rolehippie/loki/compare/v3.6.0...v3.6.1) (2025-03-31)


### Bugfixes

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.8.2 ([#45](https://github.com/rolehippie/loki/issues/45)) ([fb793af](https://github.com/rolehippie/loki/commit/fb793af08567e936c267cd194fcb0215c3870e93))

## [3.6.0](https://github.com/rolehippie/loki/compare/v3.5.0...v3.6.0) (2025-02-17)


### Features

* **deps:** update dependency grafana/loki to v3.4.0 ([#41](https://github.com/rolehippie/loki/issues/41)) ([7d59caa](https://github.com/rolehippie/loki/commit/7d59caacdd398d105abf6bc7701c0755c326a70b))


### Bugfixes

* **deps:** update dependency grafana/loki to v3.4.1 ([#42](https://github.com/rolehippie/loki/issues/42)) ([f00f330](https://github.com/rolehippie/loki/commit/f00f330d936f0c58f7926f9f57cfc3c10db8a206))
* **deps:** update dependency grafana/loki to v3.4.2 ([#43](https://github.com/rolehippie/loki/issues/43)) ([b2daef5](https://github.com/rolehippie/loki/commit/b2daef55e3636a91936038563c6be0e1f6ab0f97))

## [3.5.0](https://github.com/rolehippie/loki/compare/v3.4.2...v3.5.0) (2025-01-20)


### Features

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.8.0 ([#39](https://github.com/rolehippie/loki/issues/39)) ([1967887](https://github.com/rolehippie/loki/commit/19678878bec1b8fec1b430d005a431fef4f46b48))


### Bugfixes

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.8.1 ([#40](https://github.com/rolehippie/loki/issues/40)) ([11fff8a](https://github.com/rolehippie/loki/commit/11fff8a0dc49691acf55c138fda167b260ead6b6))

## [3.4.2](https://github.com/rolehippie/loki/compare/v3.4.1...v3.4.2) (2024-12-23)


### Bugfixes

* **deps:** update dependency grafana/loki to v3.3.2 ([#38](https://github.com/rolehippie/loki/issues/38)) ([1443ea4](https://github.com/rolehippie/loki/commit/1443ea4ff88e7b87c21691ac22a62de4e67010ec))

## [3.4.1](https://github.com/rolehippie/loki/compare/v3.4.0...v3.4.1) (2024-12-09)


### Bugfixes

* **deps:** update dependency grafana/loki to v3.3.1 ([#37](https://github.com/rolehippie/loki/issues/37)) ([7053d45](https://github.com/rolehippie/loki/commit/7053d4575a890b57af7e4dc3cb7f75310db98b96))

## [3.4.0](https://github.com/rolehippie/loki/compare/v3.3.2...v3.4.0) (2024-11-25)


### Features

* **deps:** update dependency grafana/loki to v3.3.0 ([#34](https://github.com/rolehippie/loki/issues/34)) ([b6c4f08](https://github.com/rolehippie/loki/commit/b6c4f083987a9baef99882e6034f3fe9b3d22938))

## [3.3.2](https://github.com/rolehippie/loki/compare/v3.3.1...v3.3.2) (2024-10-28)


### Bugfixes

* **deps:** update dependency grafana/loki to v3.2.1 ([4b84fd8](https://github.com/rolehippie/loki/commit/4b84fd802d9c714630b95394e4e99a71b97e36d1))

## [3.3.1](https://github.com/rolehippie/loki/compare/v3.3.0...v3.3.1) (2024-10-14)


### Bugfixes

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.7.1 ([0e4561e](https://github.com/rolehippie/loki/commit/0e4561e5a3fe7237ab0b5349bb3b5305d0d6bf12))

## [3.3.0](https://github.com/rolehippie/loki/compare/v3.2.0...v3.3.0) (2024-10-07)


### Features

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.7.0 ([d5c2ee3](https://github.com/rolehippie/loki/commit/d5c2ee330cdae41d90a2a202a1db58c3dcd4ad9c))

## [3.2.0](https://github.com/rolehippie/loki/compare/v3.1.1...v3.2.0) (2024-09-23)


### Features

* **deps:** update dependency grafana/loki to v3.2.0 ([1af06c2](https://github.com/rolehippie/loki/commit/1af06c232915594c02aa19290d76268fe10485b3))

## [3.1.1](https://github.com/rolehippie/loki/compare/v3.1.0...v3.1.1) (2024-08-19)


### Bugfixes

* **deps:** update dependency grafana/loki to v3.1.1 ([2b66d86](https://github.com/rolehippie/loki/commit/2b66d86bf02e475d3e037e6eaeb32a38a620bd6d))

## [3.1.0](https://github.com/rolehippie/loki/compare/v3.0.0...v3.1.0) (2024-07-08)


### Features

* **deps:** update dependency grafana/loki to v3.1.0 ([302df00](https://github.com/rolehippie/loki/commit/302df0081a505874f40b2c3e20c5ad1efeebcebc))

## [3.0.0](https://github.com/rolehippie/loki/compare/v2.1.1...v3.0.0) (2024-04-22)


### Features

* **deps:** update dependency grafana/loki to v3 ([99235c8](https://github.com/rolehippie/loki/commit/99235c88540f6056ca819b19d67fa5c37b9fd97e))


### Bugfixes

* **deps:** update dependency grafana/loki to v2.9.7 ([b11474f](https://github.com/rolehippie/loki/commit/b11474fa349e64ed594d72b8c3667bc7640a9931))

## [2.1.1](https://github.com/rolehippie/loki/compare/v2.1.0...v2.1.1) (2024-03-25)


### Bugfixes

* **deps:** update dependency grafana/loki to v2.9.6 ([c9bc93c](https://github.com/rolehippie/loki/commit/c9bc93c76481a30c3d7f107b6d0e43b9b0754e26))

## [2.1.0](https://github.com/rolehippie/loki/compare/v2.0.0...v2.1.0) (2024-03-18)


### Features

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.6.0 ([857f0df](https://github.com/rolehippie/loki/commit/857f0df7734c0bd7ecd89c76b40078332cb1fed0))


### Bugfixes

* **deps:** update dependency grafana/loki to v2.9.5 ([ee88266](https://github.com/rolehippie/loki/commit/ee88266d16bd8a6f88314ec34a5ffe9eb5da36e5))

## [2.0.0](https://github.com/rolehippie/loki/compare/v1.5.5...v2.0.0) (2024-02-12)


### Features

* drop support for ubuntu 18.04 ([116f42c](https://github.com/rolehippie/loki/commit/116f42cc1d724a7db4f2a92c8906b844c4ac220e))
* used full qualified collection names ([9b2e062](https://github.com/rolehippie/loki/commit/9b2e0621ef3c14716cc152d8b7435d2bab62cb3d))


### Bugfixes

* remove meta requirements and document used collections ([2aa8b31](https://github.com/rolehippie/loki/commit/2aa8b31067883973c1ed58dd442907a76ade850b))

## [1.5.5](https://github.com/rolehippie/loki/compare/v1.5.4...v1.5.5) (2024-01-29)


### Bugfixes

* **deps:** update dependency grafana/loki to v2.9.4 ([f222fdd](https://github.com/rolehippie/loki/commit/f222fdd9bb416474c07afe0fa97741dd287da17c))

## [1.5.4](https://github.com/rolehippie/loki/compare/v1.5.3...v1.5.4) (2023-12-18)


### Bugfixes

* **deps:** update dependency grafana/loki to v2.9.3 ([e88dc6c](https://github.com/rolehippie/loki/commit/e88dc6c15af4df3f610770250f8903b228d04820))

## [1.5.3](https://github.com/rolehippie/loki/compare/v1.5.2...v1.5.3) (2023-10-23)


### Bugfixes

* **deps:** update dependency grafana/loki to v2.9.2 ([61c980d](https://github.com/rolehippie/loki/commit/61c980d6780171b69dbf5331d18ea1cbada98b0b))

## [1.5.2](https://github.com/rolehippie/loki/compare/v1.5.1...v1.5.2) (2023-09-25)


### Bugfixes

* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.5.1 ([6e2be9b](https://github.com/rolehippie/loki/commit/6e2be9bbf2c91dc4f56b8eb7c812902d9c455ae6))

## [1.5.1](https://github.com/rolehippie/loki/compare/v1.5.0...v1.5.1) (2023-09-18)


### Bugfixes

* **deps:** update dependency grafana/loki to v2.9.1 ([8fb7dda](https://github.com/rolehippie/loki/commit/8fb7ddaa17752c08480155038125c159f8c6a1cc))

## [1.5.0](https://github.com/rolehippie/loki/compare/v1.4.0...v1.5.0) (2023-09-11)


### Features

* **deps:** update dependency grafana/loki to v2.9.0 ([fb22c63](https://github.com/rolehippie/loki/commit/fb22c63158b507e37325f04792dd64c9ab45512b))
* **deps:** update dependency oauth2-proxy/oauth2-proxy to v7.5.0 ([4932f82](https://github.com/rolehippie/loki/commit/4932f826c525b6bd4b8d707c55f01b995d864d32))

## [1.4.0](https://github.com/rolehippie/loki/compare/v1.3.0...v1.4.0) (2023-08-31)


### Features

* add more options for entirely flexible config ([902a64d](https://github.com/rolehippie/loki/commit/902a64d438044d01cb2a3e3af2edaf2ce301cef5))
* add options for the ingester config ([8b06934](https://github.com/rolehippie/loki/commit/8b069349a1431019e41539252ae3918a35ca33f5))

## [1.3.0](https://github.com/rolehippie/loki/compare/v1.2.2...v1.3.0) (2023-08-24)


### Features

* add optional defaults for cpu and memory limit ([3dca09d](https://github.com/rolehippie/loki/commit/3dca09d04e53e2613a71123cd0673c9f342ad52b))

## [1.2.2](https://github.com/rolehippie/loki/compare/v1.2.1...v1.2.2) (2023-08-14)


### Bugfixes

* **deps:** update dependency grafana/loki to v2.8.4 ([2f2c3a2](https://github.com/rolehippie/loki/commit/2f2c3a25cfef5f4a9f4c2a718776ac9346ad3192))

## [1.2.1](https://github.com/rolehippie/loki/compare/v1.2.0...v1.2.1) (2023-07-24)


### Bugfixes

* **deps:** update dependency grafana/loki to v2.8.3 ([c69c231](https://github.com/rolehippie/loki/commit/c69c231c5582d7475996e56d55f7005c2953b1f1))

## [1.2.0](https://github.com/rolehippie/loki/compare/v1.1.0...v1.2.0) (2023-07-14)


### Features

* add defaults for limits config ([03f33b1](https://github.com/rolehippie/loki/commit/03f33b103e611d304c24773cb1b4514854e70468))

## [1.1.0](https://github.com/rolehippie/loki/compare/v1.0.0...v1.1.0) (2023-07-06)


### Features

* add options to disable access and auth logging for oauth2 proxy ([1504267](https://github.com/rolehippie/loki/commit/15042678568d8e0a2b4d5e965721ce8fa3d3803c))
* create docker network ([0b40c73](https://github.com/rolehippie/loki/commit/0b40c73c1011d4b88dab59ea3639cc184616c734))

## 1.0.0 (2023-07-05)


### Features

* initial commit ([8e9e80e](https://github.com/rolehippie/loki/commit/8e9e80ecb9ba3f841c6b2244ba069860dd715868))
* rename all files to yml ([5082589](https://github.com/rolehippie/loki/commit/5082589c40e12a80a5750a1b21ea5c4d78553e84))
