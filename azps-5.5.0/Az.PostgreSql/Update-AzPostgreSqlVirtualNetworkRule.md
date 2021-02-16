---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/update-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Update-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: a430247083e84b3d35f820b3c1e2d5f04f4979b5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100218041"
---
# <span data-ttu-id="90dfb-101">Update-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="90dfb-101">Update-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="90dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="90dfb-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="90dfb-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="90dfb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="90dfb-104">SYNTAX</span></span>

### <span data-ttu-id="90dfb-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="90dfb-105">UpdateExpanded (Default)</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="90dfb-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="90dfb-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="90dfb-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="90dfb-107">DESCRIPTION</span></span>
<span data-ttu-id="90dfb-108">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="90dfb-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="90dfb-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="90dfb-109">EXAMPLES</span></span>

### <span data-ttu-id="90dfb-110">Пример 1. Обновление правила виртуальной сети PostgreSql по имени</span><span class="sxs-lookup"><span data-stu-id="90dfb-110">Example 1: Update PostgreSql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default2"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="90dfb-111">Этот cmdlet обновляет по имени виртуальное правило сети PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="90dfb-111">This cmdlet updates PostgreSql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="90dfb-112">Пример 2. Обновление виртуальных правил сети PostgreSql с помощью удостоверений.</span><span class="sxs-lookup"><span data-stu-id="90dfb-112">Example 2: Update PostgreSql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.Network/virtualNetworks/PostgreSqlVNet/subnets/default"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Update-AzPostgreSqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="90dfb-113">Эти cmdlets обновляют виртуальное правило сети PostgreSql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="90dfb-113">These cmdlets update PostgreSql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="90dfb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90dfb-114">PARAMETERS</span></span>

### <span data-ttu-id="90dfb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90dfb-115">-AsJob</span></span>
<span data-ttu-id="90dfb-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="90dfb-116">Run the command as a job</span></span>

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

### <span data-ttu-id="90dfb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90dfb-117">-DefaultProfile</span></span>
<span data-ttu-id="90dfb-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="90dfb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90dfb-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="90dfb-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="90dfb-120">Создайте правило брандмауэра до того, как в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="90dfb-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="90dfb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="90dfb-121">-InputObject</span></span>
<span data-ttu-id="90dfb-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="90dfb-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="90dfb-123">-Name</span><span class="sxs-lookup"><span data-stu-id="90dfb-123">-Name</span></span>
<span data-ttu-id="90dfb-124">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="90dfb-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="90dfb-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="90dfb-125">-NoWait</span></span>
<span data-ttu-id="90dfb-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="90dfb-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="90dfb-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90dfb-127">-PassThru</span></span>
<span data-ttu-id="90dfb-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="90dfb-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="90dfb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90dfb-129">-ResourceGroupName</span></span>
<span data-ttu-id="90dfb-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90dfb-130">The name of the resource group.</span></span>
<span data-ttu-id="90dfb-131">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="90dfb-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="90dfb-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90dfb-132">-ServerName</span></span>
<span data-ttu-id="90dfb-133">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="90dfb-133">The name of the server.</span></span>

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

### <span data-ttu-id="90dfb-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="90dfb-134">-SubnetId</span></span>
<span data-ttu-id="90dfb-135">Это ARM ресурса виртуальной подсети сети.</span><span class="sxs-lookup"><span data-stu-id="90dfb-135">The ARM resource id of the virtual network subnet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90dfb-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="90dfb-136">-SubscriptionId</span></span>
<span data-ttu-id="90dfb-137">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="90dfb-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="90dfb-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="90dfb-138">-Confirm</span></span>
<span data-ttu-id="90dfb-139">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="90dfb-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90dfb-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90dfb-140">-WhatIf</span></span>
<span data-ttu-id="90dfb-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90dfb-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90dfb-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="90dfb-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90dfb-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90dfb-143">CommonParameters</span></span>
<span data-ttu-id="90dfb-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90dfb-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90dfb-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90dfb-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90dfb-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="90dfb-146">INPUTS</span></span>

### <span data-ttu-id="90dfb-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="90dfb-147">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="90dfb-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="90dfb-148">OUTPUTS</span></span>

### <span data-ttu-id="90dfb-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="90dfb-149">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="90dfb-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="90dfb-150">NOTES</span></span>

<span data-ttu-id="90dfb-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="90dfb-151">ALIASES</span></span>

<span data-ttu-id="90dfb-152">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="90dfb-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="90dfb-153">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="90dfb-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="90dfb-154">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="90dfb-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="90dfb-155">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="90dfb-155">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="90dfb-156">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="90dfb-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="90dfb-157">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="90dfb-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="90dfb-158">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="90dfb-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="90dfb-159">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="90dfb-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="90dfb-160">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="90dfb-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="90dfb-161">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="90dfb-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="90dfb-162">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="90dfb-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="90dfb-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="90dfb-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="90dfb-164">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="90dfb-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="90dfb-165">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="90dfb-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="90dfb-166">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="90dfb-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="90dfb-167">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="90dfb-167">RELATED LINKS</span></span>

