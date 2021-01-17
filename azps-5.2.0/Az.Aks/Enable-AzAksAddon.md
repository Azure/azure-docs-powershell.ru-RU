---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddon.md
ms.openlocfilehash: de4453129ee626ac7eeeaa20fa14c1068011c001
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399447"
---
# <span data-ttu-id="464c3-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="464c3-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="464c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="464c3-102">SYNOPSIS</span></span>
<span data-ttu-id="464c3-103">В включить надстройки для aks.</span><span class="sxs-lookup"><span data-stu-id="464c3-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="464c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="464c3-104">SYNTAX</span></span>

### <span data-ttu-id="464c3-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="464c3-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="464c3-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="464c3-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="464c3-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="464c3-107">DESCRIPTION</span></span>
<span data-ttu-id="464c3-108">В включить надстройки для aks.</span><span class="sxs-lookup"><span data-stu-id="464c3-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="464c3-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="464c3-109">EXAMPLES</span></span>

### <span data-ttu-id="464c3-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="464c3-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="464c3-111">В включить `HttpApplicationRouting` `Monitoring` надстройки, и для `AzurePolicy` `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="464c3-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="464c3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="464c3-112">PARAMETERS</span></span>

### <span data-ttu-id="464c3-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="464c3-113">-ClusterName</span></span>
<span data-ttu-id="464c3-114">Название кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="464c3-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="464c3-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="464c3-115">-ClusterObject</span></span>
<span data-ttu-id="464c3-116">Объект PSKubernetesCluster, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="464c3-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="464c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="464c3-117">-DefaultProfile</span></span>
<span data-ttu-id="464c3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="464c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="464c3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="464c3-119">-Name</span></span>
<span data-ttu-id="464c3-120">Название кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="464c3-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="464c3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="464c3-121">-ResourceGroupName</span></span>
<span data-ttu-id="464c3-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="464c3-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="464c3-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="464c3-123">-SubnetName</span></span>
<span data-ttu-id="464c3-124">Имя подсети VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="464c3-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="464c3-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="464c3-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="464c3-126">ИД ресурса в рабочей области мониторинга.</span><span class="sxs-lookup"><span data-stu-id="464c3-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="464c3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="464c3-127">-Confirm</span></span>
<span data-ttu-id="464c3-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="464c3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="464c3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="464c3-129">-WhatIf</span></span>
<span data-ttu-id="464c3-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="464c3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="464c3-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="464c3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="464c3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="464c3-132">CommonParameters</span></span>
<span data-ttu-id="464c3-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="464c3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="464c3-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="464c3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="464c3-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="464c3-135">INPUTS</span></span>

### <span data-ttu-id="464c3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="464c3-136">System.String</span></span>

### <span data-ttu-id="464c3-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="464c3-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="464c3-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="464c3-138">OUTPUTS</span></span>

### <span data-ttu-id="464c3-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="464c3-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="464c3-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="464c3-140">NOTES</span></span>

## <span data-ttu-id="464c3-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="464c3-141">RELATED LINKS</span></span>
