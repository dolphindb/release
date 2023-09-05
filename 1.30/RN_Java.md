# Release Notes for DolphinDB Java API

## New Features

- Added support for constructing data of BasicDecimal32 and BasicDecimal64 types from strings. (**1.30.22.3**)
- Added support for calling the `JSONObject.toJSONString` method from fastjson library to serialize DolphinDB data types defined in the Java API. (**1.30.22.3**)
- The `add` method of the `BasicDecimal32Vector` and `BasicDecimal64Vector` classes now supports data of String type. (**1.30.22.3**)
- The `addRange` method of the `BasicDecimal32Vector` and `BasicDecimal64Vector` classes now supports String arrays. (**1.30.22.3**)

## Improvements

- Reduced the JAR file size for DolphinDB Java API dependencies. (**1.30.22.3**)
- Renamed `tableAppneder` to `AutoFitTableAppender`.  (**1.30.22.3**)
- Optimized the `ErrorCodeInfo` code, and changed its access modifier to public. (**1.30.22.3**)

