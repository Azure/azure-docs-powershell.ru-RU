---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: 82e06a4736a613111efac452eb1fced2713dc470
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415756"
---
# <span data-ttu-id="bc24f-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="bc24f-101">Set-AzResource</span></span>

## <span data-ttu-id="bc24f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc24f-102">SYNOPSIS</span></span>
<span data-ttu-id="bc24f-103">Изменяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="bc24f-103">Modifies a resource.</span></span>

## <span data-ttu-id="bc24f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bc24f-104">SYNTAX</span></span>

### <span data-ttu-id="bc24f-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bc24f-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc24f-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bc24f-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bc24f-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="bc24f-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bc24f-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="bc24f-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bc24f-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bc24f-109">DESCRIPTION</span></span>
<span data-ttu-id="bc24f-110">**Cmdlet Set-AzResource** изменяет существующий ресурс Azure.</span><span class="sxs-lookup"><span data-stu-id="bc24f-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="bc24f-111">Укажите ресурс, который нужно изменить по имени, типу или по коду.</span><span class="sxs-lookup"><span data-stu-id="bc24f-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="bc24f-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bc24f-112">EXAMPLES</span></span>

### <span data-ttu-id="bc24f-113">Пример 1. Изменение ресурса</span><span class="sxs-lookup"><span data-stu-id="bc24f-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="bc24f-114">Первая команда получает ресурс ContosoSite с помощью командлета Get-AzResource, а затем сохраняет его в $Resource переменной.</span><span class="sxs-lookup"><span data-stu-id="bc24f-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="bc24f-115">Вторая команда изменяет свойство $Resource.</span><span class="sxs-lookup"><span data-stu-id="bc24f-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="bc24f-116">Конечная команда обновляет ресурс в $Resource.</span><span class="sxs-lookup"><span data-stu-id="bc24f-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="bc24f-117">Пример 2. Изменение всех ресурсов в заданной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="bc24f-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="bc24f-118">Первая команда получает ресурсы в группе ресурсов testrg, а затем сохраняет их в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="bc24f-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="bc24f-119">Вторая команда итерирует каждый из этих ресурсов в группе ресурсов и добавляет к ним новый тег.</span><span class="sxs-lookup"><span data-stu-id="bc24f-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="bc24f-120">Конечная команда обновляет каждый из этих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc24f-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="bc24f-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bc24f-121">PARAMETERS</span></span>

### <span data-ttu-id="bc24f-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="bc24f-122">-ApiVersion</span></span>
<span data-ttu-id="bc24f-123">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bc24f-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="bc24f-124">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="bc24f-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bc24f-125">-AsJob</span></span>
<span data-ttu-id="bc24f-126">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bc24f-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bc24f-127">-DefaultProfile</span></span>
<span data-ttu-id="bc24f-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="bc24f-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="bc24f-129">-ExtensionResourceName</span></span>
<span data-ttu-id="bc24f-130">Указывает имя ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="bc24f-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="bc24f-131">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных "Имя сервера".</span><span class="sxs-lookup"><span data-stu-id="bc24f-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="bc24f-132">-ExtensionResourceType</span></span>
<span data-ttu-id="bc24f-133">Тип ресурса для ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="bc24f-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="bc24f-134">Например, если ресурсом расширения является база данных, укажите следующее: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="bc24f-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-135">-Force</span><span class="sxs-lookup"><span data-stu-id="bc24f-135">-Force</span></span>
<span data-ttu-id="bc24f-136">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="bc24f-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bc24f-137">-InputObject</span></span>
<span data-ttu-id="bc24f-138">Объектное представление ресурса, который нужно обновить.</span><span class="sxs-lookup"><span data-stu-id="bc24f-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-139">-Kind</span><span class="sxs-lookup"><span data-stu-id="bc24f-139">-Kind</span></span>
<span data-ttu-id="bc24f-140">Определяет тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="bc24f-140">Specifies the resource kind for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="bc24f-141">-ODataQuery</span></span>
<span data-ttu-id="bc24f-142">Указывает фильтр стилей Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="bc24f-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="bc24f-143">Этот cmdlet добавит это значение к запросу в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="bc24f-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="bc24f-144">-Plan</span></span>
<span data-ttu-id="bc24f-145">Определяет свойства плана ресурсов (в качестве hash table) для ресурса.</span><span class="sxs-lookup"><span data-stu-id="bc24f-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="bc24f-146">-Pre</span></span>
<span data-ttu-id="bc24f-147">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="bc24f-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="bc24f-148">-Properties</span></span>
<span data-ttu-id="bc24f-149">Определяет свойства ресурса.</span><span class="sxs-lookup"><span data-stu-id="bc24f-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bc24f-150">-ResourceGroupName</span></span>
<span data-ttu-id="bc24f-151">Указывает имя группы ресурсов, для которой этот cmdlet изменяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="bc24f-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bc24f-152">-ResourceId</span></span>
<span data-ttu-id="bc24f-153">Указывает полностью определенный ИД ресурса, включая подписку, как по следующему примеру: `/subscriptions/` ИД подписки.`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="bc24f-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bc24f-154">-ResourceName</span></span>
<span data-ttu-id="bc24f-155">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="bc24f-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="bc24f-156">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="bc24f-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="bc24f-157">-ResourceType</span></span>
<span data-ttu-id="bc24f-158">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="bc24f-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="bc24f-159">Например, для базы данных тип ресурса: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="bc24f-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="bc24f-160">-Sku</span></span>
<span data-ttu-id="bc24f-161">Указывает объект SKU ресурса в качестве hash table.</span><span class="sxs-lookup"><span data-stu-id="bc24f-161">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="bc24f-162">-Tag</span></span>
<span data-ttu-id="bc24f-163">Пары значений ключа в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="bc24f-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="bc24f-164">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="bc24f-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="bc24f-165">-TenantLevel</span></span>
<span data-ttu-id="bc24f-166">Указывает на то, что этот cmdlet работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="bc24f-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="bc24f-167">-UsePatchSemantics</span></span>
<span data-ttu-id="bc24f-168">Указывает на то, что для обновления объекта с помощью этого cmdlet используется HTTP-ИСПРАВЛЕНИЕ, а не HTTP PUT.</span><span class="sxs-lookup"><span data-stu-id="bc24f-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bc24f-169">-Confirm</span></span>
<span data-ttu-id="bc24f-170">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="bc24f-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bc24f-171">-WhatIf</span></span>
<span data-ttu-id="bc24f-172">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bc24f-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bc24f-173">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bc24f-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bc24f-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc24f-174">CommonParameters</span></span>
<span data-ttu-id="bc24f-175">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bc24f-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc24f-176">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bc24f-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc24f-177">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bc24f-177">INPUTS</span></span>

### <span data-ttu-id="bc24f-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="bc24f-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="bc24f-179">System.String</span><span class="sxs-lookup"><span data-stu-id="bc24f-179">System.String</span></span>

### <span data-ttu-id="bc24f-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="bc24f-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="bc24f-181">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="bc24f-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="bc24f-182">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bc24f-182">OUTPUTS</span></span>

### <span data-ttu-id="bc24f-183">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="bc24f-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="bc24f-184">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bc24f-184">NOTES</span></span>

## <span data-ttu-id="bc24f-185">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bc24f-185">RELATED LINKS</span></span>


[<span data-ttu-id="bc24f-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="bc24f-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="bc24f-187">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="bc24f-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="bc24f-188">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="bc24f-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="bc24f-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="bc24f-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
