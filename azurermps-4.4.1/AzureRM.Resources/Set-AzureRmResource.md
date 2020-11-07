---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: d3e7a1e947eb03c52c2cd8e032a359eb7765be03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734234"
---
# <span data-ttu-id="9ab4d-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9ab4d-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="9ab4d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ab4d-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab4d-103">Изменяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ab4d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ab4d-104">SYNTAX</span></span>

### <span data-ttu-id="9ab4d-105">Идентификатор ресурса (по умолчанию).</span><span class="sxs-lookup"><span data-stu-id="9ab4d-105">The resource Id. (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9ab4d-106">Ресурс, находящийся на уровне подписки.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-106">Resource that resides at the subscription level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab4d-107">Ресурс, находящийся на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-107">Resource that resides at the tenant level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9ab4d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ab4d-108">DESCRIPTION</span></span>
<span data-ttu-id="9ab4d-109">Командлет **Set-AzureRmResource** изменяет существующий ресурс Azure.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="9ab4d-110">Укажите ресурс, который нужно изменить по имени и типу или по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="9ab4d-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ab4d-111">EXAMPLES</span></span>

### <span data-ttu-id="9ab4d-112">Пример 1: изменение ресурса</span><span class="sxs-lookup"><span data-stu-id="9ab4d-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="9ab4d-113">Первая команда получает ресурс с именем ContosoSite с помощью командлета Get-AzureRmResource и сохраняет его в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="9ab4d-114">Вторая команда изменяет свойство $Resource.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="9ab4d-115">Последняя команда обновляет ресурс так, чтобы он соответствовал $Resource.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="9ab4d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ab4d-116">PARAMETERS</span></span>

### <span data-ttu-id="9ab4d-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9ab4d-117">-ApiVersion</span></span>
<span data-ttu-id="9ab4d-118">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9ab4d-119">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9ab4d-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="9ab4d-120">-ExtensionResourceName</span></span>
<span data-ttu-id="9ab4d-121">Указывает имя ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-121">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="9ab4d-122">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="9ab4d-122">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="9ab4d-123">имя базы данных сервера доменных имен `/`</span><span class="sxs-lookup"><span data-stu-id="9ab4d-123">server name`/`database name</span></span>

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

### <span data-ttu-id="9ab4d-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9ab4d-124">-ExtensionResourceType</span></span>
<span data-ttu-id="9ab4d-125">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="9ab4d-126">Например, если ресурсом расширения является база данных, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="9ab4d-126">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="9ab4d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="9ab4d-127">-Force</span></span>
<span data-ttu-id="9ab4d-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9ab4d-129">-Видах</span><span class="sxs-lookup"><span data-stu-id="9ab4d-129">-Kind</span></span>
<span data-ttu-id="9ab4d-130">Указывает ресурс ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-130">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="9ab4d-131">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9ab4d-131">-ODataQuery</span></span>
<span data-ttu-id="9ab4d-132">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="9ab4d-132">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="9ab4d-133">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-133">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="9ab4d-134">-Планирование</span><span class="sxs-lookup"><span data-stu-id="9ab4d-134">-Plan</span></span>
<span data-ttu-id="9ab4d-135">Определяет свойства плана ресурсов в виде хэш-таблицы для ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-135">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="9ab4d-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="9ab4d-136">-Pre</span></span>
<span data-ttu-id="9ab4d-137">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9ab4d-138">-Свойства</span><span class="sxs-lookup"><span data-stu-id="9ab4d-138">-Properties</span></span>
<span data-ttu-id="9ab4d-139">Определяет свойства ресурса для ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-139">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="9ab4d-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab4d-140">-ResourceGroupName</span></span>
<span data-ttu-id="9ab4d-141">Указывает имя группы ресурсов, в которой этот командлет изменяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-141">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="9ab4d-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ab4d-142">-ResourceId</span></span>
<span data-ttu-id="9ab4d-143">Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="9ab4d-143">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="9ab4d-144">`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9ab4d-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="9ab4d-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9ab4d-145">-ResourceName</span></span>
<span data-ttu-id="9ab4d-146">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-146">Specifies the name of the resource.</span></span>
<span data-ttu-id="9ab4d-147">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="9ab4d-147">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="9ab4d-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9ab4d-148">-ResourceType</span></span>
<span data-ttu-id="9ab4d-149">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-149">Specifies the type of the resource.</span></span>
<span data-ttu-id="9ab4d-150">Например, для базы данных тип ресурса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="9ab4d-150">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="9ab4d-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="9ab4d-151">-Sku</span></span>
<span data-ttu-id="9ab4d-152">Указывает объект SKU ресурса в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-152">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="9ab4d-153">-Тег</span><span class="sxs-lookup"><span data-stu-id="9ab4d-153">-Tag</span></span>
<span data-ttu-id="9ab4d-154">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9ab4d-155">Например:</span><span class="sxs-lookup"><span data-stu-id="9ab4d-155">For example:</span></span>

<span data-ttu-id="9ab4d-156">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="9ab4d-156">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9ab4d-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9ab4d-157">-TenantLevel</span></span>
<span data-ttu-id="9ab4d-158">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="9ab4d-159">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="9ab4d-159">-UsePatchSemantics</span></span>
<span data-ttu-id="9ab4d-160">Указывает на то, что этот командлет использует исправление HTTP для обновления объекта вместо HTTP-вставки.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-160">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="9ab4d-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ab4d-161">-Confirm</span></span>
<span data-ttu-id="9ab4d-162">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ab4d-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ab4d-163">-WhatIf</span></span>
<span data-ttu-id="9ab4d-164">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ab4d-165">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ab4d-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab4d-166">-DefaultProfile</span></span>
<span data-ttu-id="9ab4d-167">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ab4d-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab4d-168">CommonParameters</span></span>
<span data-ttu-id="9ab4d-169">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ab4d-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab4d-170">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ab4d-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab4d-171">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ab4d-171">INPUTS</span></span>

## <span data-ttu-id="9ab4d-172">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ab4d-172">OUTPUTS</span></span>

### <span data-ttu-id="9ab4d-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9ab4d-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9ab4d-174">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ab4d-174">NOTES</span></span>

## <span data-ttu-id="9ab4d-175">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ab4d-175">RELATED LINKS</span></span>

[<span data-ttu-id="9ab4d-176">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9ab4d-176">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="9ab4d-177">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9ab4d-177">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="9ab4d-178">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9ab4d-178">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="9ab4d-179">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9ab4d-179">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="9ab4d-180">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="9ab4d-180">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
