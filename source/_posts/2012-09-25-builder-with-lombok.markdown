---
layout: post
title: "Builder With Lombok"
date: 2012-09-25 13:41:35 +0000
comments: true
published: true
categories: [Java, Testing, Unit testing]
keywords: "java testing, builder pattern, builder implementation, lombok"
description: "Describing a very clean and simple technique for incorportating the  builder pattern espcially for unit tests"
---

The Builder Pattern is well known as an alternative to the constructors with multiple arguments; it increases code readability and the fluent interface allows object creation without passing null in the constructor etc. In a recent project, I was creating the domain objects and wanted to generate the builders for these objects cleanly and automatically; the less code the better. There are several Eclipse plugins that can generate the boilerplate code but there is a very clean way to remove the need for these plugins.

<!-- more -->

[lombok-pg](https://github.com/peichhorn/lombok-pg) provides an alternative. This library extends [Project Lombok](http://projectlombok.org/) with even more funky stuff and one of those things is `@Builder`. The usage is best illustrated with a simple example.

``` java
package co.uk.agiletech.ecommerce.domain;

import java.util.List;

import lombok.Builder;
import lombok.Data;

@Data
@Builder
public class Customer {

    private String title;
    private String firstName;
    private String lastName;
    private List<Order> orders;

    public boolean hasOrders() {
        return orders != null && orders.isEmpty();
    }
}
```

The builder can then be used in the test cases with ease.

``` java
package co.uk.agiletech.ecommerce.domain;

import static co.uk.agiletech.ecommerce.domain.Customer.customer;
import static org.hamcrest.MatcherAssert.assertThat;
import static org.hamcrest.Matchers.is;

import org.junit.Test;

public class CustomerTest {

    private Customer customer;

    @Test
    public void returnsFalseWhenCustomerHasNoOrders() {
        customer = customer().title("Mr")
                             .firstName("John")
                             .lastName("Smith")
                             .build();
        assertThat(customer.hasOrders(), is(false));
    }
}
```

 


