---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: 0f0a1c530e4f02e031307006c0e6bf994f9a7c5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963347"
---
# <span data-ttu-id="8d679-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="8d679-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="8d679-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d679-102">SYNOPSIS</span></span>
<span data-ttu-id="8d679-103">Удалите управляемый кластер Кубберсетей.</span><span class="sxs-lookup"><span data-stu-id="8d679-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="8d679-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8d679-104">SYNTAX</span></span>

### <span data-ttu-id="8d679-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8d679-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d679-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d679-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d679-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8d679-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d679-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d679-108">DESCRIPTION</span></span>
<span data-ttu-id="8d679-109">Удалите управляемый кластер Кубберсетей.</span><span class="sxs-lookup"><span data-stu-id="8d679-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="8d679-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8d679-110">EXAMPLES</span></span>

### <span data-ttu-id="8d679-111">Удаление существующего управляемого кластера "Кубберсети"</span><span class="sxs-lookup"><span data-stu-id="8d679-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="8d679-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d679-112">PARAMETERS</span></span>

### <span data-ttu-id="8d679-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8d679-113">-AsJob</span></span>
<span data-ttu-id="8d679-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8d679-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d679-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d679-115">-DefaultProfile</span></span>
<span data-ttu-id="8d679-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d679-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d679-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8d679-117">-Force</span></span>
<span data-ttu-id="8d679-118">Удаление управляемого кластера "Кубберсети" без запроса</span><span class="sxs-lookup"><span data-stu-id="8d679-118">Remove managed Kubernetes cluster without prompt</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d679-119">-Id</span><span class="sxs-lookup"><span data-stu-id="8d679-119">-Id</span></span>
<span data-ttu-id="8d679-120">ИД кластера управляемых кубарныхсетей</span><span class="sxs-lookup"><span data-stu-id="8d679-120">Id of a managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8d679-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8d679-121">-InputObject</span></span>
<span data-ttu-id="8d679-122">Объект PSKubernetesCluster, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="8d679-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="8d679-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8d679-123">-Name</span></span>
<span data-ttu-id="8d679-124">Название кластера "Кубберсети"</span><span class="sxs-lookup"><span data-stu-id="8d679-124">Name of your managed Kubernetes cluster</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d679-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d679-125">-PassThru</span></span>
<span data-ttu-id="8d679-126">Возвращает "Истина" в случае успешного удаления.</span><span class="sxs-lookup"><span data-stu-id="8d679-126">Returns true if deletion is successful</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d679-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d679-127">-ResourceGroupName</span></span>
<span data-ttu-id="8d679-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="8d679-128">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: GroupNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d679-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8d679-129">-Confirm</span></span>
<span data-ttu-id="8d679-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8d679-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d679-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d679-131">-WhatIf</span></span>
<span data-ttu-id="8d679-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d679-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d679-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8d679-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d679-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d679-134">CommonParameters</span></span>
<span data-ttu-id="8d679-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d679-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d679-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d679-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d679-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8d679-137">INPUTS</span></span>

### <span data-ttu-id="8d679-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="8d679-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="8d679-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8d679-139">System.String</span></span>

## <span data-ttu-id="8d679-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8d679-140">OUTPUTS</span></span>

### <span data-ttu-id="8d679-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d679-141">System.Boolean</span></span>

## <span data-ttu-id="8d679-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8d679-142">NOTES</span></span>

## <span data-ttu-id="8d679-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d679-143">RELATED LINKS</span></span>
