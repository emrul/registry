
---
title: "getTopicSubscriptions"
title_tag: "alicloud.mns.getTopicSubscriptions"
meta_desc: "Documentation for the alicloud.mns.getTopicSubscriptions function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

This data source provides a list of MNS topic subscriptions in an Alibaba Cloud account according to the specified parameters.


{{% examples %}}

## Example Usage

{{< chooser language "typescript,python,go,csharp" / >}}





{{< example csharp >}}

```csharp
using Pulumi;
using AliCloud = Pulumi.AliCloud;

class MyStack : Stack
{
    public MyStack()
    {
        var subscriptions = Output.Create(AliCloud.Mns.GetTopicSubscriptions.InvokeAsync(new AliCloud.Mns.GetTopicSubscriptionsArgs
        {
            NamePrefix = "tf-",
            TopicName = "topic_name",
        }));
        this.FirstTopicSubscriptionId = subscriptions.Apply(subscriptions => subscriptions.Subscriptions[0].Id);
    }

    [Output("firstTopicSubscriptionId")]
    public Output<string> FirstTopicSubscriptionId { get; set; }
}
```


{{< /example >}}


{{< example go >}}

```go
package main

import (
	"github.com/pulumi/pulumi-alicloud/sdk/v3/go/alicloud/mns"
	"github.com/pulumi/pulumi/sdk/v3/go/pulumi"
)

func main() {
	pulumi.Run(func(ctx *pulumi.Context) error {
		opt0 := "tf-"
		subscriptions, err := mns.GetTopicSubscriptions(ctx, &mns.GetTopicSubscriptionsArgs{
			NamePrefix: &opt0,
			TopicName:  "topic_name",
		}, nil)
		if err != nil {
			return err
		}
		ctx.Export("firstTopicSubscriptionId", subscriptions.Subscriptions[0].Id)
		return nil
	})
}
```


{{< /example >}}


{{< example python >}}

```python
import pulumi
import pulumi_alicloud as alicloud

subscriptions = alicloud.mns.get_topic_subscriptions(name_prefix="tf-",
    topic_name="topic_name")
pulumi.export("firstTopicSubscriptionId", subscriptions.subscriptions[0].id)
```


{{< /example >}}


{{< example typescript >}}


```typescript
import * as pulumi from "@pulumi/pulumi";
import * as alicloud from "@pulumi/alicloud";

const subscriptions = pulumi.output(alicloud.mns.getTopicSubscriptions({
    namePrefix: "tf-",
    topicName: "topic_name",
}, { async: true }));

export const firstTopicSubscriptionId = subscriptions.subscriptions[0].id;
```


{{< /example >}}





{{% /examples %}}




## Using getTopicSubscriptions {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getTopicSubscriptions<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetTopicSubscriptionsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetTopicSubscriptionsResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_topic_subscriptions(</span><span class="nx">name_prefix</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                            <span class="nx">output_file</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                            <span class="nx">topic_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                            <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetTopicSubscriptionsResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>GetTopicSubscriptions<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">GetTopicSubscriptionsArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">GetTopicSubscriptionsResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `GetTopicSubscriptions` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetTopicSubscriptions </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetTopicSubscriptionsResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetTopicSubscriptionsArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="topicname_csharp">
<a href="#topicname_csharp" style="color: inherit; text-decoration: inherit;">Topic<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Two topics on a single account in the same region cannot have the same name. A topic name must start with an English letter or a digit, and can contain English letters, digits, and hyphens, with the length not exceeding 256 characters.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="nameprefix_csharp">
<a href="#nameprefix_csharp" style="color: inherit; text-decoration: inherit;">Name<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string to filter resulting subscriptions of the topic by their name prefixs.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="topicname_go">
<a href="#topicname_go" style="color: inherit; text-decoration: inherit;">Topic<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Two topics on a single account in the same region cannot have the same name. A topic name must start with an English letter or a digit, and can contain English letters, digits, and hyphens, with the length not exceeding 256 characters.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="nameprefix_go">
<a href="#nameprefix_go" style="color: inherit; text-decoration: inherit;">Name<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string to filter resulting subscriptions of the topic by their name prefixs.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="topicname_nodejs">
<a href="#topicname_nodejs" style="color: inherit; text-decoration: inherit;">topic<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Two topics on a single account in the same region cannot have the same name. A topic name must start with an English letter or a digit, and can contain English letters, digits, and hyphens, with the length not exceeding 256 characters.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="nameprefix_nodejs">
<a href="#nameprefix_nodejs" style="color: inherit; text-decoration: inherit;">name<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A string to filter resulting subscriptions of the topic by their name prefixs.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="topic_name_python">
<a href="#topic_name_python" style="color: inherit; text-decoration: inherit;">topic_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Two topics on a single account in the same region cannot have the same name. A topic name must start with an English letter or a digit, and can contain English letters, digits, and hyphens, with the length not exceeding 256 characters.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="name_prefix_python">
<a href="#name_prefix_python" style="color: inherit; text-decoration: inherit;">name_<wbr>prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A string to filter resulting subscriptions of the topic by their name prefixs.
{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getTopicSubscriptions Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="names_csharp">
<a href="#names_csharp" style="color: inherit; text-decoration: inherit;">Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}A list of subscription names.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subscriptions_csharp">
<a href="#subscriptions_csharp" style="color: inherit; text-decoration: inherit;">Subscriptions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#gettopicsubscriptionssubscription">List&lt;Pulumi.<wbr>Ali<wbr>Cloud.<wbr>Mns.<wbr>Outputs.<wbr>Get<wbr>Topic<wbr>Subscriptions<wbr>Subscription&gt;</a></span>
    </dt>
    <dd>{{% md %}}A list of subscriptions. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="topicname_csharp">
