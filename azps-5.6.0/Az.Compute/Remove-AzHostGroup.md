---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: f05855c7fa677c384e9d8d0c5385d6014d80d312
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983304"
---
# <span data-ttu-id="cc7e7-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="cc7e7-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="cc7e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc7e7-102">SYNOPSIS</span></span>
<span data-ttu-id="cc7e7-103">Удаляет группу хостов.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-103">Removes a host group.</span></span>

## <span data-ttu-id="cc7e7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cc7e7-104">SYNTAX</span></span>

### <span data-ttu-id="cc7e7-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cc7e7-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc7e7-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="cc7e7-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc7e7-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="cc7e7-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc7e7-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cc7e7-108">DESCRIPTION</span></span>
<span data-ttu-id="cc7e7-109">Этот cmdlet удалит группу host (Хост)</span><span class="sxs-lookup"><span data-stu-id="cc7e7-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="cc7e7-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cc7e7-110">EXAMPLES</span></span>

### <span data-ttu-id="cc7e7-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cc7e7-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="cc7e7-112">Эта команда получает и удаляет заданную группу хостов.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="cc7e7-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="cc7e7-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="cc7e7-114">Эта команда удаляет заданную группу хостов.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-114">This command removes the given host group.</span></span>

## <span data-ttu-id="cc7e7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc7e7-115">PARAMETERS</span></span>

### <span data-ttu-id="cc7e7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc7e7-116">-AsJob</span></span>
<span data-ttu-id="cc7e7-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cc7e7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc7e7-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc7e7-118">-DefaultProfile</span></span>
<span data-ttu-id="cc7e7-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc7e7-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc7e7-120">-InputObject</span></span>
<span data-ttu-id="cc7e7-121">Локальный объект группы хостов.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7e7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cc7e7-122">-Name</span></span>
<span data-ttu-id="cc7e7-123">Имя группы хостов.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7e7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc7e7-124">-ResourceGroupName</span></span>
<span data-ttu-id="cc7e7-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7e7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc7e7-126">-ResourceId</span></span>
<span data-ttu-id="cc7e7-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc7e7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc7e7-128">-Confirm</span></span>
<span data-ttu-id="cc7e7-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc7e7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cc7e7-130">-WhatIf</span></span>
<span data-ttu-id="cc7e7-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc7e7-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc7e7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc7e7-133">CommonParameters</span></span>
<span data-ttu-id="cc7e7-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc7e7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc7e7-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc7e7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc7e7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cc7e7-136">INPUTS</span></span>

### <span data-ttu-id="cc7e7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="cc7e7-137">System.String</span></span>

### <span data-ttu-id="cc7e7-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="cc7e7-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="cc7e7-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cc7e7-139">OUTPUTS</span></span>

### <span data-ttu-id="cc7e7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="cc7e7-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="cc7e7-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cc7e7-141">NOTES</span></span>

## <span data-ttu-id="cc7e7-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cc7e7-142">RELATED LINKS</span></span>
