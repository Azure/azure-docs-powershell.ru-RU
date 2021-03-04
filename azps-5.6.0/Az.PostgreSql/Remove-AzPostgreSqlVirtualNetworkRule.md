---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/powershell/module/az.postgresql/remove-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Remove-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: 9dffbd1feebc2813450293ef3d0a2ae640a3f305
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953624"
---
# <span data-ttu-id="9df16-101">Remove-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9df16-101">Remove-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="9df16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9df16-102">SYNOPSIS</span></span>
<span data-ttu-id="9df16-103">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="9df16-103">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="9df16-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9df16-104">SYNTAX</span></span>

### <span data-ttu-id="9df16-105">Delete (По умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9df16-105">Delete (Default)</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9df16-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9df16-106">DeleteViaIdentity</span></span>
```
Remove-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9df16-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9df16-107">DESCRIPTION</span></span>
<span data-ttu-id="9df16-108">Удаляет правило виртуальной сети с заданным именем.</span><span class="sxs-lookup"><span data-stu-id="9df16-108">Deletes the virtual network rule with the given name.</span></span>

## <span data-ttu-id="9df16-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9df16-109">EXAMPLES</span></span>

### <span data-ttu-id="9df16-110">Пример 1. Удаление правила виртуальной сети PostgreSql server по имени</span><span class="sxs-lookup"><span data-stu-id="9df16-110">Example 1: Remove PostgreSql server Virtual Network Rule by name</span></span>
```powershell
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

```

<span data-ttu-id="9df16-111">Этот cmdlet removes PostgreSql server Virtual Network Rule by name.</span><span class="sxs-lookup"><span data-stu-id="9df16-111">This cmdlet removes PostgreSql server Virtual Network Rule by name.</span></span>

### <span data-ttu-id="9df16-112">Пример 2. Удаление правила виртуальной сети PostgreSql server по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="9df16-112">Example 2: Remove PostgreSql server Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Remove-AzPostgreSqlVirtualNetworkRule -InputObject $ID
 
```

<span data-ttu-id="9df16-113">Эти cmdlets remove PostgreSql server Virtual Network Rule by identity.</span><span class="sxs-lookup"><span data-stu-id="9df16-113">These cmdlets remove PostgreSql server Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="9df16-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9df16-114">PARAMETERS</span></span>

### <span data-ttu-id="9df16-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9df16-115">-AsJob</span></span>
<span data-ttu-id="9df16-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="9df16-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9df16-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9df16-117">-DefaultProfile</span></span>
<span data-ttu-id="9df16-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9df16-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9df16-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9df16-119">-InputObject</span></span>
<span data-ttu-id="9df16-120">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="9df16-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9df16-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9df16-121">-Name</span></span>
<span data-ttu-id="9df16-122">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="9df16-122">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9df16-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9df16-123">-NoWait</span></span>
<span data-ttu-id="9df16-124">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="9df16-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9df16-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9df16-125">-PassThru</span></span>
<span data-ttu-id="9df16-126">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="9df16-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9df16-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9df16-127">-ResourceGroupName</span></span>
<span data-ttu-id="9df16-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9df16-128">The name of the resource group.</span></span>
<span data-ttu-id="9df16-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="9df16-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="9df16-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="9df16-130">-ServerName</span></span>
<span data-ttu-id="9df16-131">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9df16-131">The name of the server.</span></span>

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

### <span data-ttu-id="9df16-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9df16-132">-SubscriptionId</span></span>
<span data-ttu-id="9df16-133">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9df16-133">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="9df16-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9df16-134">-Confirm</span></span>
<span data-ttu-id="9df16-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9df16-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9df16-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9df16-136">-WhatIf</span></span>
<span data-ttu-id="9df16-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9df16-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9df16-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9df16-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9df16-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9df16-139">CommonParameters</span></span>
<span data-ttu-id="9df16-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9df16-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9df16-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9df16-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9df16-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9df16-142">INPUTS</span></span>

### <span data-ttu-id="9df16-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="9df16-143">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="9df16-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9df16-144">OUTPUTS</span></span>

### <span data-ttu-id="9df16-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9df16-145">System.Boolean</span></span>

## <span data-ttu-id="9df16-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9df16-146">NOTES</span></span>

<span data-ttu-id="9df16-147">ALIASES</span><span class="sxs-lookup"><span data-stu-id="9df16-147">ALIASES</span></span>

<span data-ttu-id="9df16-148">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="9df16-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9df16-149">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="9df16-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9df16-150">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9df16-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9df16-151">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="9df16-151">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9df16-152">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="9df16-152">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="9df16-153">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="9df16-153">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="9df16-154">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="9df16-154">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="9df16-155">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="9df16-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9df16-156">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="9df16-156">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="9df16-157">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9df16-157">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="9df16-158">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="9df16-158">The name is case insensitive.</span></span>
  - <span data-ttu-id="9df16-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="9df16-159">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="9df16-160">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="9df16-160">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="9df16-161">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="9df16-161">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="9df16-162">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="9df16-162">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="9df16-163">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9df16-163">RELATED LINKS</span></span>

