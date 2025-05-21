# chet


PS D:\Haven1\dev-onboarding-template> slither .
'npx hardhat clean' running (wd: D:\Haven1\dev-onboarding-template)
'npx hardhat clean --global' running (wd: D:\Haven1\dev-onboarding-template)
'npx hardhat compile --force' running (wd: D:\Haven1\dev-onboarding-template)
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
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) has bitwise-xor operator ^ instead of the exponentiation operator **:
         - inverse = (3 * denominator) ^ 2 (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#116)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) has bitwise-xor operator ^ instead of the exponentiation operator **:
         - inverse = (3 * denominator) ^ 2 (node_modules/@openzeppelin/contracts/utils/math/Math.sol#116)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#incorrect-exponentiation
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
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#101)
        - inverse = (3 * denominator) ^ 2 (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#116)
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#120)
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#121)
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#122)
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#123)
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#124)
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#125)
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) performs a multiplication on the result of a division:
        - prod0 = prod0 / twos (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#104)
        - result = prod0 * inverse (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#131)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts/utils/math/Math.sol#101)
        - inverse = (3 * denominator) ^ 2 (node_modules/@openzeppelin/contracts/utils/math/Math.sol#116)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts/utils/math/Math.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts/utils/math/Math.sol#120)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts/utils/math/Math.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts/utils/math/Math.sol#121)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts/utils/math/Math.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts/utils/math/Math.sol#122)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts/utils/math/Math.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts/utils/math/Math.sol#123)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts/utils/math/Math.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts/utils/math/Math.sol#124)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) performs a multiplication on the result of a division:
        - denominator = denominator / twos (node_modules/@openzeppelin/contracts/utils/math/Math.sol#101)
        - inverse *= 2 - denominator * inverse (node_modules/@openzeppelin/contracts/utils/math/Math.sol#125)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) performs a multiplication on the result of a division:
        - prod0 = prod0 / twos (node_modules/@openzeppelin/contracts/utils/math/Math.sol#104)
        - result = prod0 * inverse (node_modules/@openzeppelin/contracts/utils/math/Math.sol#131)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#divide-before-multiply
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
ERC1967UpgradeUpgradeable._upgradeToAndCall(address,bytes,bool) (node_modules/@openzeppelin/contracts-upgradeable/proxy/ERC1967/ERC1967UpgradeUpgradeable.sol#65-70) ignores return value by AddressUpgradeable.functionDelegateCall(newImplementation,data) (node_modules/@openzeppelin/contracts-upgradeable/proxy/ERC1967/ERC1967UpgradeUpgradeable.sol#68)
ERC1967UpgradeUpgradeable._upgradeBeaconToAndCall(address,bytes,bool) (node_modules/@openzeppelin/contracts-upgradeable/proxy/ERC1967/ERC1967UpgradeUpgradeable.sol#156-162) ignores return value by AddressUpgradeable.functionDelegateCall(IBeaconUpgradeable(newBeacon).implementation(),data) (node_modules/@openzeppelin/contracts-upgradeable/proxy/ERC1967/ERC1967UpgradeUpgradeable.sol#160)
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
ProofOfIdentity.addAttribute(string,SupportedAttributeType).name (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#455) shadows:
        - ERC721Upgradeable.name() (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#84-86) (function)
        - IERC721MetadataUpgradeable.name() (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/extensions/IERC721MetadataUpgradeable.sol#16) (function)
ProofOfIdentity.setAttributeName(uint256,string).name (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#779) shadows:
        - ERC721Upgradeable.name() (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#84-86) (function)
        - IERC721MetadataUpgradeable.name() (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/extensions/IERC721MetadataUpgradeable.sol#16) (function)
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
Reentrancy in NFTAuction.initialize(address,address,address,address,address,string[],uint256[],Config) (contracts/examples/nft-auction/NFTAuction.sol#176-215):
        External calls:
        - __H1DevelopedApplication_init(feeContract_,association_,developer_,feeCollector_,fnSigs_,fnFees_) (contracts/examples/nft-auction/NFTAuction.sol#194-201)
                - IFeeContract(feeContract_).setGraceContract(true) (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#312)
        State variables written after the call(s):
        - _auctionKind = auctionConfig_.kind (contracts/examples/nft-auction/NFTAuction.sol#209)
        - _auctionLength = auctionConfig_.length (contracts/examples/nft-auction/NFTAuction.sol#210)
        - _beneficiary = auctionConfig_.beneficiary (contracts/examples/nft-auction/NFTAuction.sol#214)
        - _highestBid = auctionConfig_.startingBid (contracts/examples/nft-auction/NFTAuction.sol#211)
        - _nft = IERC721Upgradeable(auctionConfig_.nft) (contracts/examples/nft-auction/NFTAuction.sol#212)
        - _nftId = auctionConfig_.nftID (contracts/examples/nft-auction/NFTAuction.sol#213)
        - _proofOfIdentity = IProofOfIdentity(proofOfIdentity_) (contracts/examples/nft-auction/NFTAuction.sol#207)
        - __ReentrancyGuard_init() (contracts/examples/nft-auction/NFTAuction.sol#203)
                - _status = _NOT_ENTERED (node_modules/@openzeppelin/contracts-upgradeable/security/ReentrancyGuardUpgradeable.sol#45)
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
ERC721Upgradeable._checkOnERC721Received(address,address,uint256,bytes) (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#404-426) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#418-420)
AddressUpgradeable._revert(bytes,string) (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#231-243) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#236-239)
StorageSlotUpgradeable.getAddressSlot(bytes32) (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#62-67) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#64-66)
StorageSlotUpgradeable.getBooleanSlot(bytes32) (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#72-77) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#74-76)
StorageSlotUpgradeable.getBytes32Slot(bytes32) (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#82-87) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#84-86)
StorageSlotUpgradeable.getUint256Slot(bytes32) (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#92-97) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#94-96)
StorageSlotUpgradeable.getStringSlot(bytes32) (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#102-107) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#104-106)
StorageSlotUpgradeable.getStringSlot(string) (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#112-117) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#114-116)
StorageSlotUpgradeable.getBytesSlot(bytes32) (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#122-127) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#124-126)
StorageSlotUpgradeable.getBytesSlot(bytes) (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#132-137) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#134-136)
StringsUpgradeable.toString(uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/StringsUpgradeable.sol#19-39) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StringsUpgradeable.sol#25-27)
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/StringsUpgradeable.sol#31-33)
MathUpgradeable.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#55-134) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#62-66)
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#85-92)
        - INLINE ASM (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#99-108)
ERC721._checkOnERC721Received(address,address,uint256,bytes) (node_modules/@openzeppelin/contracts/token/ERC721/ERC721.sol#399-421) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts/token/ERC721/ERC721.sol#413-415)
Address._revert(bytes,string) (node_modules/@openzeppelin/contracts/utils/Address.sol#231-243) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts/utils/Address.sol#236-239)
Strings.toString(uint256) (node_modules/@openzeppelin/contracts/utils/Strings.sol#19-39) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts/utils/Strings.sol#25-27)
        - INLINE ASM (node_modules/@openzeppelin/contracts/utils/Strings.sol#31-33)
Math.mulDiv(uint256,uint256,uint256) (node_modules/@openzeppelin/contracts/utils/math/Math.sol#55-134) uses assembly
        - INLINE ASM (node_modules/@openzeppelin/contracts/utils/math/Math.sol#62-66)
        - INLINE ASM (node_modules/@openzeppelin/contracts/utils/math/Math.sol#85-92)
        - INLINE ASM (node_modules/@openzeppelin/contracts/utils/math/Math.sol#99-108)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#assembly-usage
INFO:Detectors:
3 different versions of Solidity are used:
        - Version constraint ^0.8.0 is used by:
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/access/AccessControlUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/access/IAccessControlUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/interfaces/IERC1967Upgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/interfaces/draft-IERC1822Upgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/proxy/beacon/IBeaconUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/security/PausableUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/security/ReentrancyGuardUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/IERC721ReceiverUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/IERC721Upgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/extensions/IERC721MetadataUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/ContextUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#5)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/StringsUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/introspection/IERC165Upgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/math/SignedMathUpgradeable.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/access/AccessControl.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/access/IAccessControl.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/token/ERC721/ERC721.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/token/ERC721/IERC721.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/token/ERC721/IERC721Receiver.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/token/ERC721/extensions/IERC721Metadata.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/utils/Context.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/utils/Strings.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/utils/introspection/ERC165.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/utils/introspection/IERC165.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/utils/math/Math.sol#4)
                -^0.8.0 (node_modules/@openzeppelin/contracts/utils/math/SignedMath.sol#4)
                -^0.8.0 (contracts/examples/nft-auction/NFTAuction.sol#2)
                -^0.8.0 (contracts/examples/nft-auction/components/Errors.sol#2)
                -^0.8.0 (contracts/examples/nft-auction/components/NFTAuctionConfig.sol#2)
                -^0.8.0 (contracts/examples/simple-storage/SimpleStorage.sol#3)
                -^0.8.0 (contracts/vendor/fee/FeeContract.sol#2)
                -^0.8.0 (contracts/vendor/fee/interfaces/IFeeContract.sol#2)
                -^0.8.0 (contracts/vendor/fee/interfaces/IFeeOracle.sol#2)
                -^0.8.0 (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#3)
                -^0.8.0 (contracts/vendor/h1-developed-application/components/Errors.sol#3)
                -^0.8.0 (contracts/vendor/h1-developed-application/components/H1DevelopedAccessControl.sol#3)
                -^0.8.0 (contracts/vendor/h1-developed-application/components/H1DevelopedPausable.sol#3)
                -^0.8.0 (contracts/vendor/h1-developed-application/components/H1DevelopedUtils.sol#3)
                -^0.8.0 (contracts/vendor/h1-developed-application/interfaces/IH1DevelopedApplication.sol#2)
                -^0.8.0 (contracts/vendor/h1-developed-application/interfaces/IH1DevelopedPausable.sol#2)
                -^0.8.0 (contracts/vendor/mocks/FixedFeeOracle.sol#2)
                -^0.8.0 (contracts/vendor/mocks/MockAccountManager.sol#2)
                -^0.8.0 (contracts/vendor/mocks/MockNFT.sol#2)
                -^0.8.0 (contracts/vendor/mocks/MockPermissionsInterface.sol#2)
                -^0.8.0 (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#2)
                -^0.8.0 (contracts/vendor/proof-of-identity/interfaces/IProofOfIdentity.sol#2)
                -^0.8.0 (contracts/vendor/proof-of-identity/interfaces/vendor/IAccountManager.sol#2)
                -^0.8.0 (contracts/vendor/proof-of-identity/interfaces/vendor/IPermissionsInterface.sol#2)
                -^0.8.0 (contracts/vendor/proof-of-identity/libraries/AttributeUtils.sol#3)
                -^0.8.0 (contracts/vendor/proof-of-identity/libraries/BytesConversion.sol#3)
        - Version constraint ^0.8.2 is used by:
                -^0.8.2 (node_modules/@openzeppelin/contracts-upgradeable/proxy/ERC1967/ERC1967UpgradeUpgradeable.sol#4)
                -^0.8.2 (node_modules/@openzeppelin/contracts-upgradeable/proxy/utils/Initializable.sol#4)
        - Version constraint ^0.8.1 is used by:
                -^0.8.1 (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#4)
                -^0.8.1 (node_modules/@openzeppelin/contracts/utils/Address.sol#4)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#different-pragma-directives-are-used
INFO:Detectors:
FeeContract.initialize(address,address[],uint256[],address,address,address,uint256,uint256,uint256,uint256) (contracts/vendor/fee/FeeContract.sol#340-416) has costly operations inside a loop:
        - _contractShares += weight (contracts/vendor/fee/FeeContract.sol#412)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#costly-operations-inside-a-loop
INFO:Detectors:
Version constraint ^0.8.0 contains known severe issues (https://solidity.readthedocs.io/en/latest/bugs.html)
        - FullInlinerNonExpressionSplitArgumentEvaluationOrder
        - MissingSideEffectsOnSelectorAccess
        - AbiReencodingHeadOverflowWithStaticArrayCleanup
        - DirtyBytesArrayToStorage
        - DataLocationChangeInInternalOverride
        - NestedCalldataArrayAbiReencodingSizeValidation
        - SignedImmutables
        - ABIDecodeTwoDimensionalArrayMemory
        - KeccakCaching.
It is used by:
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/access/AccessControlUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/access/IAccessControlUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/interfaces/IERC1967Upgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/interfaces/draft-IERC1822Upgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/proxy/beacon/IBeaconUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/security/PausableUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/security/ReentrancyGuardUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/IERC721ReceiverUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/IERC721Upgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/extensions/IERC721MetadataUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/ContextUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/StorageSlotUpgradeable.sol#5)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/StringsUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/introspection/IERC165Upgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/math/MathUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts-upgradeable/utils/math/SignedMathUpgradeable.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/access/AccessControl.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/access/IAccessControl.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/token/ERC721/ERC721.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/token/ERC721/IERC721.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/token/ERC721/IERC721Receiver.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/token/ERC721/extensions/IERC721Metadata.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/utils/Context.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/utils/Strings.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/utils/introspection/ERC165.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/utils/introspection/IERC165.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/utils/math/Math.sol#4)
        - ^0.8.0 (node_modules/@openzeppelin/contracts/utils/math/SignedMath.sol#4)
        - ^0.8.0 (contracts/examples/nft-auction/NFTAuction.sol#2)
        - ^0.8.0 (contracts/examples/nft-auction/components/Errors.sol#2)
        - ^0.8.0 (contracts/examples/nft-auction/components/NFTAuctionConfig.sol#2)
        - ^0.8.0 (contracts/examples/simple-storage/SimpleStorage.sol#3)
        - ^0.8.0 (contracts/vendor/fee/FeeContract.sol#2)
        - ^0.8.0 (contracts/vendor/fee/interfaces/IFeeContract.sol#2)
        - ^0.8.0 (contracts/vendor/fee/interfaces/IFeeOracle.sol#2)
        - ^0.8.0 (contracts/vendor/h1-developed-application/H1DevelopedApplication.sol#3)
        - ^0.8.0 (contracts/vendor/h1-developed-application/components/Errors.sol#3)
        - ^0.8.0 (contracts/vendor/h1-developed-application/components/H1DevelopedAccessControl.sol#3)
        - ^0.8.0 (contracts/vendor/h1-developed-application/components/H1DevelopedPausable.sol#3)
        - ^0.8.0 (contracts/vendor/h1-developed-application/components/H1DevelopedUtils.sol#3)
        - ^0.8.0 (contracts/vendor/h1-developed-application/interfaces/IH1DevelopedApplication.sol#2)
        - ^0.8.0 (contracts/vendor/h1-developed-application/interfaces/IH1DevelopedPausable.sol#2)
        - ^0.8.0 (contracts/vendor/mocks/FixedFeeOracle.sol#2)
        - ^0.8.0 (contracts/vendor/mocks/MockAccountManager.sol#2)
        - ^0.8.0 (contracts/vendor/mocks/MockNFT.sol#2)
        - ^0.8.0 (contracts/vendor/mocks/MockPermissionsInterface.sol#2)
        - ^0.8.0 (contracts/vendor/proof-of-identity/ProofOfIdentity.sol#2)
        - ^0.8.0 (contracts/vendor/proof-of-identity/interfaces/IProofOfIdentity.sol#2)
        - ^0.8.0 (contracts/vendor/proof-of-identity/interfaces/vendor/IAccountManager.sol#2)
        - ^0.8.0 (contracts/vendor/proof-of-identity/interfaces/vendor/IPermissionsInterface.sol#2)
        - ^0.8.0 (contracts/vendor/proof-of-identity/libraries/AttributeUtils.sol#3)
        - ^0.8.0 (contracts/vendor/proof-of-identity/libraries/BytesConversion.sol#3)
Version constraint ^0.8.2 contains known severe issues (https://solidity.readthedocs.io/en/latest/bugs.html)
        - FullInlinerNonExpressionSplitArgumentEvaluationOrder
        - MissingSideEffectsOnSelectorAccess
        - AbiReencodingHeadOverflowWithStaticArrayCleanup
        - DirtyBytesArrayToStorage
        - DataLocationChangeInInternalOverride
        - NestedCalldataArrayAbiReencodingSizeValidation
        - SignedImmutables
        - ABIDecodeTwoDimensionalArrayMemory
        - KeccakCaching.
It is used by:
        - ^0.8.2 (node_modules/@openzeppelin/contracts-upgradeable/proxy/ERC1967/ERC1967UpgradeUpgradeable.sol#4)
        - ^0.8.2 (node_modules/@openzeppelin/contracts-upgradeable/proxy/utils/Initializable.sol#4)
Version constraint ^0.8.1 contains known severe issues (https://solidity.readthedocs.io/en/latest/bugs.html)
        - FullInlinerNonExpressionSplitArgumentEvaluationOrder
        - MissingSideEffectsOnSelectorAccess
        - AbiReencodingHeadOverflowWithStaticArrayCleanup
        - DirtyBytesArrayToStorage
        - DataLocationChangeInInternalOverride
        - NestedCalldataArrayAbiReencodingSizeValidation
        - SignedImmutables
        - ABIDecodeTwoDimensionalArrayMemory
        - KeccakCaching.
It is used by:
        - ^0.8.1 (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#4)
        - ^0.8.1 (node_modules/@openzeppelin/contracts/utils/Address.sol#4)
Reference: https://github.com/crytic/slither/wiki/Detector-Documentation#incorrect-versions-of-solidity
INFO:Detectors:
Low level call in AddressUpgradeable.sendValue(address,uint256) (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#64-69):
        - (success,None) = recipient.call{value: amount}() (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#67)
Low level call in AddressUpgradeable.functionCallWithValue(address,bytes,uint256,string) (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#128-137):
        - (success,returndata) = target.call{value: value}(data) (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#135)
Low level call in AddressUpgradeable.functionStaticCall(address,bytes,string) (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#155-162):
        - (success,returndata) = target.staticcall(data) (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#160)
Low level call in AddressUpgradeable.functionDelegateCall(address,bytes,string) (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#180-187):
        - (success,returndata) = target.delegatecall(data) (node_modules/@openzeppelin/contracts-upgradeable/utils/AddressUpgradeable.sol#185)
Low level call in Address.sendValue(address,uint256) (node_modules/@openzeppelin/contracts/utils/Address.sol#64-69):
        - (success,None) = recipient.call{value: amount}() (node_modules/@openzeppelin/contracts/utils/Address.sol#67)
Low level call in Address.functionCallWithValue(address,bytes,uint256,string) (node_modules/@openzeppelin/contracts/utils/Address.sol#128-137):
        - (success,returndata) = target.call{value: value}(data) (node_modules/@openzeppelin/contracts/utils/Address.sol#135)
Low level call in Address.functionStaticCall(address,bytes,string) (node_modules/@openzeppelin/contracts/utils/Address.sol#155-162):
        - (success,returndata) = target.staticcall(data) (node_modules/@openzeppelin/contracts/utils/Address.sol#160)
Low level call in Address.functionDelegateCall(address,bytes,string) (node_modules/@openzeppelin/contracts/utils/Address.sol#180-187):
        - (success,returndata) = target.delegatecall(data) (node_modules/@openzeppelin/contracts/utils/Address.sol#185)
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
Function AccessControlUpgradeable.__AccessControl_init() (node_modules/@openzeppelin/contracts-upgradeable/access/AccessControlUpgradeable.sol#76-77) is not in mixedCase
Function AccessControlUpgradeable.__AccessControl_init_unchained() (node_modules/@openzeppelin/contracts-upgradeable/access/AccessControlUpgradeable.sol#79-80) is not in mixedCase
Variable AccessControlUpgradeable.__gap (node_modules/@openzeppelin/contracts-upgradeable/access/AccessControlUpgradeable.sol#260) is not in mixedCase
Function ERC1967UpgradeUpgradeable.__ERC1967Upgrade_init() (node_modules/@openzeppelin/contracts-upgradeable/proxy/ERC1967/ERC1967UpgradeUpgradeable.sol#30-31) is not in mixedCase
Function ERC1967UpgradeUpgradeable.__ERC1967Upgrade_init_unchained() (node_modules/@openzeppelin/contracts-upgradeable/proxy/ERC1967/ERC1967UpgradeUpgradeable.sol#33-34) is not in mixedCase
Variable ERC1967UpgradeUpgradeable.__gap (node_modules/@openzeppelin/contracts-upgradeable/proxy/ERC1967/ERC1967UpgradeUpgradeable.sol#169) is not in mixedCase
Function UUPSUpgradeable.__UUPSUpgradeable_init() (node_modules/@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol#48-49) is not in mixedCase
Function UUPSUpgradeable.__UUPSUpgradeable_init_unchained() (node_modules/@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol#51-52) is not in mixedCase
Variable UUPSUpgradeable.__self (node_modules/@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol#24) is not in mixedCase
Variable UUPSUpgradeable.__gap (node_modules/@openzeppelin/contracts-upgradeable/proxy/utils/UUPSUpgradeable.sol#111) is not in mixedCase
Function PausableUpgradeable.__Pausable_init() (node_modules/@openzeppelin/contracts-upgradeable/security/PausableUpgradeable.sol#34-36) is not in mixedCase
Function PausableUpgradeable.__Pausable_init_unchained() (node_modules/@openzeppelin/contracts-upgradeable/security/PausableUpgradeable.sol#38-40) is not in mixedCase
Variable PausableUpgradeable.__gap (node_modules/@openzeppelin/contracts-upgradeable/security/PausableUpgradeable.sol#116) is not in mixedCase
Function ReentrancyGuardUpgradeable.__ReentrancyGuard_init() (node_modules/@openzeppelin/contracts-upgradeable/security/ReentrancyGuardUpgradeable.sol#40-42) is not in mixedCase
Function ReentrancyGuardUpgradeable.__ReentrancyGuard_init_unchained() (node_modules/@openzeppelin/contracts-upgradeable/security/ReentrancyGuardUpgradeable.sol#44-46) is not in mixedCase
Variable ReentrancyGuardUpgradeable.__gap (node_modules/@openzeppelin/contracts-upgradeable/security/ReentrancyGuardUpgradeable.sol#88) is not in mixedCase
Function ERC721Upgradeable.__ERC721_init(string,string) (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#45-47) is not in mixedCase
Function ERC721Upgradeable.__ERC721_init_unchained(string,string) (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#49-52) is not in mixedCase
Function ERC721Upgradeable.__unsafe_increaseBalance(address,uint256) (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#468-470) is not in mixedCase
Variable ERC721Upgradeable.__gap (node_modules/@openzeppelin/contracts-upgradeable/token/ERC721/ERC721Upgradeable.sol#477) is not in mixedCase
Function ContextUpgradeable.__Context_init() (node_modules/@openzeppelin/contracts-upgradeable/utils/ContextUpgradeable.sol#18-19) is not in mixedCase
Function ContextUpgradeable.__Context_init_unchained() (node_modules/@openzeppelin/contracts-upgradeable/utils/ContextUpgradeable.sol#21-22) is not in mixedCase
Variable ContextUpgradeable.__gap (node_modules/@openzeppelin/contracts-upgradeable/utils/ContextUpgradeable.sol#40) is not in mixedCase
Function ERC165Upgradeable.__ERC165_init() (node_modules/@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol#24-25) is not in mixedCase
Function ERC165Upgradeable.__ERC165_init_unchained() (node_modules/@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol#27-28) is not in mixedCase
Variable ERC165Upgradeable.__gap (node_modules/@openzeppelin/contracts-upgradeable/utils/introspection/ERC165Upgradeable.sol#41) is not in mixedCase
Function ERC721.__unsafe_increaseBalance(address,uint256) (node_modules/@openzeppelin/contracts/token/ERC721/ERC721.sol#463-465) is not in mixedCase
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
INFO:Slither:. analyzed (58 contracts with 100 detectors), 163 result(s) found
PS D:\Haven1\dev-onboarding-template> AFTER STEP 4
