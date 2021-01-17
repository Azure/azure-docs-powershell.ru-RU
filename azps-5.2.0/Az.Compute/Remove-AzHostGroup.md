---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98399383"
---
# <span data-ttu-id="42050-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="42050-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="42050-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42050-102">SYNOPSIS</span></span>
<span data-ttu-id="42050-103">Удаляет группу хостов.</span><span class="sxs-lookup"><span data-stu-id="42050-103">Removes a host group.</span></span>

## <span data-ttu-id="42050-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="42050-104">SYNTAX</span></span>

### <span data-ttu-id="42050-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="42050-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42050-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="42050-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="42050-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="42050-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42050-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="42050-108">DESCRIPTION</span></span>
<span data-ttu-id="42050-109">Этот cmdlet удалит группу host (Хост)</span><span class="sxs-lookup"><span data-stu-id="42050-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="42050-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="42050-110">EXAMPLES</span></span>

### <span data-ttu-id="42050-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="42050-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="42050-112">Эта команда получает и удаляет заданную группу хостов.</span><span class="sxs-lookup"><span data-stu-id="42050-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="42050-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="42050-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="42050-114">Эта команда удаляет заданную группу хостов.</span><span class="sxs-lookup"><span data-stu-id="42050-114">This command removes the given host group.</span></span>

## <span data-ttu-id="42050-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42050-115">PARAMETERS</span></span>

### <span data-ttu-id="42050-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42050-116">-AsJob</span></span>
<span data-ttu-id="42050-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="42050-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="42050-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42050-118">-DefaultProfile</span></span>
<span data-ttu-id="42050-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="42050-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42050-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42050-120">-InputObject</span></span>
<span data-ttu-id="42050-121">Локальный объект группы хостов.</span><span class="sxs-lookup"><span data-stu-id="42050-121">The local object of the host group.</span></span>

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

### <span data-ttu-id="42050-122">-Name</span><span class="sxs-lookup"><span data-stu-id="42050-122">-Name</span></span>
<span data-ttu-id="42050-123">Имя группы хостов.</span><span class="sxs-lookup"><span data-stu-id="42050-123">The name of the host group.</span></span>

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

### <span data-ttu-id="42050-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42050-124">-ResourceGroupName</span></span>
<span data-ttu-id="42050-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="42050-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="42050-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="42050-126">-ResourceId</span></span>
<span data-ttu-id="42050-127">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="42050-127">The ID of the resource.</span></span>

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

### <span data-ttu-id="42050-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="42050-128">-Confirm</span></span>
<span data-ttu-id="42050-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="42050-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42050-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42050-130">-WhatIf</span></span>
<span data-ttu-id="42050-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42050-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42050-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="42050-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42050-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42050-133">CommonParameters</span></span>
<span data-ttu-id="42050-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42050-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42050-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42050-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42050-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="42050-136">INPUTS</span></span>

### <span data-ttu-id="42050-137">System.String</span><span class="sxs-lookup"><span data-stu-id="42050-137">System.String</span></span>

### <span data-ttu-id="42050-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="42050-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="42050-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="42050-139">OUTPUTS</span></span>

### <span data-ttu-id="42050-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="42050-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="42050-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="42050-141">NOTES</span></span>

## <span data-ttu-id="42050-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="42050-142">RELATED LINKS</span></span>
