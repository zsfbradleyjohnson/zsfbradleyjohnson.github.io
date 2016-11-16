---
layout: page
title: Author
permalink: /author/
slug: author
---

  #import <Foundation/Foundation.h>

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
@property (nonatomic , assign) NSUInteger  workExperienceNumber;
@property (nonatomic , strong) NSArray   * pastCompany;
@property (nonatomic , strong) NSArray   * pastProject;

@end
`
