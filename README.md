# Slashing Protection Interchange Tests (EIP-3076)

Tests for EIP-3076:

https://eips.ethereum.org/EIPS/eip-3076

Discussion:

https://ethereum-magicians.org/t/eip-3076-validator-client-interchange-format-slashing-protection/4883

## How to run

Each test directory contains an interchange file and some extra data about how to test it.

For example:

```json
{
  "name": "single_validator_genesis_attestation",
  "genesis_validators_root": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "steps": [
    {
      "should_succeed": true,
      "contains_slashable_data": false,
      "interchange": {
        "metadata": {
          "interchange_format_version": "5",
          "genesis_validators_root": "0x0000000000000000000000000000000000000000000000000000000000000000"
        },
        "data": [
          {
            "pubkey": "0x9498619d44f1c5df1ba7950041ed069244e7cb5ec46783c6c87e47cd6761e7c99b7ef20e2fd3102575dcf961e73f3d22c1d055e47ae946b0e6cd3c9e08468576954d156ce4935accc31833d10d0796aa47d2a35d95d6c999179f60eca007c20435b87bf3dbd027f7b21f4fda4fcade3dd7f0d9342a64bf0ab659fa9306e57ff1eab0aa5a5c6415d9c081fb4326146e5f445b724d9283923ee81b0d866ffb2ea4474741862d8eb5a223d0ff0db047efcc4d39859fa1abaa4b65eefa1ff0538af4a3e43875bdf20f153eab213189d6330fcf8f3f261ff331db4a62694aad257dd412bdf7cb831cdd8b00ab1391ba5930a4090616ae3023b165723ee7b57d85a45de413de1cfa2b61d4b6cb2e2137d983b5b5fef63fa6ca2699cd3ad2ce3d3c0fcc6cd6b87ebf9417aef7124292314cfecd6861896f21de56c2aba6dfc47f56a0f41cecd64cd82e11b77acdcac060cdf676ffd5e326345f4fa75d8315bcb6096d4643234df5bd5bc541fc5bcd7908a1c651425984032866749f76e31b0531dd2841c1d7ecfb60d7f4c9ed5d71d11823633207726d37584928e64fb7c4490efc6495bdda2ebd689f068cbe02b7acf597b1cfd586ea90254098d51783e8eee7a319c613a65f19e4a55bd05b6c845822475f163a74099a30283028b321e0e1d6526699bf5540ff5c5ff35eca1188620256e5fddad71a515f146f11c8d690990d2567de9bc0d7e056e9918e6fbef423486e7b47684807fd5c408eb18c010d7de6ad297e2cb5a2072f117b0c38ec4107f3d686c55a3d73b035c2f1b55144fa785f1d6818061465373cf5cfa67097d533bfa5324da08f145259215202964ea8d5aad2a2cbf058e7b7ba167151092380b12eba0248476263af1f62fa5173f865273baf2b9714d052368bd782595df6dbf61ffb3d15dde65b2cd1360db2bfa1a2279f7ca59f9c83041f4d6ce3c4b39568c21439443f2969eea67ec8d9c46474038b24a0f76059fc501e379e6e82894a29501de9f0f462a15880bc8e4e3a7d7a5bb51b72549866a69b6ac4fcb1d1a03d13ab321057f69098c927c2c6e3ad55791f204b704f79c75ab7874b22dc99bd08316783a1bf0996af9465840f06c328bae6836f93e3065e363273c5582e8710dc85fc7424d777f067d22f40d0febcf9c1ad28a6b02e33bdec72834c506b6074d89726e049678b566563ef23a179d7ec711f88d49c98669f494f2bf4a199c957ba2a1e97d8d322e7f16fe4c5c4b98588803e8e31dad9d3b904143e91cb33ce62d8d7bb17e1a4b718165632c1ae4663c75159991869b0ef68f8bcd3bc40b214ebdf98e1e22a80d34ffc5b7ad3694a5bed6b16cdf3b7af86f3c335201447ce1d265f5dceecf30709328e3c6b12b9530ef60cb4386ff9285b970903f85b12914288248cb9a15139049006551e97406e89c579b61a40914ff5eb12a1e97a60a77afec6d619ba00474dba9042e8d5328794edda92020a7b5b597b57831ae3cbee183fe9ef1aae504980d266054b99496c144c85e21b9a4d751e613a50c305d84a0aea099cecd5c7c5eac3d1d86c9048d781ce2d0b20f7aadd83bfa684fe02ff6c84cad6b75c78c824e998af8c4061609c840caa8c0366841570e735f6e55582e474e7f013270acd200a0834ad7d8e98b8cf159e0774aad3e84ecda22a079f59da0a96a0e4041d56a566eed22c63017ba422bdb96724c4257fa926cd3d17ad803d09b851cc662d544db5a843c31df7442c7c4cb752890da39ad2574f27b655556c4082322b4cd2067d30478fa9ac8688ce7c315988f50dad984e985abf8dbd37a1c74f42b5a5d1f646eb8c0d1f2882a4e704f92169fe06655f2a208f56436691bc8ea2ea460b20f590bc5e05e75ef02b087c8e19fddd898b8869fa542a1bbc08abd76245cd72efcb6df1c0d2d5fc21815080d204ff49f56ad50e5a0bbb9d111613efe1c60ee44fe64ccb492bda1d03e10f161e09003f8ecaa00961b8ce37e7113d3f626458b60409434778241158a5484487ed2c897cf21d2258146947a7924791680ac4398c99e58880928644012550fffc4ec96e347f00db8b3950b22b5d1da80581663377f08f10236a302e4901ab1c742853ce56a16f9ce3b9c258149f8429259da7202301d9c77d992fb2f4f7f80551197c323d469d7d9ec54094c6dc9fb385554769538e48be199bffa8f6d31ef498c0763220200b176fa63ce11458fdc44496890ee7031c17b39cbdcfe22fa6792d98261dc22139a4b336f3090301a2ab9d4d808b45b28a3ec529db7baa7a0d30f4e9f65203663be8ff204090064bba69d449e5ed5ded88e4d70e34b26f133815c07d2e3660503458b5b81b83c5c3ae69318aa367fc4c32b88feadd9bd3a4e83447bfe14d2826a1f16b218bccdd11a3209c5411d2818c0ad5edf6948016939193f9836bc79596615fb0c432264aec5ceeffcb3666f4be87200e64921122329bdead7829cebf35445e828b23e9d5fd788aaebbea81ac825050c3a1d583ad866ad9c8cade963e86bdcb50aa6eda13ff0e9fe7ecb049ac3aeeb88518c13ee7d8d3a087435af1266f497f20186097cb4817d6348b0a676a434035c1ae26e8bea023817938dbfcd48897c07bc7c40419a151b5933a30a1abc74a93e6f4df9363ee114f841d18609e953f00ba48e7408ceb3aff4f0207d383d086041f3942c199bbc03ca77017a4741e1dbc16b89bd9ab1a2c29e768458e521d0e34756a89fef07a2464b73cb2726333d973278d6b955e3aa64948e7122c1e0ab632be9478b76b99200a43a379f3acc9bc31e891eb686a2741ad3b337a4466af2188a02ec3b4b5f5e2f89bf1073cd74cc53cb356ad1f8fa47658f26c3553b7ed4334dec6c9868f906b877da89239683a626d7ff4a3d1160f07cbe266d7efb5f892f86a29de6501bb0f0d7ae7f96e4cb0284669ad7e44643ca570fadadd8020ff2408968c5152d708a43db509ced814ae18aefe01f25aa901b7a1fbb058f4ca0d38e5c480a235606587c34a4696dda4221398a1be3b1d818dc753c8f6650d88ad557aa0ab3cd63cb518e1e6f33c4e09b1f5be0941d90a0cf4539b409f031de5d388b3c28c155623a7e358ea6971cb1cd78db4f1fd9a27d49d168fe747a50394893862a25d3860c9625c14988283e4ec4e9bfb1ee36bc4e5893e938e4824478daea4d504afa06a6e56ed27d9fe05ed7930e547cc4c26ffcd15c6beaecf1b387ec0bb1df570d8acc2ea67f36c37a7994d2cc6f7ff02ffc5d8bb63a892b740174bddb30de660478ce538057cc6e9cd51fc698377d08af005c2dfe548f3080822df0ba66d30977baa994a5d55cb4faa15d5c08ed65140f16da0cb6fd25eb180554870a3fd9e7bd47808fe6daabdd1075f4da641a19481db0a9956c71e434a59ae64b38c64f6ed7c20596a43b5533658b9c638619d4f8d6204feb2a3101fbbad63c5590b2b77738c8e53526edb1dfd6ad4de489ab2b62d9c17460181eff95021166d592241b4146f134ca516a3373ef8d98a5ded7717a8bf9ef117a6a249ccce9e7c60607bf0cf03e269f0bd3a698a5cc37bef58206d6bfd93a95bf8866a8393e738c25e85aefb83992f6b05113a548bd55c3eff86fcc606471c75e5e3263fbc46c75b8056a9f776a72a35844b88a739d7833c5922a2",
            "signed_blocks": [],
            "signed_attestations": [
              {
                "source_epoch": "0",
                "target_epoch": "0"
              }
            ]
          }
        ]
      },
      "blocks": [],
      "attestations": [
        {
          "pubkey": "0x9498619d44f1c5df1ba7950041ed069244e7cb5ec46783c6c87e47cd6761e7c99b7ef20e2fd3102575dcf961e73f3d22c1d055e47ae946b0e6cd3c9e08468576954d156ce4935accc31833d10d0796aa47d2a35d95d6c999179f60eca007c20435b87bf3dbd027f7b21f4fda4fcade3dd7f0d9342a64bf0ab659fa9306e57ff1eab0aa5a5c6415d9c081fb4326146e5f445b724d9283923ee81b0d866ffb2ea4474741862d8eb5a223d0ff0db047efcc4d39859fa1abaa4b65eefa1ff0538af4a3e43875bdf20f153eab213189d6330fcf8f3f261ff331db4a62694aad257dd412bdf7cb831cdd8b00ab1391ba5930a4090616ae3023b165723ee7b57d85a45de413de1cfa2b61d4b6cb2e2137d983b5b5fef63fa6ca2699cd3ad2ce3d3c0fcc6cd6b87ebf9417aef7124292314cfecd6861896f21de56c2aba6dfc47f56a0f41cecd64cd82e11b77acdcac060cdf676ffd5e326345f4fa75d8315bcb6096d4643234df5bd5bc541fc5bcd7908a1c651425984032866749f76e31b0531dd2841c1d7ecfb60d7f4c9ed5d71d11823633207726d37584928e64fb7c4490efc6495bdda2ebd689f068cbe02b7acf597b1cfd586ea90254098d51783e8eee7a319c613a65f19e4a55bd05b6c845822475f163a74099a30283028b321e0e1d6526699bf5540ff5c5ff35eca1188620256e5fddad71a515f146f11c8d690990d2567de9bc0d7e056e9918e6fbef423486e7b47684807fd5c408eb18c010d7de6ad297e2cb5a2072f117b0c38ec4107f3d686c55a3d73b035c2f1b55144fa785f1d6818061465373cf5cfa67097d533bfa5324da08f145259215202964ea8d5aad2a2cbf058e7b7ba167151092380b12eba0248476263af1f62fa5173f865273baf2b9714d052368bd782595df6dbf61ffb3d15dde65b2cd1360db2bfa1a2279f7ca59f9c83041f4d6ce3c4b39568c21439443f2969eea67ec8d9c46474038b24a0f76059fc501e379e6e82894a29501de9f0f462a15880bc8e4e3a7d7a5bb51b72549866a69b6ac4fcb1d1a03d13ab321057f69098c927c2c6e3ad55791f204b704f79c75ab7874b22dc99bd08316783a1bf0996af9465840f06c328bae6836f93e3065e363273c5582e8710dc85fc7424d777f067d22f40d0febcf9c1ad28a6b02e33bdec72834c506b6074d89726e049678b566563ef23a179d7ec711f88d49c98669f494f2bf4a199c957ba2a1e97d8d322e7f16fe4c5c4b98588803e8e31dad9d3b904143e91cb33ce62d8d7bb17e1a4b718165632c1ae4663c75159991869b0ef68f8bcd3bc40b214ebdf98e1e22a80d34ffc5b7ad3694a5bed6b16cdf3b7af86f3c335201447ce1d265f5dceecf30709328e3c6b12b9530ef60cb4386ff9285b970903f85b12914288248cb9a15139049006551e97406e89c579b61a40914ff5eb12a1e97a60a77afec6d619ba00474dba9042e8d5328794edda92020a7b5b597b57831ae3cbee183fe9ef1aae504980d266054b99496c144c85e21b9a4d751e613a50c305d84a0aea099cecd5c7c5eac3d1d86c9048d781ce2d0b20f7aadd83bfa684fe02ff6c84cad6b75c78c824e998af8c4061609c840caa8c0366841570e735f6e55582e474e7f013270acd200a0834ad7d8e98b8cf159e0774aad3e84ecda22a079f59da0a96a0e4041d56a566eed22c63017ba422bdb96724c4257fa926cd3d17ad803d09b851cc662d544db5a843c31df7442c7c4cb752890da39ad2574f27b655556c4082322b4cd2067d30478fa9ac8688ce7c315988f50dad984e985abf8dbd37a1c74f42b5a5d1f646eb8c0d1f2882a4e704f92169fe06655f2a208f56436691bc8ea2ea460b20f590bc5e05e75ef02b087c8e19fddd898b8869fa542a1bbc08abd76245cd72efcb6df1c0d2d5fc21815080d204ff49f56ad50e5a0bbb9d111613efe1c60ee44fe64ccb492bda1d03e10f161e09003f8ecaa00961b8ce37e7113d3f626458b60409434778241158a5484487ed2c897cf21d2258146947a7924791680ac4398c99e58880928644012550fffc4ec96e347f00db8b3950b22b5d1da80581663377f08f10236a302e4901ab1c742853ce56a16f9ce3b9c258149f8429259da7202301d9c77d992fb2f4f7f80551197c323d469d7d9ec54094c6dc9fb385554769538e48be199bffa8f6d31ef498c0763220200b176fa63ce11458fdc44496890ee7031c17b39cbdcfe22fa6792d98261dc22139a4b336f3090301a2ab9d4d808b45b28a3ec529db7baa7a0d30f4e9f65203663be8ff204090064bba69d449e5ed5ded88e4d70e34b26f133815c07d2e3660503458b5b81b83c5c3ae69318aa367fc4c32b88feadd9bd3a4e83447bfe14d2826a1f16b218bccdd11a3209c5411d2818c0ad5edf6948016939193f9836bc79596615fb0c432264aec5ceeffcb3666f4be87200e64921122329bdead7829cebf35445e828b23e9d5fd788aaebbea81ac825050c3a1d583ad866ad9c8cade963e86bdcb50aa6eda13ff0e9fe7ecb049ac3aeeb88518c13ee7d8d3a087435af1266f497f20186097cb4817d6348b0a676a434035c1ae26e8bea023817938dbfcd48897c07bc7c40419a151b5933a30a1abc74a93e6f4df9363ee114f841d18609e953f00ba48e7408ceb3aff4f0207d383d086041f3942c199bbc03ca77017a4741e1dbc16b89bd9ab1a2c29e768458e521d0e34756a89fef07a2464b73cb2726333d973278d6b955e3aa64948e7122c1e0ab632be9478b76b99200a43a379f3acc9bc31e891eb686a2741ad3b337a4466af2188a02ec3b4b5f5e2f89bf1073cd74cc53cb356ad1f8fa47658f26c3553b7ed4334dec6c9868f906b877da89239683a626d7ff4a3d1160f07cbe266d7efb5f892f86a29de6501bb0f0d7ae7f96e4cb0284669ad7e44643ca570fadadd8020ff2408968c5152d708a43db509ced814ae18aefe01f25aa901b7a1fbb058f4ca0d38e5c480a235606587c34a4696dda4221398a1be3b1d818dc753c8f6650d88ad557aa0ab3cd63cb518e1e6f33c4e09b1f5be0941d90a0cf4539b409f031de5d388b3c28c155623a7e358ea6971cb1cd78db4f1fd9a27d49d168fe747a50394893862a25d3860c9625c14988283e4ec4e9bfb1ee36bc4e5893e938e4824478daea4d504afa06a6e56ed27d9fe05ed7930e547cc4c26ffcd15c6beaecf1b387ec0bb1df570d8acc2ea67f36c37a7994d2cc6f7ff02ffc5d8bb63a892b740174bddb30de660478ce538057cc6e9cd51fc698377d08af005c2dfe548f3080822df0ba66d30977baa994a5d55cb4faa15d5c08ed65140f16da0cb6fd25eb180554870a3fd9e7bd47808fe6daabdd1075f4da641a19481db0a9956c71e434a59ae64b38c64f6ed7c20596a43b5533658b9c638619d4f8d6204feb2a3101fbbad63c5590b2b77738c8e53526edb1dfd6ad4de489ab2b62d9c17460181eff95021166d592241b4146f134ca516a3373ef8d98a5ded7717a8bf9ef117a6a249ccce9e7c60607bf0cf03e269f0bd3a698a5cc37bef58206d6bfd93a95bf8866a8393e738c25e85aefb83992f6b05113a548bd55c3eff86fcc606471c75e5e3263fbc46c75b8056a9f776a72a35844b88a739d7833c5922a2",
          "source_epoch": "0",
          "target_epoch": "0",
          "should_succeed": false
        }
      ]
    }
  ]
}
```

