---
external help file: ''
Module Name: Az.MariaDb
online version: https://docs.microsoft.com/powershell/module/az.mariadb/get-azmariadbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MariaDb/help/Get-AzMariaDbVirtualNetworkRule.md
ms.openlocfilehash: dda229292436d07cf5383343cb85472b92881cdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970643"
---
# <span data-ttu-id="b9e6f-101">Get-AzMariaDbVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9e6f-101">Get-AzMariaDbVirtualNetworkRule</span></span>

## <span data-ttu-id="b9e6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9e6f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9e6f-103">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-103">Gets a virtual network rule.</span></span>

## <span data-ttu-id="b9e6f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b9e6f-104">SYNTAX</span></span>

### <span data-ttu-id="b9e6f-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b9e6f-105">List (Default)</span></span>
```
Get-AzMariaDbVirtualNetworkRule -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b9e6f-106">Получить</span><span class="sxs-lookup"><span data-stu-id="b9e6f-106">Get</span></span>
```
Get-AzMariaDbVirtualNetworkRule -Name <String> -ResourceGroupName <String> -ServerName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="b9e6f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b9e6f-107">GetViaIdentity</span></span>
```
Get-AzMariaDbVirtualNetworkRule -InputObject <IMariaDbIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="b9e6f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b9e6f-108">DESCRIPTION</span></span>
<span data-ttu-id="b9e6f-109">Получает виртуальное правило сети.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-109">Gets a virtual network rule.</span></span>

## <span data-ttu-id="b9e6f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b9e6f-110">EXAMPLES</span></span>

### <span data-ttu-id="b9e6f-111">Пример 1. Список всех виртуальных правил сети в рамках MariaDB</span><span class="sxs-lookup"><span data-stu-id="b9e6f-111">Example 1: List all virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
vnetrule-Adsefc Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="b9e6f-112">Эта команда содержит список всех виртуальных правил сети в рамках MariaDB.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-112">This command lists all virtual network rule under a MariaDB.</span></span>

### <span data-ttu-id="b9e6f-113">Пример 2. Получите виртуальное правило сети для MariaDB</span><span class="sxs-lookup"><span data-stu-id="b9e6f-113">Example 2: Get virtual network rule under a MariaDB</span></span>
```powershell
PS C:\> Get-AzMariaDbVirtualNetworkRule -ResourceGroupName mariadb-test-qu5ov0 -ServerName mariadb-test-9pebvn -Name vnetrule-QdMJpU

Name            Type
----            ----
vnetrule-QdMJpU Microsoft.DBforMariaDB/servers/virtualNetworkRules
```

<span data-ttu-id="b9e6f-114">Эта команда получает виртуальное правило сети в MariaDB.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-114">This command gets virtual network rule under a MariaDB.</span></span>

## <span data-ttu-id="b9e6f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b9e6f-115">PARAMETERS</span></span>

### <span data-ttu-id="b9e6f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9e6f-116">-DefaultProfile</span></span>
<span data-ttu-id="b9e6f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9e6f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9e6f-118">-InputObject</span></span>
<span data-ttu-id="b9e6f-119">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9e6f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b9e6f-120">-Name</span></span>
<span data-ttu-id="b9e6f-121">Имя правила виртуальной сети.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-121">The name of the virtual network rule.</span></span>

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

### <span data-ttu-id="b9e6f-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9e6f-122">-PassThru</span></span>
<span data-ttu-id="b9e6f-123">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-123">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b9e6f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9e6f-124">-ResourceGroupName</span></span>
<span data-ttu-id="b9e6f-125">Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-125">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b9e6f-126">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-126">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b9e6f-127">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b9e6f-127">-ServerName</span></span>
<span data-ttu-id="b9e6f-128">Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-128">The name of the server.</span></span>

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

### <span data-ttu-id="b9e6f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9e6f-129">-SubscriptionId</span></span>
<span data-ttu-id="b9e6f-130">Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-130">The subscription ID that identifies an Azure subscription.</span></span>

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

### <span data-ttu-id="b9e6f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9e6f-131">CommonParameters</span></span>
<span data-ttu-id="b9e6f-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9e6f-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b9e6f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9e6f-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b9e6f-134">INPUTS</span></span>

### <span data-ttu-id="b9e6f-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span><span class="sxs-lookup"><span data-stu-id="b9e6f-135">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.IMariaDbIdentity</span></span>

## <span data-ttu-id="b9e6f-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b9e6f-136">OUTPUTS</span></span>

### <span data-ttu-id="b9e6f-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="b9e6f-137">Microsoft.Azure.PowerShell.Cmdlets.MariaDb.Models.Api20180601Preview.IVirtualNetworkRule</span></span>

## <span data-ttu-id="b9e6f-138">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b9e6f-138">NOTES</span></span>

<span data-ttu-id="b9e6f-139">ALIASES</span><span class="sxs-lookup"><span data-stu-id="b9e6f-139">ALIASES</span></span>

<span data-ttu-id="b9e6f-140">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="b9e6f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9e6f-141">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9e6f-142">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9e6f-143">INPUTOBJECT <IMariaDbIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="b9e6f-143">INPUTOBJECT <IMariaDbIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9e6f-144">`[ConfigurationName <String>]`: имя конфигурации сервера.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-144">`[ConfigurationName <String>]`: The name of the server configuration.</span></span>
  - <span data-ttu-id="b9e6f-145">`[DatabaseName <String>]`: имя базы данных.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-145">`[DatabaseName <String>]`: The name of the database.</span></span>
  - <span data-ttu-id="b9e6f-146">`[FirewallRuleName <String>]`: имя правила брандмауэра сервера.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-146">`[FirewallRuleName <String>]`: The name of the server firewall rule.</span></span>
  - <span data-ttu-id="b9e6f-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="b9e6f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9e6f-148">`[LocationName <String>]`: название расположения.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-148">`[LocationName <String>]`: The name of the location.</span></span>
  - <span data-ttu-id="b9e6f-149">`[ResourceGroupName <String>]`: Имя группы ресурсов, которая содержит ресурс.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b9e6f-150">Это значение можно получить через API Диспетчера ресурсов Azure или на портале.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b9e6f-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: Имя политики оповещения системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-151">`[SecurityAlertPolicyName <SecurityAlertPolicyName?>]`: The name of the security alert policy.</span></span>
  - <span data-ttu-id="b9e6f-152">`[ServerName <String>]`: Имя сервера.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-152">`[ServerName <String>]`: The name of the server.</span></span>
  - <span data-ttu-id="b9e6f-153">`[SubscriptionId <String>]`. Идентификатор подписки, который определяет подписку Azure.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-153">`[SubscriptionId <String>]`: The subscription ID that identifies an Azure subscription.</span></span>
  - <span data-ttu-id="b9e6f-154">`[VirtualNetworkRuleName <String>]`: Имя виртуального правила сети.</span><span class="sxs-lookup"><span data-stu-id="b9e6f-154">`[VirtualNetworkRuleName <String>]`: The name of the virtual network rule.</span></span>

## <span data-ttu-id="b9e6f-155">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b9e6f-155">RELATED LINKS</span></span>

