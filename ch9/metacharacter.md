# 元字符

匹配单个字符

——-

边界字符

^ $ \A


|元字符|说明|
|:—————|:——————|
|`.`   |匹配除换行外任意字符|
|`[]`  |字符集合，匹配方括号中任意一个字符|
|`[^]` |对字符集合取非 举例 [^0-9]|
|`\d`  |匹配数字字符|
|`\D`  |匹配非数字字符|
|`\w`  |匹配数字、字母、下划线|
|`\W`  |非匹配数字、字母、下划线|
|`\s`  |匹配任意空白符（换行、空格、回车、制表、换页）|
|`\S`  |匹配任意非空白符（换行、空格、回车、制表、换页）|
|`^`   |行首匹配|
|`$`   |行尾匹配|
|`\A`  ||
|`\Z`  ||
|`\b`  ||
|`\B`  ||
......


