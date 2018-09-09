# Bookmarklets
This are all the [bookmarklets](https://en.wikipedia.org/wiki/Bookmarklet) I created.

## [4chan Image Expander][1]
Expands all image in a 4chan thread to their bigger variant.

## [Archive][2]
Open the current URL in archive.org.

## [QR Code][3]
Open a QR Code corresponding to the current URL.

## [YouTube Full Size][4]
Open a YouTube Video with the full Browser Size.

## [YouTube Mix][5]
Opens a YouTube Mix corresponding to the currently playing Video, even if YouTube doesn't show you Mix as an option.

[1]: javascript:!function(){for(var%20e=document.getElementsByClassName(%22fileThumb%22),n=0;n%3Ce.length;n++)ImageExpansion.expand(e[n].getElementsByTagName(%22img%22)[0])}();

[2]: javascript:!function(){window.location=%22https://web.archive.org/web/%22+window.location.href.replace(/https%3F%253F:\/\//i,%22%22)}();

[3]: javascript:!function(){current_url=encodeURIComponent(window.location.href),api_url=%22https://api.qrserver.com/v1/create-qr-code/%253Fdata=%22,window.location=api_url+current_url}();

[4]: javascript:(function(){function%20queryVariable(variable){var%20query=window.location.search.substring(1);var%20vars=query.split(%22%26%22);for(var%20i=0;i%3Cvars.length;i++){var%20pair=vars[i].split(%22=%22);if(pair[0]==variable){return%20pair[1];}}return(false);}var%20o=queryVariable(%22v%22)window.location=%22https://www.youtube.com/embed/%22+o})();

[5]: javascript:(function(){function%20queryVariable(variable){var%20query=window.location.search.substring(1);var%20vars=query.split(%22%26%22);for(var%20i=0;i%3Cvars.length;i++){var%20pair=vars[i].split(%22=%22);if(pair[0]==variable){return%20pair[1];}}return(false);}var%20o=queryVariable(%22v%22)window.location=%22https://www.youtube.com/watch%253Fv=%22+o+%22%2526list=RD%22+o})();
