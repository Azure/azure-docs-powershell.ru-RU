---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Aks.dll-Help.xml
Module Name: Az.Aks
online version: https://docs.microsoft.com/en-us/powershell/module/az.aks/remove-azakscluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Aks/Aks/help/Remove-AzAksCluster.md
ms.openlocfilehash: d6364030eedb75b59c5f9a86bb57499864270fa2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399071"
---
# <span data-ttu-id="5ec31-101">Remove-AzAksCluster</span><span class="sxs-lookup"><span data-stu-id="5ec31-101">Remove-AzAksCluster</span></span>

## <span data-ttu-id="5ec31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ec31-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec31-103">Удалите управляемый кластер Кубберсетей.</span><span class="sxs-lookup"><span data-stu-id="5ec31-103">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5ec31-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5ec31-104">SYNTAX</span></span>

### <span data-ttu-id="5ec31-105">GroupNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5ec31-105">GroupNameParameterSet (Default)</span></span>
```
Remove-AzAksCluster [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ec31-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec31-106">InputObjectParameterSet</span></span>
```
Remove-AzAksCluster -InputObject <PSKubernetesCluster> [-PassThru] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ec31-107">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec31-107">IdParameterSet</span></span>
```
Remove-AzAksCluster [-Id] <String> [-PassThru] [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ec31-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5ec31-108">DESCRIPTION</span></span>
<span data-ttu-id="5ec31-109">Удалите управляемый кластер Кубберсетей.</span><span class="sxs-lookup"><span data-stu-id="5ec31-109">Delete a managed Kubernetes cluster.</span></span>

## <span data-ttu-id="5ec31-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5ec31-110">EXAMPLES</span></span>

### <span data-ttu-id="5ec31-111">Удаление существующего управляемого кластера "Кубберсети"</span><span class="sxs-lookup"><span data-stu-id="5ec31-111">Delete an existing managed Kubernetes cluster</span></span>
```powershell
PS C:\> Remove-AzAks -ResourceGroupName group -Name myCluster
```

## <span data-ttu-id="5ec31-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ec31-112">PARAMETERS</span></span>

### <span data-ttu-id="5ec31-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ec31-113">-AsJob</span></span>
<span data-ttu-id="5ec31-114">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5ec31-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5ec31-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec31-115">-DefaultProfile</span></span>
<span data-ttu-id="5ec31-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec31-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ec31-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5ec31-117">-Force</span></span>
<span data-ttu-id="5ec31-118">Удаление управляемого кластера "Кубберсети" без запроса</span><span class="sxs-lookup"><span data-stu-id="5ec31-118">Remove managed Kubernetes cluster without prompt</span></span>

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

### <span data-ttu-id="5ec31-119">-Id</span><span class="sxs-lookup"><span data-stu-id="5ec31-119">-Id</span></span>
<span data-ttu-id="5ec31-120">ИД кластера управляемых кубарныхсетей</span><span class="sxs-lookup"><span data-stu-id="5ec31-120">Id of a managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5ec31-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5ec31-121">-InputObject</span></span>
<span data-ttu-id="5ec31-122">Объект PSKubernetesCluster, который обычно проходит через конвейер.</span><span class="sxs-lookup"><span data-stu-id="5ec31-122">A PSKubernetesCluster object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5ec31-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5ec31-123">-Name</span></span>
<span data-ttu-id="5ec31-124">Название кластера "Кубберсети"</span><span class="sxs-lookup"><span data-stu-id="5ec31-124">Name of your managed Kubernetes cluster</span></span>

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

### <span data-ttu-id="5ec31-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ec31-125">-PassThru</span></span>
<span data-ttu-id="5ec31-126">Возвращает "Истина" в случае успешного удаления.</span><span class="sxs-lookup"><span data-stu-id="5ec31-126">Returns true if deletion is successful</span></span>

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

### <span data-ttu-id="5ec31-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ec31-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ec31-128">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="5ec31-128">Resource group name</span></span>

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

### <span data-ttu-id="5ec31-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5ec31-129">-Confirm</span></span>
<span data-ttu-id="5ec31-130">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ec31-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ec31-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ec31-131">-WhatIf</span></span>
<span data-ttu-id="5ec31-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ec31-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ec31-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5ec31-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ec31-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec31-134">CommonParameters</span></span>
<span data-ttu-id="5ec31-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec31-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec31-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ec31-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec31-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5ec31-137">INPUTS</span></span>

### <span data-ttu-id="5ec31-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span><span class="sxs-lookup"><span data-stu-id="5ec31-138">Microsoft.Azure.Commands.Aks.Models.PSKubernetesCluster</span></span>

### <span data-ttu-id="5ec31-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5ec31-139">System.String</span></span>

## <span data-ttu-id="5ec31-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5ec31-140">OUTPUTS</span></span>

### <span data-ttu-id="5ec31-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5ec31-141">System.Boolean</span></span>

## <span data-ttu-id="5ec31-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5ec31-142">NOTES</span></span>

## <span data-ttu-id="5ec31-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5ec31-143">RELATED LINKS</span></span>