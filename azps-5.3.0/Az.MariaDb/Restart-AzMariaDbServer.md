---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: 19a2c0f8638d74f47acb9d639a8de9275667155a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507124"
---
# <span data-ttu-id="fcf6c-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="fcf6c-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="fcf6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcf6c-102">SYNOPSIS</span></span>
<span data-ttu-id="fcf6c-103">Перезапуск сервера.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-103">Restarts a server.</span></span>

## <span data-ttu-id="fcf6c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fcf6c-104">SYNTAX</span></span>

### <span data-ttu-id="fcf6c-105">Имя Сервера (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fcf6c-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="fcf6c-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="fcf6c-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fcf6c-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fcf6c-107">DESCRIPTION</span></span>
<span data-ttu-id="fcf6c-108">Перезапуск сервера.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-108">Restarts a server.</span></span>

## <span data-ttu-id="fcf6c-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fcf6c-109">EXAMPLES</span></span>

### <span data-ttu-id="fcf6c-110">Пример 1. Перезапуск Приложения MariaDB</span><span class="sxs-lookup"><span data-stu-id="fcf6c-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="fcf6c-111">Эта команда перезапустит MariaDB.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="fcf6c-112">Пример 2. Перезапуск Приложения MariaDB</span><span class="sxs-lookup"><span data-stu-id="fcf6c-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="fcf6c-113">Эта команда перезапустит MariaDB.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="fcf6c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fcf6c-114">PARAMETERS</span></span>

### <span data-ttu-id="fcf6c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fcf6c-115">-AsJob</span></span>
<span data-ttu-id="fcf6c-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="fcf6c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="fcf6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcf6c-117">-DefaultProfile</span></span>
<span data-ttu-id="fcf6c-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcf6c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fcf6c-119">-InputObject</span></span>
<span data-ttu-id="fcf6c-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="fcf6c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="fcf6c-121">-Name</span></span>
<span data-ttu-id="fcf6c-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-122">The name of the server.</span></span>

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

### <span data-ttu-id="fcf6c-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fcf6c-123">-NoWait</span></span>
<span data-ttu-id="fcf6c-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="fcf6c-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fcf6c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcf6c-125">-PassThru</span></span>
<span data-ttu-id="fcf6c-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="fcf6c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcf6c-127">-ResourceGroupName</span></span>
<span data-ttu-id="fcf6c-128">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fcf6c-129">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fcf6c-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fcf6c-130">-SubscriptionId</span></span>
<span data-ttu-id="fcf6c-131">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="fcf6c-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fcf6c-132">-Confirm</span></span>
<span data-ttu-id="fcf6c-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcf6c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcf6c-134">-WhatIf</span></span>
<span data-ttu-id="fcf6c-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fcf6c-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcf6c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcf6c-137">CommonParameters</span></span>
<span data-ttu-id="fcf6c-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcf6c-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fcf6c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcf6c-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fcf6c-140">INPUTS</span></span>

### <span data-ttu-id="fcf6c-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="fcf6c-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="fcf6c-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fcf6c-142">OUTPUTS</span></span>

### <span data-ttu-id="fcf6c-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="fcf6c-143">System.Boolean</span></span>

## <span data-ttu-id="fcf6c-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fcf6c-144">NOTES</span></span>

<span data-ttu-id="fcf6c-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="fcf6c-145">ALIASES</span></span>

<span data-ttu-id="fcf6c-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="fcf6c-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fcf6c-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fcf6c-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fcf6c-149">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="fcf6c-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="fcf6c-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="fcf6c-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="fcf6c-152">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="fcf6c-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="fcf6c-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="fcf6c-154">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="fcf6c-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="fcf6c-156">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="fcf6c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="fcf6c-158">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="fcf6c-159">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="fcf6c-160">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="fcf6c-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="fcf6c-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fcf6c-161">RELATED LINKS</span></span>

