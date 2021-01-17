---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98415815"
---
# <span data-ttu-id="2884e-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="2884e-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="2884e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2884e-102">SYNOPSIS</span></span>
<span data-ttu-id="2884e-103">API для обновления определенных свойств подключенного ресурса кластера</span><span class="sxs-lookup"><span data-stu-id="2884e-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="2884e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2884e-104">SYNTAX</span></span>

### <span data-ttu-id="2884e-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2884e-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2884e-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2884e-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2884e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2884e-107">DESCRIPTION</span></span>
<span data-ttu-id="2884e-108">API для обновления определенных свойств подключенного ресурса кластера</span><span class="sxs-lookup"><span data-stu-id="2884e-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="2884e-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2884e-109">EXAMPLES</span></span>

### <span data-ttu-id="2884e-110">Пример 1. Обновление подключенных куберсетей</span><span class="sxs-lookup"><span data-stu-id="2884e-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="2884e-111">Эта команда обновляет подключенные куберсети.</span><span class="sxs-lookup"><span data-stu-id="2884e-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="2884e-112">Пример 2. Обновление подключенных куберсетей с помощью объекта</span><span class="sxs-lookup"><span data-stu-id="2884e-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="2884e-113">Эта команда обновляет подключенные к объектам куберсети.</span><span class="sxs-lookup"><span data-stu-id="2884e-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="2884e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2884e-114">PARAMETERS</span></span>

### <span data-ttu-id="2884e-115">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="2884e-115">-ClusterName</span></span>
<span data-ttu-id="2884e-116">Название кластера "Кубберсети", на котором он называется.</span><span class="sxs-lookup"><span data-stu-id="2884e-116">The name of the Kubernetes cluster on which get is called.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2884e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2884e-117">-DefaultProfile</span></span>
<span data-ttu-id="2884e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2884e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2884e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2884e-119">-InputObject</span></span>
<span data-ttu-id="2884e-120">Параметр Identity To construct (Параметр identity To construct), см. раздел NOTES для свойств INPUTOBJECT и создание hash table.</span><span class="sxs-lookup"><span data-stu-id="2884e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2884e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2884e-121">-ResourceGroupName</span></span>
<span data-ttu-id="2884e-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2884e-122">The name of the resource group.</span></span>
<span data-ttu-id="2884e-123">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="2884e-123">The name is case insensitive.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2884e-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2884e-124">-SubscriptionId</span></span>
<span data-ttu-id="2884e-125">ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="2884e-125">The ID of the target subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2884e-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="2884e-126">-Tag</span></span>
<span data-ttu-id="2884e-127">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2884e-127">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2884e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2884e-128">-Confirm</span></span>
<span data-ttu-id="2884e-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="2884e-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2884e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2884e-130">-WhatIf</span></span>
<span data-ttu-id="2884e-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2884e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2884e-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="2884e-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2884e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2884e-133">CommonParameters</span></span>
<span data-ttu-id="2884e-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2884e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2884e-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2884e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2884e-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2884e-136">INPUTS</span></span>

### <span data-ttu-id="2884e-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="2884e-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="2884e-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2884e-138">OUTPUTS</span></span>

### <span data-ttu-id="2884e-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="2884e-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="2884e-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2884e-140">NOTES</span></span>

<span data-ttu-id="2884e-141">ALIASES</span><span class="sxs-lookup"><span data-stu-id="2884e-141">ALIASES</span></span>

<span data-ttu-id="2884e-142">СЛОЖНЫЕ СВОЙСТВА ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="2884e-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="2884e-143">Чтобы создать описанные ниже параметры, создайте hash table, содержащую нужные свойства.</span><span class="sxs-lookup"><span data-stu-id="2884e-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2884e-144">Чтобы получить сведения о hash tables, запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="2884e-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="2884e-145">INPUTOBJECT <IConnectedKubernetesIdentity> : Параметр identity</span><span class="sxs-lookup"><span data-stu-id="2884e-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2884e-146">`[ClusterName <String>]`Название кластера "Кубберсети", на котором он называется.</span><span class="sxs-lookup"><span data-stu-id="2884e-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="2884e-147">`[Id <String>]`: путь удостоверения ресурса</span><span class="sxs-lookup"><span data-stu-id="2884e-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2884e-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2884e-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="2884e-149">Имя нечувствительно к делу.</span><span class="sxs-lookup"><span data-stu-id="2884e-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="2884e-150">`[SubscriptionId <String>]`: ИД целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="2884e-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="2884e-151">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2884e-151">RELATED LINKS</span></span>

