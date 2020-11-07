---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: 9b1f12060ca7cc161f4f7fbe7c99948d9ddd10f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734000"
---
# <span data-ttu-id="49115-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49115-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="49115-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49115-102">SYNOPSIS</span></span>
<span data-ttu-id="49115-103">Изменяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="49115-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49115-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49115-104">SYNTAX</span></span>

### <span data-ttu-id="49115-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49115-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="49115-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="49115-106">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49115-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="49115-107">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49115-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49115-108">DESCRIPTION</span></span>
<span data-ttu-id="49115-109">Командлет **Set-AzureRmResource** изменяет существующий ресурс Azure.</span><span class="sxs-lookup"><span data-stu-id="49115-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="49115-110">Укажите ресурс, который нужно изменить по имени и типу или по ИДЕНТИФИКАТОРу.</span><span class="sxs-lookup"><span data-stu-id="49115-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="49115-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49115-111">EXAMPLES</span></span>

### <span data-ttu-id="49115-112">Пример 1: изменение ресурса</span><span class="sxs-lookup"><span data-stu-id="49115-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="49115-113">Первая команда получает ресурс с именем ContosoSite с помощью командлета Get-AzureRmResource и сохраняет его в переменной $Resource.</span><span class="sxs-lookup"><span data-stu-id="49115-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="49115-114">Вторая команда изменяет свойство $Resource.</span><span class="sxs-lookup"><span data-stu-id="49115-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="49115-115">Последняя команда обновляет ресурс так, чтобы он соответствовал $Resource.</span><span class="sxs-lookup"><span data-stu-id="49115-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="49115-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49115-116">PARAMETERS</span></span>

### <span data-ttu-id="49115-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="49115-117">-ApiVersion</span></span>
<span data-ttu-id="49115-118">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49115-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="49115-119">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="49115-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="49115-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="49115-120">-AsJob</span></span>
<span data-ttu-id="49115-121">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="49115-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="49115-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49115-122">-DefaultProfile</span></span>
<span data-ttu-id="49115-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="49115-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="49115-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="49115-124">-ExtensionResourceName</span></span>
<span data-ttu-id="49115-125">Указывает имя ресурса расширения для ресурса.</span><span class="sxs-lookup"><span data-stu-id="49115-125">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="49115-126">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="49115-126">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="49115-127">имя базы данных сервера доменных имен `/`</span><span class="sxs-lookup"><span data-stu-id="49115-127">server name`/`database name</span></span>

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

### <span data-ttu-id="49115-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="49115-128">-ExtensionResourceType</span></span>
<span data-ttu-id="49115-129">Указывает тип ресурса для расширения ресурса.</span><span class="sxs-lookup"><span data-stu-id="49115-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="49115-130">Например, если ресурсом расширения является база данных, укажите следующее:</span><span class="sxs-lookup"><span data-stu-id="49115-130">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="49115-131">-Force</span><span class="sxs-lookup"><span data-stu-id="49115-131">-Force</span></span>
<span data-ttu-id="49115-132">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="49115-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="49115-133">-Видах</span><span class="sxs-lookup"><span data-stu-id="49115-133">-Kind</span></span>
<span data-ttu-id="49115-134">Указывает ресурс ресурсов.</span><span class="sxs-lookup"><span data-stu-id="49115-134">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49115-135">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="49115-135">-ODataQuery</span></span>
<span data-ttu-id="49115-136">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="49115-136">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="49115-137">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="49115-137">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="49115-138">-Планирование</span><span class="sxs-lookup"><span data-stu-id="49115-138">-Plan</span></span>
<span data-ttu-id="49115-139">Определяет свойства плана ресурсов в виде хэш-таблицы для ресурса.</span><span class="sxs-lookup"><span data-stu-id="49115-139">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49115-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="49115-140">-Pre</span></span>
<span data-ttu-id="49115-141">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="49115-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="49115-142">-Свойства</span><span class="sxs-lookup"><span data-stu-id="49115-142">-Properties</span></span>
<span data-ttu-id="49115-143">Определяет свойства ресурса для ресурса.</span><span class="sxs-lookup"><span data-stu-id="49115-143">Specifies resource properties for the resource.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49115-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49115-144">-ResourceGroupName</span></span>
<span data-ttu-id="49115-145">Указывает имя группы ресурсов, в которой этот командлет изменяет ресурс.</span><span class="sxs-lookup"><span data-stu-id="49115-145">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="49115-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="49115-146">-ResourceId</span></span>
<span data-ttu-id="49115-147">Указывает полный идентификатор ресурса, включая подписку, как показано в следующем примере:</span><span class="sxs-lookup"><span data-stu-id="49115-147">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="49115-148">`/subscriptions/`Идентификатор подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="49115-148">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="49115-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="49115-149">-ResourceName</span></span>
<span data-ttu-id="49115-150">Указывает имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="49115-150">Specifies the name of the resource.</span></span>
<span data-ttu-id="49115-151">Например, чтобы указать базу данных, используйте следующий формат:</span><span class="sxs-lookup"><span data-stu-id="49115-151">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="49115-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="49115-152">-ResourceType</span></span>
<span data-ttu-id="49115-153">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="49115-153">Specifies the type of the resource.</span></span>
<span data-ttu-id="49115-154">Например, для базы данных тип ресурса выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="49115-154">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="49115-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="49115-155">-Sku</span></span>
<span data-ttu-id="49115-156">Указывает объект SKU ресурса в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="49115-156">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="49115-157">-Тег</span><span class="sxs-lookup"><span data-stu-id="49115-157">-Tag</span></span>
<span data-ttu-id="49115-158">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="49115-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="49115-159">Например:</span><span class="sxs-lookup"><span data-stu-id="49115-159">For example:</span></span>

<span data-ttu-id="49115-160">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="49115-160">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49115-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="49115-161">-TenantLevel</span></span>
<span data-ttu-id="49115-162">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="49115-162">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="49115-163">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="49115-163">-UsePatchSemantics</span></span>
<span data-ttu-id="49115-164">Указывает на то, что этот командлет использует исправление HTTP для обновления объекта вместо HTTP-вставки.</span><span class="sxs-lookup"><span data-stu-id="49115-164">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="49115-165">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49115-165">-Confirm</span></span>
<span data-ttu-id="49115-166">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49115-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49115-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49115-167">-WhatIf</span></span>
<span data-ttu-id="49115-168">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49115-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49115-169">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49115-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49115-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49115-170">CommonParameters</span></span>
<span data-ttu-id="49115-171">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49115-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49115-172">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49115-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49115-173">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49115-173">INPUTS</span></span>

### <span data-ttu-id="49115-174">Ничего</span><span class="sxs-lookup"><span data-stu-id="49115-174">None</span></span>
<span data-ttu-id="49115-175">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="49115-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="49115-176">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49115-176">OUTPUTS</span></span>

### <span data-ttu-id="49115-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="49115-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="49115-178">Пуск</span><span class="sxs-lookup"><span data-stu-id="49115-178">NOTES</span></span>

## <span data-ttu-id="49115-179">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49115-179">RELATED LINKS</span></span>

[<span data-ttu-id="49115-180">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49115-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="49115-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49115-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="49115-182">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49115-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="49115-183">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49115-183">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="49115-184">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="49115-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
