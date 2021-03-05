---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/powershell/module/az.mysql/get-azmysqlflexibleserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlFlexibleServer.md
ms.openlocfilehash: cbbe321f23fb95bca8a4a70dd59f30ec098cf2d0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012008"
---
# <span data-ttu-id="26685-101">Get-AzMySqlFlexibleServer</span><span class="sxs-lookup"><span data-stu-id="26685-101">Get-AzMySqlFlexibleServer</span></span>

## <span data-ttu-id="26685-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26685-102">SYNOPSIS</span></span>
<span data-ttu-id="26685-103">Получает сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="26685-103">Gets information about a server.</span></span>

## <span data-ttu-id="26685-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="26685-104">SYNTAX</span></span>

### <span data-ttu-id="26685-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="26685-105">List1 (Default)</span></span>
```
Get-AzMySqlFlexibleServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26685-106">Получить</span><span class="sxs-lookup"><span data-stu-id="26685-106">Get</span></span>
```
Get-AzMySqlFlexibleServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26685-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="26685-107">GetViaIdentity</span></span>
```
Get-AzMySqlFlexibleServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="26685-108">Список</span><span class="sxs-lookup"><span data-stu-id="26685-108">List</span></span>
```
Get-AzMySqlFlexibleServer -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="26685-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="26685-109">DESCRIPTION</span></span>
<span data-ttu-id="26685-110">Получает сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="26685-110">Gets information about a server.</span></span>

## <span data-ttu-id="26685-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="26685-111">EXAMPLES</span></span>

### <span data-ttu-id="26685-112">Пример 1. Доступ к серверу MySql с контекстом по умолчанию</span><span class="sxs-lookup"><span data-stu-id="26685-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11  westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="26685-113">Этот cmdlet получает серверы MySql с контекстом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="26685-113">This cmdlet gets MySql servers with default context.</span></span>

### <span data-ttu-id="26685-114">Пример 2. Как получить mySql-сервер по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="26685-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test     westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="26685-115">Этот cmdlet получает серверы MySql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="26685-115">This cmdlet gets MySql servers by resource group and server name.</span></span>

### <span data-ttu-id="26685-116">Пример 3. Список всех серверов MySql в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="26685-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlFlexibleServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test-11 westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
mysql-test-12 westus2   mysql_test2        5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="26685-117">Этот cmdlet перечисляет все серверы MySql в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26685-117">This cmdlet lists all the MySql servers in the specified resource group.</span></span>

### <span data-ttu-id="26685-118">Пример 4. Как получить mySql-сервер по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="26685-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBForMySql/flexibleServers/mysql-test"
PS C:\> Get-AzMySqlFlexibleServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName          SkuTier        
----          -------- ------------------ ------- ----------------------- ---------------- -------------
mysql-test    westus2   mysql_test         5.7     5120                    Standard_D2ds_v4 GeneralPurpose
```

<span data-ttu-id="26685-119">Эти списки с помощью этих списков можно подавлять mySql-серверы по удостоверениям.</span><span class="sxs-lookup"><span data-stu-id="26685-119">This cmdlet lists gets MySql servers by identity.</span></span>

## <span data-ttu-id="26685-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26685-120">PARAMETERS</span></span>

### <span data-ttu-id="26685-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26685-121">-DefaultProfile</span></span>
<span data-ttu-id="26685-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="26685-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26685-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="26685-123">-InputObject</span></span>
<span data-ttu-id="26685-124">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="26685-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="26685-125">-Name</span><span class="sxs-lookup"><span data-stu-id="26685-125">-Name</span></span>
<span data-ttu-id="26685-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="26685-126">The name of the server.</span></span>

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

### <span data-ttu-id="26685-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26685-127">-ResourceGroupName</span></span>
<span data-ttu-id="26685-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26685-128">The name of the resource group.</span></span>
<span data-ttu-id="26685-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="26685-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="26685-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="26685-130">-SubscriptionId</span></span>
<span data-ttu-id="26685-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="26685-131">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="26685-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26685-132">CommonParameters</span></span>
<span data-ttu-id="26685-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26685-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26685-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="26685-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26685-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="26685-135">INPUTS</span></span>

### <span data-ttu-id="26685-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="26685-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="26685-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="26685-137">OUTPUTS</span></span>

### <span data-ttu-id="26685-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span><span class="sxs-lookup"><span data-stu-id="26685-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20200701Preview.IServerAutoGenerated</span></span>

## <span data-ttu-id="26685-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="26685-139">NOTES</span></span>

<span data-ttu-id="26685-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="26685-140">ALIASES</span></span>

<span data-ttu-id="26685-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="26685-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="26685-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="26685-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="26685-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="26685-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="26685-144">INPUTOBJECT <IMySqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="26685-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="26685-145">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="26685-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="26685-146">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="26685-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="26685-147">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="26685-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="26685-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="26685-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="26685-149">`[KeyName <String>]`: имя ключа сервера.</span><span class="sxs-lookup"><span data-stu-id="26685-149">`[KeyName <String>]`: The name of the server key.</span></span>
  - <span data-ttu-id="26685-150">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="26685-150">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="26685-151">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="26685-151">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="26685-152">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="26685-152">The name is case insensitive.</span></span>
  - <span data-ttu-id="26685-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="26685-153">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="26685-154">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="26685-154">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="26685-155">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="26685-155">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="26685-156">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="26685-156">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="26685-157">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="26685-157">RELATED LINKS</span></span>

