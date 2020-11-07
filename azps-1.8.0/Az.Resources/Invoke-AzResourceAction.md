---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 9a971618c205380a4ca2b049563fc8ee4542e681
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729409"
---
# <span data-ttu-id="9f2d1-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="9f2d1-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="9f2d1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f2d1-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2d1-103">Вызывает действие с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="9f2d1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f2d1-104">SYNTAX</span></span>

### <span data-ttu-id="9f2d1-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9f2d1-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9f2d1-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="9f2d1-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9f2d1-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="9f2d1-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f2d1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f2d1-108">DESCRIPTION</span></span>
<span data-ttu-id="9f2d1-109">Командлет **Invoke-AzResourceAction** вызывает действие с указанным ресурсом Azure.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="9f2d1-110">Чтобы получить список поддерживаемых действий, воспользуйтесь средством "Обозреватель ресурсов Azure".</span><span class="sxs-lookup"><span data-stu-id="9f2d1-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="9f2d1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f2d1-111">EXAMPLES</span></span>

## <span data-ttu-id="9f2d1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f2d1-112">PARAMETERS</span></span>

### <span data-ttu-id="9f2d1-113">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="9f2d1-113">-Action</span></span>
<span data-ttu-id="9f2d1-114">Указывает имя вызываемого действия.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-114">Specifies the name of the action to invoke.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ActionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2d1-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9f2d1-115">-ApiVersion</span></span>
<span data-ttu-id="9f2d1-116">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-116">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="9f2d1-117">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-117">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="9f2d1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f2d1-118">-DefaultProfile</span></span>
<span data-ttu-id="9f2d1-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="9f2d1-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9f2d1-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="9f2d1-120">-ExtensionResourceName</span></span>
<span data-ttu-id="9f2d1-121">Указывает имя ресурса расширения для ресурса, в котором этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-121">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="9f2d1-122">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных имени сервера</span><span class="sxs-lookup"><span data-stu-id="9f2d1-122">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="9f2d1-123">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="9f2d1-123">-ExtensionResourceType</span></span>
<span data-ttu-id="9f2d1-124">Указывает тип ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-124">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="9f2d1-125">Например: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="9f2d1-125">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="9f2d1-126">-Force</span><span class="sxs-lookup"><span data-stu-id="9f2d1-126">-Force</span></span>
<span data-ttu-id="9f2d1-127">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9f2d1-128">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="9f2d1-128">-ODataQuery</span></span>
<span data-ttu-id="9f2d1-129">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="9f2d1-129">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="9f2d1-130">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-130">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="9f2d1-131">-Parameters</span><span class="sxs-lookup"><span data-stu-id="9f2d1-131">-Parameters</span></span>
<span data-ttu-id="9f2d1-132">Задает параметры, которые являются хэш-таблицами для действия, вызванного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-132">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Object

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f2d1-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="9f2d1-133">-Pre</span></span>
<span data-ttu-id="9f2d1-134">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="9f2d1-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f2d1-135">-ResourceGroupName</span></span>
<span data-ttu-id="9f2d1-136">Указывает имя группы ресурсов, в которой этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-136">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="9f2d1-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9f2d1-137">-ResourceId</span></span>
<span data-ttu-id="9f2d1-138">Указывает полный ИД ресурса ресурса, в котором этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-138">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="9f2d1-139">Идентификатор включает подписку, как показано в следующем примере: `/subscriptions/` ИД подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9f2d1-139">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="9f2d1-140">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9f2d1-140">-ResourceName</span></span>
<span data-ttu-id="9f2d1-141">Указывает имя ресурса ресурса, который этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-141">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="9f2d1-142">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="9f2d1-142">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="9f2d1-143">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="9f2d1-143">-ResourceType</span></span>
<span data-ttu-id="9f2d1-144">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-144">Specifies the type of the resource.</span></span>
<span data-ttu-id="9f2d1-145">Например, для базы данных тип ресурса выглядит следующим образом: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="9f2d1-145">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="9f2d1-146">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="9f2d1-146">-TenantLevel</span></span>
<span data-ttu-id="9f2d1-147">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-147">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="9f2d1-148">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f2d1-148">-Confirm</span></span>
<span data-ttu-id="9f2d1-149">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f2d1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f2d1-150">-WhatIf</span></span>
<span data-ttu-id="9f2d1-151">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9f2d1-152">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f2d1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2d1-153">CommonParameters</span></span>
<span data-ttu-id="9f2d1-154">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f2d1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2d1-155">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f2d1-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2d1-156">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f2d1-156">INPUTS</span></span>

### <span data-ttu-id="9f2d1-157">System. String</span><span class="sxs-lookup"><span data-stu-id="9f2d1-157">System.String</span></span>

## <span data-ttu-id="9f2d1-158">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f2d1-158">OUTPUTS</span></span>

### <span data-ttu-id="9f2d1-159">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="9f2d1-159">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="9f2d1-160">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f2d1-160">NOTES</span></span>

## <span data-ttu-id="9f2d1-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f2d1-161">RELATED LINKS</span></span>
