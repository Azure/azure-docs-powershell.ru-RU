---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 30e361d77f3c3b738703e1dde075ccbabc38b0b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979848"
---
# <span data-ttu-id="63d4d-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="63d4d-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="63d4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63d4d-102">SYNOPSIS</span></span>
<span data-ttu-id="63d4d-103">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="63d4d-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="63d4d-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63d4d-104">SYNTAX</span></span>

### <span data-ttu-id="63d4d-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63d4d-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="63d4d-106">Получить</span><span class="sxs-lookup"><span data-stu-id="63d4d-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="63d4d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="63d4d-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="63d4d-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63d4d-108">DESCRIPTION</span></span>
<span data-ttu-id="63d4d-109">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="63d4d-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="63d4d-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63d4d-110">EXAMPLES</span></span>

### <span data-ttu-id="63d4d-111">Пример 1. Список всех правил виртуальной сети в указанном сервере MySql</span><span class="sxs-lookup"><span data-stu-id="63d4d-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="63d4d-112">Этот cmdlet lists all the Virtual Network Rules in specified MySql server.</span><span class="sxs-lookup"><span data-stu-id="63d4d-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="63d4d-113">Пример 2. Получить виртуальное правило сети по имени</span><span class="sxs-lookup"><span data-stu-id="63d4d-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="63d4d-114">Этот cmdlet получает виртуальное правило сети по имени.</span><span class="sxs-lookup"><span data-stu-id="63d4d-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="63d4d-115">Пример 3. Получить виртуальное правило сети по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="63d4d-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="63d4d-116">Этот cmdlet получает виртуальное правило сети по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="63d4d-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="63d4d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63d4d-117">PARAMETERS</span></span>

### <span data-ttu-id="63d4d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63d4d-118">-DefaultProfile</span></span>
<span data-ttu-id="63d4d-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63d4d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63d4d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63d4d-120">-InputObject</span></span>
<span data-ttu-id="63d4d-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="63d4d-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63d4d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="63d4d-122">-Name</span></span>
<span data-ttu-id="63d4d-123">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="63d4d-123">The name of the virtual network rule.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: VirtualNetworkRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d4d-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="63d4d-124">-PassThru</span></span>
<span data-ttu-id="63d4d-125">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="63d4d-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="63d4d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63d4d-126">-ResourceGroupName</span></span>
<span data-ttu-id="63d4d-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63d4d-127">The name of the resource group.</span></span>
<span data-ttu-id="63d4d-128">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="63d4d-128">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d4d-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="63d4d-129">-ServerName</span></span>
<span data-ttu-id="63d4d-130">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="63d4d-130">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d4d-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63d4d-131">-SubscriptionId</span></span>
<span data-ttu-id="63d4d-132">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="63d4d-132">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d4d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d4d-133">CommonParameters</span></span>
<span data-ttu-id="63d4d-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63d4d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d4d-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63d4d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d4d-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63d4d-136">INPUTS</span></span>

### <span data-ttu-id="63d4d-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="63d4d-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="63d4d-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63d4d-138">OUTPUTS</span></span>

### <span data-ttu-id="63d4d-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="63d4d-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="63d4d-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63d4d-140">NOTES</span></span>

<span data-ttu-id="63d4d-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="63d4d-141">ALIASES</span></span>

<span data-ttu-id="63d4d-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="63d4d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="63d4d-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="63d4d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="63d4d-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="63d4d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="63d4d-145">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="63d4d-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="63d4d-146">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="63d4d-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="63d4d-147">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="63d4d-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="63d4d-148">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="63d4d-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="63d4d-149">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="63d4d-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="63d4d-150">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="63d4d-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="63d4d-151">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="63d4d-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="63d4d-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63d4d-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="63d4d-153">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="63d4d-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="63d4d-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="63d4d-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="63d4d-155">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="63d4d-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="63d4d-156">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="63d4d-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="63d4d-157">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="63d4d-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="63d4d-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63d4d-158">RELATED LINKS</span></span>

