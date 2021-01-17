---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlVirtualNetworkRule.md
ms.openlocfilehash: 8756626488dcc1f5f2a41a06d30581a67db74bb3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403892"
---
# <span data-ttu-id="56e58-101">Get-AzMySqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="56e58-101">Get-AzMySqlVirtualNetworkRule</span></span>

## <span data-ttu-id="56e58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56e58-102">SYNOPSIS</span></span>
<span data-ttu-id="56e58-103">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="56e58-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="56e58-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="56e58-104">SYNTAX</span></span>

### <span data-ttu-id="56e58-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="56e58-105">List (Default)</span></span>
```
Get-AzMySqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="56e58-106">Получить</span><span class="sxs-lookup"><span data-stu-id="56e58-106">Get</span></span>
```
Get-AzMySqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="56e58-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="56e58-107">GetViaIdentity</span></span>
```
Get-AzMySqlVirtualNetworkRule -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="56e58-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56e58-108">DESCRIPTION</span></span>
<span data-ttu-id="56e58-109">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="56e58-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="56e58-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="56e58-110">EXAMPLES</span></span>

### <span data-ttu-id="56e58-111">Пример 1. Список всех правил виртуальной сети в указанном сервере MySql</span><span class="sxs-lookup"><span data-stu-id="56e58-111">Example 1: Lists all the Virtual Network Rules in specified MySql server</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="56e58-112">Этот cmdlet lists all the Virtual Network Rules in specified MySql server.</span><span class="sxs-lookup"><span data-stu-id="56e58-112">This cmdlet lists all the Virtual Network Rules in specified MySql server.</span></span>

### <span data-ttu-id="56e58-113">Пример 2. Получить виртуальное правило сети по имени</span><span class="sxs-lookup"><span data-stu-id="56e58-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzMySqlVirtualNetworkRule -Name vnet -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="56e58-114">Этот cmdlet получает виртуальное правило сети по имени.</span><span class="sxs-lookup"><span data-stu-id="56e58-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="56e58-115">Пример 3. Получить виртуальное правило сети по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="56e58-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test/virtualNetworkRules/vnet"
PS C:\> Get-AzMySqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforMySQL/servers/virtualNetworkRules
```

<span data-ttu-id="56e58-116">Этот cmdlet получает виртуальное правило сети по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="56e58-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="56e58-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="56e58-117">PARAMETERS</span></span>

### <span data-ttu-id="56e58-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56e58-118">-DefaultProfile</span></span>
<span data-ttu-id="56e58-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56e58-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56e58-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="56e58-120">-InputObject</span></span>
<span data-ttu-id="56e58-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="56e58-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="56e58-122">-Name</span><span class="sxs-lookup"><span data-stu-id="56e58-122">-Name</span></span>
<span data-ttu-id="56e58-123">Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="56e58-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="56e58-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="56e58-124">-PassThru</span></span>
<span data-ttu-id="56e58-125">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="56e58-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="56e58-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56e58-126">-ResourceGroupName</span></span>
<span data-ttu-id="56e58-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56e58-127">The name of the resource group.</span></span>
<span data-ttu-id="56e58-128">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="56e58-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="56e58-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="56e58-129">-ServerName</span></span>
<span data-ttu-id="56e58-130">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="56e58-130">The name of the server.</span></span>

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

### <span data-ttu-id="56e58-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="56e58-131">-SubscriptionId</span></span>
<span data-ttu-id="56e58-132">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="56e58-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="56e58-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56e58-133">CommonParameters</span></span>
<span data-ttu-id="56e58-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56e58-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56e58-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56e58-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56e58-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="56e58-136">INPUTS</span></span>

### <span data-ttu-id="56e58-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="56e58-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="56e58-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="56e58-138">OUTPUTS</span></span>

### <span data-ttu-id="56e58-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="56e58-139">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="56e58-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="56e58-140">NOTES</span></span>

<span data-ttu-id="56e58-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="56e58-141">ALIASES</span></span>

<span data-ttu-id="56e58-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="56e58-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="56e58-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="56e58-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="56e58-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="56e58-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="56e58-145">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="56e58-145">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="56e58-146">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="56e58-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="56e58-147">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="56e58-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="56e58-148">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="56e58-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="56e58-149">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="56e58-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="56e58-150">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="56e58-150">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="56e58-151">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="56e58-151">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="56e58-152">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="56e58-152">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="56e58-153">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="56e58-153">The name is case insensitive.</span></span>
  - <span data-ttu-id="56e58-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="56e58-154">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="56e58-155">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="56e58-155">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="56e58-156">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="56e58-156">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="56e58-157">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="56e58-157">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="56e58-158">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56e58-158">RELATED LINKS</span></span>

