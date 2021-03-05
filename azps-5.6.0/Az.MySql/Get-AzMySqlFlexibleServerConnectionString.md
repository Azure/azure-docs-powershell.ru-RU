---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserverconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServerConnectionString.md
ms.openlocfilehash: a1f5c89b33ad4d547907bd63427a45ef262518c1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011955"
---
# <span data-ttu-id="63639-101">Get-AzMySqlFlexibleServerConnectionString</span><span class="sxs-lookup"><span data-stu-id="63639-101">Get-AzMySqlFlexibleServerConnectionString</span></span>

## <span data-ttu-id="63639-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63639-102">SYNOPSIS</span></span>
<span data-ttu-id="63639-103">Получите строку подключения в соответствии с поставщиком клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="63639-103">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="63639-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="63639-104">SYNTAX</span></span>

### <span data-ttu-id="63639-105">Получить (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="63639-105">Get (Default)</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="63639-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="63639-106">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServerConnectionString -Client <String> -InputObject <IMySqlIdentity>
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="63639-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="63639-107">DESCRIPTION</span></span>
<span data-ttu-id="63639-108">Получите строку подключения в соответствии с поставщиком клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="63639-108">Get the connection string according to client connection provider.</span></span>

## <span data-ttu-id="63639-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="63639-109">EXAMPLES</span></span>

### <span data-ttu-id="63639-110">Пример 1. Получить строку подключения по имени</span><span class="sxs-lookup"><span data-stu-id="63639-110">Example 1: Get connection string by name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServerConnectionString -Client Python -ResourceGroupName PowershellMySqlTest -Name mysql-test

cnx = mysql.connector.connect(user=mysql_user, password="{your_password}", host="mysql-test.mysql.database.azure.com", port=3306, database="{your_database}", ssl_ca="{ca-cert filename}", ssl_disabled=False)
```

<span data-ttu-id="63639-111">Этот cmdlet shows connection string of a client by server name.</span><span class="sxs-lookup"><span data-stu-id="63639-111">This cmdlet shows connection string of a client by server name.</span></span>

### <span data-ttu-id="63639-112">Пример 2. Получить строку подключения к серверу MySql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="63639-112">Example 2: Get MySql server connection string by identity</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -ServerName mysql-test | Get-AzMySqlFlexibleServerConnectionString -Client PHP

$con=mysqli_init(); mysqli_real_connect($con, "mysql-test.mysql.database.azure.com", "mysql_test", {your_password}, {your_database}, 3306);
```

<span data-ttu-id="63639-113">Этот cmdlet получает строку подключения MySql server по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="63639-113">This cmdlet gets MySql server connection string by identity.</span></span>

## <span data-ttu-id="63639-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="63639-114">PARAMETERS</span></span>

### <span data-ttu-id="63639-115">-Client</span><span class="sxs-lookup"><span data-stu-id="63639-115">-Client</span></span>
<span data-ttu-id="63639-116">Поставщик клиентских подключений.</span><span class="sxs-lookup"><span data-stu-id="63639-116">Client connection provider.</span></span>

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

### <span data-ttu-id="63639-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63639-117">-DefaultProfile</span></span>
<span data-ttu-id="63639-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="63639-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="63639-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63639-119">-InputObject</span></span>
<span data-ttu-id="63639-120">Сервер строки подключения.</span><span class="sxs-lookup"><span data-stu-id="63639-120">The server for the connection string.</span></span>
<span data-ttu-id="63639-121">Сведения о конструкции см. в разделе "Заметки" свойств INPUTOBJECT и создании таблицы с hash.</span><span class="sxs-lookup"><span data-stu-id="63639-121">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="63639-122">-Name</span><span class="sxs-lookup"><span data-stu-id="63639-122">-Name</span></span>
<span data-ttu-id="63639-123">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="63639-123">The name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: ServerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63639-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63639-124">-ResourceGroupName</span></span>
<span data-ttu-id="63639-125">Имя группы ресурсов, которая содержит ресурс. Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="63639-125">The name of the resource group that contains the resource, You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63639-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="63639-126">-SubscriptionId</span></span>
<span data-ttu-id="63639-127">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="63639-127">The subscription ID that identifies an Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63639-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63639-128">CommonParameters</span></span>
<span data-ttu-id="63639-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63639-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63639-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="63639-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63639-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="63639-131">INPUTS</span></span>

### <span data-ttu-id="63639-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="63639-132">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="63639-133">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="63639-133">OUTPUTS</span></span>

### <span data-ttu-id="63639-134">System.String</span><span class="sxs-lookup"><span data-stu-id="63639-134">System.String</span></span>

## <span data-ttu-id="63639-135">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="63639-135">NOTES</span></span>

<span data-ttu-id="63639-136">ALIASES</span><span class="sxs-lookup"><span data-stu-id="63639-136">ALIASES</span></span>

<span data-ttu-id="63639-137">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="63639-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="63639-138">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="63639-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="63639-139">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="63639-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="63639-140">INPUTOBJECT: <IMySqlIdentity> сервер для строки подключения.</span><span class="sxs-lookup"><span data-stu-id="63639-140">INPUTOBJECT <IMySqlIdentity>: The server for the connection string.</span></span>
  - <span data-ttu-id="63639-141">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="63639-141">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="63639-142">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="63639-142">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="63639-143">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="63639-143">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="63639-144">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="63639-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="63639-145">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="63639-145">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="63639-146">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="63639-146">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="63639-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="63639-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="63639-148">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="63639-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="63639-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="63639-149">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="63639-150">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="63639-150">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="63639-151">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="63639-151">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="63639-152">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="63639-152">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="63639-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="63639-153">RELATED LINKS</span></span>

