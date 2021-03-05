---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: da4cd54b9865cdf30487a7e49e5581474ebb2a35
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012531"
---
# <span data-ttu-id="6cc4a-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="6cc4a-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="6cc4a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6cc4a-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc4a-103">Возвращает свойства указанного подключенного кластера, включая имя, удостоверение, свойства и дополнительные сведения о кластере.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="6cc4a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6cc4a-104">SYNTAX</span></span>

### <span data-ttu-id="6cc4a-105">Список1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6cc4a-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6cc4a-106">Получить</span><span class="sxs-lookup"><span data-stu-id="6cc4a-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6cc4a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6cc4a-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="6cc4a-108">Список</span><span class="sxs-lookup"><span data-stu-id="6cc4a-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6cc4a-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6cc4a-109">DESCRIPTION</span></span>
<span data-ttu-id="6cc4a-110">Возвращает свойства указанного подключенного кластера, включая имя, удостоверение, свойства и дополнительные сведения о кластере.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="6cc4a-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6cc4a-111">EXAMPLES</span></span>

### <span data-ttu-id="6cc4a-112">Пример 1. Все подключенные к интернету сети в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="6cc4a-112">Example 1: Get all connected kubernetes under a subscription</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6cc4a-113">Эта команда получает все подключенные к подписке куберсети.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="6cc4a-114">Пример 2. Все подключенные к кубберсети в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="6cc4a-114">Example 2: Get all connected kubernetes under the resource group</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks

Location Name              Type
-------- ----              ----
eastus   connected-aks       Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks  Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks1 Microsoft.Kubernetes/connectedClusters
eastus   connected-pwsh-aks3 Microsoft.Kubernetes/connectedClusters
eastus   connected-aks-cli1  Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6cc4a-115">Эта команда получает все подключенные к группе ресурсов куберсети.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="6cc4a-116">Пример 3. Подключение к кубберсетям</span><span class="sxs-lookup"><span data-stu-id="6cc4a-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6cc4a-117">Эта команда получает подключенные куберсети.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="6cc4a-118">Пример 4. Подключение к кубберсетям по объектам</span><span class="sxs-lookup"><span data-stu-id="6cc4a-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="6cc4a-119">Эта команда получает подключенные к объекту куберсети.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="6cc4a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6cc4a-120">PARAMETERS</span></span>

### <span data-ttu-id="6cc4a-121">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="6cc4a-121">-ClusterName</span></span>
<span data-ttu-id="6cc4a-122">Название кластера "Кубберсети", на котором он называется.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-122">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc4a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cc4a-123">-DefaultProfile</span></span>
<span data-ttu-id="6cc4a-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6cc4a-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6cc4a-125">-InputObject</span></span>
<span data-ttu-id="6cc4a-126">Параметр identity To построить, см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc4a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc4a-127">-ResourceGroupName</span></span>
<span data-ttu-id="6cc4a-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-128">The name of the resource group.</span></span>
<span data-ttu-id="6cc4a-129">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="6cc4a-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6cc4a-130">-SubscriptionId</span></span>
<span data-ttu-id="6cc4a-131">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="6cc4a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc4a-132">CommonParameters</span></span>
<span data-ttu-id="6cc4a-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc4a-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6cc4a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc4a-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6cc4a-135">INPUTS</span></span>

### <span data-ttu-id="6cc4a-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="6cc4a-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="6cc4a-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6cc4a-137">OUTPUTS</span></span>

### <span data-ttu-id="6cc4a-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="6cc4a-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api20210301.IConnectedCluster</span></span>

## <span data-ttu-id="6cc4a-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6cc4a-139">NOTES</span></span>

<span data-ttu-id="6cc4a-140">ALIASES</span><span class="sxs-lookup"><span data-stu-id="6cc4a-140">ALIASES</span></span>

<span data-ttu-id="6cc4a-141">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="6cc4a-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6cc4a-142">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6cc4a-143">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6cc4a-144">INPUTOBJECT <IConnectedKubernetesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="6cc4a-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6cc4a-145">`[ClusterName <String>]`Название кластера "Кубберсети", на котором он называется.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="6cc4a-146">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="6cc4a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6cc4a-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="6cc4a-148">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="6cc4a-149">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="6cc4a-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="6cc4a-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6cc4a-150">RELATED LINKS</span></span>

