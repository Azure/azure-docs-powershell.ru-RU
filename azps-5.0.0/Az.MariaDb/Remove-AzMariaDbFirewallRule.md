---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248641"
---
# <span data-ttu-id="95ca1-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="95ca1-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="95ca1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95ca1-102">SYNOPSIS</span></span>
<span data-ttu-id="95ca1-103">Удаляет правило брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="95ca1-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="95ca1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95ca1-104">SYNTAX</span></span>

### <span data-ttu-id="95ca1-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="95ca1-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="95ca1-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="95ca1-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="95ca1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95ca1-107">DESCRIPTION</span></span>
<span data-ttu-id="95ca1-108">Удаляет правило брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="95ca1-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="95ca1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95ca1-109">EXAMPLES</span></span>

### <span data-ttu-id="95ca1-110">Пример 1: Удаление правила брандмауэра в MariaDB</span><span class="sxs-lookup"><span data-stu-id="95ca1-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="95ca1-111">Эта команда удаляет правило брандмауэра в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="95ca1-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="95ca1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95ca1-112">PARAMETERS</span></span>

### <span data-ttu-id="95ca1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="95ca1-113">-AsJob</span></span>
<span data-ttu-id="95ca1-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="95ca1-114">Run the command as a job</span></span>

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

### <span data-ttu-id="95ca1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95ca1-115">-DefaultProfile</span></span>
<span data-ttu-id="95ca1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95ca1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95ca1-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="95ca1-117">-InputObject</span></span>
<span data-ttu-id="95ca1-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="95ca1-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95ca1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95ca1-119">-Name</span></span>
<span data-ttu-id="95ca1-120">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="95ca1-120">The name of the server firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: FirewallRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ca1-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="95ca1-121">-NoWait</span></span>
<span data-ttu-id="95ca1-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="95ca1-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="95ca1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="95ca1-123">-PassThru</span></span>
<span data-ttu-id="95ca1-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="95ca1-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="95ca1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="95ca1-125">-ResourceGroupName</span></span>
<span data-ttu-id="95ca1-126">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="95ca1-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="95ca1-127">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="95ca1-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ca1-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="95ca1-128">-ServerName</span></span>
<span data-ttu-id="95ca1-129">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="95ca1-129">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ca1-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="95ca1-130">-SubscriptionId</span></span>
<span data-ttu-id="95ca1-131">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="95ca1-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="95ca1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="95ca1-132">-Confirm</span></span>
<span data-ttu-id="95ca1-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="95ca1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="95ca1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="95ca1-134">-WhatIf</span></span>
<span data-ttu-id="95ca1-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="95ca1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="95ca1-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="95ca1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="95ca1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95ca1-137">CommonParameters</span></span>
<span data-ttu-id="95ca1-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95ca1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95ca1-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95ca1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95ca1-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95ca1-140">INPUTS</span></span>

### <span data-ttu-id="95ca1-141">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="95ca1-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="95ca1-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95ca1-142">OUTPUTS</span></span>

### <span data-ttu-id="95ca1-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="95ca1-143">System.Boolean</span></span>

## <span data-ttu-id="95ca1-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="95ca1-144">NOTES</span></span>

<span data-ttu-id="95ca1-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="95ca1-145">ALIASES</span></span>

<span data-ttu-id="95ca1-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="95ca1-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="95ca1-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="95ca1-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="95ca1-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="95ca1-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="95ca1-149">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="95ca1-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="95ca1-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="95ca1-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="95ca1-151">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="95ca1-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="95ca1-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="95ca1-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="95ca1-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="95ca1-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="95ca1-154">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="95ca1-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="95ca1-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="95ca1-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="95ca1-156">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="95ca1-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="95ca1-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="95ca1-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="95ca1-158">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="95ca1-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="95ca1-159">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="95ca1-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="95ca1-160">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="95ca1-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="95ca1-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95ca1-161">RELATED LINKS</span></span>