<a href="#topicname_csharp" style="color: inherit; text-decoration: inherit;">Topic<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nameprefix_csharp">
<a href="#nameprefix_csharp" style="color: inherit; text-decoration: inherit;">Name<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_csharp">
<a href="#outputfile_csharp" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="names_go">
<a href="#names_go" style="color: inherit; text-decoration: inherit;">Names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}A list of subscription names.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subscriptions_go">
<a href="#subscriptions_go" style="color: inherit; text-decoration: inherit;">Subscriptions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#gettopicsubscriptionssubscription">[]Get<wbr>Topic<wbr>Subscriptions<wbr>Subscription</a></span>
    </dt>
    <dd>{{% md %}}A list of subscriptions. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="topicname_go">
<a href="#topicname_go" style="color: inherit; text-decoration: inherit;">Topic<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nameprefix_go">
<a href="#nameprefix_go" style="color: inherit; text-decoration: inherit;">Name<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_go">
<a href="#outputfile_go" style="color: inherit; text-decoration: inherit;">Output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="names_nodejs">
<a href="#names_nodejs" style="color: inherit; text-decoration: inherit;">names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}A list of subscription names.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subscriptions_nodejs">
<a href="#subscriptions_nodejs" style="color: inherit; text-decoration: inherit;">subscriptions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#gettopicsubscriptionssubscription">Get<wbr>Topic<wbr>Subscriptions<wbr>Subscription[]</a></span>
    </dt>
    <dd>{{% md %}}A list of subscriptions. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="topicname_nodejs">
