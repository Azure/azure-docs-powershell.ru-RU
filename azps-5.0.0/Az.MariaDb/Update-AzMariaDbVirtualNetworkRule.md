---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/update-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Update-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 9ec9113ba17ec28e7cef934a4b857e4cbf0acce0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94250089"
---
# <span data-ttu-id="4c0cf-101">Update-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4c0cf-101">Update-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="4c0cf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4c0cf-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0cf-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="4c0cf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4c0cf-104">SYNTAX</span></span>

### <span data-ttu-id="4c0cf-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4c0cf-105">UpdateExpanded (Default)</span></span>
```
Update-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint] [-SubnetId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4c0cf-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4c0cf-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-IgnoreMissingVnetServiceEndpoint]
 [-SubnetId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="4c0cf-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c0cf-107">DESCRIPTION</span></span>
<span data-ttu-id="4c0cf-108">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="4c0cf-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4c0cf-109">EXAMPLES</span></span>

### <span data-ttu-id="4c0cf-110">Пример 1: обновление правила виртуальной сети MariaDB</span><span class="sxs-lookup"><span data-stu-id="4c0cf-110">Example 1: Update MariaDB virtual network rule</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name vnet -ResourceGroupName mariadb-test-qu5ov0
PS C:\> Update-AzMariaDbVirtualNetworkRule -ServerName mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 -Name vnetrule-QdMJpU -SubnetId $vnet.Subnets[0].Id -IgnoreMissingVnetServiceEndpoint

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="4c0cf-111">Эта команда обновляет правило виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-111">This command updates a virtual network rule.</span></span>

## <span data-ttu-id="4c0cf-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4c0cf-112">PARAMETERS</span></span>

### <span data-ttu-id="4c0cf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4c0cf-113">-AsJob</span></span>
<span data-ttu-id="4c0cf-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="4c0cf-114">Run the command as a job</span></span>

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

### <span data-ttu-id="4c0cf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0cf-115">-DefaultProfile</span></span>
<span data-ttu-id="4c0cf-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0cf-117">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="4c0cf-117">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="4c0cf-118">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-118">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="4c0cf-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c0cf-119">-InputObject</span></span>
<span data-ttu-id="4c0cf-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0cf-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4c0cf-121">-Name</span></span>
<span data-ttu-id="4c0cf-122">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0cf-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="4c0cf-123">-NoWait</span></span>
<span data-ttu-id="4c0cf-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="4c0cf-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4c0cf-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c0cf-125">-PassThru</span></span>
<span data-ttu-id="4c0cf-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4c0cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c0cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="4c0cf-128">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4c0cf-129">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0cf-130">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="4c0cf-130">-ServerName</span></span>
<span data-ttu-id="4c0cf-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-131">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0cf-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="4c0cf-132">-SubnetId</span></span>
<span data-ttu-id="4c0cf-133">Идентификатор ресурса ARM для подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-133">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="4c0cf-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4c0cf-134">-SubscriptionId</span></span>
<span data-ttu-id="4c0cf-135">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-135">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0cf-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4c0cf-136">-Confirm</span></span>
<span data-ttu-id="4c0cf-137">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0cf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c0cf-138">-WhatIf</span></span>
<span data-ttu-id="4c0cf-139">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c0cf-140">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-140">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c0cf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0cf-141">CommonParameters</span></span>
<span data-ttu-id="4c0cf-142">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0cf-143">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c0cf-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0cf-144">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4c0cf-144">INPUTS</span></span>

### <span data-ttu-id="4c0cf-145">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="4c0cf-145">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="4c0cf-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4c0cf-146">OUTPUTS</span></span>

### <span data-ttu-id="4c0cf-147">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="4c0cf-147">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="4c0cf-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="4c0cf-148">NOTES</span></span>

<span data-ttu-id="4c0cf-149">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="4c0cf-149">ALIASES</span></span>

<span data-ttu-id="4c0cf-150">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4c0cf-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4c0cf-151">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4c0cf-152">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4c0cf-153">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="4c0cf-153">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4c0cf-154">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-154">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4c0cf-155">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-155">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4c0cf-156">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-156">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4c0cf-157">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="4c0cf-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4c0cf-158">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-158">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4c0cf-159">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-159">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4c0cf-160">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-160">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4c0cf-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-161">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4c0cf-162">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-162">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4c0cf-163">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-163">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="4c0cf-164">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="4c0cf-164">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4c0cf-165">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4c0cf-165">RELATED LINKS</span></span>
