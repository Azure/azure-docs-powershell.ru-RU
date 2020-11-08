---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azaks
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAks.md
ms.openlocfilehash: 25a138b326a2fc086138f25a3d85f5182ba027fb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065690"
---
# <span data-ttu-id="e632a-101">Remove-AzAks</span><span class="sxs-lookup"><span data-stu-id="e632a-101">Remove-AzAks</span></span>

## <span data-ttu-id="e632a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e632a-102">SYNOPSIS</span></span>
<span data-ttu-id="e632a-103">Удаление управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e632a-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e632a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e632a-104">SYNTAX</span></span>

### <span data-ttu-id="e632a-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e632a-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAks [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e632a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e632a-106">InputObjectParameterSet</span></span>
```
Remove-AzAks -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e632a-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e632a-107">IdParameterSet</span></span>
```
Remove-AzAks [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e632a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e632a-108">DESCRIPTION</span></span>
<span data-ttu-id="e632a-109">Удаление управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="e632a-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="e632a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e632a-110">EXAMPLES</span></span>

### <span data-ttu-id="e632a-111">Удаление существующего управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="e632a-111">Delete an existing managed Kubernetes cluster</span></span>
```
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="e632a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e632a-112">PARAMETERS</span></span>

### <span data-ttu-id="e632a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e632a-113">-AsJob</span></span>
<span data-ttu-id="e632a-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e632a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e632a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e632a-115">-DefaultProfile</span></span>
<span data-ttu-id="e632a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e632a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e632a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="e632a-117">-Force</span></span>
<span data-ttu-id="e632a-118">Удаление управляемого кластера Kubernetes без запроса</span><span class="sxs-lookup"><span data-stu-id="e632a-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="e632a-119">-ID</span><span class="sxs-lookup"><span data-stu-id="e632a-119">-Id</span></span>
<span data-ttu-id="e632a-120">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="e632a-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e632a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e632a-121">-InputObject</span></span>
<span data-ttu-id="e632a-122">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="e632a-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="e632a-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e632a-123">-Name</span></span>
<span data-ttu-id="e632a-124">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="e632a-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="e632a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e632a-125">-PassThru</span></span>
<span data-ttu-id="e632a-126">Возвращает значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="e632a-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="e632a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e632a-127">-ResourceGroupName</span></span>
<span data-ttu-id="e632a-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e632a-128">Resource group name</span></span>

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

### <span data-ttu-id="e632a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e632a-129">-Confirm</span></span>
<span data-ttu-id="e632a-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e632a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e632a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e632a-131">-WhatIf</span></span>
<span data-ttu-id="e632a-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e632a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e632a-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e632a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e632a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e632a-134">CommonParameters</span></span>
<span data-ttu-id="e632a-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e632a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e632a-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e632a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e632a-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e632a-137">INPUTS</span></span>

### <span data-ttu-id="e632a-138">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="e632a-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="e632a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e632a-139">System.String</span></span>

## <span data-ttu-id="e632a-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e632a-140">OUTPUTS</span></span>

### <span data-ttu-id="e632a-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e632a-141">System.Boolean</span></span>

## <span data-ttu-id="e632a-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="e632a-142">NOTES</span></span>

## <span data-ttu-id="e632a-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e632a-143">RELATED LINKS</span></span>