<a href="#topicname_nodejs" style="color: inherit; text-decoration: inherit;">topic<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="nameprefix_nodejs">
<a href="#nameprefix_nodejs" style="color: inherit; text-decoration: inherit;">name<wbr>Prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="outputfile_nodejs">
<a href="#outputfile_nodejs" style="color: inherit; text-decoration: inherit;">output<wbr>File</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The provider-assigned unique ID for this managed resource.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="names_python">
<a href="#names_python" style="color: inherit; text-decoration: inherit;">names</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}A list of subscription names.
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="subscriptions_python">
<a href="#subscriptions_python" style="color: inherit; text-decoration: inherit;">subscriptions</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#gettopicsubscriptionssubscription">Sequence[Get<wbr>Topic<wbr>Subscriptions<wbr>Subscription]</a></span>
    </dt>
    <dd>{{% md %}}A list of subscriptions. Each element contains the following attributes:
{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="topic_name_python">
<a href="#topic_name_python" style="color: inherit; text-decoration: inherit;">topic_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_prefix_python">
<a href="#name_prefix_python" style="color: inherit; text-decoration: inherit;">name_<wbr>prefix</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="output_file_python">
<a href="#output_file_python" style="color: inherit; text-decoration: inherit;">output_<wbr>file</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="gettopicsubscriptionssubscription">Get<wbr>Topic<wbr>Subscriptions<wbr>Subscription</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="endpoint_csharp">
<a href="#endpoint_csharp" style="color: inherit; text-decoration: inherit;">Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Describe the terminal address of the message received in this subscription.
* `filter_tag`- A string to filter resulting messages of the topic by their message tag.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="filtertag_csharp">
<a href="#filtertag_csharp" style="color: inherit; text-decoration: inherit;">Filter<wbr>Tag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the topic subscription. The value is set to `name`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the subscription.
* `topic_name`- The topic which The subscription belongs to was named with the name.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notifycontentformat_csharp">
<a href="#notifycontentformat_csharp" style="color: inherit; text-decoration: inherit;">Notify<wbr>Content<wbr>Format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The NotifyContentFormat attribute of Subscription. This attribute specifies the content format of the messages pushed to users.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notifystrategy_csharp">
<a href="#notifystrategy_csharp" style="color: inherit; text-decoration: inherit;">Notify<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The NotifyStrategy attribute of Subscription. This attribute specifies the retry strategy when message sending fails.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="topicname_csharp">
<a href="#topicname_csharp" style="color: inherit; text-decoration: inherit;">Topic<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Two topics on a single account in the same region cannot have the same name. A topic name must start with an English letter or a digit, and can contain English letters, digits, and hyphens, with the length not exceeding 256 characters.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="endpoint_go">
<a href="#endpoint_go" style="color: inherit; text-decoration: inherit;">Endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Describe the terminal address of the message received in this subscription.
* `filter_tag`- A string to filter resulting messages of the topic by their message tag.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="filtertag_go">
<a href="#filtertag_go" style="color: inherit; text-decoration: inherit;">Filter<wbr>Tag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the topic subscription. The value is set to `name`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the subscription.
* `topic_name`- The topic which The subscription belongs to was named with the name.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notifycontentformat_go">
<a href="#notifycontentformat_go" style="color: inherit; text-decoration: inherit;">Notify<wbr>Content<wbr>Format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The NotifyContentFormat attribute of Subscription. This attribute specifies the content format of the messages pushed to users.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notifystrategy_go">
<a href="#notifystrategy_go" style="color: inherit; text-decoration: inherit;">Notify<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The NotifyStrategy attribute of Subscription. This attribute specifies the retry strategy when message sending fails.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="topicname_go">
<a href="#topicname_go" style="color: inherit; text-decoration: inherit;">Topic<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Two topics on a single account in the same region cannot have the same name. A topic name must start with an English letter or a digit, and can contain English letters, digits, and hyphens, with the length not exceeding 256 characters.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="endpoint_nodejs">
<a href="#endpoint_nodejs" style="color: inherit; text-decoration: inherit;">endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Describe the terminal address of the message received in this subscription.
* `filter_tag`- A string to filter resulting messages of the topic by their message tag.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="filtertag_nodejs">
<a href="#filtertag_nodejs" style="color: inherit; text-decoration: inherit;">filter<wbr>Tag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The ID of the topic subscription. The value is set to `name`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the subscription.
* `topic_name`- The topic which The subscription belongs to was named with the name.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notifycontentformat_nodejs">
<a href="#notifycontentformat_nodejs" style="color: inherit; text-decoration: inherit;">notify<wbr>Content<wbr>Format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The NotifyContentFormat attribute of Subscription. This attribute specifies the content format of the messages pushed to users.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notifystrategy_nodejs">
<a href="#notifystrategy_nodejs" style="color: inherit; text-decoration: inherit;">notify<wbr>Strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The NotifyStrategy attribute of Subscription. This attribute specifies the retry strategy when message sending fails.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="topicname_nodejs">
<a href="#topicname_nodejs" style="color: inherit; text-decoration: inherit;">topic<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Two topics on a single account in the same region cannot have the same name. A topic name must start with an English letter or a digit, and can contain English letters, digits, and hyphens, with the length not exceeding 256 characters.
{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="endpoint_python">
<a href="#endpoint_python" style="color: inherit; text-decoration: inherit;">endpoint</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Describe the terminal address of the message received in this subscription.
* `filter_tag`- A string to filter resulting messages of the topic by their message tag.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="filter_tag_python">
<a href="#filter_tag_python" style="color: inherit; text-decoration: inherit;">filter_<wbr>tag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The ID of the topic subscription. The value is set to `name`.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the subscription.
* `topic_name`- The topic which The subscription belongs to was named with the name.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notify_content_format_python">
<a href="#notify_content_format_python" style="color: inherit; text-decoration: inherit;">notify_<wbr>content_<wbr>format</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The NotifyContentFormat attribute of Subscription. This attribute specifies the content format of the messages pushed to users.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="notify_strategy_python">
<a href="#notify_strategy_python" style="color: inherit; text-decoration: inherit;">notify_<wbr>strategy</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The NotifyStrategy attribute of Subscription. This attribute specifies the retry strategy when message sending fails.
{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="topic_name_python">
<a href="#topic_name_python" style="color: inherit; text-decoration: inherit;">topic_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Two topics on a single account in the same region cannot have the same name. A topic name must start with an English letter or a digit, and can contain English letters, digits, and hyphens, with the length not exceeding 256 characters.
{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-alicloud">https://github.com/pulumi/pulumi-alicloud</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
	<dt>Notes</dt>
	<dd>{{% md %}}This Pulumi package is based on the [`alicloud` Terraform Provider](https://github.com/aliyun/terraform-provider-alicloud).{{% /md %}}</dd>
</dl>
