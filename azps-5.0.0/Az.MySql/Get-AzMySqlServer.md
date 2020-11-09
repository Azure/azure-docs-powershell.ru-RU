---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlServer.md
ms.openlocfilehash: e2187c95237cdb89915c47fc7089fd5f9d38cff1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317207"
---
# <span data-ttu-id="313cd-101">Get-AzMySqlServer</span><span class="sxs-lookup"><span data-stu-id="313cd-101">Get-AzMySqlServer</span></span>

## <span data-ttu-id="313cd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="313cd-102">SYNOPSIS</span></span>
<span data-ttu-id="313cd-103">Получение сведений о сервере.</span><span class="sxs-lookup"><span data-stu-id="313cd-103">Gets information about a server.</span></span>

## <span data-ttu-id="313cd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="313cd-104">SYNTAX</span></span>

### <span data-ttu-id="313cd-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="313cd-105">List1 (Default)</span></span>
```
Get-AzMySqlServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="313cd-106">Получить</span><span class="sxs-lookup"><span data-stu-id="313cd-106">Get</span></span>
```
Get-AzMySqlServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="313cd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="313cd-107">GetViaIdentity</span></span>
```
Get-AzMySqlServer -InputObject <IMySqlIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="313cd-108">Список</span><span class="sxs-lookup"><span data-stu-id="313cd-108">List</span></span>
```
Get-AzMySqlServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="313cd-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="313cd-109">DESCRIPTION</span></span>
<span data-ttu-id="313cd-110">Получение сведений о сервере.</span><span class="sxs-lookup"><span data-stu-id="313cd-110">Gets information about a server.</span></span>

## <span data-ttu-id="313cd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="313cd-111">EXAMPLES</span></span>

### <span data-ttu-id="313cd-112">Пример 1: получение сервера MySql с контекстом по умолчанию</span><span class="sxs-lookup"><span data-stu-id="313cd-112">Example 1: Get MySql server with default context</span></span>
```powershell
PS C:\> Get-AzMySqlServer

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-11 eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="313cd-113">Этот командлет получает сервер MySql с контекстом по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="313cd-113">This cmdlet gets MySql server with default context.</span></span>

### <span data-ttu-id="313cd-114">Пример 2: получение сервера MySql по группе ресурсов и имени сервера</span><span class="sxs-lookup"><span data-stu-id="313cd-114">Example 2: Get MySql server by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest -Name mysql-test

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="313cd-115">Этот командлет получает сервер MySql по группе ресурсов и имени сервера.</span><span class="sxs-lookup"><span data-stu-id="313cd-115">This cmdlet gets MySql server by resource group and server name.</span></span>

### <span data-ttu-id="313cd-116">Пример 3: список всех серверов MySql в указанной группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="313cd-116">Example 3: Lists all the MySql servers in specified resource group</span></span>
```powershell
PS C:\> Get-AzMySqlServer -ResourceGroupName PowershellMySqlTest

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="313cd-117">Этот командлет выводит список всех серверов MySql в указанной группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="313cd-117">This cmdlet lists all the MySql servers in specified resource group.</span></span>

### <span data-ttu-id="313cd-118">Пример 4: получение сервера MySql по удостоверению</span><span class="sxs-lookup"><span data-stu-id="313cd-118">Example 4: Get MySql server by identity</span></span>
```powershell
PS C:\> $ID = "/subscriptions/<SubscriptionId>/resourceGroups/PowershellMySqlTest/providers/Microsoft.DBforMySQL/servers/mysql-test"
PS C:\> Get-AzMySqlServer -InputObject $ID

Name          Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----          -------- ------------------ ------- ----------------------- -------   -------        ------------
mysql-test    eastus   mysql_test         5.7     5120                    GP_Gen5_4 GeneralPurpose Enabled
```

<span data-ttu-id="313cd-119">Этот командлет возвращает сервер MySql по идентификатору.</span><span class="sxs-lookup"><span data-stu-id="313cd-119">This cmdlet lists gets MySql server by identity.</span></span>

## <span data-ttu-id="313cd-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="313cd-120">PARAMETERS</span></span>

### <span data-ttu-id="313cd-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="313cd-121">-DefaultProfile</span></span>
<span data-ttu-id="313cd-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="313cd-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="313cd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="313cd-123">-InputObject</span></span>
<span data-ttu-id="313cd-124">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="313cd-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="313cd-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="313cd-125">-Name</span></span>
<span data-ttu-id="313cd-126">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="313cd-126">The name of the server.</span></span>

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

### <span data-ttu-id="313cd-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="313cd-127">-ResourceGroupName</span></span>
<span data-ttu-id="313cd-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="313cd-128">The name of the resource group.</span></span>
<span data-ttu-id="313cd-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="313cd-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="313cd-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="313cd-130">-SubscriptionId</span></span>
<span data-ttu-id="313cd-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="313cd-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="313cd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="313cd-132">CommonParameters</span></span>
<span data-ttu-id="313cd-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="313cd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="313cd-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="313cd-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="313cd-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="313cd-135">INPUTS</span></span>

### <span data-ttu-id="313cd-136">Microsoft. Azure. PowerShell. командлеты. MySql. Models. IMySqlIdentity</span><span class="sxs-lookup"><span data-stu-id="313cd-136">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.IMySqlIdentity</span></span>

## <span data-ttu-id="313cd-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="313cd-137">OUTPUTS</span></span>

### <span data-ttu-id="313cd-138">Microsoft. Azure. PowerShell. командлеты. MySql. Models. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="313cd-138">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="313cd-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="313cd-139">NOTES</span></span>

<span data-ttu-id="313cd-140">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="313cd-140">ALIASES</span></span>

<span data-ttu-id="313cd-141">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="313cd-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="313cd-142">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="313cd-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="313cd-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="313cd-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="313cd-144">INPUTOBJECT <IMySqlIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="313cd-144">INPUTOBJECT <IMySqlIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="313cd-145">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="313cd-145">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="313cd-146">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="313cd-146">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="313cd-147">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="313cd-147">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="313cd-148">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="313cd-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="313cd-149">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="313cd-149">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="313cd-150">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="313cd-150">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="313cd-151">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="313cd-151">The name is case insensitive.</span></span>
  - <span data-ttu-id="313cd-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="313cd-152">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="313cd-153">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="313cd-153">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="313cd-154">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="313cd-154">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="313cd-155">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="313cd-155">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="313cd-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="313cd-156">RELATED LINKS</span></span>

