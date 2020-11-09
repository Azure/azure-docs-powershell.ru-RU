---
external help file: ''
Module Name: Az.PostgreSql
online version: https://docs.microsoft.com/en-us/powershell/module/az.postgresql/get-azpostgresqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PostgreSql/help/Get-AzPostgreSqlServer.md
ms.openlocfilehash: 71fb10b0aeed85a716a834b42b1bdae3e5f7b270
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317885"
---
# <span data-ttu-id="94d19-101">Get-AzPostgreSqlServer</span><span class="sxs-lookup"><span data-stu-id="94d19-101">Get-AzPostgreSqlServer</span></span>

## <span data-ttu-id="94d19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="94d19-102">SYNOPSIS</span></span>
<span data-ttu-id="94d19-103">Получение сведений о сервере.</span><span class="sxs-lookup"><span data-stu-id="94d19-103">Gets information about a server.</span></span>

## <span data-ttu-id="94d19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="94d19-104">SYNTAX</span></span>

### <span data-ttu-id="94d19-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="94d19-105">List1 (Default)</span></span>
```
Get-AzPostgreSqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94d19-106">Получить</span><span class="sxs-lookup"><span data-stu-id="94d19-106">Get</span></span>
```
Get-AzPostgreSqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94d19-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="94d19-107">GetViaIdentity</span></span>
```
Get-AzPostgreSqlServer -InputObject <IPostgreSqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="94d19-108">Список</span><span class="sxs-lookup"><span data-stu-id="94d19-108">List</span></span>
```
Get-AzPostgreSqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="94d19-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="94d19-109">DESCRIPTION</span></span>
<span data-ttu-id="94d19-110">Получение сведений о сервере.</span><span class="sxs-lookup"><span data-stu-id="94d19-110">Gets information about a server.</span></span>

## <span data-ttu-id="94d19-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="94d19-111">EXAMPLES</span></span>

### <span data-ttu-id="94d19-112">Пример 1: получение сервера PostgreSql с контекстом по умолчанию</span><span class="sxs-lookup"><span data-stu-id="94d19-112">Example 1: Get PostgreSql server with default context</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="94d19-113">Этот командлет получает сервер PostgreSql с контекстом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="94d19-113">This cmdlet gets PostgreSql server with default context.</span></span>

### <span data-ttu-id="94d19-114">Пример 2: получение сервера PostgreSql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="94d19-114">Example 2: Get PostgreSql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG -Name PostgreSqlTestServer

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="94d19-115">Этот командлет получает PostgreSql Server по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="94d19-115">This cmdlet gets PostgreSql server by resource group and server name.</span></span>

### <span data-ttu-id="94d19-116">Пример 3: список всех серверов PostgreSql в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="94d19-116">Example 3: Lists all the PostgreSql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzPostgreSqlServer -ResourceGroupName PostgreSqlTestRG

Name                        Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                        -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver        eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="94d19-117">Этот командлет выводит список всех серверов PostgreSql в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94d19-117">This cmdlet lists all the PostgreSql servers in specified resource group.</span></span>

### <span data-ttu-id="94d19-118">Пример 4: получение удостоверения сервера PostgreSql</span><span class="sxs-lookup"><span data-stu-id="94d19-118">Example 4: Get PostgreSql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PostgreSqlTestRG/providers/Microsoft.DBforPostgreSQL/servers/postgresqltestserver"
PS C:\> Get-AzPostgreSqlServer -InputObject $ID

Name                 Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----                 -------- ------------------ ------- ----------------------- -------   -------        --------------
postgresqltestserver eastus   pwsh               9.6     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="94d19-119">Этот командлет возвращает PostgreSql Server по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="94d19-119">This cmdlet lists gets PostgreSql server by identity.</span></span>

## <span data-ttu-id="94d19-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="94d19-120">PARAMETERS</span></span>

### <span data-ttu-id="94d19-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d19-121">-DefaultProfile</span></span>
<span data-ttu-id="94d19-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="94d19-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94d19-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94d19-123">-InputObject</span></span>
<span data-ttu-id="94d19-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="94d19-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="94d19-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="94d19-125">-Name</span></span>
<span data-ttu-id="94d19-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="94d19-126">The name of the server.</span></span>

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

### <span data-ttu-id="94d19-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94d19-127">-ResourceGroupName</span></span>
<span data-ttu-id="94d19-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94d19-128">The name of the resource group.</span></span>
<span data-ttu-id="94d19-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="94d19-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="94d19-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="94d19-130">-SubscriptionId</span></span>
<span data-ttu-id="94d19-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="94d19-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="94d19-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d19-132">CommonParameters</span></span>
<span data-ttu-id="94d19-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="94d19-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d19-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94d19-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d19-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="94d19-135">INPUTS</span></span>

### <span data-ttu-id="94d19-136">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. IPostgreSqlIdentity</span><span class="sxs-lookup"><span data-stu-id="94d19-136">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.IPostgreSqlIdentity</span></span>

## <span data-ttu-id="94d19-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="94d19-137">OUTPUTS</span></span>

### <span data-ttu-id="94d19-138">Microsoft. Azure. PowerShell. командлеты. PostgreSql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="94d19-138">Microsoft.Azure.PowerShell.Cmdlets.PostgreSql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="94d19-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="94d19-139">NOTES</span></span>

<span data-ttu-id="94d19-140">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="94d19-140">ALIASES</span></span>

<span data-ttu-id="94d19-141">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="94d19-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="94d19-142">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="94d19-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="94d19-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="94d19-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="94d19-144">INPUTOBJECT <IPostgreSqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="94d19-144">INPUTOBJECT <IPostgreSqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="94d19-145">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="94d19-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="94d19-146">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="94d19-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="94d19-147">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="94d19-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="94d19-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="94d19-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="94d19-149">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="94d19-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="94d19-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="94d19-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="94d19-151">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="94d19-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="94d19-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="94d19-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="94d19-153">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="94d19-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="94d19-154">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="94d19-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="94d19-155">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="94d19-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="94d19-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="94d19-156">RELATED LINKS</span></span>

