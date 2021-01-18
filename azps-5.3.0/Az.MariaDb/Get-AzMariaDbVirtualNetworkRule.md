---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/en-us/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: 7ae1159c3cd5f5feea3d836a421dd9fe08c78da8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98507140"
---
# <span data-ttu-id="73539-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="73539-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="73539-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73539-102">SYNOPSIS</span></span>
<span data-ttu-id="73539-103">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="73539-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="73539-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73539-104">SYNTAX</span></span>

### <span data-ttu-id="73539-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="73539-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="73539-106">Получить</span><span class="sxs-lookup"><span data-stu-id="73539-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="73539-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="73539-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="73539-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73539-108">DESCRIPTION</span></span>
<span data-ttu-id="73539-109">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="73539-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="73539-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73539-110">EXAMPLES</span></span>

### <span data-ttu-id="73539-111">Пример 1. Список всех виртуальных правил сети в рамках MariaDB</span><span class="sxs-lookup"><span data-stu-id="73539-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="73539-112">Эта команда содержит список всех виртуальных правил сети в рамках MariaDB.</span><span class="sxs-lookup"><span data-stu-id="73539-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="73539-113">Пример 2. Получите виртуальное правило сети для MariaDB</span><span class="sxs-lookup"><span data-stu-id="73539-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="73539-114">Эта команда получает виртуальное правило сети в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="73539-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="73539-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73539-115">PARAMETERS</span></span>

### <span data-ttu-id="73539-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73539-116">-DefaultProfile</span></span>
<span data-ttu-id="73539-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="73539-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73539-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73539-118">-InputObject</span></span>
<span data-ttu-id="73539-119">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="73539-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="73539-120">-Name</span><span class="sxs-lookup"><span data-stu-id="73539-120">-Name</span></span>
<span data-ttu-id="73539-121">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="73539-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="73539-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73539-122">-PassThru</span></span>
<span data-ttu-id="73539-123">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="73539-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="73539-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73539-124">-ResourceGroupName</span></span>
<span data-ttu-id="73539-125">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="73539-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="73539-126">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="73539-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="73539-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="73539-127">-ServerName</span></span>
<span data-ttu-id="73539-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="73539-128">The name of the server.</span></span>

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

### <span data-ttu-id="73539-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="73539-129">-SubscriptionId</span></span>
<span data-ttu-id="73539-130">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="73539-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="73539-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73539-131">CommonParameters</span></span>
<span data-ttu-id="73539-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73539-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73539-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73539-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73539-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73539-134">INPUTS</span></span>

### <span data-ttu-id="73539-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="73539-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="73539-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73539-136">OUTPUTS</span></span>

### <span data-ttu-id="73539-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="73539-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="73539-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73539-138">NOTES</span></span>

<span data-ttu-id="73539-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="73539-139">ALIASES</span></span>

<span data-ttu-id="73539-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="73539-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="73539-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="73539-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="73539-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="73539-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="73539-143">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="73539-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="73539-144">`[ConfigurationName <String>]`: Имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="73539-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="73539-145">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="73539-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="73539-146">`[FirewallRuleName <String>]`: Имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="73539-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="73539-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="73539-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="73539-148">`[LocationName <String>]`: Название расположения.</span><span class="sxs-lookup"><span data-stu-id="73539-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="73539-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="73539-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="73539-150">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="73539-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="73539-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="73539-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="73539-152">`[ServerName <String>]`: имя сервера.</span><span class="sxs-lookup"><span data-stu-id="73539-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="73539-153">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="73539-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="73539-154">`[VirtualNetworkRuleName <String>]`: имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="73539-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="73539-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73539-155">RELATED LINKS</span></span>

