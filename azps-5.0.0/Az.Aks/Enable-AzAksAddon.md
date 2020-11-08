---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247898"
---
# <span data-ttu-id="79c7b-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="79c7b-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="79c7b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="79c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="79c7b-103">Включите надстройки для AKS.</span><span class="sxs-lookup"><span data-stu-id="79c7b-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="79c7b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="79c7b-104">SYNTAX</span></span>

### <span data-ttu-id="79c7b-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79c7b-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79c7b-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79c7b-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79c7b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79c7b-107">DESCRIPTION</span></span>
<span data-ttu-id="79c7b-108">Включите надстройки для AKS.</span><span class="sxs-lookup"><span data-stu-id="79c7b-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="79c7b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="79c7b-109">EXAMPLES</span></span>

### <span data-ttu-id="79c7b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="79c7b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="79c7b-111">Включите надстройки `HttpApplicationRouting` ,, `Monitoring` `AzurePolicy` `VirtualNode` и `KubeDashboard` для AKS.</span><span class="sxs-lookup"><span data-stu-id="79c7b-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="79c7b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="79c7b-112">PARAMETERS</span></span>

### <span data-ttu-id="79c7b-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="79c7b-113">-ClusterName</span></span>
<span data-ttu-id="79c7b-114">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="79c7b-114">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c7b-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="79c7b-115">-ClusterObject</span></span>
<span data-ttu-id="79c7b-116">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="79c7b-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79c7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c7b-117">-DefaultProfile</span></span>
<span data-ttu-id="79c7b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79c7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c7b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="79c7b-119">-Name</span></span>
<span data-ttu-id="79c7b-120">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="79c7b-120">Kubernetes managed cluster Name.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c7b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79c7b-121">-ResourceGroupName</span></span>
<span data-ttu-id="79c7b-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79c7b-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: defaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c7b-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="79c7b-123">-SubnetName</span></span>
<span data-ttu-id="79c7b-124">Имя подсети VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="79c7b-124">Subnet name of VirtualNode.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c7b-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="79c7b-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="79c7b-126">Идентификатор ресурса рабочей области мониторинга.</span><span class="sxs-lookup"><span data-stu-id="79c7b-126">Resource Id of the workspace of Monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79c7b-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79c7b-127">-Confirm</span></span>
<span data-ttu-id="79c7b-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="79c7b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c7b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c7b-129">-WhatIf</span></span>
<span data-ttu-id="79c7b-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="79c7b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79c7b-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="79c7b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c7b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c7b-132">CommonParameters</span></span>
<span data-ttu-id="79c7b-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="79c7b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c7b-134">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79c7b-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c7b-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="79c7b-135">INPUTS</span></span>

### <span data-ttu-id="79c7b-136">System. String</span><span class="sxs-lookup"><span data-stu-id="79c7b-136">System.String</span></span>

### <span data-ttu-id="79c7b-137">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="79c7b-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="79c7b-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="79c7b-138">OUTPUTS</span></span>

### <span data-ttu-id="79c7b-139">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="79c7b-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="79c7b-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="79c7b-140">NOTES</span></span>

## <span data-ttu-id="79c7b-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79c7b-141">RELATED LINKS</span></span>
