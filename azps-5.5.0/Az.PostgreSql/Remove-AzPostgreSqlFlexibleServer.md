---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/remove-azpostgresqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlFlexibleServer.md
ms.openlocfilehash: 00ba72ba38cc73f92b0da3c7cdf2f8143a936347
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236260"
---
# <span data-ttu-id="095e8-101">Remove-AzPostgreSqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="095e8-101">Remove-AzPostgreSqlFlexibleServer</span></span>

## <span data-ttu-id="095e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="095e8-102">SYNOPSIS</span></span>
<span data-ttu-id="095e8-103">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="095e8-103">Deletes a server.</span></span>

## <span data-ttu-id="095e8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="095e8-104">SYNTAX</span></span>

### <span data-ttu-id="095e8-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="095e8-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="095e8-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="095e8-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlFlexibleServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="095e8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="095e8-107">DESCRIPTION</span></span>
<span data-ttu-id="095e8-108">Удаляет сервер.</span><span class="sxs-lookup"><span data-stu-id="095e8-108">Deletes a server.</span></span>

## <span data-ttu-id="095e8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="095e8-109">EXAMPLES</span></span>

### <span data-ttu-id="095e8-110">Пример 1. Удаление сервера PostgreSql по имени группы ресурсов и сервера</span><span class="sxs-lookup"><span data-stu-id="095e8-110">Example 1: Remove PostgreSql server by resourceGroup and server name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlFlexibleServer -ResourceGroupName PowershellPostgreSqlTest -Name postgresql-test

```

<span data-ttu-id="095e8-111">Этот cmdlet removes PostgreSql server by resourceGroup и имя сервера.</span><span class="sxs-lookup"><span data-stu-id="095e8-111">This cmdlet removes PostgreSql server by resourceGroup and server name.</span></span>

### <span data-ttu-id="095e8-112">Пример 2. Удаление сервера PostgreSql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="095e8-112">Example 2: Remove PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellPostgreSqlTest/providers/Microsoft.DBForPostgreSql/flexibleServers/postgresql-test"
PS C:\> Remove-AzPostgreSqlFlexibleServer -InputObject $ID
 
```

<span data-ttu-id="095e8-113">Эти cmdlets remove PostgreSql server by identity.</span><span class="sxs-lookup"><span data-stu-id="095e8-113">These cmdlets remove PostgreSql server by identity.</span></span>

## <span data-ttu-id="095e8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="095e8-114">PARAMETERS</span></span>

### <span data-ttu-id="095e8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="095e8-115">-AsJob</span></span>
<span data-ttu-id="095e8-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="095e8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="095e8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="095e8-117">-DefaultProfile</span></span>
<span data-ttu-id="095e8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="095e8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="095e8-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="095e8-119">-InputObject</span></span>
<span data-ttu-id="095e8-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="095e8-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="095e8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="095e8-121">-Name</span></span>
<span data-ttu-id="095e8-122">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="095e8-122">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="095e8-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="095e8-123">-NoWait</span></span>
<span data-ttu-id="095e8-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="095e8-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="095e8-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="095e8-125">-PassThru</span></span>
<span data-ttu-id="095e8-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="095e8-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="095e8-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="095e8-127">-ResourceGroupName</span></span>
<span data-ttu-id="095e8-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="095e8-128">The name of the resource group.</span></span>
<span data-ttu-id="095e8-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="095e8-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="095e8-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="095e8-130">-SubscriptionId</span></span>
<span data-ttu-id="095e8-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="095e8-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="095e8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="095e8-132">-Confirm</span></span>
<span data-ttu-id="095e8-133">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="095e8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="095e8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="095e8-134">-WhatIf</span></span>
<span data-ttu-id="095e8-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="095e8-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="095e8-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="095e8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="095e8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="095e8-137">CommonParameters</span></span>
<span data-ttu-id="095e8-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="095e8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="095e8-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="095e8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="095e8-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="095e8-140">INPUTS</span></span>

### <span data-ttu-id="095e8-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="095e8-141">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="095e8-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="095e8-142">OUTPUTS</span></span>

### <span data-ttu-id="095e8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="095e8-143">System.Boolean</span></span>

## <span data-ttu-id="095e8-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="095e8-144">NOTES</span></span>

<span data-ttu-id="095e8-145">ALIASES</span><span class="sxs-lookup"><span data-stu-id="095e8-145">ALIASES</span></span>

<span data-ttu-id="095e8-146">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="095e8-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="095e8-147">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="095e8-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="095e8-148">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="095e8-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="095e8-149">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="095e8-149">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="095e8-150">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="095e8-150">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="095e8-151">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="095e8-151">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="095e8-152">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="095e8-152">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="095e8-153">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="095e8-153">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="095e8-154">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="095e8-154">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="095e8-155">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="095e8-155">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="095e8-156">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="095e8-156">The name is case insensitive.</span></span>
  - <span data-ttu-id="095e8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="095e8-157">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="095e8-158">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="095e8-158">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="095e8-159">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="095e8-159">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="095e8-160">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="095e8-160">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="095e8-161">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="095e8-161">RELATED LINKS</span></span>

