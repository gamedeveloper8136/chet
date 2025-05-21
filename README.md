> slither ./contracts
WARNING:Slither:No contract was analyzed
INFO:Slither:./contracts analyzed (0 contracts with 100 detectors), 0 result(s) found
PS D:\Haven1\dev-onboarding-template> slither . --filter-paths "node_modules"
'npx hardhat clean' running (wd: D:\Haven1\dev-onboarding-template)
'npx' returned non-zero exit code 1
An unexpected error occurred:
stderr: Error: Cannot find module 'solidity-docgen'
stderr: Require stack:
stderr: - D:\Haven1\dev-onboarding-template\hardhat.config.ts
stderr: - D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\core\config\config-loading.js
stderr: - D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\cli\cli.js
stderr: - D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\cli\bootstrap.js
stderr:     at Function.<anonymous> (node:internal/modules/cjs/loader:1401:15)
stderr:     at Function.Module._resolveFilename.sharedData.moduleResolveFilenameHook.installedValue [as _resolveFilename] (D:\Haven1\dev-onboarding-template\node_modules\@cspotcode\source-map-support\source-map-support.js:811:30)
stderr:     at defaultResolveImpl (node:internal/modules/cjs/loader:1057:19)
stderr:     at resolveForCJSWithHooks (node:internal/modules/cjs/loader:1062:22)
stderr:     at Function._load (node:internal/modules/cjs/loader:1211:37)
stderr:     at TracingChannel.traceSync (node:diagnostics_channel:322:14)
stderr:     at wrapModuleLoad (node:internal/modules/cjs/loader:235:24)
stderr:     at Module.require (node:internal/modules/cjs/loader:1487:12)
stderr:     at require (node:internal/modules/helpers:135:16)
stderr:     at Object.<anonymous> (D:\Haven1\dev-onboarding-template\hardhat.config.ts:8:1) {
stderr:   code: 'MODULE_NOT_FOUND',
stderr:   requireStack: [
stderr:     'D:\\Haven1\\dev-onboarding-template\\hardhat.config.ts',
stderr:     'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\core\\config\\config-loading.js',
stderr:     'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\cli\\cli.js',
stderr:     'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\cli\\bootstrap.js'
stderr:   ]
stderr: }
'npx hardhat clean --global' running (wd: D:\Haven1\dev-onboarding-template)
'npx' returned non-zero exit code 1
An unexpected error occurred:
stderr: Error: Cannot find module 'solidity-docgen'
stderr: Require stack:
stderr: - D:\Haven1\dev-onboarding-template\hardhat.config.ts
stderr: - D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\core\config\config-loading.js
stderr: - D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\cli\cli.js
stderr: - D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\cli\bootstrap.js
stderr:     at Function.<anonymous> (node:internal/modules/cjs/loader:1401:15)
stderr:     at Function.Module._resolveFilename.sharedData.moduleResolveFilenameHook.installedValue [as _resolveFilename] (D:\Haven1\dev-onboarding-template\node_modules\@cspotcode\source-map-support\source-map-support.js:811:30)
stderr:     at defaultResolveImpl (node:internal/modules/cjs/loader:1057:19)
stderr:     at resolveForCJSWithHooks (node:internal/modules/cjs/loader:1062:22)
stderr:     at Function._load (node:internal/modules/cjs/loader:1211:37)
stderr:     at TracingChannel.traceSync (node:diagnostics_channel:322:14)
stderr:     at wrapModuleLoad (node:internal/modules/cjs/loader:235:24)
stderr:     at Module.require (node:internal/modules/cjs/loader:1487:12)
stderr:     at require (node:internal/modules/helpers:135:16)
stderr:     at Object.<anonymous> (D:\Haven1\dev-onboarding-template\hardhat.config.ts:8:1) {
stderr:   code: 'MODULE_NOT_FOUND',
stderr:   requireStack: [
stderr:     'D:\\Haven1\\dev-onboarding-template\\hardhat.config.ts',
stderr:     'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\core\\config\\config-loading.js',
stderr:     'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\cli\\cli.js',
stderr:     'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\cli\\bootstrap.js'
stderr:   ]
stderr: }
Problem executing hardhat: An unexpected error occurred:
Error: Cannot find module 'solidity-docgen'
Require stack:
- D:\Haven1\dev-onboarding-template\hardhat.config.ts
- D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\core\config\config-loading.js
- D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\cli\cli.js
- D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\cli\bootstrap.js
    at Function.<anonymous> (node:internal/modules/cjs/loader:1401:15)
    at Function.Module._resolveFilename.sharedData.moduleResolveFilenameHook.installedValue [as _resolveFilename] (D:\Haven1\dev-onboarding-template\node_modules\@cspotcode\source-map-support\source-map-support.js:811:30)
    at defaultResolveImpl (node:internal/modules/cjs/loader:1057:19)
    at resolveForCJSWithHooks (node:internal/modules/cjs/loader:1062:22)
    at Function._load (node:internal/modules/cjs/loader:1211:37)
    at TracingChannel.traceSync (node:diagnostics_channel:322:14)
    at wrapModuleLoad (node:internal/modules/cjs/loader:235:24)
    at Module.require (node:internal/modules/cjs/loader:1487:12)
    at require (node:internal/modules/helpers:135:16)
    at Object.<anonymous> (D:\Haven1\dev-onboarding-template\hardhat.config.ts:8:1) {
  code: 'MODULE_NOT_FOUND',
  requireStack: [
    'D:\\Haven1\\dev-onboarding-template\\hardhat.config.ts',
    'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\core\\config\\config-loading.js',
    'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\cli\\cli.js',
    'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\cli\\bootstrap.js'
  ]
}

