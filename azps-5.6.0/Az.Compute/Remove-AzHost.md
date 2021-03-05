---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 21c623187e72406d1120e225bf567a48bb2e6f30
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983315"
---
# <span data-ttu-id="c59c3-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="c59c3-101">Remove-AzHost</span></span>

## <span data-ttu-id="c59c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c59c3-102">SYNOPSIS</span></span>
<span data-ttu-id="c59c3-103">Удаляет хост.</span><span class="sxs-lookup"><span data-stu-id="c59c3-103">Removes a host.</span></span>

## <span data-ttu-id="c59c3-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c59c3-104">SYNTAX</span></span>

### <span data-ttu-id="c59c3-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c59c3-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c59c3-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="c59c3-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c59c3-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="c59c3-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c59c3-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c59c3-108">DESCRIPTION</span></span>
<span data-ttu-id="c59c3-109">Этот cmdlet удалит хост.</span><span class="sxs-lookup"><span data-stu-id="c59c3-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="c59c3-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c59c3-110">EXAMPLES</span></span>

### <span data-ttu-id="c59c3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c59c3-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="c59c3-112">Эта команда получает и удаляет данный хост.</span><span class="sxs-lookup"><span data-stu-id="c59c3-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="c59c3-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="c59c3-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="c59c3-114">Эта команда удаляет данный хост.</span><span class="sxs-lookup"><span data-stu-id="c59c3-114">This command removes the given host.</span></span>

## <span data-ttu-id="c59c3-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c59c3-115">PARAMETERS</span></span>

### <span data-ttu-id="c59c3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c59c3-116">-AsJob</span></span>
<span data-ttu-id="c59c3-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="c59c3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c59c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c59c3-118">-DefaultProfile</span></span>
<span data-ttu-id="c59c3-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c59c3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c59c3-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="c59c3-120">-HostGroupName</span></span>
<span data-ttu-id="c59c3-121">Имя группы хостов.</span><span class="sxs-lookup"><span data-stu-id="c59c3-121">The name of the host group.</span></span>

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

### <span data-ttu-id="c59c3-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c59c3-122">-InputObject</span></span>
<span data-ttu-id="c59c3-123">Локальный объект хоста.</span><span class="sxs-lookup"><span data-stu-id="c59c3-123">The local object of the host.</span></span>

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

### <span data-ttu-id="c59c3-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c59c3-124">-Name</span></span>
<span data-ttu-id="c59c3-125">Имя хоста.</span><span class="sxs-lookup"><span data-stu-id="c59c3-125">The name of the host.</span></span>

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

### <span data-ttu-id="c59c3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c59c3-126">-ResourceGroupName</span></span>
<span data-ttu-id="c59c3-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="c59c3-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="c59c3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c59c3-128">-ResourceId</span></span>
<span data-ttu-id="c59c3-129">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="c59c3-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="c59c3-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c59c3-130">-Confirm</span></span>
<span data-ttu-id="c59c3-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="c59c3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c59c3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c59c3-132">-WhatIf</span></span>
<span data-ttu-id="c59c3-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c59c3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c59c3-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c59c3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c59c3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c59c3-135">CommonParameters</span></span>
<span data-ttu-id="c59c3-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c59c3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c59c3-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c59c3-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c59c3-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c59c3-138">INPUTS</span></span>

### <span data-ttu-id="c59c3-139">System.String</span><span class="sxs-lookup"><span data-stu-id="c59c3-139">System.String</span></span>

### <span data-ttu-id="c59c3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="c59c3-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="c59c3-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c59c3-141">OUTPUTS</span></span>

### <span data-ttu-id="c59c3-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="c59c3-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="c59c3-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c59c3-143">NOTES</span></span>

## <span data-ttu-id="c59c3-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c59c3-144">RELATED LINKS</span></span>
