---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 7779a5405f50fe87f7a9e631b40cbdc8cb40fe5a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410876"
---
# <span data-ttu-id="73ad8-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="73ad8-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="73ad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="73ad8-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="73ad8-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="73ad8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73ad8-104">SYNTAX</span></span>

### <span data-ttu-id="73ad8-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73ad8-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="73ad8-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="73ad8-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="73ad8-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73ad8-107">DESCRIPTION</span></span>
<span data-ttu-id="73ad8-108">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="73ad8-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="73ad8-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73ad8-109">EXAMPLES</span></span>

### <span data-ttu-id="73ad8-110">Пример 1. Обновление правила виртуальной сети MySql по имени</span><span class="sxs-lookup"><span data-stu-id="73ad8-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="73ad8-111">Этот cmdlet обновляет по имени виртуальное правило сети MySql.</span><span class="sxs-lookup"><span data-stu-id="73ad8-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="73ad8-112">Пример 2. Обновление правила виртуальной сети MySql с помощью удостоверений.</span><span class="sxs-lookup"><span data-stu-id="73ad8-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="73ad8-113">Эти cmdlets обновляют виртуальное правило сети MySql по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="73ad8-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="73ad8-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73ad8-114">PARAMETERS</span></span>

### <span data-ttu-id="73ad8-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73ad8-115">-AsJob</span></span>
<span data-ttu-id="73ad8-116">Запуск команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="73ad8-116">Run the command as a job</span></span>

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

### <span data-ttu-id="73ad8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73ad8-117">-DefaultProfile</span></span>
<span data-ttu-id="73ad8-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73ad8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73ad8-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="73ad8-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="73ad8-120">Создайте правило брандмауэра до того, как в виртуальной сети будет включена конечная точка службы VNET.</span><span class="sxs-lookup"><span data-stu-id="73ad8-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="73ad8-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73ad8-121">-InputObject</span></span>
<span data-ttu-id="73ad8-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="73ad8-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73ad8-123">-Name</span><span class="sxs-lookup"><span data-stu-id="73ad8-123">-Name</span></span>
<span data-ttu-id="73ad8-124">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="73ad8-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="73ad8-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="73ad8-125">-NoWait</span></span>
<span data-ttu-id="73ad8-126">Запуск команды асинхронно</span><span class="sxs-lookup"><span data-stu-id="73ad8-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="73ad8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73ad8-127">-PassThru</span></span>
<span data-ttu-id="73ad8-128">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="73ad8-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="73ad8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73ad8-129">-ResourceGroupName</span></span>
<span data-ttu-id="73ad8-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73ad8-130">The name of the resource group.</span></span>
<span data-ttu-id="73ad8-131">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="73ad8-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="73ad8-132">-ServerName</span><span class="sxs-lookup"><span data-stu-id="73ad8-132">-ServerName</span></span>
<span data-ttu-id="73ad8-133">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="73ad8-133">The name of the server.</span></span>

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

### <span data-ttu-id="73ad8-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="73ad8-134">-SubnetId</span></span>
<span data-ttu-id="73ad8-135">Это ARM ресурса виртуальной подсети сети.</span><span class="sxs-lookup"><span data-stu-id="73ad8-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="73ad8-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73ad8-136">-SubscriptionId</span></span>
<span data-ttu-id="73ad8-137">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="73ad8-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="73ad8-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73ad8-138">-Confirm</span></span>
<span data-ttu-id="73ad8-139">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73ad8-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73ad8-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73ad8-140">-WhatIf</span></span>
<span data-ttu-id="73ad8-141">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73ad8-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73ad8-142">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="73ad8-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73ad8-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73ad8-143">CommonParameters</span></span>
<span data-ttu-id="73ad8-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73ad8-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73ad8-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73ad8-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73ad8-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73ad8-146">INPUTS</span></span>

### <span data-ttu-id="73ad8-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="73ad8-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="73ad8-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73ad8-148">OUTPUTS</span></span>

### <span data-ttu-id="73ad8-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="73ad8-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="73ad8-150">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73ad8-150">NOTES</span></span>

<span data-ttu-id="73ad8-151">ALIASES</span><span class="sxs-lookup"><span data-stu-id="73ad8-151">ALIASES</span></span>

<span data-ttu-id="73ad8-152">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="73ad8-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73ad8-153">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="73ad8-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73ad8-154">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73ad8-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73ad8-155">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="73ad8-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73ad8-156">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="73ad8-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="73ad8-157">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="73ad8-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="73ad8-158">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="73ad8-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="73ad8-159">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="73ad8-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73ad8-160">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="73ad8-160">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="73ad8-161">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="73ad8-161">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="73ad8-162">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="73ad8-162">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="73ad8-163">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="73ad8-163">The name is case insensitive.</span></span>
  - <span data-ttu-id="73ad8-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="73ad8-164">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="73ad8-165">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="73ad8-165">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="73ad8-166">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="73ad8-166">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="73ad8-167">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="73ad8-167">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="73ad8-168">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73ad8-168">RELATED LINKS</span></span>
