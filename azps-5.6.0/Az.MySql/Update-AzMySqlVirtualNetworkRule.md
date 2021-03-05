---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 572943ea0f694b5a3a68ff4c1c030a1a3a1fc0f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101968739"
---
# <span data-ttu-id="0fad9-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0fad9-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="0fad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fad9-102">SYNOPSIS</span></span>
<span data-ttu-id="0fad9-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0fad9-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="0fad9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0fad9-104">SYNTAX</span></span>

### <span data-ttu-id="0fad9-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0fad9-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="0fad9-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0fad9-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="0fad9-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fad9-107">DESCRIPTION</span></span>
<span data-ttu-id="0fad9-108">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="0fad9-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="0fad9-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0fad9-109">EXAMPLES</span></span>

### <span data-ttu-id="0fad9-110">Пример 1. Обновление правила виртуальной сети MySql по имени</span><span class="sxs-lookup"><span data-stu-id="0fad9-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="0fad9-111">Этот cmdlet обновляет по имени виртуальное правило сети MySql.</span><span class="sxs-lookup"><span data-stu-id="0fad9-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="0fad9-112">Пример 2. Обновление виртуальных сетевых правил MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="0fad9-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="0fad9-113">Эти cmdlets обновляют виртуальное правило сети MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="0fad9-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="0fad9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fad9-114">PARAMETERS</span></span>

### <span data-ttu-id="0fad9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fad9-115">-AsJob</span></span>
<span data-ttu-id="0fad9-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="0fad9-116">Run the command as a job</span></span>

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

### <span data-ttu-id="0fad9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fad9-117">-DefaultProfile</span></span>
<span data-ttu-id="0fad9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fad9-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fad9-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="0fad9-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="0fad9-120">Создайте правило брандмауэра до того, как в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="0fad9-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="0fad9-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fad9-121">-InputObject</span></span>
<span data-ttu-id="0fad9-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="0fad9-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fad9-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0fad9-123">-Name</span></span>
<span data-ttu-id="0fad9-124">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="0fad9-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="0fad9-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0fad9-125">-NoWait</span></span>
<span data-ttu-id="0fad9-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="0fad9-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0fad9-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fad9-127">-PassThru</span></span>
<span data-ttu-id="0fad9-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="0fad9-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0fad9-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fad9-129">-ResourceGroupName</span></span>
<span data-ttu-id="0fad9-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fad9-130">The name of the resource group.</span></span>
<span data-ttu-id="0fad9-131">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="0fad9-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0fad9-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0fad9-132">-ServerName</span></span>
<span data-ttu-id="0fad9-133">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="0fad9-133">The name of the server.</span></span>

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

### <span data-ttu-id="0fad9-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="0fad9-134">-SubnetId</span></span>
<span data-ttu-id="0fad9-135">Это ARM ресурса виртуальной подсети сети.</span><span class="sxs-lookup"><span data-stu-id="0fad9-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="0fad9-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0fad9-136">-SubscriptionId</span></span>
<span data-ttu-id="0fad9-137">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0fad9-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="0fad9-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fad9-138">-Confirm</span></span>
<span data-ttu-id="0fad9-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fad9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fad9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fad9-140">-WhatIf</span></span>
<span data-ttu-id="0fad9-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fad9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fad9-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0fad9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fad9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fad9-143">CommonParameters</span></span>
<span data-ttu-id="0fad9-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fad9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fad9-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fad9-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fad9-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0fad9-146">INPUTS</span></span>

### <span data-ttu-id="0fad9-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="0fad9-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="0fad9-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0fad9-148">OUTPUTS</span></span>

### <span data-ttu-id="0fad9-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0fad9-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="0fad9-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0fad9-150">NOTES</span></span>

<span data-ttu-id="0fad9-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="0fad9-151">ALIASES</span></span>

<span data-ttu-id="0fad9-152">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="0fad9-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0fad9-153">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="0fad9-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0fad9-154">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0fad9-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0fad9-155">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="0fad9-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0fad9-156">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="0fad9-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="0fad9-157">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="0fad9-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="0fad9-158">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="0fad9-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="0fad9-159">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="0fad9-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0fad9-160">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="0fad9-160">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="0fad9-161">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="0fad9-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="0fad9-162">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fad9-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="0fad9-163">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="0fad9-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="0fad9-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="0fad9-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="0fad9-165">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="0fad9-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="0fad9-166">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="0fad9-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="0fad9-167">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="0fad9-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="0fad9-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fad9-168">RELATED LINKS</span></span>

