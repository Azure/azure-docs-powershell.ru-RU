---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/disable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Disable-AzAksAddOn.md
ms.openlocfilehash: 616695e60d945e545cfbb8c1b2fb7ba81ae9caa5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100224468"
---
# <span data-ttu-id="c4562-101">Disable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="c4562-101">Disable-AzAksAddOn</span></span>

## <span data-ttu-id="c4562-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4562-102">SYNOPSIS</span></span>
<span data-ttu-id="c4562-103">Отключать надстройки для aks.</span><span class="sxs-lookup"><span data-stu-id="c4562-103">Disable the addons for aks.</span></span>

## <span data-ttu-id="c4562-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c4562-104">SYNTAX</span></span>

### <span data-ttu-id="c4562-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c4562-105">defaultParameterSet (Default)</span></span>
```
Disable-AzAksAddOn [-ResourceGroupName] <String> [-ClusterName] <String> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4562-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4562-106">InputObjectParameterSet</span></span>
```
Disable-AzAksAddOn -ClusterObject <PSKubernetesCluster> [-Name <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4562-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c4562-107">DESCRIPTION</span></span>
<span data-ttu-id="c4562-108">Отключать надстройки для aks.</span><span class="sxs-lookup"><span data-stu-id="c4562-108">Disable the addons for aks.</span></span>

## <span data-ttu-id="c4562-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c4562-109">EXAMPLES</span></span>

### <span data-ttu-id="c4562-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c4562-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Disable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard
```

<span data-ttu-id="c4562-111">Отключать `HttpApplicationRouting` `Monitoring` надстройки, и для `AzurePolicy` `VirtualNode` `KubeDashboard` ака.</span><span class="sxs-lookup"><span data-stu-id="c4562-111">Disable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="c4562-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4562-112">PARAMETERS</span></span>

### <span data-ttu-id="c4562-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c4562-113">-ClusterName</span></span>
<span data-ttu-id="c4562-114">Название кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c4562-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="c4562-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="c4562-115">-ClusterObject</span></span>
<span data-ttu-id="c4562-116">Объект PSKubernetesCluster, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="c4562-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="c4562-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4562-117">-DefaultProfile</span></span>
<span data-ttu-id="c4562-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c4562-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4562-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c4562-119">-Name</span></span>
<span data-ttu-id="c4562-120">Название кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="c4562-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="c4562-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c4562-121">-ResourceGroupName</span></span>
<span data-ttu-id="c4562-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c4562-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="c4562-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4562-123">-Confirm</span></span>
<span data-ttu-id="c4562-124">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c4562-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4562-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4562-125">-WhatIf</span></span>
<span data-ttu-id="c4562-126">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4562-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4562-127">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c4562-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4562-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4562-128">CommonParameters</span></span>
<span data-ttu-id="c4562-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4562-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4562-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c4562-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4562-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c4562-131">INPUTS</span></span>

### <span data-ttu-id="c4562-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c4562-132">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="c4562-133">System.String</span><span class="sxs-lookup"><span data-stu-id="c4562-133">System.String</span></span>

## <span data-ttu-id="c4562-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c4562-134">OUTPUTS</span></span>

### <span data-ttu-id="c4562-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="c4562-135">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="c4562-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c4562-136">NOTES</span></span>

## <span data-ttu-id="c4562-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c4562-137">RELATED LINKS</span></span>
