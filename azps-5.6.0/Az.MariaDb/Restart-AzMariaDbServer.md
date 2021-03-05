---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/restart-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Restart-AzMariaDbServer.md
ms.openlocfilehash: e8367638f2bcfcf54f0b3183180f2ab8d70b3ffc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003923"
---
# <span data-ttu-id="2a504-101">Restart-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="2a504-101">Restart-AzMariaDbServer</span></span>

## <span data-ttu-id="2a504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a504-102">SYNOPSIS</span></span>
<span data-ttu-id="2a504-103">Перезапуск сервера.</span><span class="sxs-lookup"><span data-stu-id="2a504-103">Restarts a server.</span></span>

## <span data-ttu-id="2a504-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2a504-104">SYNTAX</span></span>

### <span data-ttu-id="2a504-105">Имя Сервера (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2a504-105">ServerName (Default)</span></span>
```
Restart-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2a504-106">ServerObject</span><span class="sxs-lookup"><span data-stu-id="2a504-106">ServerObject</span></span>
```
Restart-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2a504-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2a504-107">DESCRIPTION</span></span>
<span data-ttu-id="2a504-108">Перезапуск сервера.</span><span class="sxs-lookup"><span data-stu-id="2a504-108">Restarts a server.</span></span>

## <span data-ttu-id="2a504-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2a504-109">EXAMPLES</span></span>

### <span data-ttu-id="2a504-110">Пример 1. Перезапуск Приложения MariaDB</span><span class="sxs-lookup"><span data-stu-id="2a504-110">Example 1: Restart a MariaDB</span></span>
```powershell
PS C:\> Restart-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0

```

<span data-ttu-id="2a504-111">Эта команда перезапустит MariaDB.</span><span class="sxs-lookup"><span data-stu-id="2a504-111">This command restart a MariaDB.</span></span>

### <span data-ttu-id="2a504-112">Пример 2. Перезапуск Приложения MariaDB</span><span class="sxs-lookup"><span data-stu-id="2a504-112">Example 2: Restart a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -Name mariadb-test-9pebvn -ResourceGroupName mariadb-test-qu5ov0 | Restart-AzMariaDbServer

```

<span data-ttu-id="2a504-113">Эта команда перезапустит MariaDB.</span><span class="sxs-lookup"><span data-stu-id="2a504-113">This command restart a MariaDB.</span></span>

## <span data-ttu-id="2a504-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a504-114">PARAMETERS</span></span>

### <span data-ttu-id="2a504-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2a504-115">-AsJob</span></span>
<span data-ttu-id="2a504-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="2a504-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2a504-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a504-117">-DefaultProfile</span></span>
<span data-ttu-id="2a504-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2a504-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a504-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2a504-119">-InputObject</span></span>
<span data-ttu-id="2a504-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="2a504-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2a504-121">-Name</span><span class="sxs-lookup"><span data-stu-id="2a504-121">-Name</span></span>
<span data-ttu-id="2a504-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2a504-122">The name of the server.</span></span>

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

### <span data-ttu-id="2a504-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2a504-123">-NoWait</span></span>
<span data-ttu-id="2a504-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="2a504-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2a504-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a504-125">-PassThru</span></span>
<span data-ttu-id="2a504-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="2a504-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2a504-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a504-127">-ResourceGroupName</span></span>
<span data-ttu-id="2a504-128">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="2a504-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="2a504-129">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="2a504-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="2a504-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2a504-130">-SubscriptionId</span></span>
<span data-ttu-id="2a504-131">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="2a504-131">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="2a504-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2a504-132">-Confirm</span></span>
<span data-ttu-id="2a504-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a504-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a504-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a504-134">-WhatIf</span></span>
<span data-ttu-id="2a504-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a504-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a504-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2a504-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a504-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a504-137">CommonParameters</span></span>
<span data-ttu-id="2a504-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a504-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a504-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2a504-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a504-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2a504-140">INPUTS</span></span>

### <span data-ttu-id="2a504-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="2a504-141">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="2a504-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2a504-142">OUTPUTS</span></span>

### <span data-ttu-id="2a504-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="2a504-143">System.Boolean</span></span>

## <span data-ttu-id="2a504-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2a504-144">NOTES</span></span>

<span data-ttu-id="2a504-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2a504-145">ALIASES</span></span>

<span data-ttu-id="2a504-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="2a504-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2a504-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="2a504-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2a504-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2a504-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2a504-149">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="2a504-149">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2a504-150">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="2a504-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="2a504-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="2a504-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="2a504-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="2a504-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="2a504-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="2a504-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2a504-154">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="2a504-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="2a504-155">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="2a504-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="2a504-156">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="2a504-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="2a504-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="2a504-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="2a504-158">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="2a504-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="2a504-159">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="2a504-159">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="2a504-160">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="2a504-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="2a504-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2a504-161">RELATED LINKS</span></span>

