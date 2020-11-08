---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: 7a4929ffff531bb11b19b44ca9c0914c71662c8d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077646"
---
# <span data-ttu-id="9c883-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="9c883-101">Set-AzResource</span></span>

## <span data-ttu-id="9c883-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9c883-102">SYNOPSIS</span></span>
<span data-ttu-id="9c883-103">Изменяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="9c883-103">Modifies a resource.</span></span>

## <span data-ttu-id="9c883-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9c883-104">SYNTAX</span></span>

### <span data-ttu-id="9c883-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9c883-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c883-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9c883-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c883-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="9c883-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c883-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9c883-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c883-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c883-109">DESCRIPTION</span></span>
<span data-ttu-id="9c883-110">Командлет **Set-AzResource** изменяет существующий ресурс Azure.</span><span class="sxs-lookup"><span data-stu-id="9c883-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="9c883-111">Укажите ресурс, который нужно изменить по имени и типу или по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="9c883-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="9c883-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9c883-112">EXAMPLES</span></span>

### <span data-ttu-id="9c883-113">Пример 1: изменение ресурса</span><span class="sxs-lookup"><span data-stu-id="9c883-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="9c883-114">Первая команда получает ресурс с именем ContosoSite с помощью командлета Get-AzResource и сохраняет его в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="9c883-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="9c883-115">Вторая команда изменяет свойство $Resource.</span><span class="sxs-lookup"><span data-stu-id="9c883-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="9c883-116">Последняя команда обновляет ресурс так, чтобы он соответствовал $Resource.</span><span class="sxs-lookup"><span data-stu-id="9c883-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="9c883-117">Пример 2: изменение всех ресурсов в данной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="9c883-117">Example 2: Modify all resources in a given resource group</span></span>
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

<span data-ttu-id="9c883-118">Первая команда получает ресурсы в группе ресурсов testrg и сохраняет их в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="9c883-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="9c883-119">Вторая команда выполняет итерацию для каждого из этих ресурсов в группе ресурсов и добавляет к ним новый тег.</span><span class="sxs-lookup"><span data-stu-id="9c883-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="9c883-120">Последняя команда обновляет каждый из этих ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c883-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="9c883-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9c883-121">PARAMETERS</span></span>

### <span data-ttu-id="9c883-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9c883-122">-ApiVersion</span></span>
<span data-ttu-id="9c883-123">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c883-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9c883-124">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="9c883-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9c883-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c883-125">-AsJob</span></span>
<span data-ttu-id="9c883-126">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9c883-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c883-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c883-127">-DefaultProfile</span></span>
<span data-ttu-id="9c883-128">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9c883-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9c883-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="9c883-129">-ExtensionResourceName</span></span>
<span data-ttu-id="9c883-130">Указывает имя ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="9c883-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="9c883-131">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных имени сервера</span><span class="sxs-lookup"><span data-stu-id="9c883-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="9c883-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9c883-132">-ExtensionResourceType</span></span>
<span data-ttu-id="9c883-133">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="9c883-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="9c883-134">Например, если ресурсом расширения является база данных, укажите следующее: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="9c883-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="9c883-135">-Force</span><span class="sxs-lookup"><span data-stu-id="9c883-135">-Force</span></span>
<span data-ttu-id="9c883-136">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9c883-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c883-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9c883-137">-InputObject</span></span>
<span data-ttu-id="9c883-138">Объектное представление ресурса для обновления.</span><span class="sxs-lookup"><span data-stu-id="9c883-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="9c883-139">-Видах</span><span class="sxs-lookup"><span data-stu-id="9c883-139">-Kind</span></span>
<span data-ttu-id="9c883-140">Указывает ресурс ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9c883-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="9c883-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9c883-141">-ODataQuery</span></span>
<span data-ttu-id="9c883-142">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="9c883-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="9c883-143">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="9c883-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="9c883-144">-Планирование</span><span class="sxs-lookup"><span data-stu-id="9c883-144">-Plan</span></span>
<span data-ttu-id="9c883-145">Определяет свойства плана ресурсов в виде хэш-таблицы для ресурса.</span><span class="sxs-lookup"><span data-stu-id="9c883-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="9c883-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="9c883-146">-Pre</span></span>
<span data-ttu-id="9c883-147">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="9c883-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9c883-148">-Свойства</span><span class="sxs-lookup"><span data-stu-id="9c883-148">-Properties</span></span>
<span data-ttu-id="9c883-149">Определяет свойства ресурса для ресурса.</span><span class="sxs-lookup"><span data-stu-id="9c883-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="9c883-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c883-150">-ResourceGroupName</span></span>
<span data-ttu-id="9c883-151">Указывает имя группы ресурсов, в которой этот командлет изменяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="9c883-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="9c883-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c883-152">-ResourceId</span></span>
<span data-ttu-id="9c883-153">Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере: `/subscriptions/` идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9c883-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="9c883-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9c883-154">-ResourceName</span></span>
<span data-ttu-id="9c883-155">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="9c883-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="9c883-156">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9c883-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="9c883-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9c883-157">-ResourceType</span></span>
<span data-ttu-id="9c883-158">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="9c883-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="9c883-159">Например, для базы данных тип ресурса выглядит следующим образом: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="9c883-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="9c883-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="9c883-160">-Sku</span></span>
<span data-ttu-id="9c883-161">Указывает объект SKU ресурса в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="9c883-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="9c883-162">-Тег</span><span class="sxs-lookup"><span data-stu-id="9c883-162">-Tag</span></span>
<span data-ttu-id="9c883-163">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="9c883-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9c883-164">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="9c883-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9c883-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9c883-165">-TenantLevel</span></span>
<span data-ttu-id="9c883-166">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="9c883-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="9c883-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="9c883-167">-UsePatchSemantics</span></span>
<span data-ttu-id="9c883-168">Указывает на то, что этот командлет использует исправление HTTP для обновления объекта вместо HTTP-вставки.</span><span class="sxs-lookup"><span data-stu-id="9c883-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="9c883-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c883-169">-Confirm</span></span>
<span data-ttu-id="9c883-170">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9c883-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c883-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c883-171">-WhatIf</span></span>
<span data-ttu-id="9c883-172">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9c883-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c883-173">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9c883-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c883-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c883-174">CommonParameters</span></span>
<span data-ttu-id="9c883-175">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9c883-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c883-176">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c883-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c883-177">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9c883-177">INPUTS</span></span>

### <span data-ttu-id="9c883-178">Microsoft. Azure. Commands. ResourceManager. командлеты. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="9c883-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="9c883-179">System. String</span><span class="sxs-lookup"><span data-stu-id="9c883-179">System.String</span></span>

### <span data-ttu-id="9c883-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9c883-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="9c883-181">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="9c883-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="9c883-182">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9c883-182">OUTPUTS</span></span>

### <span data-ttu-id="9c883-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9c883-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9c883-184">Пуск</span><span class="sxs-lookup"><span data-stu-id="9c883-184">NOTES</span></span>

## <span data-ttu-id="9c883-185">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9c883-185">RELATED LINKS</span></span>

[<span data-ttu-id="9c883-186">Find-AzResource</span><span class="sxs-lookup"><span data-stu-id="9c883-186">Find-AzResource</span></span>](./Find-AzResource.md)

[<span data-ttu-id="9c883-187">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="9c883-187">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="9c883-188">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="9c883-188">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="9c883-189">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="9c883-189">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="9c883-190">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="9c883-190">Remove-AzResource</span></span>](./Remove-AzResource.md)
