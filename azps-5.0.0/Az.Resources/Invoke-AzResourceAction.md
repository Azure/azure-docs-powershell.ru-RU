---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316375"
---
# <span data-ttu-id="58ccf-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="58ccf-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="58ccf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58ccf-102">SYNOPSIS</span></span>
<span data-ttu-id="58ccf-103">Вызывает действие с ресурсом.</span><span class="sxs-lookup"><span data-stu-id="58ccf-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="58ccf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58ccf-104">SYNTAX</span></span>

### <span data-ttu-id="58ccf-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58ccf-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="58ccf-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="58ccf-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58ccf-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="58ccf-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58ccf-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ccf-108">DESCRIPTION</span></span>
<span data-ttu-id="58ccf-109">Командлет **Invoke-AzResourceAction** вызывает действие с указанным ресурсом Azure.</span><span class="sxs-lookup"><span data-stu-id="58ccf-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="58ccf-110">Чтобы получить список поддерживаемых действий, воспользуйтесь средством "Обозреватель ресурсов Azure".</span><span class="sxs-lookup"><span data-stu-id="58ccf-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="58ccf-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58ccf-111">EXAMPLES</span></span>

### <span data-ttu-id="58ccf-112">Пример 1: вызов для запуска виртуальной машины с ResourceId</span><span class="sxs-lookup"><span data-stu-id="58ccf-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="58ccf-113">Эта команда запускает виртуальную машину с {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="58ccf-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="58ccf-114">Пример 2: Invoke poweroffing ВМ с ResourceName</span><span class="sxs-lookup"><span data-stu-id="58ccf-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="58ccf-115">Эта команда останавливает виртуальную машину с помощью {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="58ccf-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="58ccf-116">Команда задает параметр *Force* , поэтому она не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="58ccf-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="58ccf-117">Пример 3: Invoke регистрация поставщика ресурсов с ИД ресурсов</span><span class="sxs-lookup"><span data-stu-id="58ccf-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/providers/Microsoft.Network -action register -Force

id                : /subscriptions/{subId}/providers/Microsoft.Network
namespace         : Microsoft.Network
authorizations    : {…}
resourceTypes     : {@{resourceType=virtualNetworks; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=publicIPAddresses; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=networkInterfaces; locations=System.Object[]; apiVersions=System.Object[]},
                    @{resourceType=privateEndpoints; locations=System.Object[]; apiVersions=System.Object[]}…}
registrationState : Registered
```

<span data-ttu-id="58ccf-118">Эта команда регистрирует поставщик ресурсов "Microsoft. Network".</span><span class="sxs-lookup"><span data-stu-id="58ccf-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="58ccf-119">Команда задает параметр *Force* , поэтому она не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="58ccf-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="58ccf-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58ccf-120">PARAMETERS</span></span>

### <span data-ttu-id="58ccf-121">-Action (действие)</span><span class="sxs-lookup"><span data-stu-id="58ccf-121">-Action</span></span>
<span data-ttu-id="58ccf-122">Указывает имя вызываемого действия.</span><span class="sxs-lookup"><span data-stu-id="58ccf-122">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="58ccf-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="58ccf-123">-ApiVersion</span></span>
<span data-ttu-id="58ccf-124">Указывает версию используемого API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58ccf-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="58ccf-125">Если вы не укажете версию, этот командлет использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="58ccf-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="58ccf-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ccf-126">-DefaultProfile</span></span>
<span data-ttu-id="58ccf-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="58ccf-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="58ccf-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="58ccf-128">-ExtensionResourceName</span></span>
<span data-ttu-id="58ccf-129">Указывает имя ресурса расширения для ресурса, в котором этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="58ccf-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="58ccf-130">Например, чтобы указать базу данных, используйте следующий формат: имя `/` базы данных имени сервера</span><span class="sxs-lookup"><span data-stu-id="58ccf-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="58ccf-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="58ccf-131">-ExtensionResourceType</span></span>
<span data-ttu-id="58ccf-132">Указывает тип ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="58ccf-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="58ccf-133">Например: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="58ccf-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="58ccf-134">-Force</span><span class="sxs-lookup"><span data-stu-id="58ccf-134">-Force</span></span>
<span data-ttu-id="58ccf-135">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="58ccf-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="58ccf-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="58ccf-136">-ODataQuery</span></span>
<span data-ttu-id="58ccf-137">Задает фильтр стиля Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="58ccf-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="58ccf-138">Этот командлет добавляет это значение в запрос в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="58ccf-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="58ccf-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="58ccf-139">-Parameters</span></span>
<span data-ttu-id="58ccf-140">Задает параметры, которые являются хэш-таблицами для действия, вызванного этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="58ccf-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="58ccf-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="58ccf-141">-Pre</span></span>
<span data-ttu-id="58ccf-142">Указывает на то, что этот командлет учитывает версии API предварительного выпуска, когда он автоматически определяет, какую версию использовать.</span><span class="sxs-lookup"><span data-stu-id="58ccf-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="58ccf-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ccf-143">-ResourceGroupName</span></span>
<span data-ttu-id="58ccf-144">Указывает имя группы ресурсов, в которой этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="58ccf-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="58ccf-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58ccf-145">-ResourceId</span></span>
<span data-ttu-id="58ccf-146">Указывает полный ИД ресурса ресурса, в котором этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="58ccf-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="58ccf-147">Идентификатор включает подписку, как показано в следующем примере: `/subscriptions/` ИД подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="58ccf-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="58ccf-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="58ccf-148">-ResourceName</span></span>
<span data-ttu-id="58ccf-149">Указывает имя ресурса ресурса, который этот командлет вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="58ccf-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="58ccf-150">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="58ccf-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="58ccf-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="58ccf-151">-ResourceType</span></span>
<span data-ttu-id="58ccf-152">Указывает тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="58ccf-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="58ccf-153">Например, для базы данных тип ресурса выглядит следующим образом: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="58ccf-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="58ccf-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="58ccf-154">-TenantLevel</span></span>
<span data-ttu-id="58ccf-155">Указывает на то, что этот командлет работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="58ccf-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="58ccf-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="58ccf-156">-Confirm</span></span>
<span data-ttu-id="58ccf-157">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="58ccf-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58ccf-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58ccf-158">-WhatIf</span></span>
<span data-ttu-id="58ccf-159">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="58ccf-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="58ccf-160">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="58ccf-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58ccf-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ccf-161">CommonParameters</span></span>
<span data-ttu-id="58ccf-162">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58ccf-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ccf-163">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58ccf-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ccf-164">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58ccf-164">INPUTS</span></span>

### <span data-ttu-id="58ccf-165">System. String</span><span class="sxs-lookup"><span data-stu-id="58ccf-165">System.String</span></span>

## <span data-ttu-id="58ccf-166">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58ccf-166">OUTPUTS</span></span>

### <span data-ttu-id="58ccf-167">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="58ccf-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="58ccf-168">Пуск</span><span class="sxs-lookup"><span data-stu-id="58ccf-168">NOTES</span></span>

## <span data-ttu-id="58ccf-169">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58ccf-169">RELATED LINKS</span></span>
