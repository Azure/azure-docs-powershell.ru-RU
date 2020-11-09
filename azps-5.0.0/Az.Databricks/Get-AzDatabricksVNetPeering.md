---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312848"
---
# <span data-ttu-id="5c86c-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="5c86c-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="5c86c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c86c-102">SYNOPSIS</span></span>
<span data-ttu-id="5c86c-103">Получает одноранговую сеть виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="5c86c-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="5c86c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c86c-104">SYNTAX</span></span>

### <span data-ttu-id="5c86c-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c86c-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5c86c-106">Получить</span><span class="sxs-lookup"><span data-stu-id="5c86c-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5c86c-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5c86c-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="5c86c-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c86c-108">DESCRIPTION</span></span>
<span data-ttu-id="5c86c-109">Получает одноранговую сеть виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="5c86c-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="5c86c-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c86c-110">EXAMPLES</span></span>

### <span data-ttu-id="5c86c-111">Пример 1: список всех одноранговых элементов виртуальной сети в модулях</span><span class="sxs-lookup"><span data-stu-id="5c86c-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="5c86c-112">Эта команда выводит список одноранговых элементов виртуальной сети в модулях.</span><span class="sxs-lookup"><span data-stu-id="5c86c-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="5c86c-113">Пример 2: получение одноранговой сети vnet</span><span class="sxs-lookup"><span data-stu-id="5c86c-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="5c86c-114">Эта команда получает одноранговый элемент vnet.</span><span class="sxs-lookup"><span data-stu-id="5c86c-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="5c86c-115">Пример 3: получение однорангового соединения vnet по объекту</span><span class="sxs-lookup"><span data-stu-id="5c86c-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="5c86c-116">Эта команда получает одноранговый элемент vnet по объекту.</span><span class="sxs-lookup"><span data-stu-id="5c86c-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="5c86c-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c86c-117">PARAMETERS</span></span>

### <span data-ttu-id="5c86c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c86c-118">-DefaultProfile</span></span>
<span data-ttu-id="5c86c-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c86c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c86c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c86c-120">-InputObject</span></span>
<span data-ttu-id="5c86c-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="5c86c-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5c86c-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="5c86c-122">-Name</span></span>
<span data-ttu-id="5c86c-123">Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="5c86c-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="5c86c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c86c-124">-PassThru</span></span>
<span data-ttu-id="5c86c-125">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="5c86c-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5c86c-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c86c-126">-ResourceGroupName</span></span>
<span data-ttu-id="5c86c-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c86c-127">The name of the resource group.</span></span>
<span data-ttu-id="5c86c-128">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="5c86c-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="5c86c-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5c86c-129">-SubscriptionId</span></span>
<span data-ttu-id="5c86c-130">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5c86c-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="5c86c-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5c86c-131">-WorkspaceName</span></span>
<span data-ttu-id="5c86c-132">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5c86c-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="5c86c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c86c-133">CommonParameters</span></span>
<span data-ttu-id="5c86c-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c86c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c86c-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c86c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c86c-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c86c-136">INPUTS</span></span>

### <span data-ttu-id="5c86c-137">Microsoft. Azure. PowerShell. командлеты. кирпичи. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="5c86c-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="5c86c-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c86c-138">OUTPUTS</span></span>

### <span data-ttu-id="5c86c-139">Microsoft. Azure. PowerShell. командлеты. кирпичи. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="5c86c-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="5c86c-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c86c-140">NOTES</span></span>

<span data-ttu-id="5c86c-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="5c86c-141">ALIASES</span></span>

<span data-ttu-id="5c86c-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="5c86c-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="5c86c-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="5c86c-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5c86c-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="5c86c-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="5c86c-145">INPUTOBJECT <IDatabricksIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="5c86c-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5c86c-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="5c86c-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5c86c-147">`[PeeringName <String>]`: Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="5c86c-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="5c86c-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5c86c-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="5c86c-149">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="5c86c-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="5c86c-150">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="5c86c-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="5c86c-151">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="5c86c-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="5c86c-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c86c-152">RELATED LINKS</span></span>

