---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/remove-azmariadbfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Remove-AzMariaDbFirewallRule.md
ms.openlocfilehash: 7775c4adeef0ce4b05efa2b54c6484408256f3eb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079554"
---
# <span data-ttu-id="0f7f6-101">Remove-AzMariaDbFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0f7f6-101">Remove-AzMariaDbFirewallRule</span></span>

## <span data-ttu-id="0f7f6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0f7f6-102">SYNOPSIS</span></span>
<span data-ttu-id="0f7f6-103">Удаляет правило брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-103">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="0f7f6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0f7f6-104">SYNTAX</span></span>

### <span data-ttu-id="0f7f6-105">Удалить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0f7f6-105">Delete (Default)</span></span>
```
Remove-AzMariaDbFirewallRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="0f7f6-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0f7f6-106">DeleteViaIdentity</span></span>
```
Remove-AzMariaDbFirewallRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0f7f6-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f7f6-107">DESCRIPTION</span></span>
<span data-ttu-id="0f7f6-108">Удаляет правило брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-108">Deletes a server firewall rule.</span></span>

## <span data-ttu-id="0f7f6-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0f7f6-109">EXAMPLES</span></span>

### <span data-ttu-id="0f7f6-110">Пример 1: Удаление правила брандмауэра в MariaDB</span><span class="sxs-lookup"><span data-stu-id="0f7f6-110">Example 1: Remove a firewall rule under a MariaDB</span></span>
```powershell
PS C:\> Remove-AzMariaDbFirewallRule -Name frname-001 -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-4rmtig

```

<span data-ttu-id="0f7f6-111">Эта команда удаляет правило брандмауэра в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-111">This command removes a firewall rule under a MariaDB.</span></span>

## <span data-ttu-id="0f7f6-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0f7f6-112">PARAMETERS</span></span>

### <span data-ttu-id="0f7f6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f7f6-113">-AsJob</span></span>
<span data-ttu-id="0f7f6-114">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0f7f6-114">Run the command as a job</span></span>

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

### <span data-ttu-id="0f7f6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f7f6-115">-DefaultProfile</span></span>
<span data-ttu-id="0f7f6-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f7f6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f7f6-117">-InputObject</span></span>
<span data-ttu-id="0f7f6-118">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0f7f6-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0f7f6-119">-Name</span></span>
<span data-ttu-id="0f7f6-120">Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-120">The name of the server firewall rule.</span></span>

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

### <span data-ttu-id="0f7f6-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="0f7f6-121">-NoWait</span></span>
<span data-ttu-id="0f7f6-122">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="0f7f6-122">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0f7f6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f7f6-123">-PassThru</span></span>
<span data-ttu-id="0f7f6-124">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-124">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0f7f6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f7f6-125">-ResourceGroupName</span></span>
<span data-ttu-id="0f7f6-126">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="0f7f6-127">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="0f7f6-128">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="0f7f6-128">-ServerName</span></span>
<span data-ttu-id="0f7f6-129">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-129">The name of the server.</span></span>

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

### <span data-ttu-id="0f7f6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0f7f6-130">-SubscriptionId</span></span>
<span data-ttu-id="0f7f6-131">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="0f7f6-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f7f6-132">-Confirm</span></span>
<span data-ttu-id="0f7f6-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f7f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f7f6-134">-WhatIf</span></span>
<span data-ttu-id="0f7f6-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f7f6-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f7f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f7f6-137">CommonParameters</span></span>
<span data-ttu-id="0f7f6-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f7f6-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f7f6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f7f6-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0f7f6-140">INPUTS</span></span>

### <span data-ttu-id="0f7f6-141">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="0f7f6-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="0f7f6-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0f7f6-142">OUTPUTS</span></span>

### <span data-ttu-id="0f7f6-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0f7f6-143">System.Boolean</span></span>

## <span data-ttu-id="0f7f6-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="0f7f6-144">NOTES</span></span>

<span data-ttu-id="0f7f6-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="0f7f6-145">ALIASES</span></span>

<span data-ttu-id="0f7f6-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0f7f6-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0f7f6-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0f7f6-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0f7f6-149">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="0f7f6-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0f7f6-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0f7f6-151">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0f7f6-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0f7f6-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="0f7f6-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0f7f6-154">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0f7f6-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="0f7f6-156">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="0f7f6-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0f7f6-158">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0f7f6-159">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="0f7f6-160">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0f7f6-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0f7f6-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0f7f6-161">RELATED LINKS</span></span>

