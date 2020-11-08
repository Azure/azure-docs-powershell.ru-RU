---
external help file: ''
Module Name: Az.Databricks
online version: https://docs.microsoft.com/en-us/powershell/module/az.databricks/get-azdatabricksvnetpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Databricks/help/Get-AzDatabricksVNetPeering.md
ms.openlocfilehash: d5078ac91627cdf9f7b57801e3b7a958b9bd776e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243633"
---
# <span data-ttu-id="35439-101">Get-AzDatabricksVNetPeering</span><span class="sxs-lookup"><span data-stu-id="35439-101">Get-AzDatabricksVNetPeering</span></span>

## <span data-ttu-id="35439-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35439-102">SYNOPSIS</span></span>
<span data-ttu-id="35439-103">Получает одноранговую сеть виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="35439-103">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="35439-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35439-104">SYNTAX</span></span>

### <span data-ttu-id="35439-105">Список (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35439-105">List (Default)</span></span>
```
Get-AzDatabricksVNetPeering -ResourceGroupName <String> -WorkspaceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="35439-106">Получить</span><span class="sxs-lookup"><span data-stu-id="35439-106">Get</span></span>
```
Get-AzDatabricksVNetPeering -Name <String> -ResourceGroupName <String> -WorkspaceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="35439-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35439-107">GetViaIdentity</span></span>
```
Get-AzDatabricksVNetPeering -InputObject <IDatabricksIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="35439-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35439-108">DESCRIPTION</span></span>
<span data-ttu-id="35439-109">Получает одноранговую сеть виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="35439-109">Gets the workspace vNet Peering.</span></span>

## <span data-ttu-id="35439-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35439-110">EXAMPLES</span></span>

### <span data-ttu-id="35439-111">Пример 1: список всех одноранговых элементов виртуальной сети в модулях</span><span class="sxs-lookup"><span data-stu-id="35439-111">Example 1: List all vnet peering under a databricks</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test

Name            Type
----            ----
vnetpeering-t01
vnetpeering-t02
```

<span data-ttu-id="35439-112">Эта команда выводит список одноранговых элементов виртуальной сети в модулях.</span><span class="sxs-lookup"><span data-stu-id="35439-112">This command lists all vnet peering under a databricks.</span></span>

### <span data-ttu-id="35439-113">Пример 2: получение одноранговой сети vnet</span><span class="sxs-lookup"><span data-stu-id="35439-113">Example 2: Get a vnet peering</span></span>
```powershell
PS C:\> Get-AzDatabricksVNetPeering -ResourceGroupName lucas-manual-test -WorkspaceName databricks-test01 -PeeringName MyPeering-test01

Name             Type
----             ----
MyPeering-test01
```

<span data-ttu-id="35439-114">Эта команда получает одноранговый элемент vnet.</span><span class="sxs-lookup"><span data-stu-id="35439-114">This command gets a vnet peering.</span></span>

### <span data-ttu-id="35439-115">Пример 3: получение однорангового соединения vnet по объекту</span><span class="sxs-lookup"><span data-stu-id="35439-115">Example 3: Get a vnet peering by object</span></span>
```powershell
PS C:\> New-AzDatabricksVNetPeering -Name vnetpeering-t02 -WorkspaceName databricks-test01 -ResourceGroupName lucas-manual-test -RemoteVirtualNetworkId '/subscriptions/xxxxx-xxxx-xxx-xxxxx/resourceGroups/azure-manual-test/providers/Microsoft.Network/virtualNetworks/vnet-test02' | Get-AzDatabricksVNetPeering

Name            Type
----            ----
vnetpeering-t02
```

<span data-ttu-id="35439-116">Эта команда получает одноранговый элемент vnet по объекту.</span><span class="sxs-lookup"><span data-stu-id="35439-116">This command gets a vnet peering by object.</span></span>

## <span data-ttu-id="35439-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35439-117">PARAMETERS</span></span>

### <span data-ttu-id="35439-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35439-118">-DefaultProfile</span></span>
<span data-ttu-id="35439-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35439-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35439-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35439-120">-InputObject</span></span>
<span data-ttu-id="35439-121">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="35439-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35439-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35439-122">-Name</span></span>
<span data-ttu-id="35439-123">Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="35439-123">The name of the workspace vNet peering.</span></span>

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

### <span data-ttu-id="35439-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35439-124">-PassThru</span></span>
<span data-ttu-id="35439-125">Возвращает значение истина, если команда выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="35439-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="35439-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35439-126">-ResourceGroupName</span></span>
<span data-ttu-id="35439-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35439-127">The name of the resource group.</span></span>
<span data-ttu-id="35439-128">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="35439-128">The name is case insensitive.</span></span>

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

### <span data-ttu-id="35439-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35439-129">-SubscriptionId</span></span>
<span data-ttu-id="35439-130">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="35439-130">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="35439-131">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="35439-131">-WorkspaceName</span></span>
<span data-ttu-id="35439-132">Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="35439-132">The name of the workspace.</span></span>

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

### <span data-ttu-id="35439-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35439-133">CommonParameters</span></span>
<span data-ttu-id="35439-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35439-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35439-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35439-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35439-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35439-136">INPUTS</span></span>

### <span data-ttu-id="35439-137">Microsoft. Azure. PowerShell. командлеты. кирпичи. Models. IDatabricksIdentity</span><span class="sxs-lookup"><span data-stu-id="35439-137">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.IDatabricksIdentity</span></span>

## <span data-ttu-id="35439-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35439-138">OUTPUTS</span></span>

### <span data-ttu-id="35439-139">Microsoft. Azure. PowerShell. командлеты. кирпичи. Api20180401. IVirtualNetworkPeering</span><span class="sxs-lookup"><span data-stu-id="35439-139">Microsoft.Azure.PowerShell.Cmdlets.Databricks.Models.Api20180401.IVirtualNetworkPeering</span></span>

## <span data-ttu-id="35439-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="35439-140">NOTES</span></span>

<span data-ttu-id="35439-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="35439-141">ALIASES</span></span>

<span data-ttu-id="35439-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="35439-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="35439-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="35439-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35439-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35439-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="35439-145">INPUTOBJECT <IDatabricksIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="35439-145">INPUTOBJECT <IDatabricksIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35439-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="35439-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35439-147">`[PeeringName <String>]`: Имя одноранговой сети виртуальной среды.</span><span class="sxs-lookup"><span data-stu-id="35439-147">`[PeeringName <String>]`: The name of the workspace vNet peering.</span></span>
  - <span data-ttu-id="35439-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35439-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="35439-149">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="35439-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="35439-150">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="35439-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>
  - <span data-ttu-id="35439-151">`[WorkspaceName <String>]`: Имя рабочей области.</span><span class="sxs-lookup"><span data-stu-id="35439-151">`[WorkspaceName <String>]`: The name of the workspace.</span></span>

## <span data-ttu-id="35439-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35439-152">RELATED LINKS</span></span>

