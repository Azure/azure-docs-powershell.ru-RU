---
external help file: ''
Module Name: Az.ConnectedKubernetes
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedkubernetes/update-azconnectedkubernetes
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedKubernetes/help/Update-AzConnectedKubernetes.md
ms.openlocfilehash: 2913a4288bad6c1cb8c908d80b8c751a08483a8b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235629"
---
# <span data-ttu-id="53837-101">Update-AzConnectedKubernetes</span><span class="sxs-lookup"><span data-stu-id="53837-101">Update-AzConnectedKubernetes</span></span>

## <span data-ttu-id="53837-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="53837-102">SYNOPSIS</span></span>
<span data-ttu-id="53837-103">API для обновления некоторых свойств подключенного ресурса кластера</span><span class="sxs-lookup"><span data-stu-id="53837-103">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="53837-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="53837-104">SYNTAX</span></span>

### <span data-ttu-id="53837-105">UpdateExpanded (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="53837-105">UpdateExpanded (Default)</span></span>
```
Update-AzConnectedKubernetes -ClusterName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="53837-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="53837-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzConnectedKubernetes -InputObject <IConnectedKubernetesIdentity> [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="53837-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="53837-107">DESCRIPTION</span></span>
<span data-ttu-id="53837-108">API для обновления некоторых свойств подключенного ресурса кластера</span><span class="sxs-lookup"><span data-stu-id="53837-108">API to update certain properties of the connected cluster resource</span></span>

## <span data-ttu-id="53837-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="53837-109">EXAMPLES</span></span>

### <span data-ttu-id="53837-110">Пример 1: обновление подключенного kubernetes</span><span class="sxs-lookup"><span data-stu-id="53837-110">Example 1: Update a connected kubernetes</span></span>
```powershell
PS C:\> Update-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t01 -Tag @{'key'='1'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t01 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="53837-111">Эта команда обновляет подключенный kubernetes.</span><span class="sxs-lookup"><span data-stu-id="53837-111">This command updates a connected kubernetes.</span></span>

### <span data-ttu-id="53837-112">Пример 2: обновление подключенного kubernetes по объекту</span><span class="sxs-lookup"><span data-stu-id="53837-112">Example 2: Update a connected kubernetes by object</span></span>
```powershell
PS C:\> $conn = Get-AzConnectedKubernetes -ResourceGroupName connected-aks -ClusterName ps-connaks-t03
PS C:\> Update-AzConnectedKubernetes -InputObject $conn -Tag @{'key'='2'}

Location Name           Type
-------- ----           ----
eastus   ps-connaks-t03 Microsoft.Kubernetes/connectedClusters
```

<span data-ttu-id="53837-113">Эта команда обновляет подключенный kubernetes по объекту.</span><span class="sxs-lookup"><span data-stu-id="53837-113">This command updates a connected kubernetes by object.</span></span>

## <span data-ttu-id="53837-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="53837-114">PARAMETERS</span></span>

### <span data-ttu-id="53837-115">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="53837-115">-ClusterName</span></span>
<span data-ttu-id="53837-116">Имя кластера Kubernetes, в котором вызывается Get.</span><span class="sxs-lookup"><span data-stu-id="53837-116">The name of the Kubernetes cluster on which get is called.</span></span>

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

### <span data-ttu-id="53837-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53837-117">-DefaultProfile</span></span>
<span data-ttu-id="53837-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="53837-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="53837-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53837-119">-InputObject</span></span>
<span data-ttu-id="53837-120">Параметр идентификатора для создания щелкните раздел заметок для свойств INPUTOBJECT и создайте хэш-таблицу.</span><span class="sxs-lookup"><span data-stu-id="53837-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="53837-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53837-121">-ResourceGroupName</span></span>
<span data-ttu-id="53837-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53837-122">The name of the resource group.</span></span>
<span data-ttu-id="53837-123">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="53837-123">The name is case insensitive.</span></span>

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

### <span data-ttu-id="53837-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="53837-124">-SubscriptionId</span></span>
<span data-ttu-id="53837-125">Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="53837-125">The ID of the target subscription.</span></span>

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

### <span data-ttu-id="53837-126">-Тег</span><span class="sxs-lookup"><span data-stu-id="53837-126">-Tag</span></span>
<span data-ttu-id="53837-127">Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53837-127">Resource tags.</span></span>

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

### <span data-ttu-id="53837-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53837-128">-Confirm</span></span>
<span data-ttu-id="53837-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="53837-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53837-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53837-130">-WhatIf</span></span>
<span data-ttu-id="53837-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="53837-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53837-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="53837-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53837-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53837-133">CommonParameters</span></span>
<span data-ttu-id="53837-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="53837-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53837-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53837-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53837-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="53837-136">INPUTS</span></span>

### <span data-ttu-id="53837-137">Microsoft. Azure. PowerShell. командлеты. ConnectedKubernetes. Models. IConnectedKubernetesIdentity</span><span class="sxs-lookup"><span data-stu-id="53837-137">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.IConnectedKubernetesIdentity</span></span>

## <span data-ttu-id="53837-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="53837-138">OUTPUTS</span></span>

### <span data-ttu-id="53837-139">Microsoft. Azure. PowerShell. командлеты. ConnectedKubernetes. Models. Api202001Preview. IConnectedCluster</span><span class="sxs-lookup"><span data-stu-id="53837-139">Microsoft.Azure.PowerShell.Cmdlets.ConnectedKubernetes.Models.Api202001Preview.IConnectedCluster</span></span>

## <span data-ttu-id="53837-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="53837-140">NOTES</span></span>

<span data-ttu-id="53837-141">СВЯЗЫВАЮТ</span><span class="sxs-lookup"><span data-stu-id="53837-141">ALIASES</span></span>

<span data-ttu-id="53837-142">СВОЙСТВА СЛОЖНЫХ ПАРАМЕТРОВ</span><span class="sxs-lookup"><span data-stu-id="53837-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="53837-143">Чтобы создать параметры, описанные ниже, создайте хэш-таблицу, содержащую соответствующие свойства.</span><span class="sxs-lookup"><span data-stu-id="53837-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="53837-144">Для получения сведений о хэш-таблицах запустите Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="53837-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="53837-145">INPUTOBJECT <IConnectedKubernetesIdentity> : параметр Identity</span><span class="sxs-lookup"><span data-stu-id="53837-145">INPUTOBJECT <IConnectedKubernetesIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="53837-146">`[ClusterName <String>]`: Имя кластера Kubernetes, в котором вызывается Get.</span><span class="sxs-lookup"><span data-stu-id="53837-146">`[ClusterName <String>]`: The name of the Kubernetes cluster on which get is called.</span></span>
  - <span data-ttu-id="53837-147">`[Id <String>]`: Путь к удостоверению ресурса</span><span class="sxs-lookup"><span data-stu-id="53837-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="53837-148">`[ResourceGroupName <String>]`: Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="53837-148">`[ResourceGroupName <String>]`: The name of the resource group.</span></span> <span data-ttu-id="53837-149">Имя не учитывает регистр.</span><span class="sxs-lookup"><span data-stu-id="53837-149">The name is case insensitive.</span></span>
  - <span data-ttu-id="53837-150">`[SubscriptionId <String>]`: Идентификатор целевой подписки.</span><span class="sxs-lookup"><span data-stu-id="53837-150">`[SubscriptionId <String>]`: The ID of the target subscription.</span></span>

## <span data-ttu-id="53837-151">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="53837-151">RELATED LINKS</span></span>

