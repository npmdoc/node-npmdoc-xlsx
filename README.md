# api documentation for  [xlsx (v0.9.9)](https://oss.sheetjs.com/js-xlsx/)  [![npm package](https://img.shields.io/npm/v/npmdoc-xlsx.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-xlsx) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-xlsx.svg)](https://travis-ci.org/npmdoc/node-npmdoc-xlsx)
#### Excel (XLSB/XLSX/XLSM/XLS/XML) and ODS (ODS/FODS/UOS) spreadsheet parser and writer

[![NPM](https://nodei.co/npm/xlsx.png?downloads=true)](https://www.npmjs.com/package/xlsx)

[![apidoc](https://npmdoc.github.io/node-npmdoc-xlsx/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-xlsx_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-xlsx/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-xlsx/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-xlsx/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "sheetjs"
    },
    "bin": {
        "xlsx": "./bin/xlsx.njs"
    },
    "browser": {
        "node": false,
        "crypto": false,
        "fs": false
    },
    "bugs": {
        "url": "https://github.com/SheetJS/js-xlsx/issues"
    },
    "config": {
        "blanket": {
            "pattern": "xlsx.js"
        }
    },
    "dependencies": {
        "adler-32": "~1.0.0",
        "cfb": "~0.11.1",
        "codepage": "~1.8.0",
        "commander": "~2.9.0",
        "crc-32": "~1.0.0",
        "exit-on-epipe": "~1.0.0",
        "ssf": "~0.9.0"
    },
    "description": "Excel (XLSB/XLSX/XLSM/XLS/XML) and ODS (ODS/FODS/UOS) spreadsheet parser and writer",
    "devDependencies": {
        "mocha": "",
        "uglify-js": "",
        "xlsjs": ""
    },
    "directories": {},
    "dist": {
        "shasum": "85a628139f0dd9c9bc36c5cc42cb27cdd831dfa4",
        "tarball": "https://registry.npmjs.org/xlsx/-/xlsx-0.9.9.tgz"
    },
    "engines": {
        "node": ">=0.8"
    },
    "gitHead": "01d1c32fa13a857c2fa23d89baa069c3aad51788",
    "homepage": "https://oss.sheetjs.com/js-xlsx/",
    "keywords": [
        "excel",
        "xls",
        "xlsx",
        "xlsb",
        "xlsm",
        "ods",
        "office",
        "spreadsheet"
    ],
    "license": "Apache-2.0",
    "main": "./xlsx",
    "maintainers": [
        {
            "name": "sheetjs",
            "email": "dev@sheetjs.com"
        }
    ],
    "name": "xlsx",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/SheetJS/js-xlsx.git"
    },
    "scripts": {
        "pretest": "git submodule init && git submodule update",
        "test": "make travis"
    },
    "version": "0.9.9"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module xlsx](#apidoc.module.xlsx)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>jszip (data, options)](#apidoc.element.xlsx.jszip)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>parse_fods (data, opts)](#apidoc.element.xlsx.parse_fods)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>parse_ods (zip, opts)](#apidoc.element.xlsx.parse_ods)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>parse_xlscfb (cfb, options)](#apidoc.element.xlsx.parse_xlscfb)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>parse_zip (zip, opts)](#apidoc.element.xlsx.parse_zip)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>read (data, opts)](#apidoc.element.xlsx.read)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>readFile (filename, opts)](#apidoc.element.xlsx.readFile)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>readFileSync (filename, opts)](#apidoc.element.xlsx.readFileSync)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>write (wb, opts)](#apidoc.element.xlsx.write)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>writeFile (wb, filename, opts)](#apidoc.element.xlsx.writeFile)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>writeFileAsync (filename, wb, opts, cb)](#apidoc.element.xlsx.writeFileAsync)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>writeFileSync (wb, filename, opts)](#apidoc.element.xlsx.writeFileSync)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>write_ods (wb, opts)](#apidoc.element.xlsx.write_ods)
1.  object <span class="apidocSignatureSpan">xlsx.</span>CFB
1.  object <span class="apidocSignatureSpan">xlsx.</span>CFB.utils
1.  object <span class="apidocSignatureSpan">xlsx.</span>SSF
1.  object <span class="apidocSignatureSpan">xlsx.</span>jszip.prototype
1.  object <span class="apidocSignatureSpan">xlsx.</span>utils
1.  string <span class="apidocSignatureSpan">xlsx.</span>version

#### [module xlsx.CFB](#apidoc.module.xlsx.CFB)
1.  [function <span class="apidocSignatureSpan">xlsx.CFB.</span>parse (file)](#apidoc.element.xlsx.CFB.parse)
1.  [function <span class="apidocSignatureSpan">xlsx.CFB.</span>read (blob, options)](#apidoc.element.xlsx.CFB.read)
1.  object <span class="apidocSignatureSpan">xlsx.CFB.</span>utils
1.  string <span class="apidocSignatureSpan">xlsx.CFB.</span>version

#### [module xlsx.CFB.utils](#apidoc.module.xlsx.CFB.utils)
1.  [function <span class="apidocSignatureSpan">xlsx.CFB.utils.</span>CheckField (hexstr, fld)](#apidoc.element.xlsx.CFB.utils.CheckField)
1.  [function <span class="apidocSignatureSpan">xlsx.CFB.utils.</span>ReadShift (size, t)](#apidoc.element.xlsx.CFB.utils.ReadShift)
1.  [function <span class="apidocSignatureSpan">xlsx.CFB.utils.</span>bconcat (bufs)](#apidoc.element.xlsx.CFB.utils.bconcat)
1.  [function <span class="apidocSignatureSpan">xlsx.CFB.utils.</span>prep_blob (blob, pos)](#apidoc.element.xlsx.CFB.utils.prep_blob)
1.  object <span class="apidocSignatureSpan">xlsx.CFB.utils.</span>consts

#### [module xlsx.SSF](#apidoc.module.xlsx.SSF)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>_eval (fmt, v, opts, flen)](#apidoc.element.xlsx.SSF._eval)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>_general (v, opts)](#apidoc.element.xlsx.SSF._general)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>_general_int (v, opts)](#apidoc.element.xlsx.SSF._general_int)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>_general_num (v, opts)](#apidoc.element.xlsx.SSF._general_num)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>_split (fmt)](#apidoc.element.xlsx.SSF._split)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>format (fmt, v, o)](#apidoc.element.xlsx.SSF.format)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>get_table ()](#apidoc.element.xlsx.SSF.get_table)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>is_date (fmt)](#apidoc.element.xlsx.SSF.is_date)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>load (fmt, idx)](#apidoc.element.xlsx.SSF.load)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>load_table (tbl)](#apidoc.element.xlsx.SSF.load_table)
1.  [function <span class="apidocSignatureSpan">xlsx.SSF.</span>parse_date_code (v, opts, b2)](#apidoc.element.xlsx.SSF.parse_date_code)
1.  object <span class="apidocSignatureSpan">xlsx.SSF.</span>_table
1.  object <span class="apidocSignatureSpan">xlsx.SSF.</span>opts
1.  string <span class="apidocSignatureSpan">xlsx.SSF.</span>version

#### [module xlsx.jszip](#apidoc.module.xlsx.jszip)
1.  [function <span class="apidocSignatureSpan">xlsx.</span>jszip (data, options)](#apidoc.element.xlsx.jszip.jszip)
1.  object <span class="apidocSignatureSpan">xlsx.jszip.</span>base64
1.  object <span class="apidocSignatureSpan">xlsx.jszip.</span>compressions
1.  object <span class="apidocSignatureSpan">xlsx.jszip.</span>defaults
1.  object <span class="apidocSignatureSpan">xlsx.jszip.</span>support
1.  object <span class="apidocSignatureSpan">xlsx.jszip.</span>utils

#### [module xlsx.jszip.prototype](#apidoc.module.xlsx.jszip.prototype)
1.  [function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>crc32 (input, crc)](#apidoc.element.xlsx.jszip.prototype.crc32)
1.  [function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>file (name, data, o)](#apidoc.element.xlsx.jszip.prototype.file)
1.  [function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>filter (search)](#apidoc.element.xlsx.jszip.prototype.filter)
1.  [function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>folder (arg)](#apidoc.element.xlsx.jszip.prototype.folder)
1.  [function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>generate (options)](#apidoc.element.xlsx.jszip.prototype.generate)
1.  [function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>load (data, options)](#apidoc.element.xlsx.jszip.prototype.load)
1.  [function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>remove (name)](#apidoc.element.xlsx.jszip.prototype.remove)
1.  [function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>utf8decode (input)](#apidoc.element.xlsx.jszip.prototype.utf8decode)
1.  [function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>utf8encode (string)](#apidoc.element.xlsx.jszip.prototype.utf8encode)

#### [module xlsx.utils](#apidoc.module.xlsx.utils)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>aoa_to_sheet (data, opts)](#apidoc.element.xlsx.utils.aoa_to_sheet)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>decode_cell (cstr)](#apidoc.element.xlsx.utils.decode_cell)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>decode_col (colstr)](#apidoc.element.xlsx.utils.decode_col)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>decode_range (range)](#apidoc.element.xlsx.utils.decode_range)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>decode_row (rowstr)](#apidoc.element.xlsx.utils.decode_row)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>encode_cell (cell)](#apidoc.element.xlsx.utils.encode_cell)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>encode_col (col)](#apidoc.element.xlsx.utils.encode_col)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>encode_range (cs, ce)](#apidoc.element.xlsx.utils.encode_range)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>encode_row (row)](#apidoc.element.xlsx.utils.encode_row)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>format_cell (cell, v, o)](#apidoc.element.xlsx.utils.format_cell)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>get_formulae (sheet)](#apidoc.element.xlsx.utils.get_formulae)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>make_csv (sheet, opts)](#apidoc.element.xlsx.utils.make_csv)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>make_formulae (sheet)](#apidoc.element.xlsx.utils.make_formulae)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>make_json (sheet, opts)](#apidoc.element.xlsx.utils.make_json)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>sheet_to_csv (sheet, opts)](#apidoc.element.xlsx.utils.sheet_to_csv)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>sheet_to_formulae (sheet)](#apidoc.element.xlsx.utils.sheet_to_formulae)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>sheet_to_json (sheet, opts)](#apidoc.element.xlsx.utils.sheet_to_json)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>sheet_to_row_object_array (sheet, opts)](#apidoc.element.xlsx.utils.sheet_to_row_object_array)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>split_cell (cstr)](#apidoc.element.xlsx.utils.split_cell)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>table_to_book (table, opts)](#apidoc.element.xlsx.utils.table_to_book)
1.  [function <span class="apidocSignatureSpan">xlsx.utils.</span>table_to_sheet (table, opts)](#apidoc.element.xlsx.utils.table_to_sheet)



# <a name="apidoc.module.xlsx"></a>[module xlsx](#apidoc.module.xlsx)

#### <a name="apidoc.element.xlsx.jszip"></a>[function <span class="apidocSignatureSpan">xlsx.</span>jszip (data, options)](#apidoc.element.xlsx.jszip)
- description and source-code
```javascript
function JSZip(data, options) {
    // if this constructor is used without 'new', it adds 'new' before itself:
    if(!(this instanceof JSZip)) return new JSZip(data, options);

    // object containing the files :
    // {
    //   "folder/" : {...},
    //   "folder/data.txt" : {...}
    // }
    this.files = {};

    this.comment = null;

    // Where we are in the hierarchy
    this.root = "";
    if (data) {
        this.load(data, options);
    }
    this.clone = function() {
        var newObj = new JSZip();
        for (var i in this) {
            if (typeof this[i] !== "function") {
                newObj[i] = this[i];
            }
        }
        return newObj;
    };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.parse_fods"></a>[function <span class="apidocSignatureSpan">xlsx.</span>parse_fods (data, opts)](#apidoc.element.xlsx.parse_fods)
- description and source-code
```javascript
function parse_fods(data, opts) {
	return parse_content_xml(data, opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.parse_ods"></a>[function <span class="apidocSignatureSpan">xlsx.</span>parse_ods (zip, opts)](#apidoc.element.xlsx.parse_ods)
- description and source-code
```javascript
function parse_ods(zip, opts) {
	opts = opts || ({});
	var ods = !!safegetzipfile(zip, 'objectdata');
	if(ods) var manifest = parse_manifest(getzipdata(zip, 'META-INF/manifest.xml'), opts);
	var content = getzipstr(zip, 'content.xml');
	if(!content) throw new Error("Missing content.xml in " + (ods ? "ODS" : "UOF")+ " file");
	return parse_content_xml(ods ? content : utf8read(content), opts);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.parse_xlscfb"></a>[function <span class="apidocSignatureSpan">xlsx.</span>parse_xlscfb (cfb, options)](#apidoc.element.xlsx.parse_xlscfb)
- description and source-code
```javascript
function parse_xlscfb(cfb, options) {
if(!options) options = {};
fix_read_opts(options);
reset_cp();
var CompObj, Summary, Workbook;
if(cfb.FullPaths) {
	CompObj = cfb.find('!CompObj');
	Summary = cfb.find('!SummaryInformation');
	Workbook = cfb.find('/Workbook');
} else {
	prep_blob(cfb, 0);
	Workbook = ({content: cfb});
}

if(!Workbook) Workbook = cfb.find('/Book');
var CompObjP, SummaryP, WorkbookP;

if(CompObj) CompObjP = parse_compobj(CompObj);
if(options.bookProps && !options.bookSheets) WorkbookP = ({});
else {
	if(Workbook) WorkbookP = parse_workbook(Workbook.content, options, !!Workbook.find);
	else throw new Error("Cannot find Workbook stream");
}

if(cfb.FullPaths) parse_props(cfb);

var props = {};
for(var y in cfb.Summary) props[y] = cfb.Summary[y];
for(y in cfb.DocSummary) props[y] = cfb.DocSummary[y];
WorkbookP.Props = WorkbookP.Custprops = props;<span class="apidocCodeCommentSpan"> /* TODO: split up properties */
</span>if(options.bookFiles) WorkbookP.cfb = cfb;
/*WorkbookP.CompObjP = CompObjP; // TODO: storage? */
return WorkbookP;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.parse_zip"></a>[function <span class="apidocSignatureSpan">xlsx.</span>parse_zip (zip, opts)](#apidoc.element.xlsx.parse_zip)
- description and source-code
```javascript
function parse_zip(zip, opts) {
	make_ssf(SSF);
	opts = opts || {};
	fix_read_opts(opts);
	reset_cp();

	<span class="apidocCodeCommentSpan">/* OpenDocument Part 3 Section 2.2.1 OpenDocument Package */
</span>	if(safegetzipfile(zip, 'META-INF/manifest.xml')) return parse_ods(zip, opts);
	/* UOC */
	if(safegetzipfile(zip, 'objectdata.xml')) return parse_ods(zip, opts);

	var entries = keys(zip.files).filter(nodirs).sort();
	var dir = parse_ct((getzipstr(zip, '[Content_Types].xml')), opts);
	var xlsb = false;
	var sheets, binname;
	if(dir.workbooks.length === 0) {
		binname = "xl/workbook.xml";
		if(getzipdata(zip,binname, true)) dir.workbooks.push(binname);
	}
	if(dir.workbooks.length === 0) {
		binname = "xl/workbook.bin";
		if(!getzipfile(zip,binname,true)) throw new Error("Could not find workbook");
		dir.workbooks.push(binname);
		xlsb = true;
	}
	if(dir.workbooks[0].slice(-3) == "bin") xlsb = true;
	if(xlsb) set_cp(1200);

	var themes = ({});
	var styles = ({});
	if(!opts.bookSheets && !opts.bookProps) {
		strs = [];
		if(dir.sst) strs=parse_sst(getzipdata(zip, dir.sst.replace(/^\//,'')), dir.sst, opts);

		if(opts.cellStyles && dir.themes.length) themes = parse_theme(getzipstr(zip, dir.themes[0].replace(/^\//,''), true)||"",dir.themes
[0], opts);

		if(dir.style) styles = parse_sty(getzipdata(zip, dir.style.replace(/^\//,'')),dir.style, themes, opts);
	}

	var wb = parse_wb(getzipdata(zip, dir.workbooks[0].replace(/^\//,'')), dir.workbooks[0], opts);

	var props = {}, propdata = "";

	if(dir.coreprops.length !== 0) {
		propdata = getzipstr(zip, dir.coreprops[0].replace(/^\//,''), true);
		if(propdata) props = parse_core_props(propdata);
		if(dir.extprops.length !== 0) {
			propdata = getzipstr(zip, dir.extprops[0].replace(/^\//,''), true);
			if(propdata) parse_ext_props(propdata, props);
		}
	}

	var custprops = {};
	if(!opts.bookSheets || opts.bookProps) {
		if (dir.custprops.length !== 0) {
			propdata = getzipstr(zip, dir.custprops[0].replace(/^\//,''), true);
			if(propdata) custprops = parse_cust_props(propdata, opts);
		}
	}

	var out = ({});
	if(opts.bookSheets || opts.bookProps) {
		if(wb.Sheets) sheets = wb.Sheets.map(function pluck(x){ return x.name; });
		else if(props.Worksheets && props.SheetNames.length > 0) sheets=props.SheetNames;
		if(opts.bookProps) { out.Props = props; out.Custprops = custprops; }
		if(opts.bookSheets && typeof sheets !== 'undefined') out.SheetNames = sheets;
		if(opts.bookSheets ? out.SheetNames : opts.bookProps) return out;
	}
	sheets = {};

	var deps = {};
	if(opts.bookDeps && dir.calcchain) deps=parse_cc(getzipdata(zip, dir.calcchain.replace(/^\//,'')),dir.calcchain,opts);

	var i=0;
	var sheetRels = ({});
	var path, relsPath;

	//if(!props.Worksheets) {
		var wbsheets = wb.Sheets;
		props.Worksheets = wbsheets.length;
		props.SheetNames = [];
		for(var j = 0; j != wbsheets.length; ++j) {
			props.SheetNames[j] = wbsheets[j].name;
		}
	//}

	var wbext = xlsb ? "bin" : "xml";
	var wbrelsfile = 'xl/_rels/workbook.' + wbext + '.rels';
	var wbrels = parse_rels(getzipstr(zip, wbrelsfile, true), wbrelsfile);
	if(wbrels) wbrels = safe_parse_wbrels(wbrels, wb.Sheets);
	/* Numbers iOS hack */
	var nmode = (getzipdata(zip,"xl/worksheets/sheet.xml",true))?1:0;
	for(i = 0; i != props.Worksheets; ++i) {
		var stype = "sheet";
		if(wbrels && wbrels[i]) {
			path = 'xl/' + (wbrels[i][1]).replace(/[\/]?xl\//, "");
			stype = wbrels[i][2];
		} else {
			path = 'xl/worksheets/sheet'+(i+1-nmode)+"." + wbext;
			path = path.replace(/sheet0\./,"sheet.");
		}
		relsPath = path.replace(/^(.*)(\/)([^\/]*)$/, "$1/_rels/$3.rels");
		safe_parse_sheet(zip, path, relsPath, props.SheetNames[i], sheetRels, sheets, stype, opts, wb, themes, styles);
	}

	if(dir.comments) parse_comments(zip, dir.comments, sheets, sheetRels, opts);

	out = ({
		Directory: dir,
		Workbook: wb,
		Props: props,
		Custprops: custprops,
		Deps: deps,
		Sheets: sheets,
		SheetNames: props.SheetNames,
		Strings: strs,
		Styles: styles,
		Themes: themes,
		SSF: SSF.get_table()
	});
	if(opts.bookFiles) {
		out.keys = entries;
		out.files = zip.files;
	}
	if(opts.bookVBA) {
		if ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.read"></a>[function <span class="apidocSignatureSpan">xlsx.</span>read (data, opts)](#apidoc.element.xlsx.read)
- description and source-code
```javascript
function readSync(data, opts) {
	var zip, d = data, n=[0];
	var o = opts||{};
	if(!o.type) o.type = (has_buf && Buffer.isBuffer(data)) ? "buffer" : "base64";
	if(o.type == "file") { o.type = "buffer"; d = _fs.readFileSync(data); }
	switch((n = firstbyte(d, o))[0]) {
		case 0xD0: return parse_xlscfb(CFB.read(d, o), o);
		case 0x09: return parse_xlscfb(s2a(o.type === 'base64' ? Base64.decode(d) : d), o);
		case 0x3C: return parse_xlml(d, o);
		case 0x49: if(n[1] == 0x44) return SYLK.to_workbook(d, o); break;
		case 0x54: if(n[1] == 0x41 && n[2] == 0x42 && n[3] == 0x4C) return DIF.to_workbook(d, o); break;
		case 0x50: if(n[1] == 0x4B && n[2] < 0x20 && n[3] < 0x20) return read_zip(d, o); break;
		case 0xEF: return parse_xlml(d, o);
		case 0xFF: if(n[1] == 0xFE){ return read_utf16(d, o); } break;
		case 0x03: case 0x83: case 0x8B: return DBF.to_workbook(d, o);
	}
	if(n[2] <= 12 && n[3] <= 31) return DBF.to_workbook(d, o);
	if(0x20>n[0]||n[0]>0x7F) throw new Error("Unsupported file " + n.join("|"));
	return PRN.to_workbook(d, o);
}
```
- example usage
```shell
...
  /* convert data to binary string */
  var data = new Uint8Array(arraybuffer);
  var arr = new Array();
  for(var i = 0; i != data.length; ++i) arr[i] = String.fromCharCode(data[i]);
  var bstr = arr.join("");

  /* Call XLSX */
  var workbook = XLSX.read(bstr, {type:"binary"});

  /* DO SOMETHING WITH workbook HERE */
}

oReq.send();
'''
...
```

#### <a name="apidoc.element.xlsx.readFile"></a>[function <span class="apidocSignatureSpan">xlsx.</span>readFile (filename, opts)](#apidoc.element.xlsx.readFile)
- description and source-code
```javascript
function readFileSync(filename, opts) {
	var o = opts||{}; o.type = 'file';
	return readSync(filename, o);
}
```
- example usage
```shell
...
For parsing, the first step is to read the file.  This involves acquiring the
data and feeding it into the library.  Here are a few common scenarios:

- node readFile:

'''js
if(typeof require !== 'undefined') XLSX = require('xlsx');
var workbook = XLSX.readFile('test.xlsx');
/* DO SOMETHING WITH workbook HERE */
'''

- Browser DOM Table element:

'''js
var worksheet = XLSX.utils.table_to_book(document.getElementById('tableau'));
...
```

#### <a name="apidoc.element.xlsx.readFileSync"></a>[function <span class="apidocSignatureSpan">xlsx.</span>readFileSync (filename, opts)](#apidoc.element.xlsx.readFileSync)
- description and source-code
```javascript
function readFileSync(filename, opts) {
	var o = opts||{}; o.type = 'file';
	return readSync(filename, o);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.write"></a>[function <span class="apidocSignatureSpan">xlsx.</span>write (wb, opts)](#apidoc.element.xlsx.write)
- description and source-code
```javascript
function writeSync(wb, opts) {
	check_wb(wb);
	var o = opts||{};
	switch(o.bookType || 'xlsb') {
		case 'xml':
		case 'xlml': return write_string_type(write_xlml(wb, o), o);
		case 'slk':
		case 'sylk': return write_string_type(write_slk_str(wb, o), o);
		case 'txt': return write_bstr_type(write_txt_str(wb, o), o);
		case 'csv': return write_string_type(write_csv_str(wb, o), o);
		case 'dif': return write_string_type(write_dif_str(wb, o), o);
		case 'prn': return write_string_type(write_prn_str(wb, o), o);
		case 'fods': return write_string_type(write_ods(wb, o), o);
		case 'biff2': return write_binary_type(write_biff_buf(wb, o), o);
		case 'xlsx':
		case 'xlsm':
		case 'xlsb':
		case 'ods': return write_zip_type(wb, o);
		default: throw new Error ("Unrecognized bookType |" + o.bookType + "|");
	}
}
```
- example usage
```shell
...
- browser generate binary blob and "download" to client
  (using [FileSaver.js](https://github.com/eligrey/FileSaver.js/) for download):

'''js
/* bookType can be 'xlsx' or 'xlsm' or 'xlsb' or 'ods' */
var wopts = { bookType:'xlsx', bookSST:false, type:'binary' };

var wbout = XLSX.write(workbook,wopts);

function s2ab(s) {
  var buf = new ArrayBuffer(s.length);
  var view = new Uint8Array(buf);
  for (var i=0; i!=s.length; ++i) view[i] = s.charCodeAt(i) & 0xFF;
  return buf;
}
...
```

#### <a name="apidoc.element.xlsx.writeFile"></a>[function <span class="apidocSignatureSpan">xlsx.</span>writeFile (wb, filename, opts)](#apidoc.element.xlsx.writeFile)
- description and source-code
```javascript
function writeFileSync(wb, filename, opts) {
	var o = opts||{}; o.type = 'file';
	o.file = filename;
	resolve_book_type(o);
	return writeSync(wb, o);
}
```
- example usage
```shell
...
dissemination.  The second step is to actual share the data with the end point.
Assuming 'workbook' is a workbook object:

- nodejs write to file:

'''js
/* output format determined by filename */
XLSX.writeFile(workbook, 'out.xlsx');
/* at this point, out.xlsx is a file that you can distribute */
'''

- browser generate binary blob and "download" to client
  (using [FileSaver.js](https://github.com/eligrey/FileSaver.js/) for download):

'''js
...
```

#### <a name="apidoc.element.xlsx.writeFileAsync"></a>[function <span class="apidocSignatureSpan">xlsx.</span>writeFileAsync (filename, wb, opts, cb)](#apidoc.element.xlsx.writeFileAsync)
- description and source-code
```javascript
function writeFileAsync(filename, wb, opts, cb) {
	var o = opts||{}; o.type = 'file';
	o.file = filename;
	resolve_book_type(o);
	o.type = 'buffer';
	var _cb = cb; if(!(_cb instanceof Function)) _cb = (opts);
	return _fs.writeFile(filename, writeSync(wb, o), _cb);
}
```
- example usage
```shell
...

### Writing functions

'XLSX.write(wb, write_opts)' attempts to write the workbook 'wb'

'XLSX.writeFile(wb, filename, write_opts)' attempts to write 'wb' to 'filename'

'XLSX.writeFileAsync(filename, wb, o, cb)' attempts to write 'wb' to 'filename'.
If 'o' is omitted, the writer will use the third argument as the callback.

Write options are described in the [Writing Options](#writing-options) section.

### Utilities

Utilities are available in the 'XLSX.utils' object:
...
```

#### <a name="apidoc.element.xlsx.writeFileSync"></a>[function <span class="apidocSignatureSpan">xlsx.</span>writeFileSync (wb, filename, opts)](#apidoc.element.xlsx.writeFileSync)
- description and source-code
```javascript
function writeFileSync(wb, filename, opts) {
	var o = opts||{}; o.type = 'file';
	o.file = filename;
	resolve_book_type(o);
	return writeSync(wb, o);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.write_ods"></a>[function <span class="apidocSignatureSpan">xlsx.</span>write_ods (wb, opts)](#apidoc.element.xlsx.write_ods)
- description and source-code
```javascript
function write_ods(wb, opts) {
	if(opts.bookType == "fods") return write_content_xml(wb, opts);

var zip = new jszip();
	var f = "";

	var manifest = [];
	var rdf = [];

	<span class="apidocCodeCommentSpan">/* 3:3.3 and 2:2.2.4 */
</span>	f = "mimetype";
	zip.file(f, "application/vnd.oasis.opendocument.spreadsheet");

	/* Part 1 Section 2.2 Documents */
	f = "content.xml";
	zip.file(f, write_content_xml(wb, opts));
	manifest.push([f, "text/xml"]);
	rdf.push([f, "ContentFile"]);

	/* Part 3 Section 6 Metadata Manifest File */
	f = "manifest.rdf";
	zip.file(f, write_rdf(rdf, opts));
	manifest.push([f, "application/rdf+xml"]);

	/* Part 3 Section 4 Manifest File */
	f = "META-INF/manifest.xml";
	zip.file(f, write_manifest(manifest, opts));

	return zip;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.xlsx.CFB"></a>[module xlsx.CFB](#apidoc.module.xlsx.CFB)

#### <a name="apidoc.element.xlsx.CFB.parse"></a>[function <span class="apidocSignatureSpan">xlsx.CFB.</span>parse (file)](#apidoc.element.xlsx.CFB.parse)
- description and source-code
```javascript
function parse(file) {
var mver = 3; // major version
var ssz = 512; // sector size
var nmfs = 0; // number of mini FAT sectors
var ndfs = 0; // number of DIFAT sectors
var dir_start = 0; // first directory sector location
var minifat_start = 0; // first mini FAT sector location
var difat_start = 0; // first mini FAT sector location

var fat_addrs = []; // locations of FAT sectors

<span class="apidocCodeCommentSpan">/* [MS-CFB] 2.2 Compound File Header */
</span>var blob = file.slice(0,512);
prep_blob(blob, 0);

/* major version */
var mv = check_get_mver(blob);
mver = mv[0];
switch(mver) {
	case 3: ssz = 512; break; case 4: ssz = 4096; break;
	default: throw new Error("Major Version: Expected 3 or 4 saw " + mver);
}

/* reprocess header */
if(ssz !== 512) { blob = file.slice(0,ssz); prep_blob(blob, 28 /* blob.l */); }
/* Save header for final object */
var header = file.slice(0,ssz);

check_shifts(blob, mver);

// Number of Directory Sectors
var nds = blob.read_shift(4, 'i');
if(mver === 3 && nds !== 0) throw new Error('# Directory Sectors: Expected 0 saw ' + nds);

// Number of FAT Sectors
//var nfs = blob.read_shift(4, 'i');
blob.l += 4;

// First Directory Sector Location
dir_start = blob.read_shift(4, 'i');

// Transaction Signature
blob.l += 4;

// Mini Stream Cutoff Size
blob.chk('00100000', 'Mini Stream Cutoff Size: ');

// First Mini FAT Sector Location
minifat_start = blob.read_shift(4, 'i');

// Number of Mini FAT Sectors
nmfs = blob.read_shift(4, 'i');

// First DIFAT sector location
difat_start = blob.read_shift(4, 'i');

// Number of DIFAT Sectors
ndfs = blob.read_shift(4, 'i');

// Grab FAT Sector Locations
for(var q, j = 0; j < 109; ++j) { /* 109 = (512 - blob.l)>>>2; */
	q = blob.read_shift(4, 'i');
	if(q<0) break;
	fat_addrs[j] = q;
}

/** Break the file up into sectors */
var sectors = sectorify(file, ssz);

sleuth_fat(difat_start, ndfs, sectors, ssz, fat_addrs);

/** Chains */
var sector_list = make_sector_list(sectors, dir_start, fat_addrs, ssz);

sector_list[dir_start].name = "!Directory";
if(nmfs > 0 && minifat_start !== ENDOFCHAIN) sector_list[minifat_start].name = "!MiniFAT";
sector_list[fat_addrs[0]].name = "!FAT";
sector_list.fat_addrs = fat_addrs;
sector_list.ssz = ssz;

/* [MS-CFB] 2.6.1 Compound File Directory Entry */
var files = {}, Paths = [], FileIndex = [], FullPaths = [], FullPathDir = {};
read_directory(dir_start, sector_list, sectors, Paths, nmfs, files, FileIndex);

build_full_paths(FileIndex, FullPathDir, FullPaths, Paths);

var root_name = Paths.shift();
Paths.root = root_name;

/* [MS-CFB] 2.6.4 (Unicode 3.0.1 case conversion) */
var find_path = make_find_path(FullPaths, Paths, FileIndex, files, root_name);

return {
	raw: {header: header, sectors: sectors},
	FileIndex: FileIndex,
	FullPaths: FullPaths,
	FullPathDir: FullPathDir,
	find: find_path
};
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.CFB.read"></a>[function <span class="apidocSignatureSpan">xlsx.CFB.</span>read (blob, options)](#apidoc.element.xlsx.CFB.read)
- description and source-code
```javascript
function readSync(blob, options) {
	switch(options !== undefined && options.type !== undefined ? options.type : "base64") {
		case "file": return readFileSync(blob, options);
		case "base64": return parse(s2a(Base64.decode(blob)), options);
		case "binary": return parse(s2a(blob), options);
	}
	return parse(blob);
}
```
- example usage
```shell
...
  /* convert data to binary string */
  var data = new Uint8Array(arraybuffer);
  var arr = new Array();
  for(var i = 0; i != data.length; ++i) arr[i] = String.fromCharCode(data[i]);
  var bstr = arr.join("");

  /* Call XLSX */
  var workbook = XLSX.read(bstr, {type:"binary"});

  /* DO SOMETHING WITH workbook HERE */
}

oReq.send();
'''
...
```



# <a name="apidoc.module.xlsx.CFB.utils"></a>[module xlsx.CFB.utils](#apidoc.module.xlsx.CFB.utils)

#### <a name="apidoc.element.xlsx.CFB.utils.CheckField"></a>[function <span class="apidocSignatureSpan">xlsx.CFB.utils.</span>CheckField (hexstr, fld)](#apidoc.element.xlsx.CFB.utils.CheckField)
- description and source-code
```javascript
function CheckField(hexstr, fld) {
	var m = __hexlify(this,this.l,hexstr.length>>1);
	if(m !== hexstr) throw fld + 'Expected ' + hexstr + ' saw ' + m;
	this.l += hexstr.length>>1;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.CFB.utils.ReadShift"></a>[function <span class="apidocSignatureSpan">xlsx.CFB.utils.</span>ReadShift (size, t)](#apidoc.element.xlsx.CFB.utils.ReadShift)
- description and source-code
```javascript
function ReadShift(size, t) {
	var o="", oI, oR, oo=[], w, vv, i, loc;
	switch(t) {
		case 'dbcs':
			loc = this.l;
			if(has_buf && Buffer.isBuffer(this)) o = this.slice(this.l, this.l+2*size).toString("utf16le");
			else for(i = 0; i != size; ++i) { o+=String.fromCharCode(__readUInt16LE(this, loc)); loc+=2; }
			size *= 2;
			break;

		case 'utf8': o = __utf8(this, this.l, this.l + size); break;
		case 'utf16le': size *= 2; o = __utf16le(this, this.l, this.l + size); break;

		case 'wstr':
			if(typeof cptable !== 'undefined') o = cptable.utils.decode(current_codepage, this.slice(this.l, this.l+2*size));
			else return ReadShift.call(this, size, 'dbcs');
			size = 2 * size; break;

		<span class="apidocCodeCommentSpan">/* [MS-OLEDS] 2.1.4 LengthPrefixedAnsiString */
</span>		case 'lpstr': o = __lpstr(this, this.l); size = 5 + o.length; break;
		/* [MS-OLEDS] 2.1.5 LengthPrefixedUnicodeString */
		case 'lpwstr': o = __lpwstr(this, this.l); size = 5 + o.length; if(o[o.length-1] == '\u0000') size += 2; break;

		case 'cstr': size = 0; o = "";
			while((w=__readUInt8(this, this.l + size++))!==0) oo.push(_getchar(w));
			o = oo.join(""); break;
		case '_wstr': size = 0; o = "";
			while((w=__readUInt16LE(this,this.l +size))!==0){oo.push(_getchar(w));size+=2;}
			size+=2; o = oo.join(""); break;

		/* sbcs and dbcs support continue records in the SST way TODO codepages */
		case 'dbcs-cont': o = ""; loc = this.l;
			for(i = 0; i != size; ++i) {
				if(this.lens && this.lens.indexOf(loc) !== -1) {
					w = __readUInt8(this, loc);
					this.l = loc + 1;
					vv = ReadShift.call(this, size-i, w ? 'dbcs-cont' : 'sbcs-cont');
					return oo.join("") + vv;
				}
				oo.push(_getchar(__readUInt16LE(this, loc)));
				loc+=2;
			} o = oo.join(""); size *= 2; break;

		case 'sbcs-cont': o = ""; loc = this.l;
			for(i = 0; i != size; ++i) {
				if(this.lens && this.lens.indexOf(loc) !== -1) {
					w = __readUInt8(this, loc);
					this.l = loc + 1;
					vv = ReadShift.call(this, size-i, w ? 'dbcs-cont' : 'sbcs-cont');
					return oo.join("") + vv;
				}
				oo.push(_getchar(__readUInt8(this, loc)));
				loc+=1;
			} o = oo.join(""); break;

		default:
	switch(size) {
		case 1: oI = __readUInt8(this, this.l); this.l++; return oI;
		case 2: oI = (t === 'i' ? __readInt16LE : __readUInt16LE)(this, this.l); this.l += 2; return oI;
		case 4:
			if(t === 'i' || (this[this.l+3] & 0x80)===0) { oI = __readInt32LE(this, this.l); this.l += 4; return oI; }
			else { oR = __readUInt32LE(this, this.l); this.l += 4; } return oR;
		case 8: if(t === 'f') { oR = __double(this, this.l); this.l += 8; return oR; }
		/* falls through */
		case 16: o = __hexlify(this, this.l, size); break;
	}}
	this.l+=size; return o;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.CFB.utils.bconcat"></a>[function <span class="apidocSignatureSpan">xlsx.CFB.utils.</span>bconcat (bufs)](#apidoc.element.xlsx.CFB.utils.bconcat)
- description and source-code
```javascript
bconcat = function (bufs) { return [].concat.apply([], bufs); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.CFB.utils.prep_blob"></a>[function <span class="apidocSignatureSpan">xlsx.CFB.utils.</span>prep_blob (blob, pos)](#apidoc.element.xlsx.CFB.utils.prep_blob)
- description and source-code
```javascript
function prep_blob(blob, pos) {
	blob.l = pos;
	blob.read_shift = ReadShift;
	blob.chk = CheckField;
	blob.write_shift = WriteShift;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.xlsx.SSF"></a>[module xlsx.SSF](#apidoc.module.xlsx.SSF)

#### <a name="apidoc.element.xlsx.SSF._eval"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>_eval (fmt, v, opts, flen)](#apidoc.element.xlsx.SSF._eval)
- description and source-code
```javascript
function eval_fmt(fmt, v, opts, flen) {
	var out = [], o = "", i = 0, c = "", lst='t', q, dt, j, cc;
	var hr='H';
	<span class="apidocCodeCommentSpan">/* Tokenize */
</span>	while(i < fmt.length) {
		switch((c = fmt.charAt(i))) {
			case 'G': /* General */
				if(!isgeneral(fmt, i)) throw new Error('unrecognized character ' + c + ' in ' +fmt);
				out[out.length] = {t:'G', v:'General'}; i+=7; break;
			case '"': /* Literal text */
				for(o="";(cc=fmt.charCodeAt(++i)) !== 34 && i < fmt.length;) o += String.fromCharCode(cc);
				out[out.length] = {t:'t', v:o}; ++i; break;
			case '\\': var w = fmt.charAt(++i), t = (w === "(" || w === ")") ? w : 't';
				out[out.length] = {t:t, v:w}; ++i; break;
			case '_': out[out.length] = {t:'t', v:" "}; i+=2; break;
			case '@': /* Text Placeholder */
				out[out.length] = {t:'T', v:v}; ++i; break;
			case 'B': case 'b':
				if(fmt.charAt(i+1) === "1" || fmt.charAt(i+1) === "2") {
					if(dt==null) { dt=parse_date_code(v, opts, fmt.charAt(i+1) === "2"); if(dt==null) return ""; }
					out[out.length] = {t:'X', v:fmt.substr(i,2)}; lst = c; i+=2; break;
				}
				/* falls through */
			case 'M': case 'D': case 'Y': case 'H': case 'S': case 'E':
				c = c.toLowerCase();
				/* falls through */
			case 'm': case 'd': case 'y': case 'h': case 's': case 'e': case 'g':
				if(v < 0) return "";
				if(dt==null) { dt=parse_date_code(v, opts); if(dt==null) return ""; }
				o = c; while(++i<fmt.length && fmt.charAt(i).toLowerCase() === c) o+=c;
				if(c === 'm' && lst.toLowerCase() === 'h') c = 'M'; /* m = minute */
				if(c === 'h') c = hr;
				out[out.length] = {t:c, v:o}; lst = c; break;
			case 'A':
				q={t:c, v:"A"};
				if(dt==null) dt=parse_date_code(v, opts);
				if(fmt.substr(i, 3) === "A/P") { if(dt!=null) q.v = dt.H >= 12 ? "P" : "A"; q.t = 'T'; hr='h';i+=3;}
				else if(fmt.substr(i,5) === "AM/PM") { if(dt!=null) q.v = dt.H >= 12 ? "PM" : "AM"; q.t = 'T'; i+=5; hr='h'; }
				else { q.t = "t"; ++i; }
				if(dt==null && q.t === 'T') return "";
				out[out.length] = q; lst = c; break;
			case '[':
				o = c;
				while(fmt.charAt(i++) !== ']' && i < fmt.length) o += fmt.charAt(i);
				if(o.slice(-1) !== ']') throw 'unterminated "[" block: |' + o + '|';
				if(o.match(abstime)) {
					if(dt==null) { dt=parse_date_code(v, opts); if(dt==null) return ""; }
					out[out.length] = {t:'Z', v:o.toLowerCase()};
				} else { o=""; }
				break;
			/* Numbers */
			case '.':
				if(dt != null) {
					o = c; while((c=fmt.charAt(++i)) === "0") o += c;
					out[out.length] = {t:'s', v:o}; break;
				}
				/* falls through */
			case '0': case '#':
				o = c; while(++i < fmt.length && "0#?.,E+-%".indexOf(c=fmt.charAt(i)) > -1 || c=='\\' && fmt.charAt(i+1) == "-" && "0#".indexOf
(fmt.charAt(i+2))>-1) o += c;
				out[out.length] = {t:'n', v:o}; break;
			case '?':
				o = c; while(fmt.charAt(++i) === c) o+=c;
				q={t:c, v:o}; out[out.length] = q; lst = c; break;
			case '*': ++i; if(fmt.charAt(i) == ' ' || fmt.charAt(i) == '*') ++i; break; // **
			case '(': case ')': out[out.length] = {t:(flen===1?'t':c), v:c}; ++i; break;
			case '1': case '2': case '3': case '4': case '5': case '6': case '7': case '8': case '9':
				o = c; while(i < fmt.length && "0123456789".indexOf(fmt.charAt(++i)) > -1) o+=fmt.charAt(i);
				out[out.length] = {t:'D', v:o}; break;
			case ' ': out[out.length] = {t:c, v:c}; ++i; break;
			default:
				if(",$-+/():!^&'~{}<>=€acfijklopqrtuvwxz".indexOf(c) === -1) throw new Error('unrecognized character ' + c + ' in ' + fmt);
				out[out.length] = {t:'t', v:c}; ++i; break;
		}
	}
	var bt = 0, ss0 = 0, ssm;
	for(i=out.length-1, lst='t'; i >= 0; --i) {
		switch(out[i].t) {
			case 'h': case 'H': out[i].t = hr; lst='h'; if(bt < 1) bt = 1; break;
			case 's':
				if((ssm=out[i].v.match(/\.0+$/))) ss0=Math.max(ss0,ssm[0].length-1);
				if(bt < 3) bt = 3;
			/* falls through */
			case 'd': case 'y': case 'M': case 'e': lst=out[i].t; break;
			case 'm': if(lst === 's') { out[i].t = 'M'; if(bt < 2) bt = 2; } break;
			case 'X': if(out[i].v === "B2");
				break;
			case 'Z':
				if(bt < 1 && out[i].v.match(/[Hh]/)) bt = 1;
				if(bt < 2 ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.SSF._general"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>_general (v, opts)](#apidoc.element.xlsx.SSF._general)
- description and source-code
```javascript
function general_fmt(v, opts) {
	switch(typeof v) {
		case 'string': return v;
		case 'boolean': return v ? "TRUE" : "FALSE";
		case 'number': return (v|0) === v ? general_fmt_int(v, opts) : general_fmt_num(v, opts);
	}
	throw new Error("unsupported value in General format: " + v);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.SSF._general_int"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>_general_int (v, opts)](#apidoc.element.xlsx.SSF._general_int)
- description and source-code
```javascript
function general_fmt_int(v, opts) { return ""+v; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.SSF._general_num"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>_general_num (v, opts)](#apidoc.element.xlsx.SSF._general_num)
- description and source-code
```javascript
function general_fmt_num(v, opts) {
	var V = Math.floor(Math.log(Math.abs(v))*Math.LOG10E), o;
	if(V >= -4 && V <= -1) o = v.toPrecision(10+V);
	else if(Math.abs(V) <= 9) o = gfn2(v);
	else if(V === 10) o = v.toFixed(10).substr(0,12);
	else o = gfn3(v);
	return gfn5(gfn4(o));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.SSF._split"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>_split (fmt)](#apidoc.element.xlsx.SSF._split)
- description and source-code
```javascript
function split_fmt(fmt) {
	var out = [];
	var in_str = false, cc;
	for(var i = 0, j = 0; i < fmt.length; ++i) switch((cc=fmt.charCodeAt(i))) {
		case 34:<span class="apidocCodeCommentSpan"> /* '"' */
</span>			in_str = !in_str; break;
		case 95: case 42: case 92: /* '_' '*' '\\' */
			++i; break;
		case 59: /* ';' */
			out[out.length] = fmt.substr(j,i-j);
			j = i+1;
	}
	out[out.length] = fmt.substr(j);
	if(in_str === true) throw new Error("Format |" + fmt + "| unterminated string ");
	return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.SSF.format"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>format (fmt, v, o)](#apidoc.element.xlsx.SSF.format)
- description and source-code
```javascript
function format(fmt, v, o) {
	fixopts(o != null ? o : (o=[]));
	var sfmt = "";
	switch(typeof fmt) {
		case "string": sfmt = fmt; break;
		case "number": sfmt = (o.table != null ? (o.table) : table_fmt)[fmt]; break;
	}
	if(isgeneral(sfmt,0)) return general_fmt(v, o);
	var f = choose_fmt(sfmt, v);
	if(isgeneral(f[1])) return general_fmt(v, o);
	if(v === true) v = "TRUE"; else if(v === false) v = "FALSE";
	else if(v === "" || v == null) return "";
	return eval_fmt(f[1], v, o, f[0]);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.SSF.get_table"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>get_table ()](#apidoc.element.xlsx.SSF.get_table)
- description and source-code
```javascript
function get_table() { return table_fmt; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.SSF.is_date"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>is_date (fmt)](#apidoc.element.xlsx.SSF.is_date)
- description and source-code
```javascript
function fmt_is_date(fmt) {
	var i = 0, cc = 0, c = "", o = "";
	while(i < fmt.length) {
		switch((c = fmt.charAt(i))) {
			case 'G': if(isgeneral(fmt, i)) i+= 6; i++; break;
			case '"': for(;(cc=fmt.charCodeAt(++i)) !== 34 && i < fmt.length;) ++i; ++i; break;
			case '\\': i+=2; break;
			case '_': i+=2; break;
			case '@': ++i; break;
			case 'B': case 'b':
				if(fmt.charAt(i+1) === "1" || fmt.charAt(i+1) === "2") return true;
				<span class="apidocCodeCommentSpan">/* falls through */
</span>			case 'M': case 'D': case 'Y': case 'H': case 'S': case 'E':
				/* falls through */
			case 'm': case 'd': case 'y': case 'h': case 's': case 'e': case 'g': return true;
			case 'A':
				if(fmt.substr(i, 3) === "A/P") return true;
				if(fmt.substr(i, 5) === "AM/PM") return true;
				++i; break;
			case '[':
				o = c;
				while(fmt.charAt(i++) !== ']' && i < fmt.length) o += fmt.charAt(i);
				if(o.match(abstime)) return true;
				break;
			case '.':
				/* falls through */
			case '0': case '#':
				while(i < fmt.length && ("0#?.,E+-%".indexOf(c=fmt.charAt(++i)) > -1 || c=='\\' && fmt.charAt(i+1) == "-" && "0#".indexOf(fmt
.charAt(i+2))>-1));
				break;
			case '?': while(fmt.charAt(++i) === c); break;
			case '*': ++i; if(fmt.charAt(i) == ' ' || fmt.charAt(i) == '*') ++i; break;
			case '(': case ')': ++i; break;
			case '1': case '2': case '3': case '4': case '5': case '6': case '7': case '8': case '9':
				while(i < fmt.length && "0123456789".indexOf(fmt.charAt(++i)) > -1); break;
			case ' ': ++i; break;
			default: ++i; break;
		}
	}
	return false;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.SSF.load"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>load (fmt, idx)](#apidoc.element.xlsx.SSF.load)
- description and source-code
```javascript
function load_entry(fmt, idx) { table_fmt[idx] = fmt; }
```
- example usage
```shell
...
this.files = {};

this.comment = null;

// Where we are in the hierarchy
this.root = "";
if (data) {
    this.load(data, options);
}
this.clone = function() {
    var newObj = new JSZip();
    for (var i in this) {
        if (typeof this[i] !== "function") {
            newObj[i] = this[i];
        }
...
```

#### <a name="apidoc.element.xlsx.SSF.load_table"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>load_table (tbl)](#apidoc.element.xlsx.SSF.load_table)
- description and source-code
```javascript
function load_table(tbl) { for(var i=0; i!=0x0188; ++i) if(tbl[i] !== undefined) SSF.load(tbl[i], i); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.SSF.parse_date_code"></a>[function <span class="apidocSignatureSpan">xlsx.SSF.</span>parse_date_code (v, opts, b2)](#apidoc.element.xlsx.SSF.parse_date_code)
- description and source-code
```javascript
function parse_date_code(v, opts, b2) {
	if(v > 2958465 || v < 0) return null;
	var date = (v|0), time = Math.floor(86400 * (v - date)), dow=0;
	var dout=[];
	var out={D:date, T:time, u:86400*(v-date)-time,y:0,m:0,d:0,H:0,M:0,S:0,q:0};
	if(Math.abs(out.u) < 1e-6) out.u = 0;
	fixopts(opts != null ? opts : (opts=[]));
	if(opts.date1904) date += 1462;
	if(out.u > 0.999) {
		out.u = 0;
		if(++time == 86400) { time = 0; ++date; }
	}
	if(date === 60) {dout = b2 ? [1317,10,29] : [1900,2,29]; dow=3;}
	else if(date === 0) {dout = b2 ? [1317,8,29] : [1900,1,0]; dow=6;}
	else {
		if(date > 60) --date;
		<span class="apidocCodeCommentSpan">/* 1 = Jan 1 1900 in Gregorian */
</span>		var d = new Date(1900, 0, 1);
		d.setDate(d.getDate() + date - 1);
		dout = [d.getFullYear(), d.getMonth()+1,d.getDate()];
		dow = d.getDay();
		if(date < 60) dow = (dow + 6) % 7;
		if(b2) dow = fix_hijri(d, dout);
	}
	out.y = dout[0]; out.m = dout[1]; out.d = dout[2];
	out.S = time % 60; time = Math.floor(time / 60);
	out.M = time % 60; time = Math.floor(time / 60);
	out.H = time;
	out.q = dow;
	return out;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.xlsx.jszip"></a>[module xlsx.jszip](#apidoc.module.xlsx.jszip)

#### <a name="apidoc.element.xlsx.jszip.jszip"></a>[function <span class="apidocSignatureSpan">xlsx.</span>jszip (data, options)](#apidoc.element.xlsx.jszip.jszip)
- description and source-code
```javascript
function JSZip(data, options) {
    // if this constructor is used without 'new', it adds 'new' before itself:
    if(!(this instanceof JSZip)) return new JSZip(data, options);

    // object containing the files :
    // {
    //   "folder/" : {...},
    //   "folder/data.txt" : {...}
    // }
    this.files = {};

    this.comment = null;

    // Where we are in the hierarchy
    this.root = "";
    if (data) {
        this.load(data, options);
    }
    this.clone = function() {
        var newObj = new JSZip();
        for (var i in this) {
            if (typeof this[i] !== "function") {
                newObj[i] = this[i];
            }
        }
        return newObj;
    };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.xlsx.jszip.prototype"></a>[module xlsx.jszip.prototype](#apidoc.module.xlsx.jszip.prototype)

#### <a name="apidoc.element.xlsx.jszip.prototype.crc32"></a>[function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>crc32 (input, crc)](#apidoc.element.xlsx.jszip.prototype.crc32)
- description and source-code
```javascript
crc32 = function (input, crc) {
    return crc32(input, crc);
}
```
- example usage
```shell
...

    if(useUTF8ForComment) {

unicodeCommentExtraField =
    // Version
    decToHex(1, 1) +
    // CommentCRC32
    decToHex(this.crc32(utfEncodedComment), 4) +
    // UnicodeName
    utfEncodedComment;

extraFields +=
    // Info-ZIP Unicode Path Extra Field
    "\x75\x63" +
    // size
...
```

#### <a name="apidoc.element.xlsx.jszip.prototype.file"></a>[function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>file (name, data, o)](#apidoc.element.xlsx.jszip.prototype.file)
- description and source-code
```javascript
file = function (name, data, o) {
    if (arguments.length === 1) {
        if (utils.isRegExp(name)) {
            var regexp = name;
            return this.filter(function(relativePath, file) {
                return !file.dir && regexp.test(relativePath);
            });
        }
        else { // text
            return this.filter(function(relativePath, file) {
                return !file.dir && relativePath === name;
            })[0] || null;
        }
    }
    else { // more than one argument : we have data !
        name = this.root + name;
        fileAdd.call(this, name, data, o);
    }
    return this;
}
```
- example usage
```shell
...
'use strict';

var base64 = _dereq_('./base64');

/**
Usage:
   zip = new JSZip();
   zip.file("hello.txt", "Hello, World!").file("tempfile", "nothing");
   zip.folder("images").file("smile.gif", base64Data, {base64: true});
   zip.file("Xmas.txt", "Ho ho ho !", {date : new Date("December 25, 2007 00:00:01")});
   zip.remove("tempfile");

   base64zip = zip.generate();

**/
...
```

#### <a name="apidoc.element.xlsx.jszip.prototype.filter"></a>[function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>filter (search)](#apidoc.element.xlsx.jszip.prototype.filter)
- description and source-code
```javascript
filter = function (search) {
    var result = [],
        filename, relativePath, file, fileClone;
    for (filename in this.files) {
        if (!this.files.hasOwnProperty(filename)) {
            continue;
        }
        file = this.files[filename];
        // return a new object, don't let the user mess with our internal objects :)
        fileClone = new ZipObject(file.name, file._data, extend(file.options));
        relativePath = filename.slice(this.root.length, filename.length);
        if (filename.slice(0, this.root.length) === this.root && // the file is in the current root
        search(relativePath, fileClone)) { // and the file matches the function
            result.push(fileClone);
        }
    }
    return result;
}
```
- example usage
```shell
...
'XLSX.utils.sheet_to_formulae' generates an array of commands that represent
how a person would enter data into an application.  Each entry is of the form
'A1-cell-address=formula-or-value'.  String literals are prefixed with a ''' in
accordance with Excel.  For the example sheet:

'''js
> var o = XLSX.utils.sheet_to_formulae(ws);
> o.filter(function(v, i) { return i % 5 === 0; });
[ 'A1=\'S', 'F1=\'J', 'D2=4', 'B3=3', 'G3=8' ]
'''

### Delimiter-Separated Output

As an alternative to the 'writeFile' CSV type, 'XLSX.utils.sheet_to_csv' also
produces CSV output.  The function takes an options argument:
...
```

#### <a name="apidoc.element.xlsx.jszip.prototype.folder"></a>[function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>folder (arg)](#apidoc.element.xlsx.jszip.prototype.folder)
- description and source-code
```javascript
folder = function (arg) {
    if (!arg) {
        return this;
    }

    if (utils.isRegExp(arg)) {
        return this.filter(function(relativePath, file) {
            return file.dir && arg.test(relativePath);
        });
    }

    // else, name is a new folder
    var name = this.root + arg;
    var newFolder = folderAdd.call(this, name);

    // Allow chaining by returning a new object with this folder as the root
    var ret = this.clone();
    ret.root = newFolder.name;
    return ret;
}
```
- example usage
```shell
...

var base64 = _dereq_('./base64');

/**
Usage:
   zip = new JSZip();
   zip.file("hello.txt", "Hello, World!").file("tempfile", "nothing");
   zip.folder("images").file("smile.gif", base64Data, {base64: true});
   zip.file("Xmas.txt", "Ho ho ho !", {date : new Date("December 25, 2007 00:00:01")});
   zip.remove("tempfile");

   base64zip = zip.generate();

**/
...
```

#### <a name="apidoc.element.xlsx.jszip.prototype.generate"></a>[function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>generate (options)](#apidoc.element.xlsx.jszip.prototype.generate)
- description and source-code
```javascript
generate = function (options) {
    options = extend(options || {}, {
        base64: true,
        compression: "STORE",
        type: "base64",
        comment: null
    });

    utils.checkSupport(options.type);

    var zipData = [],
        localDirLength = 0,
        centralDirLength = 0,
        writer, i,
        utfEncodedComment = utils.transformTo("string", this.utf8encode(options.comment || this.comment || ""));

    // first, generate all the zip parts.
    for (var name in this.files) {
        if (!this.files.hasOwnProperty(name)) {
            continue;
        }
        var file = this.files[name];

        var compressionName = file.options.compression || options.compression.toUpperCase();
        var compression = compressions[compressionName];
        if (!compression) {
            throw new Error(compressionName + " is not a valid compression method !");
        }

        var compressedObject = generateCompressedObjectFrom.call(this, file, compression);

        var zipPart = generateZipParts.call(this, name, file, compressedObject, localDirLength);
        localDirLength += zipPart.fileRecord.length + compressedObject.compressedSize;
        centralDirLength += zipPart.dirRecord.length;
        zipData.push(zipPart);
    }

    var dirEnd = "";

    // end of central dir signature
    dirEnd = signature.CENTRAL_DIRECTORY_END +
    // number of this disk
    "\x00\x00" +
    // number of the disk with the start of the central directory
    "\x00\x00" +
    // total number of entries in the central directory on this disk
    decToHex(zipData.length, 2) +
    // total number of entries in the central directory
    decToHex(zipData.length, 2) +
    // size of the central directory   4 bytes
    decToHex(centralDirLength, 4) +
    // offset of start of central directory with respect to the starting disk number
    decToHex(localDirLength, 4) +
    // .ZIP file comment length
    decToHex(utfEncodedComment.length, 2) +
    // .ZIP file comment
    utfEncodedComment;


    // we have all the parts (and the total length)
    // time to create a writer !
    var typeName = options.type.toLowerCase();
    if(typeName==="uint8array"||typeName==="arraybuffer"||typeName==="blob"||typeName==="nodebuffer") {
        writer = new Uint8ArrayWriter(localDirLength + centralDirLength + dirEnd.length);
    }else{
        writer = new StringWriter(localDirLength + centralDirLength + dirEnd.length);
    }

    for (i = 0; i < zipData.length; i++) {
        writer.append(zipData[i].fileRecord);
        writer.append(zipData[i].compressedObject.compressedContent);
    }
    for (i = 0; i < zipData.length; i++) {
        writer.append(zipData[i].dirRecord);
    }

    writer.append(dirEnd);

    var zip = writer.finalize();



    switch(options.type.toLowerCase()) {
        // case "zip is an Uint8Array"
        case "uint8array" :
        case "arraybuffer" :
        case "nodebuffer" :
           return utils.transformTo(options.type.toLowerCase(), zip);
        case "blob" :
           return utils.arrayBuffer2Blob(utils.transformTo("arraybuffer", zip));
        // case "zip is a string"
        case "base64" :
           return (options.base64) ? base64.encode(zip) : zip;
        default : // case "string" :
           return zip;
     }

}
```
- example usage
```shell
...
Usage:
  zip = new JSZip();
  zip.file("hello.txt", "Hello, World!").file("tempfile", "nothing");
  zip.folder("images").file("smile.gif", base64Data, {base64: true});
  zip.file("Xmas.txt", "Ho ho ho !", {date : new Date("December 25, 2007 00:00:01")});
  zip.remove("tempfile");

  base64zip = zip.generate();

**/

/**
* Representation a of zip file in js
* @constructor
* @param {String=|ArrayBuffer=|Uint8Array=} data the data to load, if any (optional).
...
```

#### <a name="apidoc.element.xlsx.jszip.prototype.load"></a>[function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>load (data, options)](#apidoc.element.xlsx.jszip.prototype.load)
- description and source-code
```javascript
load = function (data, options) {
    var files, zipEntries, i, input;
    options = options || {};
    if (options.base64) {
        data = base64.decode(data);
    }

    zipEntries = new ZipEntries(data, options);
    files = zipEntries.files;
    for (i = 0; i < files.length; i++) {
        input = files[i];
        this.file(input.fileName, input.decompressed, {
            binary: true,
            optimizedBinaryString: true,
            date: input.date,
            dir: input.dir,
            comment : input.fileComment.length ? input.fileComment : null,
            createFolders: options.createFolders
        });
    }
    if (zipEntries.zipComment.length) {
        this.comment = zipEntries.zipComment;
    }

    return this;
}
```
- example usage
```shell
...
this.files = {};

this.comment = null;

// Where we are in the hierarchy
this.root = "";
if (data) {
    this.load(data, options);
}
this.clone = function() {
    var newObj = new JSZip();
    for (var i in this) {
        if (typeof this[i] !== "function") {
            newObj[i] = this[i];
        }
...
```

#### <a name="apidoc.element.xlsx.jszip.prototype.remove"></a>[function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>remove (name)](#apidoc.element.xlsx.jszip.prototype.remove)
- description and source-code
```javascript
remove = function (name) {
    name = this.root + name;
    var file = this.files[name];
    if (!file) {
        // Look for any folders
        if (name.slice(-1) != "/") {
            name += "/";
        }
        file = this.files[name];
    }

    if (file && !file.dir) {
        // file
        delete this.files[name];
    } else {
        // maybe a folder, delete recursively
        var kids = this.filter(function(relativePath, file) {
            return file.name.slice(0, name.length) === name;
        });
        for (var i = 0; i < kids.length; i++) {
            delete this.files[kids[i].name];
        }
    }

    return this;
}
```
- example usage
```shell
...

/**
Usage:
  zip = new JSZip();
  zip.file("hello.txt", "Hello, World!").file("tempfile", "nothing");
  zip.folder("images").file("smile.gif", base64Data, {base64: true});
  zip.file("Xmas.txt", "Ho ho ho !", {date : new Date("December 25, 2007 00:00:01")});
  zip.remove("tempfile");

  base64zip = zip.generate();

**/

/**
* Representation a of zip file in js
...
```

#### <a name="apidoc.element.xlsx.jszip.prototype.utf8decode"></a>[function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>utf8decode (input)](#apidoc.element.xlsx.jszip.prototype.utf8decode)
- description and source-code
```javascript
utf8decode = function (input) {
    return utf8.utf8decode(input);
}
```
- example usage
```shell
...
// if the data is a base64 string, we decode it before checking the encoding !
if (this.options.base64) {
    result = base64.decode(result);
}
if (asUTF8 && this.options.binary) {
    // JSZip.prototype.utf8decode supports arrays as input
    // skip to array => string step, utf8decode will do it.
    result = out.utf8decode(result);
}
else {
    // no utf8 transformation, do the array => string step.
    result = utils.transformTo("string", result);
}

if (!asUTF8 && !this.options.binary) {
...
```

#### <a name="apidoc.element.xlsx.jszip.prototype.utf8encode"></a>[function <span class="apidocSignatureSpan">xlsx.jszip.prototype.</span>utf8encode (string)](#apidoc.element.xlsx.jszip.prototype.utf8encode)
- description and source-code
```javascript
utf8encode = function (string) {
    return utils.transformTo("string", utf8.utf8encode(string));
}
```
- example usage
```shell
...
   }
   else {
       // no utf8 transformation, do the array => string step.
       result = utils.transformTo("string", result);
   }

   if (!asUTF8 && !this.options.binary) {
       result = utils.transformTo("string", out.utf8encode(result));
   }
   return result;
};
/**
* A simple object representing a file in the zip file.
* @constructor
* @param {string} name the name of the file
...
```



# <a name="apidoc.module.xlsx.utils"></a>[module xlsx.utils](#apidoc.module.xlsx.utils)

#### <a name="apidoc.element.xlsx.utils.aoa_to_sheet"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>aoa_to_sheet (data, opts)](#apidoc.element.xlsx.utils.aoa_to_sheet)
- description and source-code
```javascript
function aoa_to_sheet(data, opts) {
	var o = opts || {};
	var ws = ({});
	var range = ({s: {c:10000000, r:10000000}, e: {c:0, r:0}});
	for(var R = 0; R != data.length; ++R) {
		for(var C = 0; C != data[R].length; ++C) {
			if(typeof data[R][C] === 'undefined') continue;
			var cell = ({v: data[R][C] });
			if(range.s.r > R) range.s.r = R;
			if(range.s.c > C) range.s.c = C;
			if(range.e.r < R) range.e.r = R;
			if(range.e.c < C) range.e.c = C;
			var cell_ref = encode_cell(({c:C,r:R}));
			if(cell.v === null) { if(!o.cellStubs) continue; cell.t = 'z'; }
			else if(typeof cell.v === 'number') cell.t = 'n';
			else if(typeof cell.v === 'boolean') cell.t = 'b';
			else if(cell.v instanceof Date) {
				cell.z = o.dateNF || SSF._table[14];
				if(o.cellDates) { cell.t = 'd'; cell.w = SSF.format(cell.z, datenum(cell.v)); }
				else { cell.t = 'n'; cell.v = datenum(cell.v); cell.w = SSF.format(cell.z, cell.v); }
			}
			else cell.t = 's';
			ws[cell_ref] = cell;
		}
	}
	if(range.s.c < 10000000) ws['!ref'] = encode_range(range);
	return ws;
}
```
- example usage
```shell
...
| dateNF      |  fmt 14  | Use specified date format in string output          |
| cellDates   |  false   | Store dates as type 'd' (default is 'n')            |
| sheetStubs  |  false   | Create cell objects of type 'z' for 'null' values   |

To generate the example sheet:

'''js
var ws = XLSX.utils.aoa_to_sheet([
	"SheetJS".split(""),
	[1,2,3,4,5,6,7],
	[2,3,4,5,6,7,8]
]);
'''

### HTML Table Input
...
```

#### <a name="apidoc.element.xlsx.utils.decode_cell"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>decode_cell (cstr)](#apidoc.element.xlsx.utils.decode_cell)
- description and source-code
```javascript
function decode_cell(cstr) { var splt = split_cell(cstr); return { c:decode_col(splt[0]), r:decode_row(splt[1]) }; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.decode_col"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>decode_col (colstr)](#apidoc.element.xlsx.utils.decode_col)
- description and source-code
```javascript
function decode_col(colstr) { var c = unfix_col(colstr), d = 0, i = 0; for(; i !== c.length; ++i) d = 26*d + c.charCodeAt(i) - 64
; return d - 1; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.decode_range"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>decode_range (range)](#apidoc.element.xlsx.utils.decode_range)
- description and source-code
```javascript
function decode_range(range) { var x =range.split(":").map(decode_cell); return {s:x[0],e:x[x.length-1]}; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.decode_row"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>decode_row (rowstr)](#apidoc.element.xlsx.utils.decode_row)
- description and source-code
```javascript
function decode_row(rowstr) { return parseInt(unfix_row(rowstr),10) - 1; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.encode_cell"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>encode_cell (cell)](#apidoc.element.xlsx.utils.encode_cell)
- description and source-code
```javascript
function encode_cell(cell) { return encode_col(cell.c) + encode_row(cell.r); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.encode_col"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>encode_col (col)](#apidoc.element.xlsx.utils.encode_col)
- description and source-code
```javascript
function encode_col(col) { var s=""; for(++col; col; col=Math.floor((col-1)/26)) s = String.fromCharCode(((col-1)%26) + 65) + s;
return s; }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.encode_range"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>encode_range (cs, ce)](#apidoc.element.xlsx.utils.encode_range)
- description and source-code
```javascript
function encode_range(cs, ce) {
	if(typeof ce === 'undefined' || typeof ce === 'number') {
return encode_range(cs.s, cs.e);
	}
if(typeof cs !== 'string') cs = encode_cell((cs));
	if(typeof ce !== 'string') ce = encode_cell((ce));
return cs == ce ? cs : cs + ":" + ce;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.encode_row"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>encode_row (row)](#apidoc.element.xlsx.utils.encode_row)
- description and source-code
```javascript
function encode_row(row) { return "" + (row + 1); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.format_cell"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>format_cell (cell, v, o)](#apidoc.element.xlsx.utils.format_cell)
- description and source-code
```javascript
function format_cell(cell, v, o) {
	if(cell == null || cell.t == null || cell.t == 'z') return "";
	if(cell.w !== undefined) return cell.w;
	if(cell.t == 'd' && !cell.z && o && o.dateNF) cell.z = o.dateNF;
	if(v == undefined) return safe_format_cell(cell, cell.v, o);
	return safe_format_cell(cell, v, o);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.get_formulae"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>get_formulae (sheet)](#apidoc.element.xlsx.utils.get_formulae)
- description and source-code
```javascript
function sheet_to_formulae(sheet) {
	var y = "", x, val="";
	if(sheet == null || sheet["!ref"] == null) return [];
	var r = safe_decode_range(sheet['!ref']), rr = "", cols = [], C;
	var cmds = new Array((r.e.r-r.s.r+1)*(r.e.c-r.s.c+1));
	var i = 0;
	for(C = r.s.c; C <= r.e.c; ++C) cols[C] = encode_col(C);
	for(var R = r.s.r; R <= r.e.r; ++R) {
		rr = encode_row(R);
		for(C = r.s.c; C <= r.e.c; ++C) {
			y = cols[C] + rr;
			x = sheet[y];
			val = "";
			if(x === undefined) continue;
			else if(x.F != null) {
				y = x.F;
				if(!x.f) continue;
				val = x.f;
				if(y.indexOf(":") == -1) y = y + ":" + y;
			}
			if(x.f != null) val = x.f;
			else if(x.t == 'z') continue;
			else if(x.t == 'n' && x.v != null) val = "" + x.v;
			else if(x.t == 'b') val = x.v ? "TRUE" : "FALSE";
			else if(x.w !== undefined) val = "'" + x.w;
			else if(x.v === undefined) continue;
			else if(x.t == 's') val = "'" + x.v;
			else val = ""+x.v;
			cmds[i++] = y + "=" + val;
		}
	}
	cmds.length = i;
	return cmds;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.make_csv"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>make_csv (sheet, opts)](#apidoc.element.xlsx.utils.make_csv)
- description and source-code
```javascript
function sheet_to_csv(sheet, opts) {
	var out = "", txt = "", qreg = /"/g;
	var o = opts == null ? {} : opts;
	if(sheet == null || sheet["!ref"] == null) return "";
	var r = safe_decode_range(sheet["!ref"]);
	var FS = o.FS !== undefined ? o.FS : ",", fs = FS.charCodeAt(0);
	var RS = o.RS !== undefined ? o.RS : "\n", rs = RS.charCodeAt(0);
	var endregex = new RegExp((FS=="|" ? "\\|" : FS)+"+$");
	var row = "", rr = "", cols = [];
	var i = 0, cc = 0, val;
	var R = 0, C = 0;
	for(C = r.s.c; C <= r.e.c; ++C) cols[C] = encode_col(C);
	for(R = r.s.r; R <= r.e.r; ++R) {
		var isempty = true;
		row = "";
		rr = encode_row(R);
		for(C = r.s.c; C <= r.e.c; ++C) {
			val = sheet[cols[C] + rr];
			if(val == null) txt = "";
			else if(val.v != null) {
				isempty = false;
				txt = ''+format_cell(val, null, o);
				for(i = 0, cc = 0; i !== txt.length; ++i) if((cc = txt.charCodeAt(i)) === fs || cc === rs || cc === 34) {
					txt = "\"" + txt.replace(qreg, '""') + "\""; break; }
			} else if(val.f != null && !val.F) {
				isempty = false;
				txt = '=' + val.f; if(txt.indexOf(",") >= 0) txt = '"' + txt.replace(qreg, '""') + '"';
			} else txt = "";
			<span class="apidocCodeCommentSpan">/* NOTE: Excel CSV does not support array formulae */
</span>			row += (C === r.s.c ? "" : FS) + txt;
		}
		if(o.blankrows === false && isempty) continue;
		if(o.strip) row = row.replace(endregex,"");
		out += row + RS;
	}
	return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.make_formulae"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>make_formulae (sheet)](#apidoc.element.xlsx.utils.make_formulae)
- description and source-code
```javascript
function sheet_to_formulae(sheet) {
	var y = "", x, val="";
	if(sheet == null || sheet["!ref"] == null) return [];
	var r = safe_decode_range(sheet['!ref']), rr = "", cols = [], C;
	var cmds = new Array((r.e.r-r.s.r+1)*(r.e.c-r.s.c+1));
	var i = 0;
	for(C = r.s.c; C <= r.e.c; ++C) cols[C] = encode_col(C);
	for(var R = r.s.r; R <= r.e.r; ++R) {
		rr = encode_row(R);
		for(C = r.s.c; C <= r.e.c; ++C) {
			y = cols[C] + rr;
			x = sheet[y];
			val = "";
			if(x === undefined) continue;
			else if(x.F != null) {
				y = x.F;
				if(!x.f) continue;
				val = x.f;
				if(y.indexOf(":") == -1) y = y + ":" + y;
			}
			if(x.f != null) val = x.f;
			else if(x.t == 'z') continue;
			else if(x.t == 'n' && x.v != null) val = "" + x.v;
			else if(x.t == 'b') val = x.v ? "TRUE" : "FALSE";
			else if(x.w !== undefined) val = "'" + x.w;
			else if(x.v === undefined) continue;
			else if(x.t == 's') val = "'" + x.v;
			else val = ""+x.v;
			cmds[i++] = y + "=" + val;
		}
	}
	cmds.length = i;
	return cmds;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.make_json"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>make_json (sheet, opts)](#apidoc.element.xlsx.utils.make_json)
- description and source-code
```javascript
function sheet_to_json(sheet, opts){
	var val, row, range, header = 0, offset = 1, r, hdr = [], isempty, R, C, v, vv;
	var o = opts != null ? opts : {};
	var raw = o.raw;
	var defval = o.defval;
	if(sheet == null || sheet["!ref"] == null) return [];
	range = o.range != null ? o.range : sheet["!ref"];
	if(o.header === 1) header = 1;
	else if(o.header === "A") header = 2;
	else if(Array.isArray(o.header)) header = 3;
	switch(typeof range) {
		case 'string': r = safe_decode_range(range); break;
		case 'number': r = safe_decode_range(sheet["!ref"]); r.s.r = range; break;
		default: r = range;
	}
	if(header > 0) offset = 0;
	var rr = encode_row(r.s.r);
	var cols = new Array(r.e.c-r.s.c+1);
	var out = new Array(r.e.r-r.s.r-offset+1);
	var outi = 0;
	for(C = r.s.c; C <= r.e.c; ++C) {
		cols[C] = encode_col(C);
		val = sheet[cols[C] + rr];
		switch(header) {
			case 1: hdr[C] = C; break;
			case 2: hdr[C] = cols[C]; break;
			case 3: hdr[C] = o.header[C - r.s.c]; break;
			default:
				if(val == null) continue;
				vv = v = format_cell(val, null, o);
				var counter = 0;
				for(var CC = 0; CC < hdr.length; ++CC) if(hdr[CC] == vv) vv = v + "_" + (++counter);
				hdr[C] = vv;
		}
	}

	for (R = r.s.r + offset; R <= r.e.r; ++R) {
		rr = encode_row(R);
		isempty = true;
		if(header === 1) row = [];
		else {
			row = {};
			if(Object.defineProperty) try { Object.defineProperty(row, '__rowNum__', {value:R, enumerable:false}); } catch(e) { row.__rowNum__
 = R; }
			else row.__rowNum__ = R;
		}
		for (C = r.s.c; C <= r.e.c; ++C) {
			val = sheet[cols[C] + rr];
			if(val === undefined || val.t === undefined) {
				if(defval === undefined) continue;
				if(hdr[C] != null) { row[hdr[C]] = defval; isempty = false; }
				continue;
			}
			v = val.v;
			switch(val.t){
				case 'z': if(v == null) break; continue;
				case 'e': continue;
				case 's': case 'd': case 'b': case 'n': break;
				default: throw new Error('unrecognized type ' + val.t);
			}
			if(hdr[C] != null) {
				if(v == null) {
					if(defval !== undefined) row[hdr[C]] = defval;
					else if(raw && v === null) row[hdr[C]] = null;
					else continue;
				} else {
					row[hdr[C]] = raw ? v : format_cell(val,v,o);
				}
				isempty = false;
			}
		}
		if((isempty === false) || (header === 1 ? o.blankrows !== false : !!o.blankrows)) out[outi++] = row;
	}
	out.length = outi;
	return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.sheet_to_csv"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>sheet_to_csv (sheet, opts)](#apidoc.element.xlsx.utils.sheet_to_csv)
- description and source-code
```javascript
function sheet_to_csv(sheet, opts) {
	var out = "", txt = "", qreg = /"/g;
	var o = opts == null ? {} : opts;
	if(sheet == null || sheet["!ref"] == null) return "";
	var r = safe_decode_range(sheet["!ref"]);
	var FS = o.FS !== undefined ? o.FS : ",", fs = FS.charCodeAt(0);
	var RS = o.RS !== undefined ? o.RS : "\n", rs = RS.charCodeAt(0);
	var endregex = new RegExp((FS=="|" ? "\\|" : FS)+"+$");
	var row = "", rr = "", cols = [];
	var i = 0, cc = 0, val;
	var R = 0, C = 0;
	for(C = r.s.c; C <= r.e.c; ++C) cols[C] = encode_col(C);
	for(R = r.s.r; R <= r.e.r; ++R) {
		var isempty = true;
		row = "";
		rr = encode_row(R);
		for(C = r.s.c; C <= r.e.c; ++C) {
			val = sheet[cols[C] + rr];
			if(val == null) txt = "";
			else if(val.v != null) {
				isempty = false;
				txt = ''+format_cell(val, null, o);
				for(i = 0, cc = 0; i !== txt.length; ++i) if((cc = txt.charCodeAt(i)) === fs || cc === rs || cc === 34) {
					txt = "\"" + txt.replace(qreg, '""') + "\""; break; }
			} else if(val.f != null && !val.F) {
				isempty = false;
				txt = '=' + val.f; if(txt.indexOf(",") >= 0) txt = '"' + txt.replace(qreg, '""') + '"';
			} else txt = "";
			<span class="apidocCodeCommentSpan">/* NOTE: Excel CSV does not support array formulae */
</span>			row += (C === r.s.c ? "" : FS) + txt;
		}
		if(o.blankrows === false && isempty) continue;
		if(o.strip) row = row.replace(endregex,"");
		out += row + RS;
	}
	return out;
}
```
- example usage
```shell
...

- 'strip' will remove trailing commas from each line under default 'FS/RS'
- blankrows must be set to 'false' to skip blank lines.

For the example sheet:

'''js
> console.log(XLSX.utils.sheet_to_csv(ws));
S,h,e,e,t,J,S
1,2,3,4,5,6,7
2,3,4,5,6,7,8
> console.log(XLSX.utils.sheet_to_csv(ws, {FS:"\t"}));
S	h	e	e	t	J	S
1	2	3	4	5	6	7
2	3	4	5	6	7	8
...
```

#### <a name="apidoc.element.xlsx.utils.sheet_to_formulae"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>sheet_to_formulae (sheet)](#apidoc.element.xlsx.utils.sheet_to_formulae)
- description and source-code
```javascript
function sheet_to_formulae(sheet) {
	var y = "", x, val="";
	if(sheet == null || sheet["!ref"] == null) return [];
	var r = safe_decode_range(sheet['!ref']), rr = "", cols = [], C;
	var cmds = new Array((r.e.r-r.s.r+1)*(r.e.c-r.s.c+1));
	var i = 0;
	for(C = r.s.c; C <= r.e.c; ++C) cols[C] = encode_col(C);
	for(var R = r.s.r; R <= r.e.r; ++R) {
		rr = encode_row(R);
		for(C = r.s.c; C <= r.e.c; ++C) {
			y = cols[C] + rr;
			x = sheet[y];
			val = "";
			if(x === undefined) continue;
			else if(x.F != null) {
				y = x.F;
				if(!x.f) continue;
				val = x.f;
				if(y.indexOf(":") == -1) y = y + ":" + y;
			}
			if(x.f != null) val = x.f;
			else if(x.t == 'z') continue;
			else if(x.t == 'n' && x.v != null) val = "" + x.v;
			else if(x.t == 'b') val = x.v ? "TRUE" : "FALSE";
			else if(x.w !== undefined) val = "'" + x.w;
			else if(x.v === undefined) continue;
			else if(x.t == 's') val = "'" + x.v;
			else val = ""+x.v;
			cmds[i++] = y + "=" + val;
		}
	}
	cmds.length = i;
	return cmds;
}
```
- example usage
```shell
...

'XLSX.utils.sheet_to_formulae' generates an array of commands that represent
how a person would enter data into an application.  Each entry is of the form
'A1-cell-address=formula-or-value'.  String literals are prefixed with a ''' in
accordance with Excel.  For the example sheet:

'''js
> var o = XLSX.utils.sheet_to_formulae(ws);
> o.filter(function(v, i) { return i % 5 === 0; });
[ 'A1=\'S', 'F1=\'J', 'D2=4', 'B3=3', 'G3=8' ]
'''

### Delimiter-Separated Output

As an alternative to the 'writeFile' CSV type, 'XLSX.utils.sheet_to_csv' also
...
```

#### <a name="apidoc.element.xlsx.utils.sheet_to_json"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>sheet_to_json (sheet, opts)](#apidoc.element.xlsx.utils.sheet_to_json)
- description and source-code
```javascript
function sheet_to_json(sheet, opts){
	var val, row, range, header = 0, offset = 1, r, hdr = [], isempty, R, C, v, vv;
	var o = opts != null ? opts : {};
	var raw = o.raw;
	var defval = o.defval;
	if(sheet == null || sheet["!ref"] == null) return [];
	range = o.range != null ? o.range : sheet["!ref"];
	if(o.header === 1) header = 1;
	else if(o.header === "A") header = 2;
	else if(Array.isArray(o.header)) header = 3;
	switch(typeof range) {
		case 'string': r = safe_decode_range(range); break;
		case 'number': r = safe_decode_range(sheet["!ref"]); r.s.r = range; break;
		default: r = range;
	}
	if(header > 0) offset = 0;
	var rr = encode_row(r.s.r);
	var cols = new Array(r.e.c-r.s.c+1);
	var out = new Array(r.e.r-r.s.r-offset+1);
	var outi = 0;
	for(C = r.s.c; C <= r.e.c; ++C) {
		cols[C] = encode_col(C);
		val = sheet[cols[C] + rr];
		switch(header) {
			case 1: hdr[C] = C; break;
			case 2: hdr[C] = cols[C]; break;
			case 3: hdr[C] = o.header[C - r.s.c]; break;
			default:
				if(val == null) continue;
				vv = v = format_cell(val, null, o);
				var counter = 0;
				for(var CC = 0; CC < hdr.length; ++CC) if(hdr[CC] == vv) vv = v + "_" + (++counter);
				hdr[C] = vv;
		}
	}

	for (R = r.s.r + offset; R <= r.e.r; ++R) {
		rr = encode_row(R);
		isempty = true;
		if(header === 1) row = [];
		else {
			row = {};
			if(Object.defineProperty) try { Object.defineProperty(row, '__rowNum__', {value:R, enumerable:false}); } catch(e) { row.__rowNum__
 = R; }
			else row.__rowNum__ = R;
		}
		for (C = r.s.c; C <= r.e.c; ++C) {
			val = sheet[cols[C] + rr];
			if(val === undefined || val.t === undefined) {
				if(defval === undefined) continue;
				if(hdr[C] != null) { row[hdr[C]] = defval; isempty = false; }
				continue;
			}
			v = val.v;
			switch(val.t){
				case 'z': if(v == null) break; continue;
				case 'e': continue;
				case 's': case 'd': case 'b': case 'n': break;
				default: throw new Error('unrecognized type ' + val.t);
			}
			if(hdr[C] != null) {
				if(v == null) {
					if(defval !== undefined) row[hdr[C]] = defval;
					else if(raw && v === null) row[hdr[C]] = null;
					else continue;
				} else {
					row[hdr[C]] = raw ? v : format_cell(val,v,o);
				}
				isempty = false;
			}
		}
		if((isempty === false) || (header === 1 ? o.blankrows !== false : !!o.blankrows)) out[outi++] = row;
	}
	out.length = outi;
	return out;
}
```
- example usage
```shell
...

If header is not '1', the row object will contain the non-enumerable property
'__rowNum__' that represents the row of the sheet corresponding to the entry.

For the example sheet:

'''js
> console.log(X.utils.sheet_to_json(_ws));
[ { S: 1, h: 2, e: 3, e_1: 4, t: 5, J: 6, S_1: 7 },
{ S: 2, h: 3, e: 4, e_1: 5, t: 6, J: 7, S_1: 8 } ]

> console.log(X.utils.sheet_to_json(_ws, {header:1}));
[ [ 'S', 'h', 'e', 'e', 't', 'J', 'S' ],
[ 1, 2, 3, 4, 5, 6, 7 ],
[ 2, 3, 4, 5, 6, 7, 8 ] ]
...
```

#### <a name="apidoc.element.xlsx.utils.sheet_to_row_object_array"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>sheet_to_row_object_array (sheet, opts)](#apidoc.element.xlsx.utils.sheet_to_row_object_array)
- description and source-code
```javascript
function sheet_to_json(sheet, opts){
	var val, row, range, header = 0, offset = 1, r, hdr = [], isempty, R, C, v, vv;
	var o = opts != null ? opts : {};
	var raw = o.raw;
	var defval = o.defval;
	if(sheet == null || sheet["!ref"] == null) return [];
	range = o.range != null ? o.range : sheet["!ref"];
	if(o.header === 1) header = 1;
	else if(o.header === "A") header = 2;
	else if(Array.isArray(o.header)) header = 3;
	switch(typeof range) {
		case 'string': r = safe_decode_range(range); break;
		case 'number': r = safe_decode_range(sheet["!ref"]); r.s.r = range; break;
		default: r = range;
	}
	if(header > 0) offset = 0;
	var rr = encode_row(r.s.r);
	var cols = new Array(r.e.c-r.s.c+1);
	var out = new Array(r.e.r-r.s.r-offset+1);
	var outi = 0;
	for(C = r.s.c; C <= r.e.c; ++C) {
		cols[C] = encode_col(C);
		val = sheet[cols[C] + rr];
		switch(header) {
			case 1: hdr[C] = C; break;
			case 2: hdr[C] = cols[C]; break;
			case 3: hdr[C] = o.header[C - r.s.c]; break;
			default:
				if(val == null) continue;
				vv = v = format_cell(val, null, o);
				var counter = 0;
				for(var CC = 0; CC < hdr.length; ++CC) if(hdr[CC] == vv) vv = v + "_" + (++counter);
				hdr[C] = vv;
		}
	}

	for (R = r.s.r + offset; R <= r.e.r; ++R) {
		rr = encode_row(R);
		isempty = true;
		if(header === 1) row = [];
		else {
			row = {};
			if(Object.defineProperty) try { Object.defineProperty(row, '__rowNum__', {value:R, enumerable:false}); } catch(e) { row.__rowNum__
 = R; }
			else row.__rowNum__ = R;
		}
		for (C = r.s.c; C <= r.e.c; ++C) {
			val = sheet[cols[C] + rr];
			if(val === undefined || val.t === undefined) {
				if(defval === undefined) continue;
				if(hdr[C] != null) { row[hdr[C]] = defval; isempty = false; }
				continue;
			}
			v = val.v;
			switch(val.t){
				case 'z': if(v == null) break; continue;
				case 'e': continue;
				case 's': case 'd': case 'b': case 'n': break;
				default: throw new Error('unrecognized type ' + val.t);
			}
			if(hdr[C] != null) {
				if(v == null) {
					if(defval !== undefined) row[hdr[C]] = defval;
					else if(raw && v === null) row[hdr[C]] = null;
					else continue;
				} else {
					row[hdr[C]] = raw ? v : format_cell(val,v,o);
				}
				isempty = false;
			}
		}
		if((isempty === false) || (header === 1 ? o.blankrows !== false : !!o.blankrows)) out[outi++] = row;
	}
	out.length = outi;
	return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.split_cell"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>split_cell (cstr)](#apidoc.element.xlsx.utils.split_cell)
- description and source-code
```javascript
function split_cell(cstr) { return cstr.replace(/(\$?[A-Z]*)(\$?\d*)/,"$1,$2").split(","); }
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.xlsx.utils.table_to_book"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>table_to_book (table, opts)](#apidoc.element.xlsx.utils.table_to_book)
- description and source-code
```javascript
function table_to_book(table, opts) {
	return sheet_to_workbook(parse_dom_table(table, opts), opts);
}
```
- example usage
```shell
...
var workbook = XLSX.readFile('test.xlsx');
/* DO SOMETHING WITH workbook HERE */
'''

- Browser DOM Table element:

'''js
var worksheet = XLSX.utils.table_to_book(document.getElementById('tableau'));
/* DO SOMETHING WITH workbook HERE */
'''

- ajax (for a more complete example that works in older browsers, check the demo
  at <http://oss.sheetjs.com/js-xlsx/ajax.html>):

'''js
...
```

#### <a name="apidoc.element.xlsx.utils.table_to_sheet"></a>[function <span class="apidocSignatureSpan">xlsx.utils.</span>table_to_sheet (table, opts)](#apidoc.element.xlsx.utils.table_to_sheet)
- description and source-code
```javascript
function parse_dom_table(table, opts) {
	var ws = ({});
	var rows = table.getElementsByTagName('tr');
	var range = {s:{r:0,c:0},e:{r:rows.length - 1,c:0}};
	var merges = [], midx = 0;
	var R = 0, _C = 0, C = 0, RS = 0, CS = 0;
	for(; R < rows.length; ++R) {
		var row = rows[R];
		var elts = row.children;
		for(_C = C = 0; _C < elts.length; ++_C) {
			var elt = elts[_C], v = elts[_C].innerText;
			for(midx = 0; midx < merges.length; ++midx) {
				var m = merges[midx];
				if(m.s.c == C && m.s.r <= R && R <= m.e.r) { C = m.e.c+1; midx = -1; }
			}
			<span class="apidocCodeCommentSpan">/* TODO: figure out how to extract nonstandard mso- style */
</span>			CS = +elt.getAttribute("colspan") || 1;
			if((RS = +elt.getAttribute("rowspan"))>0) merges.push({s:{r:R,c:C},e:{r:R + RS - 1, c:C + CS - 1}});
			var o = {t:'s', v:v};
			if(v != null && v.length && !isNaN(Number(v))) o = {t:'n', v:Number(v)};
			ws[encode_cell({c:C, r:R})] = o;
			C += CS;
		}
	}
	ws['!merges'] = merges;
	ws['!ref'] = encode_range(range);
	return ws;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)