To run a test, first initialize a new (empty) slashing protection database.

Then for each entry in `steps`, import the `interchange`, process the `blocks` and `attestations`,
and continue to the next step.

Determine the test outcome according to the meanings of each of the fields,
which are as follows:

* `name: string`: the name of the test-case, informational.
* `genesis_validators_root: Root`: the genesis validators root to use when
  creating the empty slashing protection database, or to compare the import
  against.
* `steps[i].should_succeed: bool`: whether the `steps[i].interchange` given is valid and should
  be imported successfully.
* `steps[i].contains_slashable_data: bool`: whether the `steps[i].interchange` contains some
  slashable data with respect to itself or the existing contents of the database.
* `steps[i].interchange: Interchange`: slashing protection interchange data as described
  by the spec.
* `steps[i].blocks: [object]`: a list of block signings to be attempted **after**
  importing the `interchange`, detailed below.
* `steps[i].attestations: [object]`: a list of attestation signings to be attempted **after**
  importing the `interchange`, detailed below.

Each block in `blocks` is structured as:

```json
{
  "pubkey": "0x9498619d44f1c5df1ba7950041ed069244e7cb5ec46783c6c87e47cd6761e7c99b7ef20e2fd3102575dcf961e73f3d22c1d055e47ae946b0e6cd3c9e08468576954d156ce4935accc31833d10d0796aa47d2a35d95d6c999179f60eca007c20435b87bf3dbd027f7b21f4fda4fcade3dd7f0d9342a64bf0ab659fa9306e57ff1eab0aa5a5c6415d9c081fb4326146e5f445b724d9283923ee81b0d866ffb2ea4474741862d8eb5a223d0ff0db047efcc4d39859fa1abaa4b65eefa1ff0538af4a3e43875bdf20f153eab213189d6330fcf8f3f261ff331db4a62694aad257dd412bdf7cb831cdd8b00ab1391ba5930a4090616ae3023b165723ee7b57d85a45de413de1cfa2b61d4b6cb2e2137d983b5b5fef63fa6ca2699cd3ad2ce3d3c0fcc6cd6b87ebf9417aef7124292314cfecd6861896f21de56c2aba6dfc47f56a0f41cecd64cd82e11b77acdcac060cdf676ffd5e326345f4fa75d8315bcb6096d4643234df5bd5bc541fc5bcd7908a1c651425984032866749f76e31b0531dd2841c1d7ecfb60d7f4c9ed5d71d11823633207726d37584928e64fb7c4490efc6495bdda2ebd689f068cbe02b7acf597b1cfd586ea90254098d51783e8eee7a319c613a65f19e4a55bd05b6c845822475f163a74099a30283028b321e0e1d6526699bf5540ff5c5ff35eca1188620256e5fddad71a515f146f11c8d690990d2567de9bc0d7e056e9918e6fbef423486e7b47684807fd5c408eb18c010d7de6ad297e2cb5a2072f117b0c38ec4107f3d686c55a3d73b035c2f1b55144fa785f1d6818061465373cf5cfa67097d533bfa5324da08f145259215202964ea8d5aad2a2cbf058e7b7ba167151092380b12eba0248476263af1f62fa5173f865273baf2b9714d052368bd782595df6dbf61ffb3d15dde65b2cd1360db2bfa1a2279f7ca59f9c83041f4d6ce3c4b39568c21439443f2969eea67ec8d9c46474038b24a0f76059fc501e379e6e82894a29501de9f0f462a15880bc8e4e3a7d7a5bb51b72549866a69b6ac4fcb1d1a03d13ab321057f69098c927c2c6e3ad55791f204b704f79c75ab7874b22dc99bd08316783a1bf0996af9465840f06c328bae6836f93e3065e363273c5582e8710dc85fc7424d777f067d22f40d0febcf9c1ad28a6b02e33bdec72834c506b6074d89726e049678b566563ef23a179d7ec711f88d49c98669f494f2bf4a199c957ba2a1e97d8d322e7f16fe4c5c4b98588803e8e31dad9d3b904143e91cb33ce62d8d7bb17e1a4b718165632c1ae4663c75159991869b0ef68f8bcd3bc40b214ebdf98e1e22a80d34ffc5b7ad3694a5bed6b16cdf3b7af86f3c335201447ce1d265f5dceecf30709328e3c6b12b9530ef60cb4386ff9285b970903f85b12914288248cb9a15139049006551e97406e89c579b61a40914ff5eb12a1e97a60a77afec6d619ba00474dba9042e8d5328794edda92020a7b5b597b57831ae3cbee183fe9ef1aae504980d266054b99496c144c85e21b9a4d751e613a50c305d84a0aea099cecd5c7c5eac3d1d86c9048d781ce2d0b20f7aadd83bfa684fe02ff6c84cad6b75c78c824e998af8c4061609c840caa8c0366841570e735f6e55582e474e7f013270acd200a0834ad7d8e98b8cf159e0774aad3e84ecda22a079f59da0a96a0e4041d56a566eed22c63017ba422bdb96724c4257fa926cd3d17ad803d09b851cc662d544db5a843c31df7442c7c4cb752890da39ad2574f27b655556c4082322b4cd2067d30478fa9ac8688ce7c315988f50dad984e985abf8dbd37a1c74f42b5a5d1f646eb8c0d1f2882a4e704f92169fe06655f2a208f56436691bc8ea2ea460b20f590bc5e05e75ef02b087c8e19fddd898b8869fa542a1bbc08abd76245cd72efcb6df1c0d2d5fc21815080d204ff49f56ad50e5a0bbb9d111613efe1c60ee44fe64ccb492bda1d03e10f161e09003f8ecaa00961b8ce37e7113d3f626458b60409434778241158a5484487ed2c897cf21d2258146947a7924791680ac4398c99e58880928644012550fffc4ec96e347f00db8b3950b22b5d1da80581663377f08f10236a302e4901ab1c742853ce56a16f9ce3b9c258149f8429259da7202301d9c77d992fb2f4f7f80551197c323d469d7d9ec54094c6dc9fb385554769538e48be199bffa8f6d31ef498c0763220200b176fa63ce11458fdc44496890ee7031c17b39cbdcfe22fa6792d98261dc22139a4b336f3090301a2ab9d4d808b45b28a3ec529db7baa7a0d30f4e9f65203663be8ff204090064bba69d449e5ed5ded88e4d70e34b26f133815c07d2e3660503458b5b81b83c5c3ae69318aa367fc4c32b88feadd9bd3a4e83447bfe14d2826a1f16b218bccdd11a3209c5411d2818c0ad5edf6948016939193f9836bc79596615fb0c432264aec5ceeffcb3666f4be87200e64921122329bdead7829cebf35445e828b23e9d5fd788aaebbea81ac825050c3a1d583ad866ad9c8cade963e86bdcb50aa6eda13ff0e9fe7ecb049ac3aeeb88518c13ee7d8d3a087435af1266f497f20186097cb4817d6348b0a676a434035c1ae26e8bea023817938dbfcd48897c07bc7c40419a151b5933a30a1abc74a93e6f4df9363ee114f841d18609e953f00ba48e7408ceb3aff4f0207d383d086041f3942c199bbc03ca77017a4741e1dbc16b89bd9ab1a2c29e768458e521d0e34756a89fef07a2464b73cb2726333d973278d6b955e3aa64948e7122c1e0ab632be9478b76b99200a43a379f3acc9bc31e891eb686a2741ad3b337a4466af2188a02ec3b4b5f5e2f89bf1073cd74cc53cb356ad1f8fa47658f26c3553b7ed4334dec6c9868f906b877da89239683a626d7ff4a3d1160f07cbe266d7efb5f892f86a29de6501bb0f0d7ae7f96e4cb0284669ad7e44643ca570fadadd8020ff2408968c5152d708a43db509ced814ae18aefe01f25aa901b7a1fbb058f4ca0d38e5c480a235606587c34a4696dda4221398a1be3b1d818dc753c8f6650d88ad557aa0ab3cd63cb518e1e6f33c4e09b1f5be0941d90a0cf4539b409f031de5d388b3c28c155623a7e358ea6971cb1cd78db4f1fd9a27d49d168fe747a50394893862a25d3860c9625c14988283e4ec4e9bfb1ee36bc4e5893e938e4824478daea4d504afa06a6e56ed27d9fe05ed7930e547cc4c26ffcd15c6beaecf1b387ec0bb1df570d8acc2ea67f36c37a7994d2cc6f7ff02ffc5d8bb63a892b740174bddb30de660478ce538057cc6e9cd51fc698377d08af005c2dfe548f3080822df0ba66d30977baa994a5d55cb4faa15d5c08ed65140f16da0cb6fd25eb180554870a3fd9e7bd47808fe6daabdd1075f4da641a19481db0a9956c71e434a59ae64b38c64f6ed7c20596a43b5533658b9c638619d4f8d6204feb2a3101fbbad63c5590b2b77738c8e53526edb1dfd6ad4de489ab2b62d9c17460181eff95021166d592241b4146f134ca516a3373ef8d98a5ded7717a8bf9ef117a6a249ccce9e7c60607bf0cf03e269f0bd3a698a5cc37bef58206d6bfd93a95bf8866a8393e738c25e85aefb83992f6b05113a548bd55c3eff86fcc606471c75e5e3263fbc46c75b8056a9f776a72a35844b88a739d7833c5922a2",
  "slot": "1",
  "signing_root": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "should_succeed": false
}
```

