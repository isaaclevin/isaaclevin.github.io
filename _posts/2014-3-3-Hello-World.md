---
layout: post
title: You're up and running!
---

Next you can update your site name, avatar and other options using the _config.yml file in the root of your repository (shown below).

![_config.yml]({{ site.baseurl }}/images/config.png)

The easiest way to make your first post is to edit this one. Go into /_posts/ and update the Hello World markdown file. For more instructions head over to the [Jekyll Now repository](https://github.com/barryclark/jekyll-now) on GitHub.

``` java
package com.jpragma.jtest;

import org.mockito.Mockito;
import org.mockito.stubbing.Answer;

import java.util.Arrays;

public class MockitoExtensions {
    private static Answer<?> alwaysThrowingAnswer = (invocation –> {
        throw new IllegalArgumentException("Unexpected call to " + invocation.getMethod() +
                " with " + Arrays.toString(invocation.getArguments()));
    });

    public static <T> T strictMock(Class<T> clazz) {
        return Mockito.mock(clazz, alwaysThrowingAnswer);
    }
}
```
