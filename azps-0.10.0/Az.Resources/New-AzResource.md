---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 7ae512f7992392bf12b17775a505313621ec3096
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/08/2020
ms.locfileid: "94077377"
---
# <span data-ttu-id="621bc-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="621bc-101">New-AzResource</span></span>

## <span data-ttu-id="621bc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="621bc-102">SYNOPSIS</span></span>
<span data-ttu-id="621bc-103">Создание ресурса.</span><span class="sxs-lookup"><span data-stu-id="621bc-103">Creates a resource.</span></span>

## <span data-ttu-id="621bc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="621bc-104">SYNTAX</span></span>

### <span data-ttu-id="621bc-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="621bc-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="621bc-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="621bc-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="621bc-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="621bc-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="621bc-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="621bc-108">DESCRIPTION</span></span>
<span data-ttu-id="621bc-109">Командлет **New-AzResource** создает ресурс Azure, например веб-сайт, сервер базы данных Azure SQL или базу данных Azure SQL, в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="621bc-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="621bc-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="621bc-110">EXAMPLES</span></span>

### <span data-ttu-id="621bc-111">Пример 1: Создание ресурса</span><span class="sxs-lookup"><span data-stu-id="621bc-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="621bc-112">Эта команда создает ресурс, который является веб-сайтом в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="621bc-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="621bc-113">Пример 2: Создание ресурса с помощью splatting</span><span class="sxs-lookup"><span data-stu-id="621bc-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="621bc-114">Эта команда создает ресурс, который является веб-сайтом в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="621bc-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="621bc-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="621bc-115">PARAMETERS</span></span>

### <span data-ttu-id="621bc-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="621bc-116">-ApiVersion</span></span>
<span data-ttu-id="621bc-117">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="621bc-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="621bc-118">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="621bc-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="621bc-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="621bc-119">-AsJob</span></span>
<span data-ttu-id="621bc-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="621bc-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="621bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621bc-121">-DefaultProfile</span></span>
<span data-ttu-id="621bc-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="621bc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="621bc-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="621bc-123">-ExtensionResourceName</span></span>
<span data-ttu-id="621bc-124">Указывает имя ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="621bc-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="621bc-125">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных имени сервера</span><span class="sxs-lookup"><span data-stu-id="621bc-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="621bc-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="621bc-126">-ExtensionResourceType</span></span>
<span data-ttu-id="621bc-127">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="621bc-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="621bc-128">Например, если ресурсом расширения является база данных, укажите следующий тип: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="621bc-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="621bc-129">-Force</span><span class="sxs-lookup"><span data-stu-id="621bc-129">-Force</span></span>
<span data-ttu-id="621bc-130">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="621bc-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="621bc-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="621bc-131">-IsFullObject</span></span>
<span data-ttu-id="621bc-132">Указывает на то, что объект, который указывает параметр *свойств* , — это полный объект.</span><span class="sxs-lookup"><span data-stu-id="621bc-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="621bc-133">-Видах</span><span class="sxs-lookup"><span data-stu-id="621bc-133">-Kind</span></span>
<span data-ttu-id="621bc-134">Указывает ресурс ресурсов.</span><span class="sxs-lookup"><span data-stu-id="621bc-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="621bc-135">-Location</span><span class="sxs-lookup"><span data-stu-id="621bc-135">-Location</span></span>
<span data-ttu-id="621bc-136">Определяет расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="621bc-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="621bc-137">Укажите расположение центра обработки данных, например, Центральный регион США или Юго-Восток.</span><span class="sxs-lookup"><span data-stu-id="621bc-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="621bc-138">Ресурс можно поместить в любое место, которое поддерживает ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="621bc-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="621bc-139">Группы ресурсов могут содержать ресурсы из различных местоположений.</span><span class="sxs-lookup"><span data-stu-id="621bc-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="621bc-140">Чтобы определить, какие расположения поддерживают каждый тип ресурсов, используйте командлет Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="621bc-140">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="621bc-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="621bc-141">-ODataQuery</span></span>
<span data-ttu-id="621bc-142">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="621bc-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="621bc-143">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="621bc-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="621bc-144">-Планирование</span><span class="sxs-lookup"><span data-stu-id="621bc-144">-Plan</span></span>
<span data-ttu-id="621bc-145">Хэш-таблица, представляющая свойства плана ресурсов.</span><span class="sxs-lookup"><span data-stu-id="621bc-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="621bc-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="621bc-146">-Pre</span></span>
<span data-ttu-id="621bc-147">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="621bc-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="621bc-148">-Свойства</span><span class="sxs-lookup"><span data-stu-id="621bc-148">-Properties</span></span>
<span data-ttu-id="621bc-149">Определяет свойства ресурса для ресурса.</span><span class="sxs-lookup"><span data-stu-id="621bc-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="621bc-150">Используйте этот параметр, чтобы указать значения свойств, специфичных для типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="621bc-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="621bc-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="621bc-151">-ResourceGroupName</span></span>
<span data-ttu-id="621bc-152">Указывает имя группы ресурсов, в которой этот командлет создает ресурс.</span><span class="sxs-lookup"><span data-stu-id="621bc-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="621bc-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="621bc-153">-ResourceId</span></span>
<span data-ttu-id="621bc-154">Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере: `/subscriptions/` идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="621bc-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="621bc-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="621bc-155">-ResourceName</span></span>
<span data-ttu-id="621bc-156">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="621bc-156">Specifies the name of the resource.</span></span> <span data-ttu-id="621bc-157">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="621bc-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="621bc-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="621bc-158">-ResourceType</span></span>
<span data-ttu-id="621bc-159">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="621bc-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="621bc-160">Например, для базы данных тип ресурса выглядит следующим образом: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="621bc-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="621bc-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="621bc-161">-Sku</span></span>
<span data-ttu-id="621bc-162">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="621bc-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="621bc-163">-Тег</span><span class="sxs-lookup"><span data-stu-id="621bc-163">-Tag</span></span>
<span data-ttu-id="621bc-164">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="621bc-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="621bc-165">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="621bc-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="621bc-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="621bc-166">-TenantLevel</span></span>
<span data-ttu-id="621bc-167">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="621bc-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="621bc-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="621bc-168">-Confirm</span></span>
<span data-ttu-id="621bc-169">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="621bc-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="621bc-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="621bc-170">-WhatIf</span></span>
<span data-ttu-id="621bc-171">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="621bc-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="621bc-172">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="621bc-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="621bc-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621bc-173">CommonParameters</span></span>
<span data-ttu-id="621bc-174">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="621bc-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621bc-175">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="621bc-175">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621bc-176">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="621bc-176">INPUTS</span></span>

### <span data-ttu-id="621bc-177">Ничего</span><span class="sxs-lookup"><span data-stu-id="621bc-177">None</span></span>

## <span data-ttu-id="621bc-178">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="621bc-178">OUTPUTS</span></span>

### <span data-ttu-id="621bc-179">Microsoft. Azure. Commands. ResourceManagement. Models. PSResource</span><span class="sxs-lookup"><span data-stu-id="621bc-179">Microsoft.Azure.Commands.ResourceManagement.Models.PSResource</span></span>

## <span data-ttu-id="621bc-180">Пуск</span><span class="sxs-lookup"><span data-stu-id="621bc-180">NOTES</span></span>

## <span data-ttu-id="621bc-181">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="621bc-181">RELATED LINKS</span></span>

[<span data-ttu-id="621bc-182">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="621bc-182">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="621bc-183">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="621bc-183">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="621bc-184">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="621bc-184">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="621bc-185">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="621bc-185">Set-AzResource</span></span>](./Set-AzResource.md)
