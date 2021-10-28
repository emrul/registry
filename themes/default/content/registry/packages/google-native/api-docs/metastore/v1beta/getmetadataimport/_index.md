
---
title: "getMetadataImport"
title_tag: "google-native.metastore/v1beta.getMetadataImport"
meta_desc: "Documentation for the google-native.metastore/v1beta.getMetadataImport function with examples, input properties, output properties, and supporting types."
layout: api
no_edit_this_page: true
---



<!-- WARNING: this file was generated by Pulumi Docs Generator. -->
<!-- Do not edit by hand unless you're certain you know what you are doing! -->

Gets details of a single import.




## Using getMetadataImport {#using}

{{< chooser language "typescript,python,go,csharp" / >}}


{{% choosable language nodejs %}}
<div class="highlight"><pre class="chroma"><code class="language-typescript" data-lang="typescript"><span class="k">function </span>getMetadataImport<span class="p">(</span><span class="nx">args</span><span class="p">:</span> <span class="nx">GetMetadataImportArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p">?:</span> <span class="nx"><a href="/docs/reference/pkg/nodejs/pulumi/pulumi/#InvokeOptions">InvokeOptions</a></span><span class="p">): Promise&lt;<span class="nx"><a href="#result">GetMetadataImportResult</a></span>></span></code></pre></div>
{{% /choosable %}}


{{% choosable language python %}}
<div class="highlight"><pre class="chroma"><code class="language-python" data-lang="python"><span class="k">def </span>get_metadata_import(</span><span class="nx">location</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">metadata_import_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">project</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">service_id</span><span class="p">:</span> <span class="nx">Optional[str]</span> = None<span class="p">,</span>
                        <span class="nx">opts</span><span class="p">:</span> <span class="nx"><a href="/docs/reference/pkg/python/pulumi/#pulumi.InvokeOptions">Optional[InvokeOptions]</a></span> = None<span class="p">) -&gt;</span> GetMetadataImportResult</code></pre></div>
{{% /choosable %}}


{{% choosable language go %}}
<div class="highlight"><pre class="chroma"><code class="language-go" data-lang="go"><span class="k">func </span>LookupMetadataImport<span class="p">(</span><span class="nx">ctx</span><span class="p"> *</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#Context">Context</a></span><span class="p">,</span> <span class="nx">args</span><span class="p"> *</span><span class="nx">LookupMetadataImportArgs</span><span class="p">,</span> <span class="nx">opts</span><span class="p"> ...</span><span class="nx"><a href="https://pkg.go.dev/github.com/pulumi/pulumi/sdk/v3/go/pulumi?tab=doc#InvokeOption">InvokeOption</a></span><span class="p">) (*<span class="nx"><a href="#result">LookupMetadataImportResult</a></span>, error)</span></code></pre></div>

> Note: This function is named `LookupMetadataImport` in the Go SDK.

{{% /choosable %}}


{{% choosable language csharp %}}
<div class="highlight"><pre class="chroma"><code class="language-csharp" data-lang="csharp"><span class="k">public static class </span><span class="nx">GetMetadataImport </span><span class="p">{</span><span class="k">
    public static </span>Task&lt;<span class="nx"><a href="#result">GetMetadataImportResult</a></span>> <span class="p">InvokeAsync(</span><span class="nx">GetMetadataImportArgs</span><span class="p"> </span><span class="nx">args<span class="p">,</span> <span class="nx"><a href="/docs/reference/pkg/dotnet/Pulumi/Pulumi.InvokeOptions.html">InvokeOptions</a></span><span class="p">? </span><span class="nx">opts = null<span class="p">)</span><span class="p">
}</span></code></pre></div>
{{% /choosable %}}



The following arguments are supported:


{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="location_csharp">
<a href="#location_csharp" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="metadataimportid_csharp">
<a href="#metadataimportid_csharp" style="color: inherit; text-decoration: inherit;">Metadata<wbr>Import<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="serviceid_csharp">
<a href="#serviceid_csharp" style="color: inherit; text-decoration: inherit;">Service<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_csharp">
<a href="#project_csharp" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="location_go">
<a href="#location_go" style="color: inherit; text-decoration: inherit;">Location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="metadataimportid_go">
<a href="#metadataimportid_go" style="color: inherit; text-decoration: inherit;">Metadata<wbr>Import<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="serviceid_go">
<a href="#serviceid_go" style="color: inherit; text-decoration: inherit;">Service<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_go">
<a href="#project_go" style="color: inherit; text-decoration: inherit;">Project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="location_nodejs">
<a href="#location_nodejs" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="metadataimportid_nodejs">
<a href="#metadataimportid_nodejs" style="color: inherit; text-decoration: inherit;">metadata<wbr>Import<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="serviceid_nodejs">
<a href="#serviceid_nodejs" style="color: inherit; text-decoration: inherit;">service<wbr>Id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_nodejs">
<a href="#project_nodejs" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="location_python">
<a href="#location_python" style="color: inherit; text-decoration: inherit;">location</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="metadata_import_id_python">
<a href="#metadata_import_id_python" style="color: inherit; text-decoration: inherit;">metadata_<wbr>import_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="service_id_python">
<a href="#service_id_python" style="color: inherit; text-decoration: inherit;">service_<wbr>id</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd><dt class="property-optional"
            title="Optional">
        <span id="project_python">
<a href="#project_python" style="color: inherit; text-decoration: inherit;">project</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}{{% /md %}}</dd></dl>
{{% /choosable %}}




## getMetadataImport Result {#result}

The following output properties are available:



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createtime_csharp">
<a href="#createtime_csharp" style="color: inherit; text-decoration: inherit;">Create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import was started.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="databasedump_csharp">
<a href="#databasedump_csharp" style="color: inherit; text-decoration: inherit;">Database<wbr>Dump</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#databasedumpresponse">Pulumi.<wbr>Google<wbr>Native.<wbr>Metastore.<wbr>V1Beta.<wbr>Outputs.<wbr>Database<wbr>Dump<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Immutable. A database dump from a pre-existing metastore's database.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_csharp">
<a href="#description_csharp" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the metadata import.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="endtime_csharp">
<a href="#endtime_csharp" style="color: inherit; text-decoration: inherit;">End<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import finished.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_csharp">
<a href="#name_csharp" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The relative resource name of the metadata import, of the form:projects/{project_number}/locations/{location_id}/services/{service_id}/metadataImports/{metadata_import_id}.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_csharp">
<a href="#state_csharp" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The current state of the metadata import.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatetime_csharp">
<a href="#updatetime_csharp" style="color: inherit; text-decoration: inherit;">Update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import was last updated.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createtime_go">
<a href="#createtime_go" style="color: inherit; text-decoration: inherit;">Create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import was started.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="databasedump_go">
<a href="#databasedump_go" style="color: inherit; text-decoration: inherit;">Database<wbr>Dump</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#databasedumpresponse">Database<wbr>Dump<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Immutable. A database dump from a pre-existing metastore's database.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_go">
<a href="#description_go" style="color: inherit; text-decoration: inherit;">Description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the metadata import.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="endtime_go">
<a href="#endtime_go" style="color: inherit; text-decoration: inherit;">End<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import finished.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_go">
<a href="#name_go" style="color: inherit; text-decoration: inherit;">Name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The relative resource name of the metadata import, of the form:projects/{project_number}/locations/{location_id}/services/{service_id}/metadataImports/{metadata_import_id}.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_go">
<a href="#state_go" style="color: inherit; text-decoration: inherit;">State</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The current state of the metadata import.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatetime_go">
<a href="#updatetime_go" style="color: inherit; text-decoration: inherit;">Update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import was last updated.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="createtime_nodejs">
<a href="#createtime_nodejs" style="color: inherit; text-decoration: inherit;">create<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import was started.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="databasedump_nodejs">
<a href="#databasedump_nodejs" style="color: inherit; text-decoration: inherit;">database<wbr>Dump</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#databasedumpresponse">Database<wbr>Dump<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Immutable. A database dump from a pre-existing metastore's database.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_nodejs">
<a href="#description_nodejs" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The description of the metadata import.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="endtime_nodejs">
<a href="#endtime_nodejs" style="color: inherit; text-decoration: inherit;">end<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import finished.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_nodejs">
<a href="#name_nodejs" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Immutable. The relative resource name of the metadata import, of the form:projects/{project_number}/locations/{location_id}/services/{service_id}/metadataImports/{metadata_import_id}.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_nodejs">
<a href="#state_nodejs" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The current state of the metadata import.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="updatetime_nodejs">
<a href="#updatetime_nodejs" style="color: inherit; text-decoration: inherit;">update<wbr>Time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import was last updated.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-"
            title="">
        <span id="create_time_python">
<a href="#create_time_python" style="color: inherit; text-decoration: inherit;">create_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import was started.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="database_dump_python">
<a href="#database_dump_python" style="color: inherit; text-decoration: inherit;">database_<wbr>dump</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type"><a href="#databasedumpresponse">Database<wbr>Dump<wbr>Response</a></span>
    </dt>
    <dd>{{% md %}}Immutable. A database dump from a pre-existing metastore's database.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="description_python">
<a href="#description_python" style="color: inherit; text-decoration: inherit;">description</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The description of the metadata import.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="end_time_python">
<a href="#end_time_python" style="color: inherit; text-decoration: inherit;">end_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import finished.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="name_python">
<a href="#name_python" style="color: inherit; text-decoration: inherit;">name</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Immutable. The relative resource name of the metadata import, of the form:projects/{project_number}/locations/{location_id}/services/{service_id}/metadataImports/{metadata_import_id}.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="state_python">
<a href="#state_python" style="color: inherit; text-decoration: inherit;">state</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The current state of the metadata import.{{% /md %}}</dd><dt class="property-"
            title="">
        <span id="update_time_python">
<a href="#update_time_python" style="color: inherit; text-decoration: inherit;">update_<wbr>time</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The time when the metadata import was last updated.{{% /md %}}</dd></dl>
{{% /choosable %}}




## Supporting Types


<h4 id="databasedumpresponse">Database<wbr>Dump<wbr>Response</h4>



{{% choosable language csharp %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="databasetype_csharp">
<a href="#databasetype_csharp" style="color: inherit; text-decoration: inherit;">Database<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="gcsuri_csharp">
<a href="#gcsuri_csharp" style="color: inherit; text-decoration: inherit;">Gcs<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A Cloud Storage object or folder URI that specifies the source from which to import metadata. It must begin with gs://.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sourcedatabase_csharp">
<a href="#sourcedatabase_csharp" style="color: inherit; text-decoration: inherit;">Source<wbr>Database</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the source database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="type_csharp">
<a href="#type_csharp" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. The type of the database dump. If unspecified, defaults to MYSQL.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language go %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="databasetype_go">
<a href="#databasetype_go" style="color: inherit; text-decoration: inherit;">Database<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="gcsuri_go">
<a href="#gcsuri_go" style="color: inherit; text-decoration: inherit;">Gcs<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A Cloud Storage object or folder URI that specifies the source from which to import metadata. It must begin with gs://.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sourcedatabase_go">
<a href="#sourcedatabase_go" style="color: inherit; text-decoration: inherit;">Source<wbr>Database</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the source database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="type_go">
<a href="#type_go" style="color: inherit; text-decoration: inherit;">Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. The type of the database dump. If unspecified, defaults to MYSQL.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language nodejs %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="databasetype_nodejs">
<a href="#databasetype_nodejs" style="color: inherit; text-decoration: inherit;">database<wbr>Type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The type of the database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="gcsuri_nodejs">
<a href="#gcsuri_nodejs" style="color: inherit; text-decoration: inherit;">gcs<wbr>Uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}A Cloud Storage object or folder URI that specifies the source from which to import metadata. It must begin with gs://.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="sourcedatabase_nodejs">
<a href="#sourcedatabase_nodejs" style="color: inherit; text-decoration: inherit;">source<wbr>Database</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}The name of the source database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="type_nodejs">
<a href="#type_nodejs" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">string</span>
    </dt>
    <dd>{{% md %}}Optional. The type of the database dump. If unspecified, defaults to MYSQL.{{% /md %}}</dd></dl>
{{% /choosable %}}

{{% choosable language python %}}
<dl class="resources-properties"><dt class="property-required"
            title="Required">
        <span id="database_type_python">
<a href="#database_type_python" style="color: inherit; text-decoration: inherit;">database_<wbr>type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The type of the database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="gcs_uri_python">
<a href="#gcs_uri_python" style="color: inherit; text-decoration: inherit;">gcs_<wbr>uri</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}A Cloud Storage object or folder URI that specifies the source from which to import metadata. It must begin with gs://.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="source_database_python">
<a href="#source_database_python" style="color: inherit; text-decoration: inherit;">source_<wbr>database</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}The name of the source database.{{% /md %}}</dd><dt class="property-required"
            title="Required">
        <span id="type_python">
<a href="#type_python" style="color: inherit; text-decoration: inherit;">type</a>
</span>
        <span class="property-indicator"></span>
        <span class="property-type">str</span>
    </dt>
    <dd>{{% md %}}Optional. The type of the database dump. If unspecified, defaults to MYSQL.{{% /md %}}</dd></dl>
{{% /choosable %}}





<h2 id="package-details">Package Details</h2>
<dl class="package-details">
	<dt>Repository</dt>
	<dd><a href="https://github.com/pulumi/pulumi-google-native">https://github.com/pulumi/pulumi-google-native</a></dd>
	<dt>License</dt>
	<dd>Apache-2.0</dd>
</dl>
