---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/update-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Update-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: f98c24ab0be3b2c35ac43642fb9d4bbf0b421c7e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236090"
---
# <span data-ttu-id="6acb3-101">Update-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6acb3-101">Update-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="6acb3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6acb3-102">SYNOPSIS</span></span>
<span data-ttu-id="6acb3-103">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6acb3-103">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="6acb3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6acb3-104">SYNTAX</span></span>

### <span data-ttu-id="6acb3-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6acb3-105">UpdateExpanded (Default)</span></span>
```
Update-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 -SubnetId <String> [-SubscriptionId <String>] [-IgnoreMissingVnetServiceEndpoint]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="6acb3-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="6acb3-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> -SubnetId <String>
 [-IgnoreMissingVnetServiceEndpoint] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6acb3-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6acb3-107">DESCRIPTION</span></span>
<span data-ttu-id="6acb3-108">Создание или обновление существующего правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6acb3-108">Creates or updates an existing virtual network rule.</span></span>

## <span data-ttu-id="6acb3-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6acb3-109">EXAMPLES</span></span>

### <span data-ttu-id="6acb3-110">Пример 1: обновление правила виртуальной сети MySql по имени</span><span class="sxs-lookup"><span data-stu-id="6acb3-110">Example 1: Update MySql Virtual Network Rule by name</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet2"
PS C:\> Update-AzMySqlVirtualNetworkRule -Name $env.VNetName -ResourceGroupName $env.resourceGroup -ServerName $env.serverName -SubnetId $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="6acb3-111">Этот командлет обновляет правило виртуальной сети MySql по имени.</span><span class="sxs-lookup"><span data-stu-id="6acb3-111">This cmdlet updates MySql Virtual Network Rule by name.</span></span>

### <span data-ttu-id="6acb3-112">Пример 2: обновление правила виртуальной сети MySql по удостоверению.</span><span class="sxs-lookup"><span data-stu-id="6acb3-112">Example 2: Update MySql Virtual Network Rule by identity.</span></span>
```powershell
PS C:\> $SubnetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.Network/virtualNetworks/MySqlVNet/subnets/MysqlSubnet1"
PS C:\> $VNetID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Update-AzMySqlVirtualNetworkRule -InputObject $VNetID -SubnetId $SubnetID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="6acb3-113">Эти командлеты обновляют правило виртуальной сети MySql по идентификаторам.</span><span class="sxs-lookup"><span data-stu-id="6acb3-113">These cmdlets update MySql Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="6acb3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6acb3-114">PARAMETERS</span></span>

### <span data-ttu-id="6acb3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6acb3-115">-AsJob</span></span>
<span data-ttu-id="6acb3-116">Выполнение команды в качестве задания</span><span class="sxs-lookup"><span data-stu-id="6acb3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="6acb3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6acb3-117">-DefaultProfile</span></span>
<span data-ttu-id="6acb3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6acb3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6acb3-119">-IgnoreMissingVnetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="6acb3-119">-IgnoreMissingVnetServiceEndpoint</span></span>
<span data-ttu-id="6acb3-120">Создайте правило брандмауэра, прежде чем в виртуальной сети будет включена конечная точка службы виртуальных сетей.</span><span class="sxs-lookup"><span data-stu-id="6acb3-120">Create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="6acb3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6acb3-121">-InputObject</span></span>
<span data-ttu-id="6acb3-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="6acb3-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6acb3-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6acb3-123">-Name</span></span>
<span data-ttu-id="6acb3-124">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6acb3-124">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="6acb3-125">-Wait</span><span class="sxs-lookup"><span data-stu-id="6acb3-125">-NoWait</span></span>
<span data-ttu-id="6acb3-126">Выполнение команды в асинхронном режиме</span><span class="sxs-lookup"><span data-stu-id="6acb3-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6acb3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6acb3-127">-PassThru</span></span>
<span data-ttu-id="6acb3-128">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="6acb3-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6acb3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6acb3-129">-ResourceGroupName</span></span>
<span data-ttu-id="6acb3-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6acb3-130">The name of the resource group.</span></span>
<span data-ttu-id="6acb3-131">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6acb3-131">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6acb3-132">-ИмяСервера</span><span class="sxs-lookup"><span data-stu-id="6acb3-132">-ServerName</span></span>
<span data-ttu-id="6acb3-133">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6acb3-133">The name of the server.</span></span>

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

### <span data-ttu-id="6acb3-134">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="6acb3-134">-SubnetId</span></span>
<span data-ttu-id="6acb3-135">Идентификатор ресурса ARM для подсети виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6acb3-135">The ARM resource id of the virtual network subnet.</span></span>

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

### <span data-ttu-id="6acb3-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6acb3-136">-SubscriptionId</span></span>
<span data-ttu-id="6acb3-137">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6acb3-137">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6acb3-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6acb3-138">-Confirm</span></span>
<span data-ttu-id="6acb3-139">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6acb3-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6acb3-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6acb3-140">-WhatIf</span></span>
<span data-ttu-id="6acb3-141">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6acb3-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6acb3-142">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6acb3-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6acb3-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6acb3-143">CommonParameters</span></span>
<span data-ttu-id="6acb3-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6acb3-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6acb3-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6acb3-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6acb3-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6acb3-146">INPUTS</span></span>

### <span data-ttu-id="6acb3-147">Microsoft. Azure. PowerShell. командлеты. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6acb3-147">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="6acb3-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6acb3-148">OUTPUTS</span></span>

### <span data-ttu-id="6acb3-149">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="6acb3-149">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="6acb3-150">Пуск</span><span class="sxs-lookup"><span data-stu-id="6acb3-150">NOTES</span></span>

<span data-ttu-id="6acb3-151">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="6acb3-151">ALIASES</span></span>

<span data-ttu-id="6acb3-152">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6acb3-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6acb3-153">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="6acb3-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6acb3-154">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6acb3-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6acb3-155">INPUTOBJECT <IMySqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="6acb3-155">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6acb3-156">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="6acb3-156">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6acb3-157">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="6acb3-157">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6acb3-158">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="6acb3-158">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6acb3-159">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="6acb3-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6acb3-160">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="6acb3-160">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6acb3-161">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6acb3-161">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6acb3-162">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="6acb3-162">The name is case insensitive.</span></span>
  - <span data-ttu-id="6acb3-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6acb3-163">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6acb3-164">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6acb3-164">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6acb3-165">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6acb3-165">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6acb3-166">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="6acb3-166">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6acb3-167">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6acb3-167">RELATED LINKS</span></span>

