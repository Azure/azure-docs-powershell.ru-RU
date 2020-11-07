---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "93913049"
---
# <span data-ttu-id="4856e-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="4856e-101">Remove-AzHost</span></span>

## <span data-ttu-id="4856e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4856e-102">SYNOPSIS</span></span>
<span data-ttu-id="4856e-103">Удаление узла.</span><span class="sxs-lookup"><span data-stu-id="4856e-103">Removes a host.</span></span>

## <span data-ttu-id="4856e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4856e-104">SYNTAX</span></span>

### <span data-ttu-id="4856e-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4856e-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4856e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="4856e-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4856e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="4856e-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4856e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4856e-108">DESCRIPTION</span></span>
<span data-ttu-id="4856e-109">Этот командлет удалит узел</span><span class="sxs-lookup"><span data-stu-id="4856e-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="4856e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4856e-110">EXAMPLES</span></span>

### <span data-ttu-id="4856e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4856e-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="4856e-112">Эта команда возвращает или удаляет заданный узел.</span><span class="sxs-lookup"><span data-stu-id="4856e-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="4856e-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4856e-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="4856e-114">Эта команда удаляет заданный узел.</span><span class="sxs-lookup"><span data-stu-id="4856e-114">This command removes the given host.</span></span>

## <span data-ttu-id="4856e-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4856e-115">PARAMETERS</span></span>

### <span data-ttu-id="4856e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4856e-116">-AsJob</span></span>
<span data-ttu-id="4856e-117">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4856e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4856e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4856e-118">-DefaultProfile</span></span>
<span data-ttu-id="4856e-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4856e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4856e-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="4856e-120">-HostGroupName</span></span>
<span data-ttu-id="4856e-121">Имя группы узлов.</span><span class="sxs-lookup"><span data-stu-id="4856e-121">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4856e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4856e-122">-InputObject</span></span>
<span data-ttu-id="4856e-123">Локальный объект узла.</span><span class="sxs-lookup"><span data-stu-id="4856e-123">The local object of the host.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHost
Parameter Sets: ObjectParameter
Aliases: Host

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4856e-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4856e-124">-Name</span></span>
<span data-ttu-id="4856e-125">Имя узла.</span><span class="sxs-lookup"><span data-stu-id="4856e-125">The name of the host.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4856e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4856e-126">-ResourceGroupName</span></span>
<span data-ttu-id="4856e-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="4856e-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="4856e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4856e-128">-ResourceId</span></span>
<span data-ttu-id="4856e-129">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="4856e-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="4856e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4856e-130">-Confirm</span></span>
<span data-ttu-id="4856e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4856e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4856e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4856e-132">-WhatIf</span></span>
<span data-ttu-id="4856e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4856e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4856e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4856e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4856e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4856e-135">CommonParameters</span></span>
<span data-ttu-id="4856e-136">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4856e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4856e-137">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4856e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4856e-138">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4856e-138">INPUTS</span></span>

### <span data-ttu-id="4856e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4856e-139">System.String</span></span>

### <span data-ttu-id="4856e-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHost</span><span class="sxs-lookup"><span data-stu-id="4856e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="4856e-141">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4856e-141">OUTPUTS</span></span>

### <span data-ttu-id="4856e-142">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="4856e-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="4856e-143">Пуск</span><span class="sxs-lookup"><span data-stu-id="4856e-143">NOTES</span></span>

## <span data-ttu-id="4856e-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4856e-144">RELATED LINKS</span></span>
