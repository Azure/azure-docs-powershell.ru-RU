---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242709"
---
# <span data-ttu-id="72417-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="72417-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="72417-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72417-102">SYNOPSIS</span></span>
<span data-ttu-id="72417-103">Возвращает пиринг vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="72417-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="72417-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="72417-104">SYNTAX</span></span>

### <span data-ttu-id="72417-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="72417-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="72417-106">Получить</span><span class="sxs-lookup"><span data-stu-id="72417-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="72417-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="72417-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="72417-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="72417-108">DESCRIPTION</span></span>
<span data-ttu-id="72417-109">Возвращает пиринг vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="72417-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="72417-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="72417-110">EXAMPLES</span></span>

### <span data-ttu-id="72417-111">Пример 1. Список всех пиринга vnet, которые находятся в списках данных</span><span class="sxs-lookup"><span data-stu-id="72417-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="72417-112">В этой команде перечислены все пиринги vnet, которые находятся в списках данных.</span><span class="sxs-lookup"><span data-stu-id="72417-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="72417-113">Пример 2. Получить пиринг vnet</span><span class="sxs-lookup"><span data-stu-id="72417-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="72417-114">Эта команда возвращает пиринг vnet.</span><span class="sxs-lookup"><span data-stu-id="72417-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="72417-115">Пример 3. Получить пиринг vnet по объекту</span><span class="sxs-lookup"><span data-stu-id="72417-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="72417-116">Эта команда получает пиринг vnet по объектам.</span><span class="sxs-lookup"><span data-stu-id="72417-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="72417-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72417-117">PARAMETERS</span></span>

### <span data-ttu-id="72417-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72417-118">-DefaultProfile</span></span>
<span data-ttu-id="72417-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="72417-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72417-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="72417-120">-InputObject</span></span>
<span data-ttu-id="72417-121">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="72417-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="72417-122">-Name</span><span class="sxs-lookup"><span data-stu-id="72417-122">-Name</span></span>
<span data-ttu-id="72417-123">Имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="72417-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="72417-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="72417-124">-PassThru</span></span>
<span data-ttu-id="72417-125">Возвращает "Истина" в случае успешной команды.</span><span class="sxs-lookup"><span data-stu-id="72417-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72417-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72417-126">-ResourceGroupName</span></span>
<span data-ttu-id="72417-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72417-127">The name of the resource group.</span></span>
<span data-ttu-id="72417-128">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="72417-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="72417-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="72417-129">-SubscriptionId</span></span>
<span data-ttu-id="72417-130">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="72417-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="72417-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="72417-131">-WorkspaceName</span></span>
<span data-ttu-id="72417-132">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="72417-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="72417-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72417-133">CommonParameters</span></span>
<span data-ttu-id="72417-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72417-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72417-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="72417-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72417-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="72417-136">INPUTS</span></span>

### <span data-ttu-id="72417-137">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Models.IDatabоsIdentity</span><span class="sxs-lookup"><span data-stu-id="72417-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="72417-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="72417-138">OUTPUTS</span></span>

### <span data-ttu-id="72417-139">Microsoft.Azure.PowerShell.Cmdlets.Datab models.Api20180401.IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="72417-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="72417-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="72417-140">NOTES</span></span>

<span data-ttu-id="72417-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="72417-141">ALIASES</span></span>

<span data-ttu-id="72417-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="72417-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="72417-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="72417-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="72417-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="72417-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="72417-145">INPUTOBJECT <IDatabricksIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="72417-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="72417-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="72417-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="72417-147">`[PeeringName <String>]`: имя пиринга vNet рабочей области.</span><span class="sxs-lookup"><span data-stu-id="72417-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="72417-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="72417-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="72417-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="72417-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="72417-150">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="72417-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="72417-151">`[WorkspaceName <String>]`: имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="72417-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="72417-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="72417-152">RELATED LINKS</span></span>

