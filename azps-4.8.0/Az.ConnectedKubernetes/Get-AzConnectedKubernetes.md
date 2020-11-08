---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/get-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Get-AzConnectedKubernetes.md
ms.openlocfilehash: 1df844fc9a040fe20b6fdcdaa6f5dccda191aba4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243396"
---
# <span data-ttu-id="44a27-101">Get-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="44a27-101">Get-AzConnectedKubernetes</span></span>

## <span data-ttu-id="44a27-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44a27-102">SYNOPSIS</span></span>
<span data-ttu-id="44a27-103">Возвращает свойства указанного подключенного кластера, включая имя, удостоверение, свойства и дополнительные сведения о кластере.</span><span class="sxs-lookup"><span data-stu-id="44a27-103">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="44a27-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44a27-104">SYNTAX</span></span>

### <span data-ttu-id="44a27-105">List1 (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44a27-105">List1 (Default)</span></span>
```
Get-AzConnectedKubernetes [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="44a27-106">Получить</span><span class="sxs-lookup"><span data-stu-id="44a27-106">Get</span></span>
```
Get-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="44a27-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="44a27-107">GetViaIdentity</span></span>
```
Get-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="44a27-108">Список</span><span class="sxs-lookup"><span data-stu-id="44a27-108">List</span></span>
```
Get-AzConnectedKubernetes -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="44a27-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44a27-109">DESCRIPTION</span></span>
<span data-ttu-id="44a27-110">Возвращает свойства указанного подключенного кластера, включая имя, удостоверение, свойства и дополнительные сведения о кластере.</span><span class="sxs-lookup"><span data-stu-id="44a27-110">Returns the properties of the specified connected cluster, including name, identity, properties, and additional cluster details.</span></span>

## <span data-ttu-id="44a27-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44a27-111">EXAMPLES</span></span>

### <span data-ttu-id="44a27-112">Пример 1: получение всех подключенных kubernetes в рамках подписки</span><span class="sxs-lookup"><span data-stu-id="44a27-112">Example 1: Get all connected kubernetes under a subscription</span></span>
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

<span data-ttu-id="44a27-113">Эта команда получает все подключенные kubernetes в рамках подписки.</span><span class="sxs-lookup"><span data-stu-id="44a27-113">This command gets all connected kubernetes under a subscription.</span></span>

### <span data-ttu-id="44a27-114">Пример 2: получение всех подключенных kubernetes в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="44a27-114">Example 2: Get all connected kubernetes under the resource group</span></span>
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

<span data-ttu-id="44a27-115">Эта команда получает все подключенные kubernetes в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44a27-115">This command gets all connected kubernetes under the resource group.</span></span>

### <span data-ttu-id="44a27-116">Пример 3: получение подключенного kubernetes</span><span class="sxs-lookup"><span data-stu-id="44a27-116">Example 3: Get a connected kubernetes</span></span>
```powershell
PS C:\> Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="44a27-117">Эта команда возвращает подключенный kubernetes.</span><span class="sxs-lookup"><span data-stu-id="44a27-117">This command gets a connected kubernetes.</span></span>

### <span data-ttu-id="44a27-118">Пример 4: получение подключенного kubernetes по объекту</span><span class="sxs-lookup"><span data-stu-id="44a27-118">Example 4: Get a connected kubernetes by object</span></span>
```powershell
PS C:\> $conAks = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -Name connected-pwsh-aks
PS C:\> Get-AzConnectedKubernetes -InputObject $conAks

Location Name             Type
-------- ----             ----
eastus   connected-pwsh-aks Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="44a27-119">Эта команда возвращает подключенный kubernetes по объекту.</span><span class="sxs-lookup"><span data-stu-id="44a27-119">This command gets a connected kubernetes by object.</span></span>

## <span data-ttu-id="44a27-120">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44a27-120">PARAMETERS</span></span>

### <span data-ttu-id="44a27-121">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="44a27-121">-ClusterName</span></span>
<span data-ttu-id="44a27-122">Имя кластера Kubernetes, в котором вызывается Get.</span><span class="sxs-lookup"><span data-stu-id="44a27-122">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="44a27-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44a27-123">-DefaultProfile</span></span>
<span data-ttu-id="44a27-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44a27-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44a27-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44a27-125">-InputObject</span></span>
<span data-ttu-id="44a27-126">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="44a27-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="44a27-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44a27-127">-ResourceGroupName</span></span>
<span data-ttu-id="44a27-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44a27-128">The name of the resource group.</span></span>
<span data-ttu-id="44a27-129">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="44a27-129">The name is case insensitive.</span></span>

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

### <span data-ttu-id="44a27-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44a27-130">-SubscriptionId</span></span>
<span data-ttu-id="44a27-131">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="44a27-131">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="44a27-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44a27-132">CommonParameters</span></span>
<span data-ttu-id="44a27-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44a27-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44a27-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44a27-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44a27-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44a27-135">INPUTS</span></span>

### <span data-ttu-id="44a27-136">Microsoft. Azure. PowerShell. командлеты. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="44a27-136">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="44a27-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44a27-137">OUTPUTS</span></span>

### <span data-ttu-id="44a27-138">Microsoft. Azure. PowerShell. командлеты. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="44a27-138">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="44a27-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="44a27-139">NOTES</span></span>

<span data-ttu-id="44a27-140">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="44a27-140">ALIASES</span></span>

<span data-ttu-id="44a27-141">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="44a27-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44a27-142">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="44a27-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44a27-143">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44a27-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44a27-144">INPUTOBJECT <IConnectedKubernetesIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="44a27-144">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44a27-145">`[ClusterName <String>]`: Имя кластера Kubernetes, в котором вызывается Get.</span><span class="sxs-lookup"><span data-stu-id="44a27-145">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="44a27-146">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="44a27-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44a27-147">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44a27-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="44a27-148">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="44a27-148">The name is case insensitive.</span></span>
  - <span data-ttu-id="44a27-149">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="44a27-149">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="44a27-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44a27-150">RELATED LINKS</span></span>

