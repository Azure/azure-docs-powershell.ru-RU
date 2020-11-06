---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: eb75c1afc0b0fa82c0fee6b734ded951fdfa519f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567523"
---
# <span data-ttu-id="0d5e8-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d5e8-101">New-AzureRmResource</span></span>

## <span data-ttu-id="0d5e8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d5e8-102">SYNOPSIS</span></span>
<span data-ttu-id="0d5e8-103">Создание ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d5e8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d5e8-104">SYNTAX</span></span>

### <span data-ttu-id="0d5e8-105">Идентификатор ресурса (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="0d5e8-105">The resource Id. (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0d5e8-106">Ресурс, находящийся на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-106">Resource that resides at the subscription level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d5e8-107">Ресурс, находящийся на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-107">Resource that resides at the tenant level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d5e8-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d5e8-108">DESCRIPTION</span></span>
<span data-ttu-id="0d5e8-109">Командлет **New-AzureRmResource** создает ресурс Azure, например веб-сайт, сервер базы данных Azure SQL или базу данных Azure SQL, в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="0d5e8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d5e8-110">EXAMPLES</span></span>

### <span data-ttu-id="0d5e8-111">Пример 1: Создание ресурса</span><span class="sxs-lookup"><span data-stu-id="0d5e8-111">Example 1: Create a resource</span></span>
```
PS C:\>New-AzureRmResource -Location "West US" -Properties @{"test"="test"} -ResourceName "TestSite06" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -Force
```

<span data-ttu-id="0d5e8-112">Эта команда создает ресурс, который является веб-сайтом в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="0d5e8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d5e8-113">PARAMETERS</span></span>

### <span data-ttu-id="0d5e8-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0d5e8-114">-ApiVersion</span></span>
<span data-ttu-id="0d5e8-115">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-115">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="0d5e8-116">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0d5e8-117">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="0d5e8-117">-ExtensionResourceName</span></span>
<span data-ttu-id="0d5e8-118">Указывает имя ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-118">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="0d5e8-119">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-119">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="0d5e8-120">имя базы данных сервера доменных имен `/`</span><span class="sxs-lookup"><span data-stu-id="0d5e8-120">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5e8-121">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="0d5e8-121">-ExtensionResourceType</span></span>
<span data-ttu-id="0d5e8-122">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-122">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="0d5e8-123">Например, если ресурсом расширения является база данных, укажите следующий тип:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-123">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5e8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0d5e8-124">-Force</span></span>
<span data-ttu-id="0d5e8-125">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0d5e8-126">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="0d5e8-126">-IsFullObject</span></span>
<span data-ttu-id="0d5e8-127">Указывает на то, что объект, который указывает параметр *свойств* , — это полный объект.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-127">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="0d5e8-128">-Видах</span><span class="sxs-lookup"><span data-stu-id="0d5e8-128">-Kind</span></span>
<span data-ttu-id="0d5e8-129">Указывает ресурс ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-129">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="0d5e8-130">-Location</span><span class="sxs-lookup"><span data-stu-id="0d5e8-130">-Location</span></span>
<span data-ttu-id="0d5e8-131">Определяет расположение ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-131">Specifies the location of the resource.</span></span>
<span data-ttu-id="0d5e8-132">Укажите расположение центра обработки данных, например, Центральный регион США или Юго-Восток.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-132">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="0d5e8-133">Ресурс можно поместить в любое место, которое поддерживает ресурсы такого типа.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-133">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="0d5e8-134">Группы ресурсов могут содержать ресурсы из различных местоположений.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-134">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="0d5e8-135">Чтобы определить, какие расположения поддерживают каждый тип ресурсов, используйте командлет Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-135">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="0d5e8-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="0d5e8-136">-ODataQuery</span></span>
<span data-ttu-id="0d5e8-137">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="0d5e8-137">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="0d5e8-138">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="0d5e8-139">-Планирование</span><span class="sxs-lookup"><span data-stu-id="0d5e8-139">-Plan</span></span>
<span data-ttu-id="0d5e8-140">Хэш-таблица, представляющая свойства плана ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-140">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="0d5e8-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="0d5e8-141">-Pre</span></span>
<span data-ttu-id="0d5e8-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0d5e8-143">-Свойства</span><span class="sxs-lookup"><span data-stu-id="0d5e8-143">-Properties</span></span>
<span data-ttu-id="0d5e8-144">Определяет свойства ресурса для ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-144">Specifies resource properties for the resource.</span></span> <span data-ttu-id="0d5e8-145">Используйте этот параметр, чтобы указать значения свойств, специфичных для типа ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-145">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="0d5e8-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d5e8-146">-ResourceGroupName</span></span>
<span data-ttu-id="0d5e8-147">Указывает имя группы ресурсов, в которой этот командлет создает ресурс.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-147">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5e8-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d5e8-148">-ResourceId</span></span>
<span data-ttu-id="0d5e8-149">Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-149">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="0d5e8-150">`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0d5e8-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5e8-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0d5e8-151">-ResourceName</span></span>
<span data-ttu-id="0d5e8-152">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-152">Specifies the name of the resource.</span></span> <span data-ttu-id="0d5e8-153">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-153">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5e8-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0d5e8-154">-ResourceType</span></span>
<span data-ttu-id="0d5e8-155">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="0d5e8-156">Например, для базы данных тип ресурса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-156">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d5e8-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="0d5e8-157">-Sku</span></span>
<span data-ttu-id="0d5e8-158">Хэш-таблица, представляющая свойства SKU.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-158">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="0d5e8-159">-Тег</span><span class="sxs-lookup"><span data-stu-id="0d5e8-159">-Tag</span></span>
<span data-ttu-id="0d5e8-160">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0d5e8-161">Например:</span><span class="sxs-lookup"><span data-stu-id="0d5e8-161">For example:</span></span>

<span data-ttu-id="0d5e8-162">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="0d5e8-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="0d5e8-163">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0d5e8-163">-TenantLevel</span></span>
<span data-ttu-id="0d5e8-164">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-164">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5e8-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d5e8-165">-Confirm</span></span>
<span data-ttu-id="0d5e8-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d5e8-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d5e8-167">-WhatIf</span></span>
<span data-ttu-id="0d5e8-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d5e8-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d5e8-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d5e8-170">-DefaultProfile</span></span>
<span data-ttu-id="0d5e8-171">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d5e8-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d5e8-172">CommonParameters</span></span>
<span data-ttu-id="0d5e8-173">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d5e8-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d5e8-174">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d5e8-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d5e8-175">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d5e8-175">INPUTS</span></span>

## <span data-ttu-id="0d5e8-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d5e8-176">OUTPUTS</span></span>

### <span data-ttu-id="0d5e8-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="0d5e8-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0d5e8-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d5e8-178">NOTES</span></span>

## <span data-ttu-id="0d5e8-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d5e8-179">RELATED LINKS</span></span>

[<span data-ttu-id="0d5e8-180">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d5e8-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="0d5e8-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d5e8-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="0d5e8-182">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d5e8-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="0d5e8-183">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d5e8-183">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="0d5e8-184">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="0d5e8-184">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
