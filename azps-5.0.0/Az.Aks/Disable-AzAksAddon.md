---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddon.md
ms.openlocfilehash: 0fca409546822ef596897adbbf755a1a4ae43e38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319397"
---
# <span data-ttu-id="fc8ba-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="fc8ba-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="fc8ba-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fc8ba-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8ba-103">Отключите надстройки для AKS.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="fc8ba-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fc8ba-104">SYNTAX</span></span>

### <span data-ttu-id="fc8ba-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fc8ba-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc8ba-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc8ba-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc8ba-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc8ba-107">DESCRIPTION</span></span>
<span data-ttu-id="fc8ba-108">Отключите надстройки для AKS.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="fc8ba-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fc8ba-109">EXAMPLES</span></span>

### <span data-ttu-id="fc8ba-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fc8ba-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="fc8ba-111">Отключите надстройки `HttpApplicationRouting` , `Monitoring` а также `AzurePolicy` `VirtualNode` и `KubeDashboard` для AKS.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="fc8ba-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fc8ba-112">PARAMETERS</span></span>

### <span data-ttu-id="fc8ba-113">-Имя_кластера</span><span class="sxs-lookup"><span data-stu-id="fc8ba-113">-ClusterName</span></span>
<span data-ttu-id="fc8ba-114">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="fc8ba-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="fc8ba-115">-ClusterObject</span></span>
<span data-ttu-id="fc8ba-116">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="fc8ba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8ba-117">-DefaultProfile</span></span>
<span data-ttu-id="fc8ba-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc8ba-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fc8ba-119">-Name</span></span>
<span data-ttu-id="fc8ba-120">Имя управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="fc8ba-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc8ba-121">-ResourceGroupName</span></span>
<span data-ttu-id="fc8ba-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="fc8ba-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc8ba-123">-Confirm</span></span>
<span data-ttu-id="fc8ba-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc8ba-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc8ba-125">-WhatIf</span></span>
<span data-ttu-id="fc8ba-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc8ba-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc8ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8ba-128">CommonParameters</span></span>
<span data-ttu-id="fc8ba-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fc8ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8ba-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc8ba-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8ba-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fc8ba-131">INPUTS</span></span>

### <span data-ttu-id="fc8ba-132">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fc8ba-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="fc8ba-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fc8ba-133">System.String</span></span>

## <span data-ttu-id="fc8ba-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fc8ba-134">OUTPUTS</span></span>

### <span data-ttu-id="fc8ba-135">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="fc8ba-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="fc8ba-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="fc8ba-136">NOTES</span></span>

## <span data-ttu-id="fc8ba-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fc8ba-137">RELATED LINKS</span></span>