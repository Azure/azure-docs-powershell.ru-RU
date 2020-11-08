---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248898"
---
# <span data-ttu-id="ac334-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="ac334-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="ac334-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ac334-102">SYNOPSIS</span></span>
<span data-ttu-id="ac334-103">Перезапускает сервер.</span><span class="sxs-lookup"><span data-stu-id="ac334-103">Restarts a server.</span></span>

## <span data-ttu-id="ac334-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ac334-104">SYNTAX</span></span>

### <span data-ttu-id="ac334-105">ServerName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ac334-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="ac334-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="ac334-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ac334-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac334-107">DESCRIPTION</span></span>
<span data-ttu-id="ac334-108">Перезапускает сервер.</span><span class="sxs-lookup"><span data-stu-id="ac334-108">Restarts a server.</span></span>

## <span data-ttu-id="ac334-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ac334-109">EXAMPLES</span></span>

### <span data-ttu-id="ac334-110">Пример 1: перезапуск MariaDB</span><span class="sxs-lookup"><span data-stu-id="ac334-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="ac334-111">Эта команда перезапустите MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ac334-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="ac334-112">Пример 2: перезапуск MariaDB</span><span class="sxs-lookup"><span data-stu-id="ac334-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="ac334-113">Эта команда перезапустите MariaDB.</span><span class="sxs-lookup"><span data-stu-id="ac334-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="ac334-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ac334-114">PARAMETERS</span></span>

### <span data-ttu-id="ac334-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac334-115">-AsJob</span></span>
<span data-ttu-id="ac334-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="ac334-116">Run the command as a job</span></span>

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

### <span data-ttu-id="ac334-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac334-117">-DefaultProfile</span></span>
<span data-ttu-id="ac334-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ac334-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac334-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac334-119">-InputObject</span></span>
<span data-ttu-id="ac334-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="ac334-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: ServerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac334-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ac334-121">-Name</span></span>
<span data-ttu-id="ac334-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ac334-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac334-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="ac334-123">-NoWait</span></span>
<span data-ttu-id="ac334-124">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="ac334-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ac334-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac334-125">-PassThru</span></span>
<span data-ttu-id="ac334-126">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="ac334-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="ac334-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac334-127">-ResourceGroupName</span></span>
<span data-ttu-id="ac334-128">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="ac334-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="ac334-129">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ac334-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac334-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ac334-130">-SubscriptionId</span></span>
<span data-ttu-id="ac334-131">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="ac334-131">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ServerName
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac334-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac334-132">-Confirm</span></span>
<span data-ttu-id="ac334-133">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ac334-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac334-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac334-134">-WhatIf</span></span>
<span data-ttu-id="ac334-135">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ac334-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac334-136">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ac334-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac334-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac334-137">CommonParameters</span></span>
<span data-ttu-id="ac334-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ac334-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac334-139">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac334-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac334-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ac334-140">INPUTS</span></span>

### <span data-ttu-id="ac334-141">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="ac334-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="ac334-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ac334-142">OUTPUTS</span></span>

### <span data-ttu-id="ac334-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ac334-143">System.Boolean</span></span>

## <span data-ttu-id="ac334-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="ac334-144">NOTES</span></span>

<span data-ttu-id="ac334-145">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="ac334-145">ALIASES</span></span>

<span data-ttu-id="ac334-146">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="ac334-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ac334-147">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="ac334-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ac334-148">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ac334-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ac334-149">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="ac334-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ac334-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="ac334-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="ac334-151">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="ac334-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="ac334-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="ac334-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="ac334-153">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="ac334-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ac334-154">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="ac334-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="ac334-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="ac334-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="ac334-156">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="ac334-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="ac334-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="ac334-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="ac334-158">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="ac334-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="ac334-159">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="ac334-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="ac334-160">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="ac334-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="ac334-161">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ac334-161">RELATED LINKS</span></span>

