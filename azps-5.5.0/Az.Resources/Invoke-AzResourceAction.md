---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 427F7300-0FEB-4F28-9C1D-27592AEBF6A0
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/invoke-azresourceaction
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Invoke-AzResourceAction.md
ms.openlocfilehash: 2feb6c48927c1cb5e092414c358b32912892a908
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240064"
---
# <span data-ttu-id="07167-101">Invoke-AzResourceAction</span><span class="sxs-lookup"><span data-stu-id="07167-101">Invoke-AzResourceAction</span></span>

## <span data-ttu-id="07167-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07167-102">SYNOPSIS</span></span>
<span data-ttu-id="07167-103">Вызывает действие для ресурса.</span><span class="sxs-lookup"><span data-stu-id="07167-103">Invokes an action on a resource.</span></span>

## <span data-ttu-id="07167-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="07167-104">SYNTAX</span></span>

### <span data-ttu-id="07167-105">ByResourceId (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07167-105">ByResourceId (Default)</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="07167-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="07167-106">BySubscriptionLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07167-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="07167-107">ByTenantLevel</span></span>
```
Invoke-AzResourceAction [-Parameters <Hashtable>] -Action <String> -ResourceName <String>
 -ResourceType <String> [-ExtensionResourceName <String>] [-ExtensionResourceType <String>]
 [-ODataQuery <String>] [-TenantLevel] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07167-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07167-108">DESCRIPTION</span></span>
<span data-ttu-id="07167-109">**Cmdlet Invoke-AzResourceAction** вызывает действие с указанным ресурсом Azure.</span><span class="sxs-lookup"><span data-stu-id="07167-109">The **Invoke-AzResourceAction** cmdlet invokes an action on a specified Azure resource.</span></span>
<span data-ttu-id="07167-110">Чтобы получить список поддерживаемых действий, используйте средство проводника ресурсов Azure.</span><span class="sxs-lookup"><span data-stu-id="07167-110">To get a list of supported actions, use the Azure Resource Explorer tool.</span></span>

## <span data-ttu-id="07167-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="07167-111">EXAMPLES</span></span>

### <span data-ttu-id="07167-112">Пример 1. Запуск VM с ResourceId</span><span class="sxs-lookup"><span data-stu-id="07167-112">Example 1: Invoke starting a VM with ResourceId</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceId /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.Compute/virtualMachines/testVM -Action start

Confirm
Are you sure you want to invoke the 'start' action on the following resource: /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Compute/virtualMachines/testVM
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```

