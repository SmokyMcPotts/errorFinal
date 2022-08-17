# errorFinal
error message given:

Error: Protect failed: expected UInt but got function (amt, decimals) {
    if (decimals === void 0) { decimals = defaultDecs; }
    if (!(Number.isInteger(decimals) && 0 <= decimals)) {
        throw Error("Expected decimals to be a nonnegative integer, but got ".concat(decimals, "."));
    }
    var _a = __read(amt.toString().split('.')), amtL = _a[0], amtR = _a[1], amtMore = _a.slice(2);
    if (amtMore.length > 0) {
        throw Error("malformed input: parseCurrency('".concat(amt, "')"));
    }
    var amtStr = "".concat(amtL, ".").concat((amtR || '').slice(0, decimals));
    return (0, CBR_1.bigNumberify)(ethers_1.ethers.utils.parseUnits(amtStr, decimals));
}: for Alice's interact field wager
Error: invalid BigNumber string (argument="value", value="function (amt, decimals) {\n    if (decimals === void 0) { decimals = defaultDecs; }\n    if (!(Number.isInteger(decimals) && 0 <= decimals)) {\n        throw Error(\"Expected decimals to be a nonnegative integer, but got \".concat(decimals, \".\"));\n    }\n    var _a = __read(amt.toString().split('.')), amtL = _a[0], amtR = _a[1], amtMore = _a.slice(2);\n    if (amtMore.length > 0) {\n        throw Error(\"malformed input: parseCurrency('\".concat(amt, \"')\"));\n    }\n    var amtStr = \"\".concat(amtL, \".\").concat((amtR || '').slice(0, decimals));\n    return (0, CBR_1.bigNumberify)(ethers_1.ethers.utils.parseUnits(amtStr, decimals));\n}", code=INVALID_ARGUMENT, version=bignumber/5.6.2)
    at Object.protect (/stdlib/dist/cjs/shared_backend.js:181:15)
    at Alice (file:///app/build/index.main.mjs:53:23)
    at /stdlib/dist/cjs/shared_impl.js:268:20
    at file:///app/index.mjs:105:7
    at processTicksAndRejections (node:internal/process/task_queues:96:5)
