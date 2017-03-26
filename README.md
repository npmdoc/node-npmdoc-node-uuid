# api documentation for  [node-uuid (v1.4.8)](https://github.com/broofa/node-uuid)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-node-uuid.svg)](https://travis-ci.org/npmdoc/node-npmdoc-node-uuid)
#### Rigorous implementation of RFC4122 (v1 and v4) UUIDs.

[![NPM](https://nodei.co/npm/node-uuid.png?downloads=true)](https://www.npmjs.com/package/node-uuid)

[![apidoc](https://npmdoc.github.io/node-npmdoc-node-uuid/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-node-uuid_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-node-uuid/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-node-uuid/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Robert Kieffer",
        "email": "robert@broofa.com"
    },
    "bin": {
        "uuid": "./bin/uuid"
    },
    "bugs": {
        "url": "https://github.com/broofa/node-uuid/issues"
    },
    "contributors": [
        {
            "name": "AJ ONeal",
            "email": "coolaj86@gmail.com"
        },
        {
            "name": "Christoph Tavan",
            "email": "dev@tavan.de"
        }
    ],
    "dependencies": {},
    "deprecated": "Use uuid module instead",
    "description": "Rigorous implementation of RFC4122 (v1 and v4) UUIDs.",
    "devDependencies": {
        "nyc": "^2.2.0"
    },
    "directories": {},
    "dist": {
        "shasum": "b040eb0923968afabf8d32fb1f17f1167fdab907",
        "tarball": "https://registry.npmjs.org/node-uuid/-/node-uuid-1.4.8.tgz"
    },
    "gitHead": "6f0f31b997cd6bec7919223e8897454350ed820f",
    "homepage": "https://github.com/broofa/node-uuid",
    "installable": true,
    "keywords": [
        "guid",
        "rfc4122",
        "uuid"
    ],
    "lib": ".",
    "licenses": [
        {
            "type": "MIT",
            "url": "https://raw.github.com/broofa/node-uuid/master/LICENSE.md"
        }
    ],
    "main": "./uuid.js",
    "maintainers": [
        {
            "name": "broofa",
            "email": "robert@broofa.com"
        },
        {
            "name": "defunctzombie",
            "email": "shtylman@gmail.com"
        }
    ],
    "name": "node-uuid",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/broofa/node-uuid.git"
    },
    "scripts": {
        "coverage": "nyc npm test && nyc report",
        "test": "node test/test.js"
    },
    "url": "http://github.com/broofa/node-uuid",
    "version": "1.4.8"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module node-uuid](#apidoc.module.node-uuid)
1.  [function <span class="apidocSignatureSpan">node-uuid.</span>BufferClass (arg, encodingOrOffset, length)](#apidoc.element.node-uuid.BufferClass)
1.  [function <span class="apidocSignatureSpan">node-uuid.</span>_nodeRNG ()](#apidoc.element.node-uuid._nodeRNG)
1.  [function <span class="apidocSignatureSpan">node-uuid.</span>_rng ()](#apidoc.element.node-uuid._rng)
1.  [function <span class="apidocSignatureSpan">node-uuid.</span>parse (s, buf, offset)](#apidoc.element.node-uuid.parse)
1.  [function <span class="apidocSignatureSpan">node-uuid.</span>unparse (buf, offset)](#apidoc.element.node-uuid.unparse)
1.  [function <span class="apidocSignatureSpan">node-uuid.</span>v1 (options, buf, offset)](#apidoc.element.node-uuid.v1)
1.  [function <span class="apidocSignatureSpan">node-uuid.</span>v4 (options, buf, offset)](#apidoc.element.node-uuid.v4)
1.  object <span class="apidocSignatureSpan">node-uuid.</span>BufferClass.prototype
1.  object <span class="apidocSignatureSpan">node-uuid.</span>sha1_browser

#### [module node-uuid.BufferClass](#apidoc.module.node-uuid.BufferClass)
1.  [function <span class="apidocSignatureSpan">node-uuid.</span>BufferClass (arg, encodingOrOffset, length)](#apidoc.element.node-uuid.BufferClass.BufferClass)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>alloc (size, fill, encoding)](#apidoc.element.node-uuid.BufferClass.alloc)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>allocUnsafe (size)](#apidoc.element.node-uuid.BufferClass.allocUnsafe)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>allocUnsafeSlow (size)](#apidoc.element.node-uuid.BufferClass.allocUnsafeSlow)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>byteLength (string, encoding)](#apidoc.element.node-uuid.BufferClass.byteLength)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>compare (a, b)](#apidoc.element.node-uuid.BufferClass.compare)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>concat (list, length)](#apidoc.element.node-uuid.BufferClass.concat)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>from (value, encodingOrOffset, length)](#apidoc.element.node-uuid.BufferClass.from)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>isBuffer (b)](#apidoc.element.node-uuid.BufferClass.isBuffer)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>isEncoding (encoding)](#apidoc.element.node-uuid.BufferClass.isEncoding)
1.  number <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>poolSize

#### [module node-uuid.BufferClass.prototype](#apidoc.module.node-uuid.BufferClass.prototype)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>asciiSlice ()](#apidoc.element.node-uuid.BufferClass.prototype.asciiSlice)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>asciiWrite ()](#apidoc.element.node-uuid.BufferClass.prototype.asciiWrite)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>base64Slice ()](#apidoc.element.node-uuid.BufferClass.prototype.base64Slice)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>base64Write ()](#apidoc.element.node-uuid.BufferClass.prototype.base64Write)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>compare (target, start, end, thisStart, thisEnd)](#apidoc.element.node-uuid.BufferClass.prototype.compare)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>copy ()](#apidoc.element.node-uuid.BufferClass.prototype.copy)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>equals (b)](#apidoc.element.node-uuid.BufferClass.prototype.equals)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>fill (val, start, end, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.fill)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>hexSlice ()](#apidoc.element.node-uuid.BufferClass.prototype.hexSlice)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>hexWrite ()](#apidoc.element.node-uuid.BufferClass.prototype.hexWrite)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>includes (val, byteOffset, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.includes)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>indexOf (val, byteOffset, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.indexOf)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>inspect ()](#apidoc.element.node-uuid.BufferClass.prototype.inspect)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>lastIndexOf (val, byteOffset, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.lastIndexOf)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>latin1Slice ()](#apidoc.element.node-uuid.BufferClass.prototype.latin1Slice)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>latin1Write ()](#apidoc.element.node-uuid.BufferClass.prototype.latin1Write)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readDoubleBE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readDoubleBE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readDoubleLE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readDoubleLE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readFloatBE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readFloatBE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readFloatLE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readFloatLE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt16BE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt16BE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt16LE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt16LE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt32BE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt32BE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt32LE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt32LE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt8 (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt8)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readIntBE (offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readIntBE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readIntLE (offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readIntLE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt16BE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt16BE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt16LE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt16LE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt32BE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt32BE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt32LE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt32LE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt8 (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt8)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUIntBE (offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUIntBE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUIntLE (offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUIntLE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>slice (start, end)](#apidoc.element.node-uuid.BufferClass.prototype.slice)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>swap16 ()](#apidoc.element.node-uuid.BufferClass.prototype.swap16)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>swap32 ()](#apidoc.element.node-uuid.BufferClass.prototype.swap32)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>swap64 ()](#apidoc.element.node-uuid.BufferClass.prototype.swap64)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>toJSON ()](#apidoc.element.node-uuid.BufferClass.prototype.toJSON)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>toString ()](#apidoc.element.node-uuid.BufferClass.prototype.toString)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>ucs2Slice ()](#apidoc.element.node-uuid.BufferClass.prototype.ucs2Slice)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>ucs2Write ()](#apidoc.element.node-uuid.BufferClass.prototype.ucs2Write)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>utf8Slice ()](#apidoc.element.node-uuid.BufferClass.prototype.utf8Slice)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>utf8Write ()](#apidoc.element.node-uuid.BufferClass.prototype.utf8Write)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>write (string, offset, length, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.write)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeDoubleBE (val, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeDoubleBE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeDoubleLE (val, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeDoubleLE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeFloatBE (val, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeFloatBE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeFloatLE (val, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeFloatLE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt16BE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt16BE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt16LE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt16LE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt32BE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt32BE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt32LE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt32LE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt8 (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt8)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeIntBE (value, offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeIntBE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeIntLE (value, offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeIntLE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt16BE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt16BE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt16LE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt16LE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt32BE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt32BE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt32LE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt32LE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt8 (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt8)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUIntBE (value, offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUIntBE)
1.  [function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUIntLE (value, offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUIntLE)

#### [module node-uuid.sha1_browser](#apidoc.module.node-uuid.sha1_browser)
1.  [function <span class="apidocSignatureSpan">node-uuid.sha1_browser.</span>hash (msg, options)](#apidoc.element.node-uuid.sha1_browser.hash)
1.  [function <span class="apidocSignatureSpan">node-uuid.sha1_browser.</span>hexBytesToString (hexStr)](#apidoc.element.node-uuid.sha1_browser.hexBytesToString)
1.  [function <span class="apidocSignatureSpan">node-uuid.sha1_browser.</span>utf8Encode (str)](#apidoc.element.node-uuid.sha1_browser.utf8Encode)



# <a name="apidoc.module.node-uuid"></a>[module node-uuid](#apidoc.module.node-uuid)

#### <a name="apidoc.element.node-uuid.BufferClass"></a>[function <span class="apidocSignatureSpan">node-uuid.</span>BufferClass (arg, encodingOrOffset, length)](#apidoc.element.node-uuid.BufferClass)
- description and source-code
```javascript
function Buffer(arg, encodingOrOffset, length) {
  // Common case.
  if (typeof arg === 'number') {
    if (typeof encodingOrOffset === 'string') {
      throw new Error(
        'If encoding is specified then the first argument must be a string'
      );
    }
    return Buffer.allocUnsafe(arg);
  }
  return Buffer.from(arg, encodingOrOffset, length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid._nodeRNG"></a>[function <span class="apidocSignatureSpan">node-uuid.</span>_nodeRNG ()](#apidoc.element.node-uuid._nodeRNG)
- description and source-code
```javascript
_nodeRNG = function () {return _rb(16);}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid._rng"></a>[function <span class="apidocSignatureSpan">node-uuid.</span>_rng ()](#apidoc.element.node-uuid._rng)
- description and source-code
```javascript
_rng = function () {return _rb(16);}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.parse"></a>[function <span class="apidocSignatureSpan">node-uuid.</span>parse (s, buf, offset)](#apidoc.element.node-uuid.parse)
- description and source-code
```javascript
function parse(s, buf, offset) {
  var i = (buf && offset) || 0, ii = 0;

  buf = buf || [];
  s.toLowerCase().replace(/[0-9a-f]{2}/g, function(oct) {
    if (ii < 16) { // Don't overflow!
      buf[i + ii++] = _hexToByte[oct];
    }
  });

  // Zero out remaining bytes if string was short
  while (ii < 16) {
    buf[i + ii++] = 0;
  }

  return buf;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.unparse"></a>[function <span class="apidocSignatureSpan">node-uuid.</span>unparse (buf, offset)](#apidoc.element.node-uuid.unparse)
- description and source-code
```javascript
function unparse(buf, offset) {
  var i = offset || 0, bth = _byteToHex;
  return  bth[buf[i++]] + bth[buf[i++]] +
          bth[buf[i++]] + bth[buf[i++]] + '-' +
          bth[buf[i++]] + bth[buf[i++]] + '-' +
          bth[buf[i++]] + bth[buf[i++]] + '-' +
          bth[buf[i++]] + bth[buf[i++]] + '-' +
          bth[buf[i++]] + bth[buf[i++]] +
          bth[buf[i++]] + bth[buf[i++]] +
          bth[buf[i++]] + bth[buf[i++]];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.v1"></a>[function <span class="apidocSignatureSpan">node-uuid.</span>v1 (options, buf, offset)](#apidoc.element.node-uuid.v1)
- description and source-code
```javascript
function v1(options, buf, offset) {
  var i = buf && offset || 0;
  var b = buf || [];

  options = options || {};

  var clockseq = (options.clockseq != null) ? options.clockseq : _clockseq;

  // UUID timestamps are 100 nano-second units since the Gregorian epoch,
  // (1582-10-15 00:00).  JSNumbers aren't precise enough for this, so
  // time is handled internally as 'msecs' (integer milliseconds) and 'nsecs'
  // (100-nanoseconds offset from msecs) since unix epoch, 1970-01-01 00:00.
  var msecs = (options.msecs != null) ? options.msecs : new Date().getTime();

  // Per 4.2.1.2, use count of uuid's generated during the current clock
  // cycle to simulate higher resolution clock
  var nsecs = (options.nsecs != null) ? options.nsecs : _lastNSecs + 1;

  // Time since last uuid creation (in msecs)
  var dt = (msecs - _lastMSecs) + (nsecs - _lastNSecs)/10000;

  // Per 4.2.1.2, Bump clockseq on clock regression
  if (dt < 0 && options.clockseq == null) {
    clockseq = clockseq + 1 & 0x3fff;
  }

  // Reset nsecs if clock regresses (new clockseq) or we've moved onto a new
  // time interval
  if ((dt < 0 || msecs > _lastMSecs) && options.nsecs == null) {
    nsecs = 0;
  }

  // Per 4.2.1.2 Throw error if too many uuids are requested
  if (nsecs >= 10000) {
    throw new Error('uuid.v1(): Can\'t create more than 10M uuids/sec');
  }

  _lastMSecs = msecs;
  _lastNSecs = nsecs;
  _clockseq = clockseq;

  // Per 4.1.4 - Convert from unix epoch to Gregorian epoch
  msecs += 12219292800000;

  // 'time_low'
  var tl = ((msecs & 0xfffffff) * 10000 + nsecs) % 0x100000000;
  b[i++] = tl >>> 24 & 0xff;
  b[i++] = tl >>> 16 & 0xff;
  b[i++] = tl >>> 8 & 0xff;
  b[i++] = tl & 0xff;

  // 'time_mid'
  var tmh = (msecs / 0x100000000 * 10000) & 0xfffffff;
  b[i++] = tmh >>> 8 & 0xff;
  b[i++] = tmh & 0xff;

  // 'time_high_and_version'
  b[i++] = tmh >>> 24 & 0xf | 0x10; // include version
  b[i++] = tmh >>> 16 & 0xff;

  // 'clock_seq_hi_and_reserved' (Per 4.2.2 - include variant)
  b[i++] = clockseq >>> 8 | 0x80;

  // 'clock_seq_low'
  b[i++] = clockseq & 0xff;

  // 'node'
  var node = options.node || _nodeId;
  for (var n = 0; n < 6; n++) {
    b[i + n] = node[n];
  }

  return buf ? buf : unparse(b);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.v4"></a>[function <span class="apidocSignatureSpan">node-uuid.</span>v4 (options, buf, offset)](#apidoc.element.node-uuid.v4)
- description and source-code
```javascript
function v4(options, buf, offset) {
  // Deprecated - 'format' argument, as supported in v1.2
  var i = buf && offset || 0;

  if (typeof(options) === 'string') {
    buf = (options === 'binary') ? new BufferClass(16) : null;
    options = null;
  }
  options = options || {};

  var rnds = options.random || (options.rng || _rng)();

  // Per 4.4, set bits for version and 'clock_seq_hi_and_reserved'
  rnds[6] = (rnds[6] & 0x0f) | 0x40;
  rnds[8] = (rnds[8] & 0x3f) | 0x80;

  // Copy bytes to buffer, if provided
  if (buf) {
    for (var ii = 0; ii < 16; ii++) {
      buf[i + ii] = rnds[ii];
    }
  }

  return buf || unparse(rnds);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-uuid.BufferClass"></a>[module node-uuid.BufferClass](#apidoc.module.node-uuid.BufferClass)

#### <a name="apidoc.element.node-uuid.BufferClass.BufferClass"></a>[function <span class="apidocSignatureSpan">node-uuid.</span>BufferClass (arg, encodingOrOffset, length)](#apidoc.element.node-uuid.BufferClass.BufferClass)
- description and source-code
```javascript
function Buffer(arg, encodingOrOffset, length) {
  // Common case.
  if (typeof arg === 'number') {
    if (typeof encodingOrOffset === 'string') {
      throw new Error(
        'If encoding is specified then the first argument must be a string'
      );
    }
    return Buffer.allocUnsafe(arg);
  }
  return Buffer.from(arg, encodingOrOffset, length);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.alloc"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>alloc (size, fill, encoding)](#apidoc.element.node-uuid.BufferClass.alloc)
- description and source-code
```javascript
alloc = function (size, fill, encoding) {
  assertSize(size);
  if (size > 0 && fill !== undefined) {
    // Since we are filling anyway, don't zero fill initially.
    // Only pay attention to encoding if it's a string. This
    // prevents accidentally sending in a number that would
    // be interpretted as a start offset.
    if (typeof encoding !== 'string')
      encoding = undefined;
    return createUnsafeBuffer(size).fill(fill, encoding);
  }
  return new FastBuffer(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.allocUnsafe"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>allocUnsafe (size)](#apidoc.element.node-uuid.BufferClass.allocUnsafe)
- description and source-code
```javascript
allocUnsafe = function (size) {
  assertSize(size);
  return allocate(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.allocUnsafeSlow"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>allocUnsafeSlow (size)](#apidoc.element.node-uuid.BufferClass.allocUnsafeSlow)
- description and source-code
```javascript
allocUnsafeSlow = function (size) {
  assertSize(size);
  return createUnsafeBuffer(size);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.byteLength"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>byteLength (string, encoding)](#apidoc.element.node-uuid.BufferClass.byteLength)
- description and source-code
```javascript
function byteLength(string, encoding) {
  if (typeof string !== 'string') {
    if (ArrayBuffer.isView(string) || isArrayBuffer(string) ||
        isSharedArrayBuffer(string)) {
      return string.byteLength;
    }

    string = '' + string;
  }

  var len = string.length;
  if (len === 0)
    return 0;

  // Use a for loop to avoid recursion
  var loweredCase = false;
  for (;;) {
    switch (encoding) {
      case 'ascii':
      case 'latin1':
      case 'binary':
        return len;

      case 'utf8':
      case 'utf-8':
      case undefined:
        return binding.byteLengthUtf8(string);

      case 'ucs2':
      case 'ucs-2':
      case 'utf16le':
      case 'utf-16le':
        return len * 2;

      case 'hex':
        return len >>> 1;

      case 'base64':
        return base64ByteLength(string, len);

      default:
        // The C++ binding defaulted to UTF8, we should too.
        if (loweredCase)
          return binding.byteLengthUtf8(string);

        encoding = ('' + encoding).toLowerCase();
        loweredCase = true;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.compare"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>compare (a, b)](#apidoc.element.node-uuid.BufferClass.compare)
- description and source-code
```javascript
function compare(a, b) {
  if (!(a instanceof Buffer) ||
      !(b instanceof Buffer)) {
    throw new TypeError('Arguments must be Buffers');
  }

  if (a === b) {
    return 0;
  }

  return binding.compare(a, b);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.concat"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>concat (list, length)](#apidoc.element.node-uuid.BufferClass.concat)
- description and source-code
```javascript
concat = function (list, length) {
  var i;
  if (!Array.isArray(list))
    throw new TypeError('"list" argument must be an Array of Buffers');

  if (list.length === 0)
    return new FastBuffer();

  if (length === undefined) {
    length = 0;
    for (i = 0; i < list.length; i++)
      length += list[i].length;
  } else {
    length = length >>> 0;
  }

  var buffer = Buffer.allocUnsafe(length);
  var pos = 0;
  for (i = 0; i < list.length; i++) {
    var buf = list[i];
    if (!Buffer.isBuffer(buf))
      throw new TypeError('"list" argument must be an Array of Buffers');
    buf.copy(buffer, pos);
    pos += buf.length;
  }

  // Note: 'length' is always equal to 'buffer.length' at this point
  if (pos < length) {
    // Zero-fill the remaining bytes if the specified 'length' was more than
    // the actual total length, i.e. if we have some remaining allocated bytes
    // there were not initialized.
    buffer.fill(0, pos, length);
  }

  return buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.from"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>from (value, encodingOrOffset, length)](#apidoc.element.node-uuid.BufferClass.from)
- description and source-code
```javascript
from = function (value, encodingOrOffset, length) {
  if (typeof value === 'number')
    throw new TypeError('"value" argument must not be a number');

  if (isArrayBuffer(value) || isSharedArrayBuffer(value))
    return fromArrayBuffer(value, encodingOrOffset, length);

  if (typeof value === 'string')
    return fromString(value, encodingOrOffset);

  return fromObject(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.isBuffer"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>isBuffer (b)](#apidoc.element.node-uuid.BufferClass.isBuffer)
- description and source-code
```javascript
function isBuffer(b) {
  return b instanceof Buffer;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.isEncoding"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.</span>isEncoding (encoding)](#apidoc.element.node-uuid.BufferClass.isEncoding)
- description and source-code
```javascript
isEncoding = function (encoding) {
  return typeof encoding === 'string' &&
         typeof internalUtil.normalizeEncoding(encoding) === 'string';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-uuid.BufferClass.prototype"></a>[module node-uuid.BufferClass.prototype](#apidoc.module.node-uuid.BufferClass.prototype)

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.asciiSlice"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>asciiSlice ()](#apidoc.element.node-uuid.BufferClass.prototype.asciiSlice)
- description and source-code
```javascript
function asciiSlice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.asciiWrite"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>asciiWrite ()](#apidoc.element.node-uuid.BufferClass.prototype.asciiWrite)
- description and source-code
```javascript
function asciiWrite() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.base64Slice"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>base64Slice ()](#apidoc.element.node-uuid.BufferClass.prototype.base64Slice)
- description and source-code
```javascript
function base64Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.base64Write"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>base64Write ()](#apidoc.element.node-uuid.BufferClass.prototype.base64Write)
- description and source-code
```javascript
function base64Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.compare"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>compare (target, start, end, thisStart, thisEnd)](#apidoc.element.node-uuid.BufferClass.prototype.compare)
- description and source-code
```javascript
function compare(target, start, end, thisStart, thisEnd) {

  if (!(target instanceof Buffer))
    throw new TypeError('Argument must be a Buffer');
  if (arguments.length === 1)
    return compare_(this, target);

  if (start === undefined)
    start = 0;
  else if (start < 0)
    throw new RangeError('out of range index');
  else
    start >>>= 0;

  if (end === undefined)
    end = target.length;
  else if (end > target.length)
    throw new RangeError('out of range index');
  else
    end >>>= 0;

  if (thisStart === undefined)
    thisStart = 0;
  else if (thisStart < 0)
    throw new RangeError('out of range index');
  else
    thisStart >>>= 0;

  if (thisEnd === undefined)
    thisEnd = this.length;
  else if (thisEnd > this.length)
    throw new RangeError('out of range index');
  else
    thisEnd >>>= 0;

  if (thisStart >= thisEnd)
    return (start >= end ? 0 : -1);
  else if (start >= end)
    return 1;

  return compareOffset(this, target, start, thisStart, end, thisEnd);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.copy"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>copy ()](#apidoc.element.node-uuid.BufferClass.prototype.copy)
- description and source-code
```javascript
function copy() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.equals"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>equals (b)](#apidoc.element.node-uuid.BufferClass.prototype.equals)
- description and source-code
```javascript
function equals(b) {
  if (!(b instanceof Buffer))
    throw new TypeError('Argument must be a Buffer');

  if (this === b)
    return true;

  return binding.compare(this, b) === 0;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.fill"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>fill (val, start, end, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.fill)
- description and source-code
```javascript
function fill(val, start, end, encoding) {
  // Handle string cases:
  if (typeof val === 'string') {
    if (typeof start === 'string') {
      encoding = start;
      start = 0;
      end = this.length;
    } else if (typeof end === 'string') {
      encoding = end;
      end = this.length;
    }

    if (encoding !== undefined && typeof encoding !== 'string') {
      throw new TypeError('encoding must be a string');
    }
    var normalizedEncoding = internalUtil.normalizeEncoding(encoding);
    if (normalizedEncoding === undefined) {
      throw new TypeError('Unknown encoding: ' + encoding);
    }

    if (val.length === 0) {
      // Previously, if val === '', the Buffer would not fill,
      // which is rather surprising.
      val = 0;
    } else if (val.length === 1) {
      var code = val.charCodeAt(0);
      if ((normalizedEncoding === 'utf8' && code < 128) ||
          normalizedEncoding === 'latin1') {
        // Fast path: If 'val' fits into a single byte, use that numeric value.
        val = code;
      }
    }
  } else if (typeof val === 'number') {
    val = val & 255;
  }

  // Invalid ranges are not set to a default, so can range check early.
  if (start < 0 || end > this.length)
    throw new RangeError('Out of range index');

  if (end <= start)
    return this;

  start = start >>> 0;
  end = end === undefined ? this.length : end >>> 0;

  binding.fill(this, val, start, end, encoding);

  return this;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.hexSlice"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>hexSlice ()](#apidoc.element.node-uuid.BufferClass.prototype.hexSlice)
- description and source-code
```javascript
function hexSlice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.hexWrite"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>hexWrite ()](#apidoc.element.node-uuid.BufferClass.prototype.hexWrite)
- description and source-code
```javascript
function hexWrite() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.includes"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>includes (val, byteOffset, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.includes)
- description and source-code
```javascript
function includes(val, byteOffset, encoding) {
  return this.indexOf(val, byteOffset, encoding) !== -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.indexOf"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>indexOf (val, byteOffset, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.indexOf)
- description and source-code
```javascript
function indexOf(val, byteOffset, encoding) {
  return bidirectionalIndexOf(this, val, byteOffset, encoding, true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.inspect"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>inspect ()](#apidoc.element.node-uuid.BufferClass.prototype.inspect)
- description and source-code
```javascript
function inspect() {
  var str = '';
  var max = exports.INSPECT_MAX_BYTES;
  if (this.length > 0) {
    str = this.toString('hex', 0, max).match(/.{2}/g).join(' ');
    if (this.length > max)
      str += ' ... ';
  }
  return '<' + this.constructor.name + ' ' + str + '>';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.lastIndexOf"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>lastIndexOf (val, byteOffset, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.lastIndexOf)
- description and source-code
```javascript
function lastIndexOf(val, byteOffset, encoding) {
  return bidirectionalIndexOf(this, val, byteOffset, encoding, false);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.latin1Slice"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>latin1Slice ()](#apidoc.element.node-uuid.BufferClass.prototype.latin1Slice)
- description and source-code
```javascript
function latin1Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.latin1Write"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>latin1Write ()](#apidoc.element.node-uuid.BufferClass.prototype.latin1Write)
- description and source-code
```javascript
function latin1Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readDoubleBE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readDoubleBE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readDoubleBE)
- description and source-code
```javascript
function readDoubleBE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 8, this.length);
  return binding.readDoubleBE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readDoubleLE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readDoubleLE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readDoubleLE)
- description and source-code
```javascript
function readDoubleLE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 8, this.length);
  return binding.readDoubleLE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readFloatBE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readFloatBE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readFloatBE)
- description and source-code
```javascript
function readFloatBE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);
  return binding.readFloatBE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readFloatLE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readFloatLE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readFloatLE)
- description and source-code
```javascript
function readFloatLE(offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);
  return binding.readFloatLE(this, offset);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readInt16BE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt16BE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt16BE)
- description and source-code
```javascript
readInt16BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  var val = this[offset + 1] | (this[offset] << 8);
  return (val & 0x8000) ? val | 0xFFFF0000 : val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readInt16LE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt16LE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt16LE)
- description and source-code
```javascript
readInt16LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  var val = this[offset] | (this[offset + 1] << 8);
  return (val & 0x8000) ? val | 0xFFFF0000 : val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readInt32BE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt32BE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt32BE)
- description and source-code
```javascript
readInt32BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return (this[offset] << 24) |
      (this[offset + 1] << 16) |
      (this[offset + 2] << 8) |
      (this[offset + 3]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readInt32LE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt32LE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt32LE)
- description and source-code
```javascript
readInt32LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return (this[offset]) |
      (this[offset + 1] << 8) |
      (this[offset + 2] << 16) |
      (this[offset + 3] << 24);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readInt8"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readInt8 (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readInt8)
- description and source-code
```javascript
readInt8 = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 1, this.length);
  var val = this[offset];
  return !(val & 0x80) ? val : (0xff - val + 1) * -1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readIntBE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readIntBE (offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readIntBE)
- description and source-code
```javascript
readIntBE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var i = byteLength;
  var mul = 1;
  var val = this[offset + --i];
  while (i > 0 && (mul *= 0x100))
    val += this[offset + --i] * mul;
  mul *= 0x80;

  if (val >= mul)
    val -= Math.pow(2, 8 * byteLength);

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readIntLE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readIntLE (offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readIntLE)
- description and source-code
```javascript
readIntLE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var val = this[offset];
  var mul = 1;
  var i = 0;
  while (++i < byteLength && (mul *= 0x100))
    val += this[offset + i] * mul;
  mul *= 0x80;

  if (val >= mul)
    val -= Math.pow(2, 8 * byteLength);

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readUInt16BE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt16BE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt16BE)
- description and source-code
```javascript
readUInt16BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  return (this[offset] << 8) | this[offset + 1];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readUInt16LE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt16LE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt16LE)
- description and source-code
```javascript
readUInt16LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 2, this.length);
  return this[offset] | (this[offset + 1] << 8);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readUInt32BE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt32BE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt32BE)
- description and source-code
```javascript
readUInt32BE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return (this[offset] * 0x1000000) +
      ((this[offset + 1] << 16) |
      (this[offset + 2] << 8) |
      this[offset + 3]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readUInt32LE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt32LE (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt32LE)
- description and source-code
```javascript
readUInt32LE = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 4, this.length);

  return ((this[offset]) |
      (this[offset + 1] << 8) |
      (this[offset + 2] << 16)) +
      (this[offset + 3] * 0x1000000);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readUInt8"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUInt8 (offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUInt8)
- description and source-code
```javascript
readUInt8 = function (offset, noAssert) {
  offset = offset >>> 0;
  if (!noAssert)
    checkOffset(offset, 1, this.length);
  return this[offset];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readUIntBE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUIntBE (offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUIntBE)
- description and source-code
```javascript
readUIntBE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var val = this[offset + --byteLength];
  var mul = 1;
  while (byteLength > 0 && (mul *= 0x100))
    val += this[offset + --byteLength] * mul;

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.readUIntLE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>readUIntLE (offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.readUIntLE)
- description and source-code
```javascript
readUIntLE = function (offset, byteLength, noAssert) {
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert)
    checkOffset(offset, byteLength, this.length);

  var val = this[offset];
  var mul = 1;
  var i = 0;
  while (++i < byteLength && (mul *= 0x100))
    val += this[offset + i] * mul;

  return val;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.slice"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>slice (start, end)](#apidoc.element.node-uuid.BufferClass.prototype.slice)
- description and source-code
```javascript
function slice(start, end) {
  const srcLength = this.length;
  start = adjustOffset(start, srcLength);
  end = end !== undefined ? adjustOffset(end, srcLength) : srcLength;
  const newLength = end > start ? end - start : 0;
  return new FastBuffer(this.buffer, this.byteOffset + start, newLength);
}
```
- example usage
```shell
...
        H[1] = (H[1]+b) >>> 0;
        H[2] = (H[2]+c) >>> 0;
        H[3] = (H[3]+d) >>> 0;
        H[4] = (H[4]+e) >>> 0;
    }

    // convert H0..H4 to hex strings (with leading zeros)
    for (var h=0; h<H.length; h++) H[h] = ('00000000'+H[h].toString(16)).slice(-8);

    // concatenate H0..H4, with separator if required
    var separator = opt.outFormat=='hex-w' ? ' ' : '';

    return H.join(separator);
};
...
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.swap16"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>swap16 ()](#apidoc.element.node-uuid.BufferClass.prototype.swap16)
- description and source-code
```javascript
function swap16() {
  // For Buffer.length < 128, it's generally faster to
  // do the swap in javascript. For larger buffers,
  // dropping down to the native code is faster.
  const len = this.length;
  if (len % 2 !== 0)
    throw new RangeError('Buffer size must be a multiple of 16-bits');
  if (len < 128) {
    for (var i = 0; i < len; i += 2)
      swap(this, i, i + 1);
    return this;
  }
  return swap16n(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.swap32"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>swap32 ()](#apidoc.element.node-uuid.BufferClass.prototype.swap32)
- description and source-code
```javascript
function swap32() {
  // For Buffer.length < 192, it's generally faster to
  // do the swap in javascript. For larger buffers,
  // dropping down to the native code is faster.
  const len = this.length;
  if (len % 4 !== 0)
    throw new RangeError('Buffer size must be a multiple of 32-bits');
  if (len < 192) {
    for (var i = 0; i < len; i += 4) {
      swap(this, i, i + 3);
      swap(this, i + 1, i + 2);
    }
    return this;
  }
  return swap32n(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.swap64"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>swap64 ()](#apidoc.element.node-uuid.BufferClass.prototype.swap64)
- description and source-code
```javascript
function swap64() {
  // For Buffer.length < 192, it's generally faster to
  // do the swap in javascript. For larger buffers,
  // dropping down to the native code is faster.
  const len = this.length;
  if (len % 8 !== 0)
    throw new RangeError('Buffer size must be a multiple of 64-bits');
  if (len < 192) {
    for (var i = 0; i < len; i += 8) {
      swap(this, i, i + 7);
      swap(this, i + 1, i + 6);
      swap(this, i + 2, i + 5);
      swap(this, i + 3, i + 4);
    }
    return this;
  }
  return swap64n(this);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.toJSON"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>toJSON ()](#apidoc.element.node-uuid.BufferClass.prototype.toJSON)
- description and source-code
```javascript
toJSON = function () {
  if (this.length) {
    const data = [];
    for (var i = 0; i < this.length; ++i)
      data[i] = this[i];
    return { type: 'Buffer', data };
  } else {
    return { type: 'Buffer', data: [] };
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.toString"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>toString ()](#apidoc.element.node-uuid.BufferClass.prototype.toString)
- description and source-code
```javascript
toString = function () {
  let result;
  if (arguments.length === 0) {
    result = this.utf8Slice(0, this.length);
  } else {
    result = slowToString.apply(this, arguments);
  }
  if (result === undefined)
    throw new Error('"toString()" failed');
  return result;
}
```
- example usage
```shell
...
        H[1] = (H[1]+b) >>> 0;
        H[2] = (H[2]+c) >>> 0;
        H[3] = (H[3]+d) >>> 0;
        H[4] = (H[4]+e) >>> 0;
    }

    // convert H0..H4 to hex strings (with leading zeros)
    for (var h=0; h<H.length; h++) H[h] = ('00000000'+H[h].toString(16)).slice(-8);

    // concatenate H0..H4, with separator if required
    var separator = opt.outFormat=='hex-w' ? ' ' : '';

    return H.join(separator);
};
...
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.ucs2Slice"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>ucs2Slice ()](#apidoc.element.node-uuid.BufferClass.prototype.ucs2Slice)
- description and source-code
```javascript
function ucs2Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.ucs2Write"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>ucs2Write ()](#apidoc.element.node-uuid.BufferClass.prototype.ucs2Write)
- description and source-code
```javascript
function ucs2Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.utf8Slice"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>utf8Slice ()](#apidoc.element.node-uuid.BufferClass.prototype.utf8Slice)
- description and source-code
```javascript
function utf8Slice() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.utf8Write"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>utf8Write ()](#apidoc.element.node-uuid.BufferClass.prototype.utf8Write)
- description and source-code
```javascript
function utf8Write() { [native code] }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.write"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>write (string, offset, length, encoding)](#apidoc.element.node-uuid.BufferClass.prototype.write)
- description and source-code
```javascript
write = function (string, offset, length, encoding) {
  // Buffer#write(string);
  if (offset === undefined) {
    encoding = 'utf8';
    length = this.length;
    offset = 0;

  // Buffer#write(string, encoding)
  } else if (length === undefined && typeof offset === 'string') {
    encoding = offset;
    length = this.length;
    offset = 0;

  // Buffer#write(string, offset[, length][, encoding])
  } else if (isFinite(offset)) {
    offset = offset >>> 0;
    if (isFinite(length)) {
      length = length >>> 0;
      if (encoding === undefined)
        encoding = 'utf8';
    } else {
      encoding = length;
      length = undefined;
    }
  } else {
    // if someone is still calling the obsolete form of write(), tell them.
    // we don't want eg buf.write("foo", "utf8", 10) to silently turn into
    // buf.write("foo", "utf8"), so we can't ignore extra args
    throw new Error('Buffer.write(string, encoding, offset[, length]) ' +
                    'is no longer supported');
  }

  var remaining = this.length - offset;
  if (length === undefined || length > remaining)
    length = remaining;

  if (string.length > 0 && (length < 0 || offset < 0))
    throw new RangeError('Attempt to write outside buffer bounds');

  if (!encoding)
    encoding = 'utf8';

  var loweredCase = false;
  for (;;) {
    switch (encoding) {
      case 'hex':
        return this.hexWrite(string, offset, length);

      case 'utf8':
      case 'utf-8':
        return this.utf8Write(string, offset, length);

      case 'ascii':
        return this.asciiWrite(string, offset, length);

      case 'latin1':
      case 'binary':
        return this.latin1Write(string, offset, length);

      case 'base64':
        // Warning: maxLength not taken into account in base64Write
        return this.base64Write(string, offset, length);

      case 'ucs2':
      case 'ucs-2':
      case 'utf16le':
      case 'utf-16le':
        return this.ucs2Write(string, offset, length);

      default:
        if (loweredCase)
          throw new TypeError('Unknown encoding: ' + encoding);
        encoding = ('' + encoding).toLowerCase();
        loweredCase = true;
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeDoubleBE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeDoubleBE (val, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeDoubleBE)
- description and source-code
```javascript
function writeDoubleBE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeDoubleBE(this, val, offset);
  else
    binding.writeDoubleBE(this, val, offset, true);
  return offset + 8;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeDoubleLE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeDoubleLE (val, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeDoubleLE)
- description and source-code
```javascript
function writeDoubleLE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeDoubleLE(this, val, offset);
  else
    binding.writeDoubleLE(this, val, offset, true);
  return offset + 8;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeFloatBE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeFloatBE (val, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeFloatBE)
- description and source-code
```javascript
function writeFloatBE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeFloatBE(this, val, offset);
  else
    binding.writeFloatBE(this, val, offset, true);
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeFloatLE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeFloatLE (val, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeFloatLE)
- description and source-code
```javascript
function writeFloatLE(val, offset, noAssert) {
  val = +val;
  offset = offset >>> 0;
  if (!noAssert)
    binding.writeFloatLE(this, val, offset);
  else
    binding.writeFloatLE(this, val, offset, true);
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeInt16BE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt16BE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt16BE)
- description and source-code
```javascript
writeInt16BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0x7fff, -0x8000);
  this[offset] = (value >>> 8);
  this[offset + 1] = value;
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeInt16LE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt16LE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt16LE)
- description and source-code
```javascript
writeInt16LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0x7fff, -0x8000);
  this[offset] = value;
  this[offset + 1] = (value >>> 8);
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeInt32BE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt32BE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt32BE)
- description and source-code
```javascript
writeInt32BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0x7fffffff, -0x80000000);
  this[offset] = (value >>> 24);
  this[offset + 1] = (value >>> 16);
  this[offset + 2] = (value >>> 8);
  this[offset + 3] = value;
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeInt32LE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt32LE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt32LE)
- description and source-code
```javascript
writeInt32LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0x7fffffff, -0x80000000);
  this[offset] = value;
  this[offset + 1] = (value >>> 8);
  this[offset + 2] = (value >>> 16);
  this[offset + 3] = (value >>> 24);
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeInt8"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeInt8 (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeInt8)
- description and source-code
```javascript
writeInt8 = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 1, 0x7f, -0x80);
  this[offset] = value;
  return offset + 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeIntBE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeIntBE (value, offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeIntBE)
- description and source-code
```javascript
writeIntBE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert) {
    checkInt(this,
             value,
             offset,
             byteLength,
             Math.pow(2, 8 * byteLength - 1) - 1,
             -Math.pow(2, 8 * byteLength - 1));
  }

  var i = byteLength - 1;
  var mul = 1;
  var sub = 0;
  this[offset + i] = value;
  while (--i >= 0 && (mul *= 0x100)) {
    if (value < 0 && sub === 0 && this[offset + i + 1] !== 0)
      sub = 1;
    this[offset + i] = ((value / mul) >> 0) - sub;
  }

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeIntLE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeIntLE (value, offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeIntLE)
- description and source-code
```javascript
writeIntLE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert) {
    checkInt(this,
             value,
             offset,
             byteLength,
             Math.pow(2, 8 * byteLength - 1) - 1,
             -Math.pow(2, 8 * byteLength - 1));
  }

  var i = 0;
  var mul = 1;
  var sub = 0;
  this[offset] = value;
  while (++i < byteLength && (mul *= 0x100)) {
    if (value < 0 && sub === 0 && this[offset + i - 1] !== 0)
      sub = 1;
    this[offset + i] = ((value / mul) >> 0) - sub;
  }

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeUInt16BE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt16BE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt16BE)
- description and source-code
```javascript
writeUInt16BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0xffff, 0);
  this[offset] = (value >>> 8);
  this[offset + 1] = value;
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeUInt16LE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt16LE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt16LE)
- description and source-code
```javascript
writeUInt16LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 2, 0xffff, 0);
  this[offset] = value;
  this[offset + 1] = (value >>> 8);
  return offset + 2;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeUInt32BE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt32BE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt32BE)
- description and source-code
```javascript
writeUInt32BE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0xffffffff, 0);
  this[offset] = (value >>> 24);
  this[offset + 1] = (value >>> 16);
  this[offset + 2] = (value >>> 8);
  this[offset + 3] = value;
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeUInt32LE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt32LE (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt32LE)
- description and source-code
```javascript
writeUInt32LE = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 4, 0xffffffff, 0);
  this[offset + 3] = (value >>> 24);
  this[offset + 2] = (value >>> 16);
  this[offset + 1] = (value >>> 8);
  this[offset] = value;
  return offset + 4;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeUInt8"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUInt8 (value, offset, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUInt8)
- description and source-code
```javascript
writeUInt8 = function (value, offset, noAssert) {
  value = +value;
  offset = offset >>> 0;
  if (!noAssert)
    checkInt(this, value, offset, 1, 0xff, 0);
  this[offset] = value;
  return offset + 1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeUIntBE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUIntBE (value, offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUIntBE)
- description and source-code
```javascript
writeUIntBE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert) {
    const maxBytes = Math.pow(2, 8 * byteLength) - 1;
    checkInt(this, value, offset, byteLength, maxBytes, 0);
  }

  var i = byteLength - 1;
  var mul = 1;
  this[offset + i] = value;
  while (--i >= 0 && (mul *= 0x100))
    this[offset + i] = (value / mul) >>> 0;

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.BufferClass.prototype.writeUIntLE"></a>[function <span class="apidocSignatureSpan">node-uuid.BufferClass.prototype.</span>writeUIntLE (value, offset, byteLength, noAssert)](#apidoc.element.node-uuid.BufferClass.prototype.writeUIntLE)
- description and source-code
```javascript
writeUIntLE = function (value, offset, byteLength, noAssert) {
  value = +value;
  offset = offset >>> 0;
  byteLength = byteLength >>> 0;
  if (!noAssert) {
    const maxBytes = Math.pow(2, 8 * byteLength) - 1;
    checkInt(this, value, offset, byteLength, maxBytes, 0);
  }

  var mul = 1;
  var i = 0;
  this[offset] = value;
  while (++i < byteLength && (mul *= 0x100))
    this[offset + i] = (value / mul) >>> 0;

  return offset + byteLength;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.node-uuid.sha1_browser"></a>[module node-uuid.sha1_browser](#apidoc.module.node-uuid.sha1_browser)

#### <a name="apidoc.element.node-uuid.sha1_browser.hash"></a>[function <span class="apidocSignatureSpan">node-uuid.sha1_browser.</span>hash (msg, options)](#apidoc.element.node-uuid.sha1_browser.hash)
- description and source-code
```javascript
hash = function (msg, options) {
    var defaults = { msgFormat: 'string', outFormat: 'hex' };
    var opt = Object.assign(defaults, options);

    switch (opt.msgFormat) {
        default: // default is to convert string to UTF-8, as SHA only deals with byte-streams
        case 'string':   msg = Sha1.utf8Encode(msg);       break;
        case 'hex-bytes':msg = Sha1.hexBytesToString(msg); break; // mostly for running tests
    }

    // constants [�4.2.1]
    var K = [ 0x5a827999, 0x6ed9eba1, 0x8f1bbcdc, 0xca62c1d6 ];

    // initial hash value [�5.3.1]
    var H = [ 0x67452301, 0xefcdab89, 0x98badcfe, 0x10325476, 0xc3d2e1f0 ];

    // PREPROCESSING [�6.1.1]

    msg += String.fromCharCode(0x80);  // add trailing '1' bit (+ 0's padding) to string [�5.1.1]

    // convert string msg into 512-bit/16-integer blocks arrays of ints [�5.2.1]
    var l = msg.length/4 + 2; // length (in 32-bit integers) of msg + �1� + appended length
    var N = Math.ceil(l/16);  // number of 16-integer-blocks required to hold 'l' ints
    var M = new Array(N);

    for (var i=0; i<N; i++) {
        M[i] = new Array(16);
        for (var j=0; j<16; j++) {  // encode 4 chars per integer, big-endian encoding
            M[i][j] = (msg.charCodeAt(i*64+j*4)<<24) | (msg.charCodeAt(i*64+j*4+1)<<16) |
                (msg.charCodeAt(i*64+j*4+2)<<8) | (msg.charCodeAt(i*64+j*4+3));
        } // note running off the end of msg is ok 'cos bitwise ops on NaN return 0
    }
    // add length (in bits) into final pair of 32-bit integers (big-endian) [�5.1.1]
    // note: most significant word would be (len-1)*8 >>> 32, but since JS converts
    // bitwise-op args to 32 bits, we need to simulate this by arithmetic operators
    M[N-1][14] = ((msg.length-1)*8) / Math.pow(2, 32); M[N-1][14] = Math.floor(M[N-1][14]);
    M[N-1][15] = ((msg.length-1)*8) & 0xffffffff;

    // HASH COMPUTATION [�6.1.2]

    for (var i=0; i<N; i++) {
        var W = new Array(80);

        // 1 - prepare message schedule 'W'
        for (var t=0;  t<16; t++) W[t] = M[i][t];
        for (var t=16; t<80; t++) W[t] = ROTL(W[t-3] ^ W[t-8] ^ W[t-14] ^ W[t-16], 1);

        // 2 - initialise five working variables a, b, c, d, e with previous hash value
        var a = H[0], b = H[1], c = H[2], d = H[3], e = H[4];

        // 3 - main loop (use JavaScript '>>> 0' to emulate UInt32 variables)
        for (var t=0; t<80; t++) {
            var s = Math.floor(t/20); // seq for blocks of 'f' functions and 'K' constants
            var T = (ROTL(a,5) + f(s,b,c,d) + e + K[s] + W[t]) >>> 0;
            e = d;
            d = c;
            c = ROTL(b, 30) >>> 0;
            b = a;
            a = T;
        }

        // 4 - compute the new intermediate hash value (note 'addition modulo 2^32' � JavaScript
        // '>>> 0' coerces to unsigned UInt32 which achieves modulo 2^32 addition)
        H[0] = (H[0]+a) >>> 0;
        H[1] = (H[1]+b) >>> 0;
        H[2] = (H[2]+c) >>> 0;
        H[3] = (H[3]+d) >>> 0;
        H[4] = (H[4]+e) >>> 0;
    }

    // convert H0..H4 to hex strings (with leading zeros)
    for (var h=0; h<H.length; h++) H[h] = ('00000000'+H[h].toString(16)).slice(-8);

    // concatenate H0..H4, with separator if required
    var separator = opt.outFormat=='hex-w' ? ' ' : '';

    return H.join(separator);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.node-uuid.sha1_browser.hexBytesToString"></a>[function <span class="apidocSignatureSpan">node-uuid.sha1_browser.</span>hexBytesToString (hexStr)](#apidoc.element.node-uuid.sha1_browser.hexBytesToString)
- description and source-code
```javascript
hexBytesToString = function (hexStr) {
    hexStr = hexStr.replace(' ', ''); // allow space-separated groups
    var str = '';
    for (var i=0; i<hexStr.length; i+=2) {
        str += String.fromCharCode(parseInt(hexStr.slice(i, i+2), 16));
    }
    return str;
}
```
- example usage
```shell
...
Sha1.hash = function(msg, options) {
var defaults = { msgFormat: 'string', outFormat: 'hex' };
var opt = Object.assign(defaults, options);

switch (opt.msgFormat) {
    default: // default is to convert string to UTF-8, as SHA only deals with byte-streams
    case 'string':   msg = Sha1.utf8Encode(msg);       break;
    case 'hex-bytes':msg = Sha1.hexBytesToString(msg); break; // mostly for running tests
}

// constants [�4.2.1]
var K = [ 0x5a827999, 0x6ed9eba1, 0x8f1bbcdc, 0xca62c1d6 ];

// initial hash value [�5.3.1]
var H = [ 0x67452301, 0xefcdab89, 0x98badcfe, 0x10325476, 0xc3d2e1f0 ];
...
```

#### <a name="apidoc.element.node-uuid.sha1_browser.utf8Encode"></a>[function <span class="apidocSignatureSpan">node-uuid.sha1_browser.</span>utf8Encode (str)](#apidoc.element.node-uuid.sha1_browser.utf8Encode)
- description and source-code
```javascript
utf8Encode = function (str) {
    return unescape(encodeURIComponent(str));
}
```
- example usage
```shell
...

Sha1.hash = function(msg, options) {
var defaults = { msgFormat: 'string', outFormat: 'hex' };
var opt = Object.assign(defaults, options);

switch (opt.msgFormat) {
    default: // default is to convert string to UTF-8, as SHA only deals with byte-streams
    case 'string':   msg = Sha1.utf8Encode(msg);       break;
    case 'hex-bytes':msg = Sha1.hexBytesToString(msg); break; // mostly for running tests
}

// constants [�4.2.1]
var K = [ 0x5a827999, 0x6ed9eba1, 0x8f1bbcdc, 0xca62c1d6 ];

// initial hash value [�5.3.1]
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
