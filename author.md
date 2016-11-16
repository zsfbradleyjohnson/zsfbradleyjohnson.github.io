---
layout: page
title: 作者介绍
permalink: /author/
slug: author
---

    #import <Foundation/Foundation.h>
    #import <UIKit/UIKit.h>

    typedef NS_ENUM(NSInteger,SexType) {
          SexTypeUnknow = 0,
          SexTypeMale,
          SexTypeFemale,
          SexTypeNeutral,
      };

    @interface Developer : NSObject

    /**
    basic attributes
    */
    @property (nonatomic , strong) NSString  * name;
    @property (nonatomic , assign) NSInteger * age;
    @property (nonatomic , assign) SexType     sex;
    @property (nonatomic , strong) NSString  * college;

    /**
    contact attributes
    */
    @property (nonatomic , strong) NSString  * phoneNumber;
    @property (nonatomic , strong) NSString  * email;
    @property (nonatomic , strong) NSString  * qqNumber;

    /**
    work experience
    */
    @property (nonatomic , assign) CGFloat     workExperienceNumber;//(单位:年)
    @property (nonatomic , strong) NSArray   * pastCompany;
    @property (nonatomic , strong) NSArray   * pastProject;

    @end

以下，是我的赋值信息：

    #import "ViewController.h"
    #import "Developer.h"

    @implementation MainViewController

    - (void)viewDidLoad {
        [super viewDidLoad];

        Developer * developer = [Developer new];

        NSMutableDictionary * attributesArray = [NSMutableDictionary new];
        [attributesArray setValue:@"周深发" forKey:@"name"];
        [attributesArray setValue:@24 forKey:@"age"];
        [attributesArray setValue:@(SexTypeMale) forKey:@"sex"];
        [attributesArray setValue:@"广东海洋大学" forKey:@"college"];

        [attributesArray setValue:@"18476658843" forKey:@"phoneNumber"];
        [attributesArray setValue:@"zsfbradleyjohnson@126.com" forKey:@"email"];
        [attributesArray setValue:@"504533850" forKey:@"qqNumber"];

        [attributesArray setValue:@2.75 forKey:@"workExperienceNumber"];
        [attributesArray setValue:@[@"深圳全民尚网网络科技有限公司",@"深圳一云网络科技有限公司",@"湛江华星网络科技有限公司"] forKey:@"pastCompany"];
        [attributesArray setValue:@[@"wifi8",@"智慧家园",@"全民公寓",@"好笔头",@"折扣买"] forKey:@"pastProject"];

        [developer setValuesForKeysWithDictionary:attributesArray];
    }

    @end

