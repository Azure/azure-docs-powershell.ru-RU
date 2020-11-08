---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 0c4f351ca224991862e6b050462270fd64fd2a33
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079341"
---
# <span data-ttu-id="a827e-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="a827e-101">New-AzResource</span></span>

## <span data-ttu-id="a827e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a827e-102">SYNOPSIS</span></span>
<span data-ttu-id="a827e-103">Создание ресурса.</span><span class="sxs-lookup"><span data-stu-id="a827e-103">Creates a resource.</span></span>

## <span data-ttu-id="a827e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a827e-104">SYNTAX</span></span>

### <span data-ttu-id="a827e-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a827e-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a827e-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="a827e-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a827e-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="a827e-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a827e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a827e-108">DESCRIPTION</span></span>
<span data-ttu-id="a827e-109">Командлет **New-AzResource** создает ресурс Azure, например веб-сайт, сервер базы данных Azure SQL или базу данных Azure SQL, в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a827e-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="a827e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a827e-110">EXAMPLES</span></span>

### <span data-ttu-id="a827e-111">Пример 1: Создание ресурса</span><span class="sxs-lookup"><span data-stu-id="a827e-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="a827e-112">Эта команда создает ресурс, который является веб-сайтом в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a827e-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="a827e-113">Пример 2: Создание ресурса с помощью splatting</span><span class="sxs-lookup"><span data-stu-id="a827e-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="a827e-114">Эта команда создает ресурс, который является веб-сайтом в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="a827e-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="a827e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a827e-115">PARAMETERS</span></span>

### <span data-ttu-id="a827e-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a827e-116">-ApiVersion</span></span>
<span data-ttu-id="a827e-117">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a827e-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="a827e-118">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="a827e-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="a827e-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a827e-119">-AsJob</span></span>
<span data-ttu-id="a827e-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="a827e-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a827e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a827e-121">-DefaultProfile</span></span>
<span data-ttu-id="a827e-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="a827e-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a827e-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="a827e-123">-ExtensionResourceName</span></span>
<span data-ttu-id="a827e-124">Указывает имя ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="a827e-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="a827e-125">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных имени сервера</span><span class="sxs-lookup"><span data-stu-id="a827e-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="a827e-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="a827e-126">-ExtensionResourceType</span></span>
<span data-ttu-id="a827e-127">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="a827e-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="a827e-128">Например, если ресурсом расширения является база данных, укажите следующий тип: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a827e-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a827e-129">-Force</span><span class="sxs-lookup"><span data-stu-id="a827e-129">-Force</span></span>
<span data-ttu-id="a827e-130">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="a827e-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a827e-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="a827e-131">-IsFullObject</span></span>
<span data-ttu-id="a827e-132">Указывает на то, что объект, который указывает параметр *свойств* , — это полный объект.</span><span class="sxs-lookup"><span data-stu-id="a827e-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="a827e-133">-Видах</span><span class="sxs-lookup"><span data-stu-id="a827e-133">-Kind</span></span>
<span data-ttu-id="a827e-134">Указывает ресурс ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a827e-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="a827e-135">-Location</span><span class="sxs-lookup"><span data-stu-id="a827e-135">-Location</span></span>
<span data-ttu-id="a827e-136">Определяет расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="a827e-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="a827e-137">Укажите расположение центра обработки данных, например, Центральный регион США или Юго-Восток.</span><span class="sxs-lookup"><span data-stu-id="a827e-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="a827e-138">Ресурс можно поместить в любое место, которое поддерживает ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="a827e-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="a827e-139">Группы ресурсов могут содержать ресурсы из различных местоположений.</span><span class="sxs-lookup"><span data-stu-id="a827e-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="a827e-140">Чтобы определить, какие расположения поддерживают каждый тип ресурсов, используйте командлет Get-AzLocation.</span><span class="sxs-lookup"><span data-stu-id="a827e-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="a827e-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="a827e-141">-ODataQuery</span></span>
<span data-ttu-id="a827e-142">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="a827e-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="a827e-143">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="a827e-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="a827e-144">-Планирование</span><span class="sxs-lookup"><span data-stu-id="a827e-144">-Plan</span></span>
<span data-ttu-id="a827e-145">Хэш-таблица, представляющая свойства плана ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a827e-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="a827e-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="a827e-146">-Pre</span></span>
<span data-ttu-id="a827e-147">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="a827e-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="a827e-148">-Свойства</span><span class="sxs-lookup"><span data-stu-id="a827e-148">-Properties</span></span>
<span data-ttu-id="a827e-149">Определяет свойства ресурса для ресурса.</span><span class="sxs-lookup"><span data-stu-id="a827e-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="a827e-150">Используйте этот параметр, чтобы указать значения свойств, специфичных для типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="a827e-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="a827e-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a827e-151">-ResourceGroupName</span></span>
<span data-ttu-id="a827e-152">Указывает имя группы ресурсов, в которой этот командлет создает ресурс.</span><span class="sxs-lookup"><span data-stu-id="a827e-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="a827e-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a827e-153">-ResourceId</span></span>
<span data-ttu-id="a827e-154">Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере: `/subscriptions/` идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a827e-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a827e-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a827e-155">-ResourceName</span></span>
<span data-ttu-id="a827e-156">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="a827e-156">Specifies the name of the resource.</span></span> <span data-ttu-id="a827e-157">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="a827e-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="a827e-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="a827e-158">-ResourceType</span></span>
<span data-ttu-id="a827e-159">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="a827e-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="a827e-160">Например, для базы данных тип ресурса выглядит следующим образом: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="a827e-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="a827e-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="a827e-161">-Sku</span></span>
<span data-ttu-id="a827e-162">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="a827e-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="a827e-163">-Тег</span><span class="sxs-lookup"><span data-stu-id="a827e-163">-Tag</span></span>
<span data-ttu-id="a827e-164">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="a827e-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="a827e-165">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="a827e-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="a827e-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="a827e-166">-TenantLevel</span></span>
<span data-ttu-id="a827e-167">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="a827e-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="a827e-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a827e-168">-Confirm</span></span>
<span data-ttu-id="a827e-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a827e-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a827e-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a827e-170">-WhatIf</span></span>
<span data-ttu-id="a827e-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a827e-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a827e-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a827e-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a827e-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a827e-173">CommonParameters</span></span>
<span data-ttu-id="a827e-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a827e-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a827e-175">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a827e-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a827e-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a827e-176">INPUTS</span></span>

### <span data-ttu-id="a827e-177">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a827e-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a827e-178">System. String</span><span class="sxs-lookup"><span data-stu-id="a827e-178">System.String</span></span>

## <span data-ttu-id="a827e-179">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a827e-179">OUTPUTS</span></span>

### <span data-ttu-id="a827e-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="a827e-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="a827e-181">Пуск</span><span class="sxs-lookup"><span data-stu-id="a827e-181">NOTES</span></span>

## <span data-ttu-id="a827e-182">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a827e-182">RELATED LINKS</span></span>

[<span data-ttu-id="a827e-183">Find-AzResource</span><span class="sxs-lookup"><span data-stu-id="a827e-183">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="a827e-184">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="a827e-184">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="a827e-185">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="a827e-185">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="a827e-186">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="a827e-186">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="a827e-187">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="a827e-187">Set-AzResource</span></span>](./Set-AzResource.md)
