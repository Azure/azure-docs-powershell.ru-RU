---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247107"
---
# <span data-ttu-id="93ca2-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="93ca2-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="93ca2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="93ca2-102">SYNOPSIS</span></span>
<span data-ttu-id="93ca2-103">Удаление управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="93ca2-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="93ca2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="93ca2-104">SYNTAX</span></span>

### <span data-ttu-id="93ca2-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="93ca2-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93ca2-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="93ca2-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="93ca2-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="93ca2-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ca2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="93ca2-108">DESCRIPTION</span></span>
<span data-ttu-id="93ca2-109">Удаление управляемого кластера Kubernetes.</span><span class="sxs-lookup"><span data-stu-id="93ca2-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="93ca2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="93ca2-110">EXAMPLES</span></span>

### <span data-ttu-id="93ca2-111">Удаление существующего управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="93ca2-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="93ca2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="93ca2-112">PARAMETERS</span></span>

### <span data-ttu-id="93ca2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="93ca2-113">-AsJob</span></span>
<span data-ttu-id="93ca2-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="93ca2-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="93ca2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ca2-115">-DefaultProfile</span></span>
<span data-ttu-id="93ca2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="93ca2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93ca2-117">-Force</span><span class="sxs-lookup"><span data-stu-id="93ca2-117">-Force</span></span>
<span data-ttu-id="93ca2-118">Удаление управляемого кластера Kubernetes без запроса</span><span class="sxs-lookup"><span data-stu-id="93ca2-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="93ca2-119">-ID</span><span class="sxs-lookup"><span data-stu-id="93ca2-119">-Id</span></span>
<span data-ttu-id="93ca2-120">Идентификатор управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="93ca2-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="93ca2-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93ca2-121">-InputObject</span></span>
<span data-ttu-id="93ca2-122">Объект PSKubernetesCluster, обычно передаваемый через конвейер.</span><span class="sxs-lookup"><span data-stu-id="93ca2-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="93ca2-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="93ca2-123">-Name</span></span>
<span data-ttu-id="93ca2-124">Имя управляемого кластера Kubernetes</span><span class="sxs-lookup"><span data-stu-id="93ca2-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="93ca2-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93ca2-125">-PassThru</span></span>
<span data-ttu-id="93ca2-126">Возвращает значение истина, если удаление прошло успешно.</span><span class="sxs-lookup"><span data-stu-id="93ca2-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="93ca2-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ca2-127">-ResourceGroupName</span></span>
<span data-ttu-id="93ca2-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="93ca2-128">Resource group name</span></span>

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

### <span data-ttu-id="93ca2-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93ca2-129">-Confirm</span></span>
<span data-ttu-id="93ca2-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="93ca2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ca2-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ca2-131">-WhatIf</span></span>
<span data-ttu-id="93ca2-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="93ca2-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ca2-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="93ca2-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ca2-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ca2-134">CommonParameters</span></span>
<span data-ttu-id="93ca2-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="93ca2-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ca2-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93ca2-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ca2-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="93ca2-137">INPUTS</span></span>

### <span data-ttu-id="93ca2-138">Microsoft. Azure. Commands. AKS. Models. PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="93ca2-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="93ca2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="93ca2-139">System.String</span></span>

## <span data-ttu-id="93ca2-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="93ca2-140">OUTPUTS</span></span>

### <span data-ttu-id="93ca2-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="93ca2-141">System.Boolean</span></span>

## <span data-ttu-id="93ca2-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="93ca2-142">NOTES</span></span>

## <span data-ttu-id="93ca2-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="93ca2-143">RELATED LINKS</span></span>
