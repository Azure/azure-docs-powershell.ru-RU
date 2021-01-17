---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98421327"
---
# <span data-ttu-id="6ccc9-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="6ccc9-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="6ccc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ccc9-102">SYNOPSIS</span></span>
<span data-ttu-id="6ccc9-103">Получает сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-103">Gets information about a server.</span></span>

## <span data-ttu-id="6ccc9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6ccc9-104">SYNTAX</span></span>

### <span data-ttu-id="6ccc9-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6ccc9-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ccc9-106">Получить</span><span class="sxs-lookup"><span data-stu-id="6ccc9-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ccc9-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6ccc9-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6ccc9-108">Список</span><span class="sxs-lookup"><span data-stu-id="6ccc9-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="6ccc9-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6ccc9-109">DESCRIPTION</span></span>
<span data-ttu-id="6ccc9-110">Получает сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-110">Gets information about a server.</span></span>

## <span data-ttu-id="6ccc9-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6ccc9-111">EXAMPLES</span></span>

### <span data-ttu-id="6ccc9-112">Пример 1. Получить сервер PostgreSql с контекстом по умолчанию</span><span class="sxs-lookup"><span data-stu-id="6ccc9-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6ccc9-113">Этот cmdlet получает сервер PostgreSql с контекстом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="6ccc9-114">Пример 2. Получить сервер PostgreSql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="6ccc9-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6ccc9-115">Этот cmdlet получает сервер PostgreSql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="6ccc9-116">Пример 3. Список всех серверов PostgreSql в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="6ccc9-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6ccc9-117">Этот cmdlet перечисляет все серверы PostgreSql в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="6ccc9-118">Пример 4. Получить сервер PostgreSql по удостоверениям</span><span class="sxs-lookup"><span data-stu-id="6ccc9-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="6ccc9-119">Этот список с помощью этих списков получает по идентификаторам Сервер PostgreSql.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="6ccc9-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ccc9-120">PARAMETERS</span></span>

### <span data-ttu-id="6ccc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ccc9-121">-DefaultProfile</span></span>
<span data-ttu-id="6ccc9-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ccc9-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ccc9-123">-InputObject</span></span>
<span data-ttu-id="6ccc9-124">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6ccc9-125">-Name</span><span class="sxs-lookup"><span data-stu-id="6ccc9-125">-Name</span></span>
<span data-ttu-id="6ccc9-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-126">The name of the server.</span></span>

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

### <span data-ttu-id="6ccc9-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ccc9-127">-ResourceGroupName</span></span>
<span data-ttu-id="6ccc9-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-128">The name of the resource group.</span></span>
<span data-ttu-id="6ccc9-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6ccc9-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6ccc9-130">-SubscriptionId</span></span>
<span data-ttu-id="6ccc9-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6ccc9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ccc9-132">CommonParameters</span></span>
<span data-ttu-id="6ccc9-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ccc9-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ccc9-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ccc9-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6ccc9-135">INPUTS</span></span>

### <span data-ttu-id="6ccc9-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="6ccc9-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="6ccc9-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6ccc9-137">OUTPUTS</span></span>

### <span data-ttu-id="6ccc9-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span><span class="sxs-lookup"><span data-stu-id="6ccc9-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="6ccc9-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6ccc9-139">NOTES</span></span>

<span data-ttu-id="6ccc9-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6ccc9-140">ALIASES</span></span>

<span data-ttu-id="6ccc9-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6ccc9-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6ccc9-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6ccc9-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6ccc9-144">INPUTOBJECT <IPostgreSqlIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="6ccc9-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6ccc9-145">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="6ccc9-146">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="6ccc9-147">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="6ccc9-148">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="6ccc9-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6ccc9-149">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="6ccc9-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6ccc9-151">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="6ccc9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="6ccc9-153">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="6ccc9-154">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="6ccc9-155">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="6ccc9-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="6ccc9-156">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6ccc9-156">RELATED LINKS</span></span>

