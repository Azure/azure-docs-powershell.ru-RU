---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlVirtualNetworkRule.md
ms.openlocfilehash: eb8fc13bd2c1ef4e829cf5d4626453909b6ff773
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410119"
---
# <span data-ttu-id="dcf04-101">Get-AzPostgreSqlVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dcf04-101">Get-AzPostgreSqlVirtualNetworkRule</span></span>

## <span data-ttu-id="dcf04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcf04-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf04-103">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="dcf04-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="dcf04-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dcf04-104">SYNTAX</span></span>

### <span data-ttu-id="dcf04-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="dcf04-105">List (Default)</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="dcf04-106">Получить</span><span class="sxs-lookup"><span data-stu-id="dcf04-106">Get</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="dcf04-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dcf04-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlVirtualNetworkRule -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="dcf04-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dcf04-108">DESCRIPTION</span></span>
<span data-ttu-id="dcf04-109">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="dcf04-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="dcf04-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dcf04-110">EXAMPLES</span></span>

### <span data-ttu-id="dcf04-111">Пример 1. Список всех правил виртуальной сети на указанном сервере PostgreSql</span><span class="sxs-lookup"><span data-stu-id="dcf04-111">Example 1: Lists all the Virtual Network Rules in specified PostgreSql server</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer 

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="dcf04-112">Этот cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span><span class="sxs-lookup"><span data-stu-id="dcf04-112">This cmdlet lists all the Virtual Network Rules in specified PostgreSql server.</span></span>

### <span data-ttu-id="dcf04-113">Пример 2. Получить виртуальное правило сети по имени</span><span class="sxs-lookup"><span data-stu-id="dcf04-113">Example 2: Get Virtual Network Rule by name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -Name vnet -ResourceGroupName PostgreSqlTestRG -ServerName PostgreSqlTestServer

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="dcf04-114">Этот cmdlet получает виртуальное правило сети по имени.</span><span class="sxs-lookup"><span data-stu-id="dcf04-114">This cmdlet gets Virtual Network Rule by name.</span></span>

### <span data-ttu-id="dcf04-115">Пример 3. Получить виртуальное правило сети по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="dcf04-115">Example 3: Get Virtual Network Rule by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/PostgreSqlTestServer/virtualNetworkRules/vnet"
PS C:\> Get-AzPostgreSqlVirtualNetworkRule -InputObject $ID

Name Type
---- ----
vnet Microsoft.DBforPostgreSQL/servers/virtualNetworkRules
```

<span data-ttu-id="dcf04-116">Этот cmdlet получает виртуальное правило сети по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="dcf04-116">This cmdlet gets Virtual Network Rule by identity.</span></span>

## <span data-ttu-id="dcf04-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcf04-117">PARAMETERS</span></span>

### <span data-ttu-id="dcf04-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf04-118">-DefaultProfile</span></span>
<span data-ttu-id="dcf04-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf04-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf04-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcf04-120">-InputObject</span></span>
<span data-ttu-id="dcf04-121">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="dcf04-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcf04-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dcf04-122">-Name</span></span>
<span data-ttu-id="dcf04-123">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="dcf04-123">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="dcf04-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dcf04-124">-PassThru</span></span>
<span data-ttu-id="dcf04-125">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="dcf04-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dcf04-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcf04-126">-ResourceGroupName</span></span>
<span data-ttu-id="dcf04-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcf04-127">The name of the resource group.</span></span>
<span data-ttu-id="dcf04-128">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="dcf04-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="dcf04-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="dcf04-129">-ServerName</span></span>
<span data-ttu-id="dcf04-130">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="dcf04-130">The name of the server.</span></span>

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

### <span data-ttu-id="dcf04-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dcf04-131">-SubscriptionId</span></span>
<span data-ttu-id="dcf04-132">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="dcf04-132">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="dcf04-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf04-133">CommonParameters</span></span>
<span data-ttu-id="dcf04-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf04-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf04-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcf04-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf04-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dcf04-136">INPUTS</span></span>

### <span data-ttu-id="dcf04-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="dcf04-137">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="dcf04-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dcf04-138">OUTPUTS</span></span>

### <span data-ttu-id="dcf04-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="dcf04-139">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IVirtualNetworkRule</span></span>

## <span data-ttu-id="dcf04-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dcf04-140">NOTES</span></span>

<span data-ttu-id="dcf04-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="dcf04-141">ALIASES</span></span>

<span data-ttu-id="dcf04-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="dcf04-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dcf04-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="dcf04-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dcf04-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dcf04-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dcf04-145">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="dcf04-145">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dcf04-146">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="dcf04-146">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="dcf04-147">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="dcf04-147">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="dcf04-148">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="dcf04-148">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="dcf04-149">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="dcf04-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dcf04-150">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="dcf04-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="dcf04-151">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dcf04-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="dcf04-152">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="dcf04-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="dcf04-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="dcf04-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="dcf04-154">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="dcf04-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="dcf04-155">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="dcf04-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="dcf04-156">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="dcf04-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="dcf04-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dcf04-157">RELATED LINKS</span></span>