<span data-ttu-id="07167-113">Эта команда запускает виртуальную машину с {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="07167-113">This command starts the Virtual Machine with {ResourceId}.</span></span>

### <span data-ttu-id="07167-114">Пример 2. Вызов управления VM с помощью названия ресурса</span><span class="sxs-lookup"><span data-stu-id="07167-114">Example 2: Invoke poweroffing a VM with ResourceName</span></span>

```powershell
PS C:\>Invoke-AzResourceAction -ResourceGroupName testGroup -ResourceName testVM -ResourceType Microsoft.Compute/virtualMachines/ -Action Poweroff -Force
```

<span data-ttu-id="07167-115">Эта команда останавливает работу виртуальной машины с {ResourceId}.</span><span class="sxs-lookup"><span data-stu-id="07167-115">This command stops the Virtual Machine with {ResourceId}.</span></span>
<span data-ttu-id="07167-116">Команда указывает параметр *Force,* поэтому запрос на подтверждение не задан.</span><span class="sxs-lookup"><span data-stu-id="07167-116">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

### <span data-ttu-id="07167-117">Пример 3. Вызов регистрации поставщика ресурсов с помощью ResourceId</span><span class="sxs-lookup"><span data-stu-id="07167-117">Example 3: Invoke registering a resource provider with ResourceId</span></span>

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

<span data-ttu-id="07167-118">Эта команда регистрирует поставщика ресурсов Microsoft.Network.</span><span class="sxs-lookup"><span data-stu-id="07167-118">This command registers a resource provider "Microsoft.Network".</span></span>
<span data-ttu-id="07167-119">Команда указывает параметр *Force,* поэтому запрос на подтверждение не задан.</span><span class="sxs-lookup"><span data-stu-id="07167-119">The command specifies the *Force* parameter, therefore, it does not prompt you for confirmation.</span></span>

## <span data-ttu-id="07167-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07167-120">PARAMETERS</span></span>

### <span data-ttu-id="07167-121">-Action</span><span class="sxs-lookup"><span data-stu-id="07167-121">-Action</span></span>
<span data-ttu-id="07167-122">Указывает имя вызываемого действия.</span><span class="sxs-lookup"><span data-stu-id="07167-122">Specifies the name of the action to invoke.</span></span>

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

### <span data-ttu-id="07167-123">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="07167-123">-ApiVersion</span></span>
<span data-ttu-id="07167-124">Определяет версию API поставщика ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07167-124">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="07167-125">Если не указать версию, этот cmdlet использует последнюю доступную версию.</span><span class="sxs-lookup"><span data-stu-id="07167-125">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="07167-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07167-126">-DefaultProfile</span></span>
<span data-ttu-id="07167-127">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="07167-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07167-128">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="07167-128">-ExtensionResourceName</span></span>
<span data-ttu-id="07167-129">Указывает имя ресурса расширения для ресурса, для которого этот cmdlet вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="07167-129">Specifies the name of an extension resource for the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="07167-130">Например, чтобы указать базу данных, используйте следующий формат: имя базы `/` данных "Имя сервера".</span><span class="sxs-lookup"><span data-stu-id="07167-130">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="07167-131">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="07167-131">-ExtensionResourceType</span></span>
<span data-ttu-id="07167-132">Тип ресурса расширения.</span><span class="sxs-lookup"><span data-stu-id="07167-132">Specifies the type of the extension resource.</span></span>
<span data-ttu-id="07167-133">Например: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="07167-133">For instance: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="07167-134">-Force</span><span class="sxs-lookup"><span data-stu-id="07167-134">-Force</span></span>
<span data-ttu-id="07167-135">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="07167-135">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07167-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="07167-136">-ODataQuery</span></span>
<span data-ttu-id="07167-137">Указывает фильтр стилей Open Data Protocol (OData).</span><span class="sxs-lookup"><span data-stu-id="07167-137">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="07167-138">Этот cmdlet добавит это значение к запросу в дополнение к любым другим фильтрам.</span><span class="sxs-lookup"><span data-stu-id="07167-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="07167-139">-Parameters</span><span class="sxs-lookup"><span data-stu-id="07167-139">-Parameters</span></span>
<span data-ttu-id="07167-140">Параметры (в качестве hash table) для действия, вызываемого этим cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07167-140">Specifies parameters, as a hash table, for the action that this cmdlet invokes.</span></span>

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

### <span data-ttu-id="07167-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="07167-141">-Pre</span></span>
<span data-ttu-id="07167-142">Указывает на то, что этот cmdlet рассматривает предварительные версии API при автоматическом определении используемой версии.</span><span class="sxs-lookup"><span data-stu-id="07167-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="07167-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07167-143">-ResourceGroupName</span></span>
<span data-ttu-id="07167-144">Указывает имя группы ресурсов, в которой этот cmdlet вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="07167-144">Specifies the name of a resource group in which this cmdlet invokes an action.</span></span>

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

### <span data-ttu-id="07167-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07167-145">-ResourceId</span></span>
<span data-ttu-id="07167-146">Определяет полностью заданный код ресурса, для которого этот cmdlet вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="07167-146">Specifies the fully qualified resource ID of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="07167-147">ИД включает подписку, как в следующем примере: `/subscriptions/` ИД подписки`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="07167-147">The ID includes the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="07167-148">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="07167-148">-ResourceName</span></span>
<span data-ttu-id="07167-149">Указывает имя ресурса, для которого этот cmdlet вызывает действие.</span><span class="sxs-lookup"><span data-stu-id="07167-149">Specifies the name of the resource of the resource on which this cmdlet invokes an action.</span></span>
<span data-ttu-id="07167-150">Например, чтобы указать базу данных, используйте следующий формат: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="07167-150">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="07167-151">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="07167-151">-ResourceType</span></span>
<span data-ttu-id="07167-152">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="07167-152">Specifies the type of the resource.</span></span>
<span data-ttu-id="07167-153">Например, для базы данных тип ресурса: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="07167-153">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="07167-154">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="07167-154">-TenantLevel</span></span>
<span data-ttu-id="07167-155">Указывает на то, что этот cmdlet работает на уровне клиента.</span><span class="sxs-lookup"><span data-stu-id="07167-155">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="07167-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07167-156">-Confirm</span></span>
<span data-ttu-id="07167-157">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07167-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07167-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07167-158">-WhatIf</span></span>
<span data-ttu-id="07167-159">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07167-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07167-160">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="07167-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07167-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07167-161">CommonParameters</span></span>
<span data-ttu-id="07167-162">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07167-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07167-163">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="07167-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07167-164">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07167-164">INPUTS</span></span>

### <span data-ttu-id="07167-165">System.String</span><span class="sxs-lookup"><span data-stu-id="07167-165">System.String</span></span>

## <span data-ttu-id="07167-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="07167-166">OUTPUTS</span></span>

### <span data-ttu-id="07167-167">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="07167-167">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="07167-168">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="07167-168">NOTES</span></span>

## <span data-ttu-id="07167-169">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07167-169">RELATED LINKS</span></span>
