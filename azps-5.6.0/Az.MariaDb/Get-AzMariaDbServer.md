---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbServer.md
ms.openlocfilehash: ac7ea6689b18c14cca2213e3856cb093f5f36287
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970648"
---
# <span data-ttu-id="4e22e-101">Get-AzMariaDbServer</span><span class="sxs-lookup"><span data-stu-id="4e22e-101">Get-AzMariaDbServer</span></span>

## <span data-ttu-id="4e22e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e22e-102">SYNOPSIS</span></span>
<span data-ttu-id="4e22e-103">Получает сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="4e22e-103">Gets information about a server.</span></span>

## <span data-ttu-id="4e22e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4e22e-104">SYNTAX</span></span>

### <span data-ttu-id="4e22e-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4e22e-105">List1 (Default)</span></span>
```
Get-AzMariaDbServer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4e22e-106">Получить</span><span class="sxs-lookup"><span data-stu-id="4e22e-106">Get</span></span>
```
Get-AzMariaDbServer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4e22e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4e22e-107">GetViaIdentity</span></span>
```
Get-AzMariaDbServer -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4e22e-108">Список</span><span class="sxs-lookup"><span data-stu-id="4e22e-108">List</span></span>
```
Get-AzMariaDbServer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="4e22e-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e22e-109">DESCRIPTION</span></span>
<span data-ttu-id="4e22e-110">Получает сведения о сервере.</span><span class="sxs-lookup"><span data-stu-id="4e22e-110">Gets information about a server.</span></span>

## <span data-ttu-id="4e22e-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4e22e-111">EXAMPLES</span></span>

### <span data-ttu-id="4e22e-112">Пример 1. Список всех MariaDB в рамках подписок</span><span class="sxs-lookup"><span data-stu-id="4e22e-112">Example 1: List all MariaDB under a subscriptions</span></span>
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

<span data-ttu-id="4e22e-113">Эта команда содержит список всех mariaDB в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="4e22e-113">This command lists all MariaDB under a subscriptions.</span></span>

### <span data-ttu-id="4e22e-114">Пример 2. Список всех MariaDB в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="4e22e-114">Example 2: List all MariaDB under a resource group</span></span>
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

<span data-ttu-id="4e22e-115">Эта команда содержит список всех mariaDB в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4e22e-115">This command lists all MariaDB under a resource group.</span></span>

### <span data-ttu-id="4e22e-116">Пример 3. Получить MariaDB</span><span class="sxs-lookup"><span data-stu-id="4e22e-116">Example 3: Get a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbServer -ResourceGroupName mariadb-test-qu5ov0 -Name mariadb-test-h3pame

Name                Location AdministratorLogin Version StorageProfileStorageMb SkuName  SkuTier SslEnforcement
----                -------- ------------------ ------- ----------------------- -------  ------- --------------
mariadb-test-h3pame eastus   qiszomtkpf         10.2    5120                    B_Gen5_1 Basic   Enabled
```

<span data-ttu-id="4e22e-117">Эта команда получает mariaDB.</span><span class="sxs-lookup"><span data-stu-id="4e22e-117">This command gets a MariaDB.</span></span>

## <span data-ttu-id="4e22e-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e22e-118">PARAMETERS</span></span>

### <span data-ttu-id="4e22e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e22e-119">-DefaultProfile</span></span>
<span data-ttu-id="4e22e-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e22e-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e22e-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4e22e-121">-InputObject</span></span>
<span data-ttu-id="4e22e-122">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="4e22e-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4e22e-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4e22e-123">-Name</span></span>
<span data-ttu-id="4e22e-124">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4e22e-124">The name of the server.</span></span>

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

### <span data-ttu-id="4e22e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e22e-125">-ResourceGroupName</span></span>
<span data-ttu-id="4e22e-126">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="4e22e-126">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4e22e-127">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="4e22e-127">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4e22e-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e22e-128">-SubscriptionId</span></span>
<span data-ttu-id="4e22e-129">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="4e22e-129">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="4e22e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e22e-130">CommonParameters</span></span>
<span data-ttu-id="4e22e-131">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e22e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e22e-132">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e22e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e22e-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4e22e-133">INPUTS</span></span>

### <span data-ttu-id="4e22e-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="4e22e-134">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="4e22e-135">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4e22e-135">OUTPUTS</span></span>

### <span data-ttu-id="4e22e-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span><span class="sxs-lookup"><span data-stu-id="4e22e-136">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IServer</span></span>

## <span data-ttu-id="4e22e-137">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4e22e-137">NOTES</span></span>

<span data-ttu-id="4e22e-138">ALIASES</span><span class="sxs-lookup"><span data-stu-id="4e22e-138">ALIASES</span></span>

<span data-ttu-id="4e22e-139">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="4e22e-139">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4e22e-140">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="4e22e-140">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4e22e-141">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4e22e-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4e22e-142">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="4e22e-142">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4e22e-143">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="4e22e-143">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="4e22e-144">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="4e22e-144">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="4e22e-145">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="4e22e-145">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="4e22e-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="4e22e-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4e22e-147">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="4e22e-147">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="4e22e-148">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="4e22e-148">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4e22e-149">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="4e22e-149">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4e22e-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="4e22e-150">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="4e22e-151">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="4e22e-151">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="4e22e-152">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="4e22e-152">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="4e22e-153">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="4e22e-153">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="4e22e-154">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e22e-154">RELATED LINKS</span></span>