'npx hardhat compile --force' running (wd: D:\Haven1\dev-onboarding-template)
'npx' returned non-zero exit code 1
An unexpected error occurred:
stderr: Error: Cannot find module 'solidity-docgen'
stderr: Require stack:
stderr: - D:\Haven1\dev-onboarding-template\hardhat.config.ts
stderr: - D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\core\config\config-loading.js
stderr: - D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\cli\cli.js
stderr: - D:\Haven1\dev-onboarding-template\node_modules\hardhat\internal\cli\bootstrap.js
stderr:     at Function.<anonymous> (node:internal/modules/cjs/loader:1401:15)
stderr:     at Function.Module._resolveFilename.sharedData.moduleResolveFilenameHook.installedValue [as _resolveFilename] (D:\Haven1\dev-onboarding-template\node_modules\@cspotcode\source-map-support\source-map-support.js:811:30)
stderr:     at defaultResolveImpl (node:internal/modules/cjs/loader:1057:19)
stderr:     at resolveForCJSWithHooks (node:internal/modules/cjs/loader:1062:22)
stderr:     at Function._load (node:internal/modules/cjs/loader:1211:37)
stderr:     at TracingChannel.traceSync (node:diagnostics_channel:322:14)
stderr:     at wrapModuleLoad (node:internal/modules/cjs/loader:235:24)
stderr:     at Module.require (node:internal/modules/cjs/loader:1487:12)
stderr:     at require (node:internal/modules/helpers:135:16)
stderr:     at Object.<anonymous> (D:\Haven1\dev-onboarding-template\hardhat.config.ts:8:1) {
stderr:   code: 'MODULE_NOT_FOUND',
stderr:   requireStack: [
stderr:     'D:\\Haven1\\dev-onboarding-template\\hardhat.config.ts',
stderr:     'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\core\\config\\config-loading.js',
stderr:     'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\cli\\cli.js',
stderr:     'D:\\Haven1\\dev-onboarding-template\\node_modules\\hardhat\\internal\\cli\\bootstrap.js'
stderr:   ]
stderr: }
INFO:Detectors:
NFTAuction._withdraw(address,uint256) (contracts/examples/nft-auction/NFTAuction.sol#484-487) sends eth to arbitrary user
        Dangerous calls:
        - (success,None) = address(to).call{value: amount}() (contracts/examples/nft-auction/NFTAuction.sol#485)
FeeContract._distributeFees() (contracts/vendor/fee/FeeContract.sol#859-873) sends eth to arbitrary user
        Dangerous calls:
        - (sent,None) = _channels[i].call{value: share}() (contracts/vendor/fee/FeeContract.sol#865)
H1DevelopedApplication._safeTransfer(address,uint256) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#827-832) sends eth to arbitrary user
        Dangerous calls:
        - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#functions-that-send-ether-to-arbitrary-destinations
INFO:Detectors:
Reentrancy in NFTAuction.bid() (contracts/examples/nft-auction/NFTAuction.sol#259-294):
        External calls:
        - _refundBid() (contracts/examples/nft-auction/NFTAuction.sol#288)
                - (success,None) = address(to).call{value: amount}() (contracts/examples/nft-auction/NFTAuction.sol#485)
        - developerFee(true,false) (contracts/examples/nft-auction/NFTAuction.sol#265)
                - _feeContract.updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#818)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        External calls sending eth:
        - _refundBid() (contracts/examples/nft-auction/NFTAuction.sol#288)
                - (success,None) = address(to).call{value: amount}() (contracts/examples/nft-auction/NFTAuction.sol#485)
        - developerFee(true,false) (contracts/examples/nft-auction/NFTAuction.sol#265)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        State variables written after the call(s):
        - _highestBid = val (contracts/examples/nft-auction/NFTAuction.sol#291)
        NFTAuction._highestBid (contracts/examples/nft-auction/NFTAuction.sol#72) can be used in cross function reentrancies:
        - NFTAuction.getHighestBid() (contracts/examples/nft-auction/NFTAuction.sol#373-375)
        - NFTAuction.initialize(address,address,address,address,address,string[],uint256[],Config) (contracts/examples/nft-auction/NFTAuction.sol#176-215)
        - _highestBidder = msg.sender (contracts/examples/nft-auction/NFTAuction.sol#290)
        NFTAuction._highestBidder (contracts/examples/nft-auction/NFTAuction.sol#67) can be used in cross function reentrancies:
        - NFTAuction.getHighestBidder() (contracts/examples/nft-auction/NFTAuction.sol#364-366)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#reentrancy-vulnerabilities
INFO:Detectors:
ProofOfIdentity._attributes (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#72) is never initialized. It is used in:
        - ProofOfIdentity.getPrimaryID(address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#524-529)
        - ProofOfIdentity.getCountryCode(address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#545-550)
        - ProofOfIdentity.getProofOfLiveliness(address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#563-568)
        - ProofOfIdentity.getUserType(address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#582-587)
        - ProofOfIdentity.getCompetencyRating(address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#599-604)
        - ProofOfIdentity.getStringAttribute(uint256,address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#622-632)
        - ProofOfIdentity.getU256Attribute(uint256,address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#650-660)
        - ProofOfIdentity.getBoolAttribute(uint256,address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#678-688)
        - ProofOfIdentity.getBytesAttribute(uint256,address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#706-716)
        - ProofOfIdentity._setAttr(address,uint256,uint256,bytes) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#870-881)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#uninitialized-state-variables
INFO:Detectors:
Reentrancy in NFTAuction.startAuction() (contracts/examples/nft-auction/NFTAuction.sol#228-241):
        External calls:
        - _nft.transferFrom(msg.sender,address(this),_nftId) (contracts/examples/nft-auction/NFTAuction.sol#235)
        State variables written after the call(s):
        - _started = true (contracts/examples/nft-auction/NFTAuction.sol#237)
        NFTAuction._started (contracts/examples/nft-auction/NFTAuction.sol#40) can be used in cross function reentrancies:
        - NFTAuction.hasStarted() (contracts/examples/nft-auction/NFTAuction.sol#427-429)
        - NFTAuction.inProgress() (contracts/examples/nft-auction/NFTAuction.sol#443-445)
        - NFTAuction.startAuction() (contracts/examples/nft-auction/NFTAuction.sol#228-241)
Reentrancy in FeeContract.updateFee() (contracts/vendor/fee/FeeContract.sol#715-731):
        External calls:
        - _refreshOracle() (contracts/vendor/fee/FeeContract.sol#718)
                - IFeeOracle(_oracle).refreshOracle() (contracts/vendor/fee/FeeContract.sol#880)
        State variables written after the call(s):
        - _networkFeeResetTimestamp = feeUpdateEpoch + block.timestamp (contracts/vendor/fee/FeeContract.sol#727)
        FeeContract._networkFeeResetTimestamp (contracts/vendor/fee/FeeContract.sol#102) can be used in cross function reentrancies:
        - FeeContract.initialize(address,address[],uint256[],address,address,address,uint256,uint256,uint256,uint256) (contracts/vendor/fee/FeeContract.sol#340-416)
        - FeeContract.nextResetTime() (contracts/vendor/fee/FeeContract.sol#737-739)
        - FeeContract.updateFee() (contracts/vendor/fee/FeeContract.sol#715-731)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#reentrancy-vulnerabilities-1
INFO:Detectors:
NFTAuction._validateUserType(address) (contracts/examples/nft-auction/NFTAuction.sol#553-556) ignores return value by (user,exp,None) = _proofOfIdentity.getUserType(account) (contracts/examples/nft-auction/NFTAuction.sol#554)
NFTAuction._validateUserTypeExn(address) (contracts/examples/nft-auction/NFTAuction.sol#572-582) ignores return value by (user,exp,None) = _proofOfIdentity.getUserType(account) (contracts/examples/nft-auction/NFTAuction.sol#573)
FeeContract.initialize(address,address[],uint256[],address,address,address,uint256,uint256,uint256,uint256) (contracts/vendor/fee/FeeContract.sol#340-416) ignores return value by IFeeOracle(oracle).refreshOracle() (contracts/vendor/fee/FeeContract.sol#378)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#unused-return
INFO:Detectors:
SimpleStorage.initialize(address,address,address,address,string[],uint256[]).feeContract (contracts/examples/simple-storage/SimpleStorage.sol#75) shadows:
        - H1DevelopedApplication.feeContract() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#726-728) (function)
SimpleStorage.initialize(address,address,address,address,string[],uint256[]).association (contracts/examples/simple-storage/SimpleStorage.sol#76) shadows:
        - H1DevelopedApplication.association() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#734-736) (function)
SimpleStorage.initialize(address,address,address,address,string[],uint256[]).developer (contracts/examples/simple-storage/SimpleStorage.sol#77) shadows:
        - H1DevelopedApplication.developer() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#742-744) (function)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#local-variable-shadowing
INFO:Detectors:
H1DevelopedApplication.setAssociation(address).association_ (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#642) lacks a zero-check on :
                - _association = association_ (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#644)
H1DevelopedApplication.setDeveloper(address).developer_ (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#657) lacks a zero-check on :
                - _developer = developer_ (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#659)
H1DevelopedApplication.setDevFeeCollector(address).devFeeCollector_ (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#672) lacks a zero-check on :
                - _devFeeCollector = devFeeCollector_ (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#674)
H1DevelopedApplication.setDevFeeCollectorAdmin(address).devFeeCollector_ (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#687) lacks a zero-check on :
                - _devFeeCollector = devFeeCollector_ (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#689)
FeeContract.initialize(address,address[],uint256[],address,address,address,uint256,uint256,uint256,uint256).oracle (contracts/vendor/fee/FeeContract.sol#341) lacks a zero-check on :
                - _oracle = oracle (contracts/vendor/fee/FeeContract.sol#395)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#missing-zero-address-validation
INFO:Detectors:
FeeContract._distributeFees() (contracts/vendor/fee/FeeContract.sol#859-873) has external calls inside a loop: (sent,None) = _channels[i].call{value: share}() (contracts/vendor/fee/FeeContract.sol#865)
        Calls stack containing the loop:
                FeeContract.distributeFees()
FeeContract._distributeFees() (contracts/vendor/fee/FeeContract.sol#859-873) has external calls inside a loop: (sent,None) = _channels[i].call{value: share}() (contracts/vendor/fee/FeeContract.sol#865)
        Calls stack containing the loop:
                FeeContract.forceDistributeFees()
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation/#calls-inside-a-loop
INFO:Detectors:
Reentrancy in FeeContract._distributeFees() (contracts/vendor/fee/FeeContract.sol#859-873):
        External calls:
        - (sent,None) = _channels[i].call{value: share}() (contracts/vendor/fee/FeeContract.sol#865)
        State variables written after the call(s):
        - _lastDistribution = block.timestamp (contracts/vendor/fee/FeeContract.sol#872)
Reentrancy in SimpleStorage.decrementCount() (contracts/examples/simple-storage/SimpleStorage.sol#124-136):
        External calls:
        - developerFee(false,true) (contracts/examples/simple-storage/SimpleStorage.sol#128)
                - _feeContract.updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#818)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        External calls sending eth:
        - developerFee(false,true) (contracts/examples/simple-storage/SimpleStorage.sol#128)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        State variables written after the call(s):
        - _count -- (contracts/examples/simple-storage/SimpleStorage.sol#131)
Reentrancy in H1DevelopedApplication.developerFee(bool,bool) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#196-217):
        External calls:
        - _updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#197)
                - _feeContract.updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#818)
        State variables written after the call(s):
        - _msgValueAfterFee = (msg.value - fee) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#205)
Reentrancy in H1DevelopedApplication.developerFee(bool,bool) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#196-217):
        External calls:
        - _updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#197)
                - _feeContract.updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#818)
        - _payFee(fee) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#208)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        - _safeTransfer(msg.sender,address(this).balance) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#213)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        External calls sending eth:
        - _payFee(fee) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#208)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        - _safeTransfer(msg.sender,address(this).balance) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#213)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        State variables written after the call(s):
        - delete _msgValueAfterFee (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#216)
Reentrancy in SimpleStorage.incrementCount() (contracts/examples/simple-storage/SimpleStorage.sol#104-113):
        External calls:
        - developerFee(false,true) (contracts/examples/simple-storage/SimpleStorage.sol#108)
                - _feeContract.updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#818)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        External calls sending eth:
        - developerFee(false,true) (contracts/examples/simple-storage/SimpleStorage.sol#108)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        State variables written after the call(s):
        - _count ++ (contracts/examples/simple-storage/SimpleStorage.sol#110)
Reentrancy in FeeContract.initialize(address,address[],uint256[],address,address,address,uint256,uint256,uint256,uint256) (contracts/vendor/fee/FeeContract.sol#340-416):
        External calls:
        - IFeeOracle(oracle).refreshOracle() (contracts/vendor/fee/FeeContract.sol#378)
        State variables written after the call(s):
        - _asscShare = asscShare (contracts/vendor/fee/FeeContract.sol#383)
        - _channels.push(channel) (contracts/vendor/fee/FeeContract.sol#413)
        - _contractShares += weight (contracts/vendor/fee/FeeContract.sol#412)
        - _fee = (IFeeOracle(oracle).consult() * _feeUSD) / SCALE (contracts/vendor/fee/FeeContract.sol#385)
        - _feeUSD = 1 * SCALE (contracts/vendor/fee/FeeContract.sol#382)
        - _gracePeriod = gracePeriod (contracts/vendor/fee/FeeContract.sol#392)
        - _h1USD = IFeeOracle(oracle).consult() (contracts/vendor/fee/FeeContract.sol#386)
        - _lastDistribution = block.timestamp (contracts/vendor/fee/FeeContract.sol#387)
        - _maxDevFee = maxDevFee (contracts/vendor/fee/FeeContract.sol#381)
        - _minDevFee = minDevFee (contracts/vendor/fee/FeeContract.sol#380)
        - _networkFeeResetTimestamp = block.timestamp + feeUpdateEpoch (contracts/vendor/fee/FeeContract.sol#394)
        - _oracle = oracle (contracts/vendor/fee/FeeContract.sol#395)
        - _weights.push(weight) (contracts/vendor/fee/FeeContract.sol#414)
        - setDistributionEpoch(86400) (contracts/vendor/fee/FeeContract.sol#389)
                - distributionEpoch = newEpochLength (contracts/vendor/fee/FeeContract.sol#703)
        - setFeeUpdateEpoch(86400) (contracts/vendor/fee/FeeContract.sol#390)
                - feeUpdateEpoch = newEpochLength (contracts/vendor/fee/FeeContract.sol#689)
Reentrancy in NFTAuction.startAuction() (contracts/examples/nft-auction/NFTAuction.sol#228-241):
        External calls:
        - _nft.transferFrom(msg.sender,address(this),_nftId) (contracts/examples/nft-auction/NFTAuction.sol#235)
        State variables written after the call(s):
        - _auctionEndTime = block.timestamp + _auctionLength (contracts/examples/nft-auction/NFTAuction.sol#238)
Reentrancy in FeeContract.updateFee() (contracts/vendor/fee/FeeContract.sol#715-731):
        External calls:
        - _refreshOracle() (contracts/vendor/fee/FeeContract.sol#718)
                - IFeeOracle(_oracle).refreshOracle() (contracts/vendor/fee/FeeContract.sol#880)
        State variables written after the call(s):
        - _fee = (oracleVal * _feeUSD) / SCALE (contracts/vendor/fee/FeeContract.sol#722)
        - _feePrior = _fee (contracts/vendor/fee/FeeContract.sol#721)
        - _h1USD = oracleVal (contracts/vendor/fee/FeeContract.sol#725)
        - _h1USDPrev = _h1USD (contracts/vendor/fee/FeeContract.sol#724)
        - _networkFeeGraceTimestamp = block.timestamp + _gracePeriod (contracts/vendor/fee/FeeContract.sol#728)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#reentrancy-vulnerabilities-2
INFO:Detectors:
Reentrancy in H1DevelopedApplication._payFee(uint256) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#800-809):
        External calls:
        - _safeTransfer(address(_feeContract),feeToAssc) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#805)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        - _safeTransfer(_devFeeCollector,feeToDev) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#806)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        Event emitted after the call(s):
        - FeePaid(_fnSigs[msg.sig].toString(),feeToAssc,feeToDev) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#808)
Reentrancy in SimpleStorage.decrementCount() (contracts/examples/simple-storage/SimpleStorage.sol#124-136):
        External calls:
        - developerFee(false,true) (contracts/examples/simple-storage/SimpleStorage.sol#128)
                - _feeContract.updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#818)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        External calls sending eth:
        - developerFee(false,true) (contracts/examples/simple-storage/SimpleStorage.sol#128)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        Event emitted after the call(s):
        - Count(msg.sender,Direction.DECR,_count,fee) (contracts/examples/simple-storage/SimpleStorage.sol#135)
Reentrancy in H1DevelopedApplication.developerFee(bool,bool) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#196-217):
        External calls:
        - _updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#197)
                - _feeContract.updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#818)
        - _payFee(fee) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#208)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        External calls sending eth:
        - _payFee(fee) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#208)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        Event emitted after the call(s):
        - FeePaid(_fnSigs[msg.sig].toString(),feeToAssc,feeToDev) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#808)
                - _payFee(fee) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#208)
Reentrancy in SimpleStorage.incrementCount() (contracts/examples/simple-storage/SimpleStorage.sol#104-113):
        External calls:
        - developerFee(false,true) (contracts/examples/simple-storage/SimpleStorage.sol#108)
                - _feeContract.updateFee() (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#818)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        External calls sending eth:
        - developerFee(false,true) (contracts/examples/simple-storage/SimpleStorage.sol#108)
                - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
        Event emitted after the call(s):
        - Count(msg.sender,Direction.INCR,_count,fee) (contracts/examples/simple-storage/SimpleStorage.sol#112)
Reentrancy in FeeContract.initialize(address,address[],uint256[],address,address,address,uint256,uint256,uint256,uint256) (contracts/vendor/fee/FeeContract.sol#340-416):
        External calls:
        - IFeeOracle(oracle).refreshOracle() (contracts/vendor/fee/FeeContract.sol#378)
        Event emitted after the call(s):
        - DistributionEpochUpdated(newEpochLength) (contracts/vendor/fee/FeeContract.sol#704)
                - setDistributionEpoch(86400) (contracts/vendor/fee/FeeContract.sol#389)
        - FeeEpochUpdated(newEpochLength) (contracts/vendor/fee/FeeContract.sol#690)
                - setFeeUpdateEpoch(86400) (contracts/vendor/fee/FeeContract.sol#390)
Reentrancy in ProofOfIdentity.issueIdentity(address,bool,string,bool,uint256,uint256[4],string) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#263-301):
        External calls:
        - _permissionsInterface.assignAccountRole(account,ORG,VTCALL) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#298)
        Event emitted after the call(s):
        - IdentityIssued(account,id) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#300)
Reentrancy in NFTAuction.startAuction() (contracts/examples/nft-auction/NFTAuction.sol#228-241):
        External calls:
        - _nft.transferFrom(msg.sender,address(this),_nftId) (contracts/examples/nft-auction/NFTAuction.sol#235)
        Event emitted after the call(s):
        - AuctionStarted(_auctionEndTime) (contracts/examples/nft-auction/NFTAuction.sol#240)
Reentrancy in ProofOfIdentity.suspendAccount(address,string) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#491-497):
        External calls:
        - _permissionsInterface.updateAccountStatus(ORG,account,1) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#495)
        Event emitted after the call(s):
        - AccountSuspended(account,reason) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#496)
Reentrancy in ProofOfIdentity.unsuspendAccount(address) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#506-511):
        External calls:
        - _permissionsInterface.updateAccountStatus(ORG,account,2) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#509)
        Event emitted after the call(s):
        - AccountUnsuspended(account) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#510)
Reentrancy in FeeContract.updateFee() (contracts/vendor/fee/FeeContract.sol#715-731):
        External calls:
        - _refreshOracle() (contracts/vendor/fee/FeeContract.sol#718)
                - IFeeOracle(_oracle).refreshOracle() (contracts/vendor/fee/FeeContract.sol#880)
        Event emitted after the call(s):
        - FeeUpdated(_fee) (contracts/vendor/fee/FeeContract.sol#730)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#reentrancy-vulnerabilities-3
INFO:Detectors:
NFTAuction.accountEligible(address) (contracts/examples/nft-auction/NFTAuction.sol#355-357) uses timestamp for comparisons
        Dangerous comparisons:
        - _hasID(acc) && ! _isSuspended(acc) && _validateUserType(acc) (contracts/examples/nft-auction/NFTAuction.sol#356)
NFTAuction.hasFinished() (contracts/examples/nft-auction/NFTAuction.sol#435-437) uses timestamp for comparisons
        Dangerous comparisons:
        - _finished || block.timestamp > _auctionEndTime (contracts/examples/nft-auction/NFTAuction.sol#436)
NFTAuction.inProgress() (contracts/examples/nft-auction/NFTAuction.sol#443-445) uses timestamp for comparisons
        Dangerous comparisons:
        - _started && block.timestamp < _auctionEndTime (contracts/examples/nft-auction/NFTAuction.sol#444)
NFTAuction._validateExpiry(uint256) (contracts/examples/nft-auction/NFTAuction.sol#509-511) uses timestamp for comparisons
        Dangerous comparisons:
        - expiry > block.timestamp (contracts/examples/nft-auction/NFTAuction.sol#510)
NFTAuction._validateUserType(address) (contracts/examples/nft-auction/NFTAuction.sol#553-556) uses timestamp for comparisons
        Dangerous comparisons:
        - _hasType(user) && _validateExpiry(exp) (contracts/examples/nft-auction/NFTAuction.sol#555)
FeeContract.updateFee() (contracts/vendor/fee/FeeContract.sol#715-731) uses timestamp for comparisons
        Dangerous comparisons:
        - block.timestamp <= _networkFeeResetTimestamp (contracts/vendor/fee/FeeContract.sol#716)
FeeContract._getFeeForPayment() (contracts/vendor/fee/FeeContract.sol#942-947) uses timestamp for comparisons
        Dangerous comparisons:
        - _networkFeeGraceTimestamp > block.timestamp (contracts/vendor/fee/FeeContract.sol#943)
FeeContract._getDevH1USD() (contracts/vendor/fee/FeeContract.sol#954-959) uses timestamp for comparisons
        Dangerous comparisons:
        - _networkFeeGraceTimestamp > block.timestamp (contracts/vendor/fee/FeeContract.sol#955)
FeeContract._canDistribute() (contracts/vendor/fee/FeeContract.sol#975-977) uses timestamp for comparisons
        Dangerous comparisons:
        - block.timestamp > _lastDistribution + distributionEpoch (contracts/vendor/fee/FeeContract.sol#976)
ProofOfIdentity._validateExpiry(uint256) (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#932-934) uses timestamp for comparisons
        Dangerous comparisons:
        - expiry > block.timestamp (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#933)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#block-timestamp
INFO:Detectors:
FeeContract.initialize(address,address[],uint256[],address,address,address,uint256,uint256,uint256,uint256) (contracts/vendor/fee/FeeContract.sol#340-416) has costly operations inside a loop:
        - _contractShares += weight (contracts/vendor/fee/FeeContract.sol#412)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#costly-operations-inside-a-loop
INFO:Detectors:
Low level call in NFTAuction._withdraw(address,uint256) (contracts/examples/nft-auction/NFTAuction.sol#484-487):
        - (success,None) = address(to).call{value: amount}() (contracts/examples/nft-auction/NFTAuction.sol#485)
Low level call in FeeContract._distributeFees() (contracts/vendor/fee/FeeContract.sol#859-873):
        - (sent,None) = _channels[i].call{value: share}() (contracts/vendor/fee/FeeContract.sol#865)
Low level call in H1DevelopedApplication._safeTransfer(address,uint256) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#827-832):
        - (success,None) = to.call{value: amount}(new bytes(0)) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#828)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#low-level-calls
INFO:Detectors:
FeeContract (contracts/vendor/fee/FeeContract.sol#21-978) should inherit from IFeeContract (contracts/vendor/fee/interfaces/IFeeContract.sol#8-202)
FixedFeeOracle (contracts/vendor/mocks/FixedFeeOracle.sol#6-37) should inherit from IFeeOracle (contracts/vendor/fee/interfaces/IFeeOracle.sol#6-14)
ProofOfIdentity (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#45-935) should inherit from IProofOfIdentity (contracts/vendor/proof-of-identity/interfaces/IProofOfIdentity.sol#9-325)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#missing-inheritance
INFO:Detectors:
Parameter FeeContract.addChannel(address,uint256)._newChannelAddress (contracts/vendor/fee/FeeContract.sol#434) is not in mixedCase
Parameter FeeContract.addChannel(address,uint256)._weight (contracts/vendor/fee/FeeContract.sol#435) is not in mixedCase
Parameter FeeContract.adjustChannel(address,address,uint256)._oldChannelAddress (contracts/vendor/fee/FeeContract.sol#472) is not in mixedCase
Parameter FeeContract.adjustChannel(address,address,uint256)._newChannelAddress (contracts/vendor/fee/FeeContract.sol#473) is not in mixedCase
Parameter FeeContract.adjustChannel(address,address,uint256)._newWeight (contracts/vendor/fee/FeeContract.sol#474) is not in mixedCase
Parameter FeeContract.removeChannel(address)._channel (contracts/vendor/fee/FeeContract.sol#509) is not in mixedCase
Function H1DevelopedApplication.__H1DevelopedApplication_init(address,address,address,address,string[],uint256[]) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#247-266) is not in mixedCase
Function H1DevelopedApplication.__H1DevelopedApplication_init_unchained(address,address,address,address,string[],uint256[]) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#271-313) is not in mixedCase
Variable H1DevelopedApplication.__gap (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#865) is not in mixedCase
Function H1DevelopedAccessControl.__H1DevelopedAccessControl_init(address,address) (contracts/vendor/h1-developed-application/components/H1DevelopedAccessControl.sol#57-62) is not in mixedCase
Function H1DevelopedAccessControl.__H1DevelopedAccessControl_init_unchained(address,address) (contracts/vendor/h1-developed-application/components/H1DevelopedAccessControl.sol#67-82) is not in mixedCase
Variable H1DevelopedAccessControl.__gap (contracts/vendor/h1-developed-application/components/H1DevelopedAccessControl.sol#97) is not in mixedCase
Function H1DevelopedPausable.__H1DevelopedPausable_init() (contracts/vendor/h1-developed-application/components/H1DevelopedPausable.sol#34-37) is not in mixedCase
Function H1DevelopedPausable.__H1DevelopedPausable_init_unchained() (contracts/vendor/h1-developed-application/components/H1DevelopedPausable.sol#42) is not in mixedCase
Variable H1DevelopedPausable.__gap (contracts/vendor/h1-developed-application/components/H1DevelopedPausable.sol#80) is not in mixedCase
Parameter MockAccountManager.updateAccountStatus(string,address,uint256)._account (contracts/vendor/mocks/MockAccountManager.sol#38) is not in mixedCase
Parameter MockAccountManager.updateAccountStatus(string,address,uint256)._action (contracts/vendor/mocks/MockAccountManager.sol#39) is not in mixedCase
Parameter MockAccountManager.assignAccountRole(address,string,string,bool)._account (contracts/vendor/mocks/MockAccountManager.sol#52) is not in mixedCase
Parameter MockPermissionsInterface.assignAccountRole(address,string,string)._account (contracts/vendor/mocks/MockPermissionsInterface.sol#15) is not in mixedCase
Parameter MockPermissionsInterface.assignAccountRole(address,string,string)._orgId (contracts/vendor/mocks/MockPermissionsInterface.sol#16) is not in mixedCase
Parameter MockPermissionsInterface.assignAccountRole(address,string,string)._roleId (contracts/vendor/mocks/MockPermissionsInterface.sol#17) is not in mixedCase
Parameter MockPermissionsInterface.updateAccountStatus(string,address,uint256)._orgId (contracts/vendor/mocks/MockPermissionsInterface.sol#23) is not in mixedCase
Parameter MockPermissionsInterface.updateAccountStatus(string,address,uint256)._account (contracts/vendor/mocks/MockPermissionsInterface.sol#24) is not in mixedCase
Parameter MockPermissionsInterface.updateAccountStatus(string,address,uint256)._action (contracts/vendor/mocks/MockPermissionsInterface.sol#25) is not in mixedCase
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#conformance-to-solidity-naming-conventions
INFO:Detectors:
Loop condition i < _channels.length (contracts/vendor/fee/FeeContract.sol#862) should use cached array length instead of referencing `length` member of the storage array.
 Loop condition i < _channels.length (contracts/vendor/fee/FeeContract.sol#903) should use cached array length instead of referencing `length` member of the storage array.
 Loop condition i < _channels.length (contracts/vendor/fee/FeeContract.sol#928) should use cached array length instead of referencing `length` member of the storage array.
 Loop condition i < _feeProposals.length (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#547) should use cached array length instead of referencing `length` member of the storage array.
 Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#cache-array-length
INFO:Detectors:
MockNFT._maxSupply (contracts/vendor/mocks/MockNFT.sol#14) should be immutable
MockPermissionsInterface._accountManager (contracts/vendor/mocks/MockPermissionsInterface.sol#8) should be immutable
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#state-variables-that-could-be-declared-immutable
INFO:Slither:. analyzed (58 contracts with 100 detectors), 85 result(s) found
PS D:\Haven1\dev-onboarding-template>