Your test-runner should attempt to sign a block with `signing_root` at the
given slot from the given `pubkey`. The `should_succeed` field describes
whether this signing should be accepted (true) or rejected (false). Clients
using a slashing protection mechanism that admits false positives may consider
a rejection as success even if `should_succeed` is true. If the block is signed
successfully it should be incorporated into the slashing protection database.

Each attestation in `attestations` is structured as:

```json
{
  "pubkey": "0x9498619d44f1c5df1ba7950041ed069244e7cb5ec46783c6c87e47cd6761e7c99b7ef20e2fd3102575dcf961e73f3d22c1d055e47ae946b0e6cd3c9e08468576954d156ce4935accc31833d10d0796aa47d2a35d95d6c999179f60eca007c20435b87bf3dbd027f7b21f4fda4fcade3dd7f0d9342a64bf0ab659fa9306e57ff1eab0aa5a5c6415d9c081fb4326146e5f445b724d9283923ee81b0d866ffb2ea4474741862d8eb5a223d0ff0db047efcc4d39859fa1abaa4b65eefa1ff0538af4a3e43875bdf20f153eab213189d6330fcf8f3f261ff331db4a62694aad257dd412bdf7cb831cdd8b00ab1391ba5930a4090616ae3023b165723ee7b57d85a45de413de1cfa2b61d4b6cb2e2137d983b5b5fef63fa6ca2699cd3ad2ce3d3c0fcc6cd6b87ebf9417aef7124292314cfecd6861896f21de56c2aba6dfc47f56a0f41cecd64cd82e11b77acdcac060cdf676ffd5e326345f4fa75d8315bcb6096d4643234df5bd5bc541fc5bcd7908a1c651425984032866749f76e31b0531dd2841c1d7ecfb60d7f4c9ed5d71d11823633207726d37584928e64fb7c4490efc6495bdda2ebd689f068cbe02b7acf597b1cfd586ea90254098d51783e8eee7a319c613a65f19e4a55bd05b6c845822475f163a74099a30283028b321e0e1d6526699bf5540ff5c5ff35eca1188620256e5fddad71a515f146f11c8d690990d2567de9bc0d7e056e9918e6fbef423486e7b47684807fd5c408eb18c010d7de6ad297e2cb5a2072f117b0c38ec4107f3d686c55a3d73b035c2f1b55144fa785f1d6818061465373cf5cfa67097d533bfa5324da08f145259215202964ea8d5aad2a2cbf058e7b7ba167151092380b12eba0248476263af1f62fa5173f865273baf2b9714d052368bd782595df6dbf61ffb3d15dde65b2cd1360db2bfa1a2279f7ca59f9c83041f4d6ce3c4b39568c21439443f2969eea67ec8d9c46474038b24a0f76059fc501e379e6e82894a29501de9f0f462a15880bc8e4e3a7d7a5bb51b72549866a69b6ac4fcb1d1a03d13ab321057f69098c927c2c6e3ad55791f204b704f79c75ab7874b22dc99bd08316783a1bf0996af9465840f06c328bae6836f93e3065e363273c5582e8710dc85fc7424d777f067d22f40d0febcf9c1ad28a6b02e33bdec72834c506b6074d89726e049678b566563ef23a179d7ec711f88d49c98669f494f2bf4a199c957ba2a1e97d8d322e7f16fe4c5c4b98588803e8e31dad9d3b904143e91cb33ce62d8d7bb17e1a4b718165632c1ae4663c75159991869b0ef68f8bcd3bc40b214ebdf98e1e22a80d34ffc5b7ad3694a5bed6b16cdf3b7af86f3c335201447ce1d265f5dceecf30709328e3c6b12b9530ef60cb4386ff9285b970903f85b12914288248cb9a15139049006551e97406e89c579b61a40914ff5eb12a1e97a60a77afec6d619ba00474dba9042e8d5328794edda92020a7b5b597b57831ae3cbee183fe9ef1aae504980d266054b99496c144c85e21b9a4d751e613a50c305d84a0aea099cecd5c7c5eac3d1d86c9048d781ce2d0b20f7aadd83bfa684fe02ff6c84cad6b75c78c824e998af8c4061609c840caa8c0366841570e735f6e55582e474e7f013270acd200a0834ad7d8e98b8cf159e0774aad3e84ecda22a079f59da0a96a0e4041d56a566eed22c63017ba422bdb96724c4257fa926cd3d17ad803d09b851cc662d544db5a843c31df7442c7c4cb752890da39ad2574f27b655556c4082322b4cd2067d30478fa9ac8688ce7c315988f50dad984e985abf8dbd37a1c74f42b5a5d1f646eb8c0d1f2882a4e704f92169fe06655f2a208f56436691bc8ea2ea460b20f590bc5e05e75ef02b087c8e19fddd898b8869fa542a1bbc08abd76245cd72efcb6df1c0d2d5fc21815080d204ff49f56ad50e5a0bbb9d111613efe1c60ee44fe64ccb492bda1d03e10f161e09003f8ecaa00961b8ce37e7113d3f626458b60409434778241158a5484487ed2c897cf21d2258146947a7924791680ac4398c99e58880928644012550fffc4ec96e347f00db8b3950b22b5d1da80581663377f08f10236a302e4901ab1c742853ce56a16f9ce3b9c258149f8429259da7202301d9c77d992fb2f4f7f80551197c323d469d7d9ec54094c6dc9fb385554769538e48be199bffa8f6d31ef498c0763220200b176fa63ce11458fdc44496890ee7031c17b39cbdcfe22fa6792d98261dc22139a4b336f3090301a2ab9d4d808b45b28a3ec529db7baa7a0d30f4e9f65203663be8ff204090064bba69d449e5ed5ded88e4d70e34b26f133815c07d2e3660503458b5b81b83c5c3ae69318aa367fc4c32b88feadd9bd3a4e83447bfe14d2826a1f16b218bccdd11a3209c5411d2818c0ad5edf6948016939193f9836bc79596615fb0c432264aec5ceeffcb3666f4be87200e64921122329bdead7829cebf35445e828b23e9d5fd788aaebbea81ac825050c3a1d583ad866ad9c8cade963e86bdcb50aa6eda13ff0e9fe7ecb049ac3aeeb88518c13ee7d8d3a087435af1266f497f20186097cb4817d6348b0a676a434035c1ae26e8bea023817938dbfcd48897c07bc7c40419a151b5933a30a1abc74a93e6f4df9363ee114f841d18609e953f00ba48e7408ceb3aff4f0207d383d086041f3942c199bbc03ca77017a4741e1dbc16b89bd9ab1a2c29e768458e521d0e34756a89fef07a2464b73cb2726333d973278d6b955e3aa64948e7122c1e0ab632be9478b76b99200a43a379f3acc9bc31e891eb686a2741ad3b337a4466af2188a02ec3b4b5f5e2f89bf1073cd74cc53cb356ad1f8fa47658f26c3553b7ed4334dec6c9868f906b877da89239683a626d7ff4a3d1160f07cbe266d7efb5f892f86a29de6501bb0f0d7ae7f96e4cb0284669ad7e44643ca570fadadd8020ff2408968c5152d708a43db509ced814ae18aefe01f25aa901b7a1fbb058f4ca0d38e5c480a235606587c34a4696dda4221398a1be3b1d818dc753c8f6650d88ad557aa0ab3cd63cb518e1e6f33c4e09b1f5be0941d90a0cf4539b409f031de5d388b3c28c155623a7e358ea6971cb1cd78db4f1fd9a27d49d168fe747a50394893862a25d3860c9625c14988283e4ec4e9bfb1ee36bc4e5893e938e4824478daea4d504afa06a6e56ed27d9fe05ed7930e547cc4c26ffcd15c6beaecf1b387ec0bb1df570d8acc2ea67f36c37a7994d2cc6f7ff02ffc5d8bb63a892b740174bddb30de660478ce538057cc6e9cd51fc698377d08af005c2dfe548f3080822df0ba66d30977baa994a5d55cb4faa15d5c08ed65140f16da0cb6fd25eb180554870a3fd9e7bd47808fe6daabdd1075f4da641a19481db0a9956c71e434a59ae64b38c64f6ed7c20596a43b5533658b9c638619d4f8d6204feb2a3101fbbad63c5590b2b77738c8e53526edb1dfd6ad4de489ab2b62d9c17460181eff95021166d592241b4146f134ca516a3373ef8d98a5ded7717a8bf9ef117a6a249ccce9e7c60607bf0cf03e269f0bd3a698a5cc37bef58206d6bfd93a95bf8866a8393e738c25e85aefb83992f6b05113a548bd55c3eff86fcc606471c75e5e3263fbc46c75b8056a9f776a72a35844b88a739d7833c5922a2",
  "source_epoch": "11",
  "target_epoch": "12",
  "signing_root": "0x0000000000000000000000000000000000000000000000000000000000000000",
  "should_succeed": true
}
```

Similarly to above, your test-runner should attempt to sign an attestation with these parameters
using the given `pubkey`, and succeed based on the value of `should_succeed`. Again, false positives
may be treated as successes, and signed attestations should be incorporated into the database.

Note that the top-level `genesis_validators_root` is not necessarily the same
as the GVR contained in the interchange, to allow us to test the case where
they are mismatched.

## Handling Slashable Data

The `contains_slashable_data` parameter is to be interpreted as follows:

- If `should_succeed` is false, then `contains_slashable_data` is irrelevant
- If `contains_slashable_data` is false, then the given interchange **must** be imported
  successfully, and the given block/attestation checks must pass.
- If `contains_slashable_data` is true, then implementations have the option to do one of two
  things:
  	- Import the interchange successfully, working around the slashable data by minification
	  or some other mechanism. If the import succeeds, all checks must pass and the test
	  should continue to the next step.
	- Reject the interchange (or partially import it), in which case the block/attestation
	  checks and all future steps should be ignored.

## Downloading the tests

The `tests` directory is released as a versioned `.tar.gz` on the [Releases](https://github.com/eth-clients/slashing-protection-interchange-tests/releases) page.

Alternatively, you could use a git submodule.
