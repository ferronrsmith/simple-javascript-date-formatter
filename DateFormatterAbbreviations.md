'yy'   - 11 (2 numeric year shortening)

'yyyy' - 2011 (Full Year)

'mmmm' - January (Full month )

'mmm'  - Jan (3 Letter month shortening )

'mm'   - Numeric month (Jan = 01)

'dddd' - Sunday - (Month word format)

'ddd'  - Sun (3 Letter day shortening )

'dd'   - Numeric day (19)

'hh':  - 11 (hour)

'nn':  - 59 (minutes)

'ss':  - 22 (seconds)

'a/p'  - 'am' or 'pm';

```

Date.prototype.format = function (f) {
    if (!this.valueOf())
        return ' ';

    var d = this;

    return f.replace(/(yy|yyyy|mmmm|mmm|mm|dddd|ddd|dd|hh|nn|ss|a\/p)/gi,
        function (val) {
            switch (val.toLowerCase()) {
                case 'yy': return d.getFullYear().substr(2);
                case 'yyyy': return d.getFullYear();
                case 'mmmm': return gsMonthNames[d.getMonth()];
                case 'mmm': return gsMonthNames[d.getMonth()].substr(0, 3);
                case 'mm': return (d.getMonth() + 1).zf(2);
                case 'dddd': return gsDayNames[d.getDay()];
                case 'ddd': return gsDayNames[d.getDay()].substr(0, 3);
                case 'dd': return d.getDate().zf(2);
                case 'hh': return ((h = d.getHours() % 12) ? h : 12).zf(2);
                case 'nn': return d.getMinutes().zf(2);
                case 'ss': return d.getSeconds().zf(2);
                case 'a/p': return d.getHours() < 12 ? 'am' : 'pm';
            }
        }
    );
}

```