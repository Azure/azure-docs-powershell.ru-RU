---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226804"
---
# <span data-ttu-id="0b5d5-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="0b5d5-101">New-AzResource</span></span>

## <span data-ttu-id="0b5d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b5d5-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5d5-103">Создает ресурс.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-103">Creates a resource.</span></span>

## <span data-ttu-id="0b5d5-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0b5d5-104">SYNTAX</span></span>

### <span data-ttu-id="0b5d5-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b5d5-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b5d5-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0b5d5-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5d5-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0b5d5-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b5d5-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b5d5-108">DESCRIPTION</span></span>
<span data-ttu-id="0b5d5-109">С его SQL создается ресурс Azure, например **веб-сайт,** сервер базы данных Azure SQL или база данных Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="0b5d5-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0b5d5-110">EXAMPLES</span></span>

### <span data-ttu-id="0b5d5-111">Пример 1. Создание ресурса</span><span class="sxs-lookup"><span data-stu-id="0b5d5-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="0b5d5-112">Эта команда создает ресурс, который является веб-сайтом в группе ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="0b5d5-113">Пример 2. Создание ресурса с помощью разгона</span><span class="sxs-lookup"><span data-stu-id="0b5d5-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US"
    Properties        = @{test = "test"}
    ResourceName      = "TestSite06"
    ResourceType      = "microsoft.web/sites"
    ResourceGroupName = "ResourceGroup11"
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="0b5d5-114">Эта команда создает ресурс, который является веб-сайтом в группе ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="0b5d5-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b5d5-115">PARAMETERS</span></span>

### <span data-ttu-id="0b5d5-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0b5d5-116">-ApiVersion</span></span>
<span data-ttu-id="0b5d5-117">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="0b5d5-118">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0b5d5-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b5d5-119">-AsJob</span></span>
<span data-ttu-id="0b5d5-120">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0b5d5-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0b5d5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5d5-121">-DefaultProfile</span></span>
<span data-ttu-id="0b5d5-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="0b5d5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0b5d5-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="0b5d5-123">-ExtensionResourceName</span></span>
<span data-ttu-id="0b5d5-124">Указывает имя ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="0b5d5-125">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных "Имя сервера".</span><span class="sxs-lookup"><span data-stu-id="0b5d5-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="0b5d5-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="0b5d5-126">-ExtensionResourceType</span></span>
<span data-ttu-id="0b5d5-127">Тип ресурса для ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="0b5d5-128">Например, если ресурс расширения является базой данных, укажите следующий тип: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0b5d5-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0b5d5-129">-Force</span><span class="sxs-lookup"><span data-stu-id="0b5d5-129">-Force</span></span>
<span data-ttu-id="0b5d5-130">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0b5d5-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="0b5d5-131">-IsFullObject</span></span>
<span data-ttu-id="0b5d5-132">Указывает на то, что объект, который определяет параметр *Properties,* является полным объектом.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="0b5d5-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="0b5d5-133">-Kind</span></span>
<span data-ttu-id="0b5d5-134">Определяет тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="0b5d5-135">-Location</span><span class="sxs-lookup"><span data-stu-id="0b5d5-135">-Location</span></span>
<span data-ttu-id="0b5d5-136">Определяет расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="0b5d5-137">Укажите расположение центра обработки данных, например в Центральной США или Юго-Восточной Азии.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="0b5d5-138">Ресурс можно разместить в любом месте, которое поддерживает ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="0b5d5-139">Группы ресурсов могут содержать ресурсы из разных мест.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="0b5d5-140">Чтобы определить, в каких расположениях поддерживается каждый тип ресурсов, используйте Get-AzLocation.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="0b5d5-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="0b5d5-141">-ODataQuery</span></span>
<span data-ttu-id="0b5d5-142">Указывает фильтр стилей Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="0b5d5-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="0b5d5-143">Этот cmdlet добавит это значение к запросу в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="0b5d5-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="0b5d5-144">-Plan</span></span>
<span data-ttu-id="0b5d5-145">Hash table that represents resource plan properties.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-145">A hash table that represents resource plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5d5-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="0b5d5-146">-Pre</span></span>
<span data-ttu-id="0b5d5-147">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0b5d5-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="0b5d5-148">-Properties</span></span>
<span data-ttu-id="0b5d5-149">Определяет свойства ресурса.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="0b5d5-150">С помощью этого параметра можно указать значения свойств, специфифичивых для типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5d5-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5d5-151">-ResourceGroupName</span></span>
<span data-ttu-id="0b5d5-152">Имя группы ресурсов, в которой этот cmdlet создает ресурс.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="0b5d5-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b5d5-153">-ResourceId</span></span>
<span data-ttu-id="0b5d5-154">Указывает полностью определенный ИД ресурса, включая подписку, как по следующему примеру: `/subscriptions/` ИД подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0b5d5-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0b5d5-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0b5d5-155">-ResourceName</span></span>
<span data-ttu-id="0b5d5-156">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-156">Specifies the name of the resource.</span></span> <span data-ttu-id="0b5d5-157">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0b5d5-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0b5d5-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0b5d5-158">-ResourceType</span></span>
<span data-ttu-id="0b5d5-159">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="0b5d5-160">Например, для базы данных тип ресурса: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0b5d5-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0b5d5-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="0b5d5-161">-Sku</span></span>
<span data-ttu-id="0b5d5-162">Hash table that represents sku properties.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="0b5d5-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="0b5d5-163">-Tag</span></span>
<span data-ttu-id="0b5d5-164">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0b5d5-165">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0b5d5-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b5d5-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0b5d5-166">-TenantLevel</span></span>
<span data-ttu-id="0b5d5-167">Указывает на то, что этот cmdlet работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0b5d5-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b5d5-168">-Confirm</span></span>
<span data-ttu-id="0b5d5-169">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b5d5-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b5d5-170">-WhatIf</span></span>
<span data-ttu-id="0b5d5-171">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b5d5-172">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b5d5-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5d5-173">CommonParameters</span></span>
<span data-ttu-id="0b5d5-174">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b5d5-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5d5-175">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0b5d5-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5d5-176">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0b5d5-176">INPUTS</span></span>

### <span data-ttu-id="0b5d5-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b5d5-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0b5d5-178">System.String</span><span class="sxs-lookup"><span data-stu-id="0b5d5-178">System.String</span></span>

## <span data-ttu-id="0b5d5-179">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0b5d5-179">OUTPUTS</span></span>

### <span data-ttu-id="0b5d5-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="0b5d5-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0b5d5-181">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0b5d5-181">NOTES</span></span>

## <span data-ttu-id="0b5d5-182">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b5d5-182">RELATED LINKS</span></span>

[<span data-ttu-id="0b5d5-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="0b5d5-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="0b5d5-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="0b5d5-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="0b5d5-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="0b5d5-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="0b5d5-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="0b5d5-186">Set-AzResource</span></span>](./Set-AzResource.md)
