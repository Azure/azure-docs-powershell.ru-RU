---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/enable-azaksaddon
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Enable-AzAksAddOn.md
ms.openlocfilehash: 1280f65659f986d0fd8402da0d3db5b1c5a92b58
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966952"
---
# <span data-ttu-id="cde76-101">Enable-AzAksAddOn</span><span class="sxs-lookup"><span data-stu-id="cde76-101">Enable-AzAksAddOn</span></span>

## <span data-ttu-id="cde76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde76-102">SYNOPSIS</span></span>
<span data-ttu-id="cde76-103">В включить надстройки для aks.</span><span class="sxs-lookup"><span data-stu-id="cde76-103">Enable the addons for aks.</span></span>

## <span data-ttu-id="cde76-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cde76-104">SYNTAX</span></span>

### <span data-ttu-id="cde76-105">defaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cde76-105">defaultParameterSet (Default)</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] [-ResourceGroupName] <String>
 [-ClusterName] <String> [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cde76-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cde76-106">InputObjectParameterSet</span></span>
```
Enable-AzAksAddOn [-WorkspaceResourceId <String>] [-SubnetName <String>] -ClusterObject <PSKubernetesCluster>
 [-Name <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cde76-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cde76-107">DESCRIPTION</span></span>
<span data-ttu-id="cde76-108">В включить надстройки для aks.</span><span class="sxs-lookup"><span data-stu-id="cde76-108">Enable the addons for aks.</span></span>

## <span data-ttu-id="cde76-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cde76-109">EXAMPLES</span></span>

### <span data-ttu-id="cde76-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cde76-110">Example 1</span></span>
```powershell
PS C:\> Get-AzAks -ResourceGroupName group -Name myCluster | Enable-AzAksAddon -Name HttpApplicationRouting,Monitoring,AzurePolicy,VirtualNode,KubeDashboard -WorkspaceResourceId xxxxx/xxxx -SubnetName subnet
```

<span data-ttu-id="cde76-111">В включить `HttpApplicationRouting` `Monitoring` надстройки, и для `AzurePolicy` `VirtualNode` `KubeDashboard` aks.</span><span class="sxs-lookup"><span data-stu-id="cde76-111">Enable the addons `HttpApplicationRouting`, `Monitoring`, `AzurePolicy`, `VirtualNode` and `KubeDashboard` for aks.</span></span>

## <span data-ttu-id="cde76-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cde76-112">PARAMETERS</span></span>

### <span data-ttu-id="cde76-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="cde76-113">-ClusterName</span></span>
<span data-ttu-id="cde76-114">Название кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cde76-114">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="cde76-115">-ClusterObject</span><span class="sxs-lookup"><span data-stu-id="cde76-115">-ClusterObject</span></span>
<span data-ttu-id="cde76-116">Объект PSKubernetesCluster, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="cde76-116">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="cde76-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde76-117">-DefaultProfile</span></span>
<span data-ttu-id="cde76-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cde76-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cde76-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cde76-119">-Name</span></span>
<span data-ttu-id="cde76-120">Название кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="cde76-120">Kubernetes managed cluster Name.</span></span>

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

### <span data-ttu-id="cde76-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cde76-121">-ResourceGroupName</span></span>
<span data-ttu-id="cde76-122">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cde76-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="cde76-123">-SubnetName</span><span class="sxs-lookup"><span data-stu-id="cde76-123">-SubnetName</span></span>
<span data-ttu-id="cde76-124">Имя подсети VirtualNode.</span><span class="sxs-lookup"><span data-stu-id="cde76-124">Subnet name of VirtualNode.</span></span>

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

### <span data-ttu-id="cde76-125">-WorkspaceResourceId</span><span class="sxs-lookup"><span data-stu-id="cde76-125">-WorkspaceResourceId</span></span>
<span data-ttu-id="cde76-126">ИД ресурса в рабочей области мониторинга.</span><span class="sxs-lookup"><span data-stu-id="cde76-126">Resource Id of the workspace of Monitoring.</span></span>

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

### <span data-ttu-id="cde76-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cde76-127">-Confirm</span></span>
<span data-ttu-id="cde76-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cde76-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cde76-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cde76-129">-WhatIf</span></span>
<span data-ttu-id="cde76-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cde76-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cde76-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cde76-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cde76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde76-132">CommonParameters</span></span>
<span data-ttu-id="cde76-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde76-134">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cde76-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde76-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cde76-135">INPUTS</span></span>

### <span data-ttu-id="cde76-136">System.String</span><span class="sxs-lookup"><span data-stu-id="cde76-136">System.String</span></span>

### <span data-ttu-id="cde76-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="cde76-137">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="cde76-138">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cde76-138">OUTPUTS</span></span>

### <span data-ttu-id="cde76-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="cde76-139">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

## <span data-ttu-id="cde76-140">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cde76-140">NOTES</span></span>

## <span data-ttu-id="cde76-141">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cde76-141">RELATED LINKS</span></span>
