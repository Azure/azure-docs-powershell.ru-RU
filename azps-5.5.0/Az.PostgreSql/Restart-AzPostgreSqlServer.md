---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/restart-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Restart-AzPostgreSqlServer.md
ms.openlocfilehash: aa5e58522aaeb1094ef2a7280b33b45e20fe03fc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100213156"
---
# <span data-ttu-id="cc5ca-101">Restart-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="cc5ca-101">Restart-AzPostgreSqlServer</span></span>

## <span data-ttu-id="cc5ca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc5ca-102">SYNOPSIS</span></span>
<span data-ttu-id="cc5ca-103">Перезапуск сервера.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-103">Restarts a server.</span></span>

## <span data-ttu-id="cc5ca-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc5ca-104">SYNTAX</span></span>

### <span data-ttu-id="cc5ca-105">Перезапуск (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc5ca-105">Restart (Default)</span></span>
```
Restart-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cc5ca-106">RestartViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cc5ca-106">RestartViaIdentity</span></span>
```
Restart-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cc5ca-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc5ca-107">DESCRIPTION</span></span>
<span data-ttu-id="cc5ca-108">Перезапуск сервера.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-108">Restarts a server.</span></span>

## <span data-ttu-id="cc5ca-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc5ca-109">EXAMPLES</span></span>

### <span data-ttu-id="cc5ca-110">Пример 1. Перезапуск сервера PostgreSql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="cc5ca-110">Example 1: Restart PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Restart-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

```

<span data-ttu-id="cc5ca-111">Этот cmdlet перезапустит сервер PostgreSql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-111">This cmdlet restarts PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="cc5ca-112">Пример 2. Перезапуск сервера PostgreSql с помощью удостоверений</span><span class="sxs-lookup"><span data-stu-id="cc5ca-112">Example 2: Restart PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/restart"
PS C:\> Restart-AzPostgreSqlServer -InputObject $ID
 
```

<span data-ttu-id="cc5ca-113">Эти cmdlets перезапустят сервер PostgreSql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-113">These cmdlets restart PostgreSql server by identity.</span></span>

## <span data-ttu-id="cc5ca-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc5ca-114">PARAMETERS</span></span>

### <span data-ttu-id="cc5ca-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc5ca-115">-AsJob</span></span>
<span data-ttu-id="cc5ca-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="cc5ca-116">Run the command as a job</span></span>

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

### <span data-ttu-id="cc5ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc5ca-117">-DefaultProfile</span></span>
<span data-ttu-id="cc5ca-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc5ca-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc5ca-119">-InputObject</span></span>
<span data-ttu-id="cc5ca-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: RestartViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc5ca-121">-Name</span><span class="sxs-lookup"><span data-stu-id="cc5ca-121">-Name</span></span>
<span data-ttu-id="cc5ca-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5ca-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="cc5ca-123">-NoWait</span></span>
<span data-ttu-id="cc5ca-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="cc5ca-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="cc5ca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc5ca-125">-PassThru</span></span>
<span data-ttu-id="cc5ca-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cc5ca-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc5ca-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc5ca-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-128">The name of the resource group.</span></span>
<span data-ttu-id="cc5ca-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-129">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5ca-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cc5ca-130">-SubscriptionId</span></span>
<span data-ttu-id="cc5ca-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Restart
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc5ca-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc5ca-132">-Confirm</span></span>
<span data-ttu-id="cc5ca-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc5ca-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc5ca-134">-WhatIf</span></span>
<span data-ttu-id="cc5ca-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc5ca-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc5ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc5ca-137">CommonParameters</span></span>
<span data-ttu-id="cc5ca-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc5ca-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc5ca-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc5ca-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc5ca-140">INPUTS</span></span>

### <span data-ttu-id="cc5ca-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="cc5ca-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="cc5ca-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc5ca-142">OUTPUTS</span></span>

### <span data-ttu-id="cc5ca-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc5ca-143">System.Boolean</span></span>

## <span data-ttu-id="cc5ca-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc5ca-144">NOTES</span></span>

<span data-ttu-id="cc5ca-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="cc5ca-145">ALIASES</span></span>

<span data-ttu-id="cc5ca-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="cc5ca-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cc5ca-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc5ca-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cc5ca-149">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="cc5ca-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc5ca-150">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="cc5ca-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="cc5ca-152">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="cc5ca-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="cc5ca-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc5ca-154">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="cc5ca-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="cc5ca-156">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="cc5ca-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="cc5ca-158">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="cc5ca-159">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="cc5ca-160">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="cc5ca-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="cc5ca-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc5ca-161">RELATED LINKS</span></span>

