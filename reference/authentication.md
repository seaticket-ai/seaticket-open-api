---
title: Authentication
excerpt: The authentication flows of Seaticket.
category: 67b7f8e66714a0002932b041
isReference: true
slug: authentication
---

All API calls must be authenticated with a valid Seaticket API token and all requests require an authorization header that looks like this:

`Authorization: Bearer {{Account-Token, Project-Token}}`

In the Seaticket API, authentication can be done using Account-Token and Project-Token.

> For versions less than 11.0,  'Bearer' should be replaced with 'Token'. 
>
> `Authorization: Token {{Account-Token, Project-Token}}`

## The two tokens

#### Account-Token

An **Account-Token** is generated with your account name and password. Most APIs can be called with an account token.

#### Project-Token

A **Project-Token** is like a password to use the APIs of a single project. You can create as many Project-Token per project as you want. Every Project-Token can have read or write permissions. This token is valid until you delete them. If a user only needs to manipulate the contents of a specific project, it is more secure to use the project API token.

You can generate **Project-Token** for a project via the Web UI, in "Project context menu -> API Token".
