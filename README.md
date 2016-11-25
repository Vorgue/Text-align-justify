# Text-align-justify
    str = "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum."

    var justify = function(str, len) {
        res = str.split(' ');
        var arr = new Array('');
        arr[0] 
        var j = 0;
        for (var i = 0; i < res.length - 1; i++) {
            res[i] = res[i] + ' ';
        }
        for (var i = 0; i < res.length; i++) {
            if (arr[j].length + res[i].length > len) {
                j++;
                arr.push('')
            }
            else if (res[i].length > len) {return "Justify length is too small"}
            arr[j] = arr[j] + res[i]
        }
        for (var i = 0; i < arr.length - 1; i++) {
            arr[i] = arr[i].addSpaces(len);
        }
        //arr = arr.map(x => x.addSpaces(len));
        return arr.join('\n')
    };

    String.prototype.addSpaces = function (len) {
        var add_count = len - this.length + 1;
        var res = this.split(' ');
        if (res.length == 1) return res;
        for (var i = 0; i < res.length - 2; i++) {
            res[i] = res[i] + ' '
        }
        var j = 0;
        for (var i = 0; i < add_count; i++) {
            if (j == res.length - 2) j = 0;
            res[j] = res[j] + ' ';
            j++
        }
        return res.join('')
    }
