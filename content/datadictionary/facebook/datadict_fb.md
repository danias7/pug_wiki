+++
title = "Facebook Data Fields"
description = ""
+++



{{% panel theme="success" header= "Description" %}}

Searchable data fields available in PULSE Kibana. These fields are indexed by using Facebook's Graph API.

Click here for more information: https://developers.facebook.com/docs/graph-api {{% /panel %}}


## Usage

|	Field  | Description |
|:--|:--|
| **`doc.context.display_name`** | Display name for the page or profile where the post, comment, or reaction resides|
| **`doc.graph_type`** | Type of content scraped from Facebook (entity, comment, post, or reaction)|
| **`doc.message`** | Text of a post or comment |
|**`doc.from.name `**| Author of a post, comment, or reaction (**doc.from.name** and **norm.author** are synonymous)|
| **'doc.from.id'** | User ID for a post.comment, or reaction|
| **'doc.cover.source'**| Backsplash image associated with the author of the post/comment/reaction|
| ```doc.picture.data.url```| Profile image associated with the author of the post/comment/reaction |
|```doc.about``` |“About” information for a Facebook page (will not exist for Facebook profiles)|
|```doc.reaction```|	If a reaction exists for a message, this field will identify what the reaction is (i.e., LIKE, LOVE, WOW, SAD, HAHA, ANGRY)|
| ```doc.parent```|ID for the original post (for posts, comments, and replies)|

*1 In some instances, inputting a field into the search bar along with a colon and a term may retrieve data specific to that query.

For instance, doc.graph_type: comment will retrieve Facebook comments.*

## Basic example

To find:

	{{%/* panel */%}}this is a panel text{{%/* /panel */%}}

{{%panel%}}this is a panel text{{%/panel%}}
