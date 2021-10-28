
---
title: "getScheduledAlertRule"
title_tag: "azure-native.securityinsights.getScheduledAlertRule"
meta_desc: "Documentation for the azure-native.securityinsights.getScheduledAlertRule function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Represents scheduled alert rule.
API Version: 2020-01-01.




## Using getScheduledAlertRule {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getScheduledAlertRule<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetScheduledAlertRuleArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetScheduledAlertRuleResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_scheduled_alert_rule(</span><span class="nx">resource_group_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                             <span class="nx">rule_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                             <span class="nx">workspace_name</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                             <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetScheduledAlertRuleResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupScheduledAlertRule<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupScheduledAlertRuleArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupScheduledAlertRuleResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupScheduledAlertRule` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetScheduledAlertRule </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetScheduledAlertRuleResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetScheduledAlertRuleArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_csharp">
<a href="#resourcegroupname_csharp" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="ruleid_csharp">
<a href="#ruleid_csharp" style="color: inherit; text-decoration: inherit;">Rule<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Alert rule ID{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspacename_csharp">
<a href="#workspacename_csharp" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the workspace.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_go">
<a href="#resourcegroupname_go" style="color: inherit; text-decoration: inherit;">Resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="ruleid_go">
<a href="#ruleid_go" style="color: inherit; text-decoration: inherit;">Rule<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Alert rule ID{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspacename_go">
<a href="#workspacename_go" style="color: inherit; text-decoration: inherit;">Workspace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the workspace.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="resourcegroupname_nodejs">
<a href="#resourcegroupname_nodejs" style="color: inherit; text-decoration: inherit;">resource<wbr>Group<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="ruleid_nodejs">
<a href="#ruleid_nodejs" style="color: inherit; text-decoration: inherit;">rule<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Alert rule ID{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspacename_nodejs">
<a href="#workspacename_nodejs" style="color: inherit; text-decoration: inherit;">workspace<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the workspace.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="resource_group_name_python">
<a href="#resource_group_name_python" style="color: inherit; text-decoration: inherit;">resource_<wbr>group_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the resource group within the user's subscription. The name is case insensitive.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="rule_id_python">
<a href="#rule_id_python" style="color: inherit; text-decoration: inherit;">rule_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Alert rule ID{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="workspace_name_python">
<a href="#workspace_name_python" style="color: inherit; text-decoration: inherit;">workspace_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the workspace.{{% /md %}}</dd></dl>
{{% /choosable %}}




## getScheduledAlertRule Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="displayname_csharp">
<a href="#displayname_csharp" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name for alerts created by this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabled_csharp">
<a href="#enabled_csharp" style="color: inherit; text-decoration: inherit;">Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether this alert rule is enabled or disabled.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_csharp">
<a href="#id_csharp" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lastmodifiedutc_csharp">
<a href="#lastmodifiedutc_csharp" style="color: inherit; text-decoration: inherit;">Last<wbr>Modified<wbr>Utc</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The last time that this alert rule has been modified.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="query_csharp">
<a href="#query_csharp" style="color: inherit; text-decoration: inherit;">Query</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The query that creates alerts for this rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="queryfrequency_csharp">
<a href="#queryfrequency_csharp" style="color: inherit; text-decoration: inherit;">Query<wbr>Frequency</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The frequency (in ISO 8601 duration format) for this alert rule to run.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="queryperiod_csharp">
<a href="#queryperiod_csharp" style="color: inherit; text-decoration: inherit;">Query<wbr>Period</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The period (in ISO 8601 duration format) that this alert rule looks at.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="severity_csharp">
<a href="#severity_csharp" style="color: inherit; text-decoration: inherit;">Severity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The severity for alerts created by this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="suppressionduration_csharp">
<a href="#suppressionduration_csharp" style="color: inherit; text-decoration: inherit;">Suppression<wbr>Duration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The suppression (in ISO 8601 duration format) to wait since last time this alert rule been triggered.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="suppressionenabled_csharp">
<a href="#suppressionenabled_csharp" style="color: inherit; text-decoration: inherit;">Suppression<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether the suppression for this alert rule is enabled or disabled.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="triggeroperator_csharp">
<a href="#triggeroperator_csharp" style="color: inherit; text-decoration: inherit;">Trigger<wbr>Operator</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The operation against the threshold that triggers alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="triggerthreshold_csharp">
<a href="#triggerthreshold_csharp" style="color: inherit; text-decoration: inherit;">Trigger<wbr>Threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The threshold triggers this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="alertruletemplatename_csharp">
<a href="#alertruletemplatename_csharp" style="color: inherit; text-decoration: inherit;">Alert<wbr>Rule<wbr>Template<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Name of the alert rule template used to create this rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="etag_csharp">
<a href="#etag_csharp" style="color: inherit; text-decoration: inherit;">Etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Etag of the azure resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tactics_csharp">
<a href="#tactics_csharp" style="color: inherit; text-decoration: inherit;">Tactics</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">List&lt;string&gt;</span>
    </dt>
    <dd>{{% md %}}The tactics of the alert rule{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="displayname_go">
<a href="#displayname_go" style="color: inherit; text-decoration: inherit;">Display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name for alerts created by this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabled_go">
<a href="#enabled_go" style="color: inherit; text-decoration: inherit;">Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether this alert rule is enabled or disabled.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_go">
<a href="#id_go" style="color: inherit; text-decoration: inherit;">Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lastmodifiedutc_go">
<a href="#lastmodifiedutc_go" style="color: inherit; text-decoration: inherit;">Last<wbr>Modified<wbr>Utc</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The last time that this alert rule has been modified.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="query_go">
<a href="#query_go" style="color: inherit; text-decoration: inherit;">Query</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The query that creates alerts for this rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="queryfrequency_go">
<a href="#queryfrequency_go" style="color: inherit; text-decoration: inherit;">Query<wbr>Frequency</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The frequency (in ISO 8601 duration format) for this alert rule to run.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="queryperiod_go">
<a href="#queryperiod_go" style="color: inherit; text-decoration: inherit;">Query<wbr>Period</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The period (in ISO 8601 duration format) that this alert rule looks at.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="severity_go">
<a href="#severity_go" style="color: inherit; text-decoration: inherit;">Severity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The severity for alerts created by this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="suppressionduration_go">
<a href="#suppressionduration_go" style="color: inherit; text-decoration: inherit;">Suppression<wbr>Duration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The suppression (in ISO 8601 duration format) to wait since last time this alert rule been triggered.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="suppressionenabled_go">
<a href="#suppressionenabled_go" style="color: inherit; text-decoration: inherit;">Suppression<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether the suppression for this alert rule is enabled or disabled.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="triggeroperator_go">
<a href="#triggeroperator_go" style="color: inherit; text-decoration: inherit;">Trigger<wbr>Operator</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The operation against the threshold that triggers alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="triggerthreshold_go">
<a href="#triggerthreshold_go" style="color: inherit; text-decoration: inherit;">Trigger<wbr>Threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The threshold triggers this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="alertruletemplatename_go">
<a href="#alertruletemplatename_go" style="color: inherit; text-decoration: inherit;">Alert<wbr>Rule<wbr>Template<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Name of the alert rule template used to create this rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="etag_go">
<a href="#etag_go" style="color: inherit; text-decoration: inherit;">Etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Etag of the azure resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tactics_go">
<a href="#tactics_go" style="color: inherit; text-decoration: inherit;">Tactics</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">[]string</span>
    </dt>
    <dd>{{% md %}}The tactics of the alert rule{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="displayname_nodejs">
<a href="#displayname_nodejs" style="color: inherit; text-decoration: inherit;">display<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The display name for alerts created by this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabled_nodejs">
<a href="#enabled_nodejs" style="color: inherit; text-decoration: inherit;">enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Determines whether this alert rule is enabled or disabled.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_nodejs">
<a href="#id_nodejs" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="lastmodifiedutc_nodejs">
<a href="#lastmodifiedutc_nodejs" style="color: inherit; text-decoration: inherit;">last<wbr>Modified<wbr>Utc</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The last time that this alert rule has been modified.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="query_nodejs">
<a href="#query_nodejs" style="color: inherit; text-decoration: inherit;">query</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The query that creates alerts for this rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="queryfrequency_nodejs">
<a href="#queryfrequency_nodejs" style="color: inherit; text-decoration: inherit;">query<wbr>Frequency</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The frequency (in ISO 8601 duration format) for this alert rule to run.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="queryperiod_nodejs">
<a href="#queryperiod_nodejs" style="color: inherit; text-decoration: inherit;">query<wbr>Period</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The period (in ISO 8601 duration format) that this alert rule looks at.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="severity_nodejs">
<a href="#severity_nodejs" style="color: inherit; text-decoration: inherit;">severity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The severity for alerts created by this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="suppressionduration_nodejs">
<a href="#suppressionduration_nodejs" style="color: inherit; text-decoration: inherit;">suppression<wbr>Duration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The suppression (in ISO 8601 duration format) to wait since last time this alert rule been triggered.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="suppressionenabled_nodejs">
<a href="#suppressionenabled_nodejs" style="color: inherit; text-decoration: inherit;">suppression<wbr>Enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">boolean</span>
    </dt>
    <dd>{{% md %}}Determines whether the suppression for this alert rule is enabled or disabled.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="triggeroperator_nodejs">
<a href="#triggeroperator_nodejs" style="color: inherit; text-decoration: inherit;">trigger<wbr>Operator</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The operation against the threshold that triggers alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="triggerthreshold_nodejs">
<a href="#triggerthreshold_nodejs" style="color: inherit; text-decoration: inherit;">trigger<wbr>Threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">number</span>
    </dt>
    <dd>{{% md %}}The threshold triggers this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Azure resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="alertruletemplatename_nodejs">
<a href="#alertruletemplatename_nodejs" style="color: inherit; text-decoration: inherit;">alert<wbr>Rule<wbr>Template<wbr>Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The Name of the alert rule template used to create this rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="etag_nodejs">
<a href="#etag_nodejs" style="color: inherit; text-decoration: inherit;">etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Etag of the azure resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tactics_nodejs">
<a href="#tactics_nodejs" style="color: inherit; text-decoration: inherit;">tactics</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string[]</span>
    </dt>
    <dd>{{% md %}}The tactics of the alert rule{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="display_name_python">
<a href="#display_name_python" style="color: inherit; text-decoration: inherit;">display_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The display name for alerts created by this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="enabled_python">
<a href="#enabled_python" style="color: inherit; text-decoration: inherit;">enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether this alert rule is enabled or disabled.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="id_python">
<a href="#id_python" style="color: inherit; text-decoration: inherit;">id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure resource Id{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="last_modified_utc_python">
<a href="#last_modified_utc_python" style="color: inherit; text-decoration: inherit;">last_<wbr>modified_<wbr>utc</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The last time that this alert rule has been modified.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure resource name{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="query_python">
<a href="#query_python" style="color: inherit; text-decoration: inherit;">query</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The query that creates alerts for this rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="query_frequency_python">
<a href="#query_frequency_python" style="color: inherit; text-decoration: inherit;">query_<wbr>frequency</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The frequency (in ISO 8601 duration format) for this alert rule to run.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="query_period_python">
<a href="#query_period_python" style="color: inherit; text-decoration: inherit;">query_<wbr>period</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The period (in ISO 8601 duration format) that this alert rule looks at.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="severity_python">
<a href="#severity_python" style="color: inherit; text-decoration: inherit;">severity</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The severity for alerts created by this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="suppression_duration_python">
<a href="#suppression_duration_python" style="color: inherit; text-decoration: inherit;">suppression_<wbr>duration</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The suppression (in ISO 8601 duration format) to wait since last time this alert rule been triggered.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="suppression_enabled_python">
<a href="#suppression_enabled_python" style="color: inherit; text-decoration: inherit;">suppression_<wbr>enabled</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">bool</span>
    </dt>
    <dd>{{% md %}}Determines whether the suppression for this alert rule is enabled or disabled.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="trigger_operator_python">
<a href="#trigger_operator_python" style="color: inherit; text-decoration: inherit;">trigger_<wbr>operator</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The operation against the threshold that triggers alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="trigger_threshold_python">
<a href="#trigger_threshold_python" style="color: inherit; text-decoration: inherit;">trigger_<wbr>threshold</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">int</span>
    </dt>
    <dd>{{% md %}}The threshold triggers this alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Azure resource type{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="alert_rule_template_name_python">
<a href="#alert_rule_template_name_python" style="color: inherit; text-decoration: inherit;">alert_<wbr>rule_<wbr>template_<wbr>name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The Name of the alert rule template used to create this rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the alert rule.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="etag_python">
<a href="#etag_python" style="color: inherit; text-decoration: inherit;">etag</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Etag of the azure resource{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="tactics_python">
<a href="#tactics_python" style="color: inherit; text-decoration: inherit;">tactics</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">Sequence[str]</span>
    </dt>
    <dd>{{% md %}}The tactics of the alert rule{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-azure-native">https://github.com/pulumi/pulumi-azure-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
