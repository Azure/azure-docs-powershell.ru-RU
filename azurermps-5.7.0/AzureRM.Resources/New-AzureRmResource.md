---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: c7a98f6fba2c690fb296c42f4f6eca902d7678bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93561543"
---
# <span data-ttu-id="1a656-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1a656-101">New-AzureRmResource</span></span>

## <span data-ttu-id="1a656-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a656-102">SYNOPSIS</span></span>
<span data-ttu-id="1a656-103">Создание ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a656-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a656-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a656-104">SYNTAX</span></span>

### <span data-ttu-id="1a656-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a656-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1a656-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="1a656-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a656-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="1a656-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a656-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a656-108">DESCRIPTION</span></span>
<span data-ttu-id="1a656-109">Командлет **New-AzureRmResource** создает ресурс Azure, например веб-сайт, сервер базы данных Azure SQL или базу данных Azure SQL, в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a656-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="1a656-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a656-110">EXAMPLES</span></span>

### <span data-ttu-id="1a656-111">Пример 1: Создание ресурса</span><span class="sxs-lookup"><span data-stu-id="1a656-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="1a656-112">Эта команда создает ресурс, который является веб-сайтом в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1a656-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="1a656-113">Пример 2: Создание ресурса с помощью splatting</span><span class="sxs-lookup"><span data-stu-id="1a656-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="1a656-114">Эта команда создает ресурс, который является веб-сайтом в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="1a656-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="1a656-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a656-115">PARAMETERS</span></span>

### <span data-ttu-id="1a656-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1a656-116">-ApiVersion</span></span>
<span data-ttu-id="1a656-117">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a656-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="1a656-118">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="1a656-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a656-119">-AsJob</span></span>
<span data-ttu-id="1a656-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="1a656-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a656-121">-DefaultProfile</span></span>
<span data-ttu-id="1a656-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="1a656-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="1a656-123">-ExtensionResourceName</span></span>
<span data-ttu-id="1a656-124">Указывает имя ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a656-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="1a656-125">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="1a656-125">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="1a656-126">имя базы данных сервера доменных имен `/`</span><span class="sxs-lookup"><span data-stu-id="1a656-126">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="1a656-127">-ExtensionResourceType</span></span>
<span data-ttu-id="1a656-128">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a656-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="1a656-129">Например, если ресурсом расширения является база данных, укажите следующий тип:</span><span class="sxs-lookup"><span data-stu-id="1a656-129">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-130">-Force</span><span class="sxs-lookup"><span data-stu-id="1a656-130">-Force</span></span>
<span data-ttu-id="1a656-131">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="1a656-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-132">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="1a656-132">-IsFullObject</span></span>
<span data-ttu-id="1a656-133">Указывает на то, что объект, который указывает параметр *свойств* , — это полный объект.</span><span class="sxs-lookup"><span data-stu-id="1a656-133">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-134">-Видах</span><span class="sxs-lookup"><span data-stu-id="1a656-134">-Kind</span></span>
<span data-ttu-id="1a656-135">Указывает ресурс ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a656-135">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-136">-Location</span><span class="sxs-lookup"><span data-stu-id="1a656-136">-Location</span></span>
<span data-ttu-id="1a656-137">Определяет расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a656-137">Specifies the location of the resource.</span></span>
<span data-ttu-id="1a656-138">Укажите расположение центра обработки данных, например, Центральный регион США или Юго-Восток.</span><span class="sxs-lookup"><span data-stu-id="1a656-138">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="1a656-139">Ресурс можно поместить в любое место, которое поддерживает ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="1a656-139">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="1a656-140">Группы ресурсов могут содержать ресурсы из различных местоположений.</span><span class="sxs-lookup"><span data-stu-id="1a656-140">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="1a656-141">Чтобы определить, какие расположения поддерживают каждый тип ресурсов, используйте командлет Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="1a656-141">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-142">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="1a656-142">-ODataQuery</span></span>
<span data-ttu-id="1a656-143">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="1a656-143">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="1a656-144">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="1a656-144">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-145">-Планирование</span><span class="sxs-lookup"><span data-stu-id="1a656-145">-Plan</span></span>
<span data-ttu-id="1a656-146">Хэш-таблица, представляющая свойства плана ресурсов.</span><span class="sxs-lookup"><span data-stu-id="1a656-146">A hash table that represents resource plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="1a656-147">-Pre</span></span>
<span data-ttu-id="1a656-148">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="1a656-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-149">-Свойства</span><span class="sxs-lookup"><span data-stu-id="1a656-149">-Properties</span></span>
<span data-ttu-id="1a656-150">Определяет свойства ресурса для ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a656-150">Specifies resource properties for the resource.</span></span> <span data-ttu-id="1a656-151">Используйте этот параметр, чтобы указать значения свойств, специфичных для типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a656-151">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a656-152">-ResourceGroupName</span></span>
<span data-ttu-id="1a656-153">Указывает имя группы ресурсов, в которой этот командлет создает ресурс.</span><span class="sxs-lookup"><span data-stu-id="1a656-153">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a656-154">-ResourceId</span></span>
<span data-ttu-id="1a656-155">Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="1a656-155">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="1a656-156">`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="1a656-156">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-157">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="1a656-157">-ResourceName</span></span>
<span data-ttu-id="1a656-158">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a656-158">Specifies the name of the resource.</span></span> <span data-ttu-id="1a656-159">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="1a656-159">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-160">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="1a656-160">-ResourceType</span></span>
<span data-ttu-id="1a656-161">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="1a656-161">Specifies the type of the resource.</span></span>
<span data-ttu-id="1a656-162">Например, для базы данных тип ресурса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1a656-162">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-163">-SKU</span><span class="sxs-lookup"><span data-stu-id="1a656-163">-Sku</span></span>
<span data-ttu-id="1a656-164">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="1a656-164">A hash table that represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-165">-Тег</span><span class="sxs-lookup"><span data-stu-id="1a656-165">-Tag</span></span>
<span data-ttu-id="1a656-166">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="1a656-166">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="1a656-167">Например:</span><span class="sxs-lookup"><span data-stu-id="1a656-167">For example:</span></span>

<span data-ttu-id="1a656-168">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="1a656-168">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-169">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="1a656-169">-TenantLevel</span></span>
<span data-ttu-id="1a656-170">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="1a656-170">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-171">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1a656-171">-Confirm</span></span>
<span data-ttu-id="1a656-172">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="1a656-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a656-173">-WhatIf</span></span>
<span data-ttu-id="1a656-174">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="1a656-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1a656-175">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="1a656-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a656-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a656-176">CommonParameters</span></span>
<span data-ttu-id="1a656-177">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a656-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a656-178">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a656-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a656-179">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a656-179">INPUTS</span></span>

### <span data-ttu-id="1a656-180">Ничего</span><span class="sxs-lookup"><span data-stu-id="1a656-180">None</span></span>
<span data-ttu-id="1a656-181">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="1a656-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1a656-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a656-182">OUTPUTS</span></span>

### <span data-ttu-id="1a656-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1a656-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1a656-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a656-184">NOTES</span></span>

## <span data-ttu-id="1a656-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a656-185">RELATED LINKS</span></span>

[<span data-ttu-id="1a656-186">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1a656-186">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="1a656-187">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1a656-187">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="1a656-188">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1a656-188">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="1a656-189">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1a656-189">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="1a656-190">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="1a656-190">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
