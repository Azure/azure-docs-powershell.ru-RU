---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlflexibleserverdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerDatabase.md
ms.openlocfilehash: 43b5563a9328a5b8f96c1fdb538dc49e721c428c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410191"
---
# <span data-ttu-id="d90b8-101">Get-AzMySqlFlexibleServerDatabase</span><span class="sxs-lookup"><span data-stu-id="d90b8-101">Get-AzMySqlFlexibleServerDatabase</span></span>

## <span data-ttu-id="d90b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d90b8-102">SYNOPSIS</span></span>
<span data-ttu-id="d90b8-103">Получает сведения о базе данных.</span><span class="sxs-lookup"><span data-stu-id="d90b8-103">Gets information about a database.</span></span>

## <span data-ttu-id="d90b8-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d90b8-104">SYNTAX</span></span>

### <span data-ttu-id="d90b8-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d90b8-105">List (Default)</span></span>
```
Get-AzMySqlFlexibleServerDatabase -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d90b8-106">Получить</span><span class="sxs-lookup"><span data-stu-id="d90b8-106">Get</span></span>
```
Get-AzMySqlFlexibleServerDatabase -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d90b8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d90b8-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerDatabase -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d90b8-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d90b8-108">DESCRIPTION</span></span>
<span data-ttu-id="d90b8-109">Получает сведения о базе данных.</span><span class="sxs-lookup"><span data-stu-id="d90b8-109">Gets information about a database.</span></span>

## <span data-ttu-id="d90b8-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d90b8-110">EXAMPLES</span></span>

### <span data-ttu-id="d90b8-111">Пример 1. Получить базу данных MySql по имени ресурса</span><span class="sxs-lookup"><span data-stu-id="d90b8-111">Example 1: Get a MySql database by resource name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test -Name flexibleserverdb

Name            Charset     Collation              
----            -------- ------------------
flexibleserverdb latin1   latin1_swedish_ci  
```

<span data-ttu-id="d90b8-112">Этот cmdlet получает MySql Server по имени ресурса.</span><span class="sxs-lookup"><span data-stu-id="d90b8-112">This cmdlet gets MySql server by resource name.</span></span>

### <span data-ttu-id="d90b8-113">Пример 2. Просмотр баз данных MySql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="d90b8-113">Example 2: Get MySql databases by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServerDatabase -InputObject $ID

Name             Charset     Collation            
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci 
```

<span data-ttu-id="d90b8-114">Этот cmdlet получает mySql Server по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="d90b8-114">This cmdlet gets a MySql server by identity.</span></span>

### <span data-ttu-id="d90b8-115">Пример 3. Список всех баз данных MySql на указанном сервере</span><span class="sxs-lookup"><span data-stu-id="d90b8-115">Example 3: Lists all the MySql databases in the specified server</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerDatabase -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name             Charset     Collation        
----             -------- ------------------
flexibleserverdb  latin1   latin1_swedish_ci  
performance_schema latin1   latin1_swedish_ci
```

<span data-ttu-id="d90b8-116">Этот cmdlet lists all the MySql servers in specified the server.</span><span class="sxs-lookup"><span data-stu-id="d90b8-116">This cmdlet lists all the MySql servers in specified the server.</span></span>

## <span data-ttu-id="d90b8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d90b8-117">PARAMETERS</span></span>

### <span data-ttu-id="d90b8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d90b8-118">-DefaultProfile</span></span>
<span data-ttu-id="d90b8-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d90b8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d90b8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d90b8-120">-InputObject</span></span>
<span data-ttu-id="d90b8-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="d90b8-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d90b8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="d90b8-122">-Name</span></span>
<span data-ttu-id="d90b8-123">Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d90b8-123">The name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d90b8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d90b8-124">-ResourceGroupName</span></span>
<span data-ttu-id="d90b8-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d90b8-125">The name of the resource group.</span></span>
<span data-ttu-id="d90b8-126">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d90b8-126">The name is case insensitive.</span></span>

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

### <span data-ttu-id="d90b8-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d90b8-127">-ServerName</span></span>
<span data-ttu-id="d90b8-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d90b8-128">The name of the server.</span></span>

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

### <span data-ttu-id="d90b8-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d90b8-129">-SubscriptionId</span></span>
<span data-ttu-id="d90b8-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d90b8-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="d90b8-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d90b8-131">CommonParameters</span></span>
<span data-ttu-id="d90b8-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d90b8-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d90b8-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d90b8-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d90b8-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d90b8-134">INPUTS</span></span>

### <span data-ttu-id="d90b8-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="d90b8-135">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="d90b8-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d90b8-136">OUTPUTS</span></span>

### <span data-ttu-id="d90b8-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span><span class="sxs-lookup"><span data-stu-id="d90b8-137">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IDatabase</span></span>

## <span data-ttu-id="d90b8-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d90b8-138">NOTES</span></span>

<span data-ttu-id="d90b8-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d90b8-139">ALIASES</span></span>

<span data-ttu-id="d90b8-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="d90b8-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d90b8-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="d90b8-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d90b8-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d90b8-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d90b8-143">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="d90b8-143">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d90b8-144">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="d90b8-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="d90b8-145">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="d90b8-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="d90b8-146">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="d90b8-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="d90b8-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="d90b8-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d90b8-148">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="d90b8-148">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="d90b8-149">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="d90b8-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="d90b8-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d90b8-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="d90b8-151">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="d90b8-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="d90b8-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d90b8-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="d90b8-153">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="d90b8-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="d90b8-154">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="d90b8-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="d90b8-155">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="d90b8-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="d90b8-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d90b8-156">RELATED LINKS</span></span>

