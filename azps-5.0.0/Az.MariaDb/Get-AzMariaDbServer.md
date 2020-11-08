---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: 43af6a438a36df5360fd062aaf22e85e95fa62a1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248904"
---
# <span data-ttu-id="5d4b5-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="5d4b5-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="5d4b5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5d4b5-102">SYNOPSIS</span></span>
<span data-ttu-id="5d4b5-103">Получение сведений о сервере.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-103">Gets information about a server.</span></span>

## <span data-ttu-id="5d4b5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5d4b5-104">SYNTAX</span></span>

### <span data-ttu-id="5d4b5-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5d4b5-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d4b5-106">Получить</span><span class="sxs-lookup"><span data-stu-id="5d4b5-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d4b5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d4b5-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5d4b5-108">Список</span><span class="sxs-lookup"><span data-stu-id="5d4b5-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d4b5-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d4b5-109">DESCRIPTION</span></span>
<span data-ttu-id="5d4b5-110">Получение сведений о сервере.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-110">Gets information about a server.</span></span>

## <span data-ttu-id="5d4b5-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5d4b5-111">EXAMPLES</span></span>

### <span data-ttu-id="5d4b5-112">Пример 1: список всех MariaDB в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="5d4b5-112">Example 1: List all MariaDB under a subscriptions</span></span>
```powershell
PS C:\> Get-AzMariaDbServer

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mrdb01                     eastus   dolauli            10.2    5120                    B_Gen5_1   Basic          Enabled
wyunchi-10                 eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi                    eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
wyunchi-eastus             eastus   wyunchi            10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="5d4b5-113">Эта команда выводит список всех MariaDB в рамках подписок.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="5d4b5-114">Пример 2: список всех MariaDB в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="5d4b5-114">Example 2: List all MariaDB under a resource group</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0

Name                       Location AdministratorLogin Version StorageProfileStorageMb SkuName    SkuTier        SslEnforcement
----                       -------- ------------------ ------- ----------------------- -------    -------        --------------
mariadb-test-h3pame        eastus   qiszomtkpf         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-4rmtig        eastus   xofavpndqj         10.2    5120                    B_Gen5_1   Basic          Enabled
mariadb-test-szp6dt        eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-9pebvn        eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-test-szp6dt-rep428 eastus   zmoxhpgjqc         10.2    5120                    GP_Gen5_4  GeneralPurpose Enabled
mariadb-asd-01             eastus   adminuser          10.2    5120                    B_Gen5_1   Basic          Enabled
rst-001                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rst-002                    eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-003           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
rstrgp02-rep-004           eastus   xpwjyfdgui         10.2    7168                    GP_Gen5_4  GeneralPurpose Enabled
```

<span data-ttu-id="5d4b5-115">Эта команда выводит список всех MariaDB в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="5d4b5-116">Пример 3: получение MariaDB</span><span class="sxs-lookup"><span data-stu-id="5d4b5-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="5d4b5-117">Эта команда возвращает MariaDB.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="5d4b5-118">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5d4b5-118">PARAMETERS</span></span>

### <span data-ttu-id="5d4b5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d4b5-119">-DefaultProfile</span></span>
<span data-ttu-id="5d4b5-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d4b5-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5d4b5-121">-InputObject</span></span>
<span data-ttu-id="5d4b5-122">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d4b5-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5d4b5-123">-Name</span></span>
<span data-ttu-id="5d4b5-124">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-124">The name of the server.</span></span>

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

### <span data-ttu-id="5d4b5-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d4b5-125">-ResourceGroupName</span></span>
<span data-ttu-id="5d4b5-126">Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="5d4b5-127">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="5d4b5-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5d4b5-128">-SubscriptionId</span></span>
<span data-ttu-id="5d4b5-129">Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="5d4b5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d4b5-130">CommonParameters</span></span>
<span data-ttu-id="5d4b5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d4b5-132">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d4b5-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d4b5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5d4b5-133">INPUTS</span></span>

### <span data-ttu-id="5d4b5-134">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="5d4b5-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="5d4b5-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5d4b5-135">OUTPUTS</span></span>

### <span data-ttu-id="5d4b5-136">Microsoft. Azure. PowerShell. командлеты. MariaDb. Models. Api20180601Preview. IServer</span><span class="sxs-lookup"><span data-stu-id="5d4b5-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="5d4b5-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="5d4b5-137">NOTES</span></span>

<span data-ttu-id="5d4b5-138">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5d4b5-138">ALIASES</span></span>

<span data-ttu-id="5d4b5-139">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5d4b5-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5d4b5-140">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d4b5-141">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5d4b5-142">INPUTOBJECT <IMariaDbIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="5d4b5-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d4b5-143">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="5d4b5-144">`[DatabaseName <String>]`: Имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="5d4b5-145">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="5d4b5-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="5d4b5-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d4b5-147">`[LocationName <String>]`: Имя расположения.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="5d4b5-148">`[ResourceGroupName <String>]`: Имя группы ресурсов, содержащей ресурс.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="5d4b5-149">Это значение можно получить в API-интерфейсе диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="5d4b5-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="5d4b5-151">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="5d4b5-152">`[SubscriptionId <String>]`: Идентификатор подписки, определяющий подписку на Azure.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="5d4b5-153">`[VirtualNetworkRuleName <String>]`: Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="5d4b5-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="5d4b5-154">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5d4b5-154">RELATED LINKS</span></span>

