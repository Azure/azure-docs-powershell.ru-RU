---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/start-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Start-AzMySqlFlexibleServer.md
ms.openlocfilehash: 876ee527c896af9a264d514c0b117018e2935d24
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968899"
---
# <span data-ttu-id="3c1b9-101">Start-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="3c1b9-101">Start-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="3c1b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3c1b9-102">SYNOPSIS</span></span>
<span data-ttu-id="3c1b9-103">Запускает сервер.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-103">Starts a server.</span></span>

## <span data-ttu-id="3c1b9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3c1b9-104">SYNTAX</span></span>

### <span data-ttu-id="3c1b9-105">Начало (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3c1b9-105">Start (Default)</span></span>
```
Start-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="3c1b9-106">StartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3c1b9-106">StartViaIdentity</span></span>
```
Start-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3c1b9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3c1b9-107">DESCRIPTION</span></span>
<span data-ttu-id="3c1b9-108">Запускает сервер.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-108">Starts a server.</span></span>

## <span data-ttu-id="3c1b9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3c1b9-109">EXAMPLES</span></span>

### <span data-ttu-id="3c1b9-110">Пример 1. Запуск сервера по имени ресурса</span><span class="sxs-lookup"><span data-stu-id="3c1b9-110">Example 1: Start the server by resource name</span></span>
```powershell
PS C:\> Start-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test
```

<span data-ttu-id="3c1b9-111">Запуск сервера по имени</span><span class="sxs-lookup"><span data-stu-id="3c1b9-111">Start the server by name</span></span>

### <span data-ttu-id="3c1b9-112">Пример 2. Запуск сервера по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="3c1b9-112">Example 2: Start the server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test/start"
PS C:\> Start-AzMySqlFlexibleServer -InputObject $ID
```

<span data-ttu-id="3c1b9-113">Запуск сервера по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="3c1b9-113">Start the server by identity</span></span>

## <span data-ttu-id="3c1b9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3c1b9-114">PARAMETERS</span></span>

### <span data-ttu-id="3c1b9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c1b9-115">-AsJob</span></span>
<span data-ttu-id="3c1b9-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="3c1b9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3c1b9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c1b9-117">-DefaultProfile</span></span>
<span data-ttu-id="3c1b9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3c1b9-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c1b9-119">-InputObject</span></span>
<span data-ttu-id="3c1b9-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: StartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3c1b9-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3c1b9-121">-Name</span></span>
<span data-ttu-id="3c1b9-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1b9-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="3c1b9-123">-NoWait</span></span>
<span data-ttu-id="3c1b9-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="3c1b9-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3c1b9-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c1b9-125">-PassThru</span></span>
<span data-ttu-id="3c1b9-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3c1b9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c1b9-127">-ResourceGroupName</span></span>
<span data-ttu-id="3c1b9-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-128">The name of the resource group.</span></span>
<span data-ttu-id="3c1b9-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1b9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3c1b9-130">-SubscriptionId</span></span>
<span data-ttu-id="3c1b9-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Start
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c1b9-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3c1b9-132">-Confirm</span></span>
<span data-ttu-id="3c1b9-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c1b9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c1b9-134">-WhatIf</span></span>
<span data-ttu-id="3c1b9-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c1b9-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c1b9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c1b9-137">CommonParameters</span></span>
<span data-ttu-id="3c1b9-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c1b9-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3c1b9-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c1b9-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3c1b9-140">INPUTS</span></span>

### <span data-ttu-id="3c1b9-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="3c1b9-141">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="3c1b9-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3c1b9-142">OUTPUTS</span></span>

### <span data-ttu-id="3c1b9-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3c1b9-143">System.Boolean</span></span>

## <span data-ttu-id="3c1b9-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3c1b9-144">NOTES</span></span>

<span data-ttu-id="3c1b9-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="3c1b9-145">ALIASES</span></span>

<span data-ttu-id="3c1b9-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="3c1b9-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3c1b9-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3c1b9-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3c1b9-149">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="3c1b9-149">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3c1b9-150">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="3c1b9-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="3c1b9-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="3c1b9-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="3c1b9-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3c1b9-154">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-154">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="3c1b9-155">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-155">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="3c1b9-156">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-156">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="3c1b9-157">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-157">The name is case insensitive.</span></span>
  - <span data-ttu-id="3c1b9-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-158">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="3c1b9-159">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-159">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="3c1b9-160">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-160">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="3c1b9-161">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="3c1b9-161">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="3c1b9-162">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3c1b9-162">RELATED LINKS</span></span>

