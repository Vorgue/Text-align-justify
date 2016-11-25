# Text-align-justify
    var justify = function(str, len) {
      var res = str.slice();
      var lines = Math.ceil(str.length/len);
      var k = 0;
      var l = 0;
      for (var i = 0; i < lines; i++) {
        while ((res[len*i + k - l] !== ' ') && (str.slice(0,len*i + k - l).indexOf(' ') !== -1)) l++;
        res = res.splice(len*i + k - l, 0, '\n');
        k++;
      }
      return res
    };

    String.prototype.splice = function(idx, rem, str) {
      return this.slice(0, idx) + str + this.slice(idx + Math.abs(rem))
    }

    var str = 'ABCDEFGHIJKLMNOPQRSTUWXYZ'
    var len = 3;
    var str2 = 'Hello world, welcome to the universe.'
    var str3 = 'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.'
    var len3 = 30;

    while ((res[len*i + k - l] !== ' ') && (str.slice(0,len*i + k - l).indexOf(' ') !== -1)) l++
