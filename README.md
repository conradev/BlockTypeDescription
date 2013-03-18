# BlockTypeDescription

BlockTypeDescription adds a block's type signature to its description.
It makes debugging more transparent, and turns an otherwise useless description into a useful one.

## Example Usage

``` objective-c
NSString * (^someBlock)(NSString *, BOOL, CGRect, float*[30]) = ^(NSString *a, BOOL b, CGRect c, float *d[30]) {
    return @"Some return value";
};
NSLog(@"This is my block! %@", someBlock);
```

### Before

```
This is my block! <__NSGlobalBlock__: 0x35c0>
```

### After

```
This is my block! <__NSGlobalBlock__: (id (^)(id, char, struct CGRect, float*[30]))>
```

## License

BlockTypeDescription is available under the MIT license. See the LICENSE file for more info.
