---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhost
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHost.md
ms.openlocfilehash: 0d3f3a34257ad32c8b606b99c3f7170fb15684b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100244072"
---
# <span data-ttu-id="9345b-101">Remove-AzHost</span><span class="sxs-lookup"><span data-stu-id="9345b-101">Remove-AzHost</span></span>

## <span data-ttu-id="9345b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9345b-102">SYNOPSIS</span></span>
<span data-ttu-id="9345b-103">Удаляет хост.</span><span class="sxs-lookup"><span data-stu-id="9345b-103">Removes a host.</span></span>

## <span data-ttu-id="9345b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9345b-104">SYNTAX</span></span>

### <span data-ttu-id="9345b-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9345b-105">DefaultParameter (Default)</span></span>
```
Remove-AzHost [-ResourceGroupName] <String> [-HostGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9345b-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="9345b-106">ResourceIdParameter</span></span>
```
Remove-AzHost [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9345b-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="9345b-107">ObjectParameter</span></span>
```
Remove-AzHost [-InputObject] <PSHost> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9345b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9345b-108">DESCRIPTION</span></span>
<span data-ttu-id="9345b-109">Этот cmdlet удалит host (Хост)</span><span class="sxs-lookup"><span data-stu-id="9345b-109">This cmdlet will delete a Host</span></span>

## <span data-ttu-id="9345b-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9345b-110">EXAMPLES</span></span>

### <span data-ttu-id="9345b-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9345b-111">Example 1</span></span>
```
PS C:\> Get-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName | Remove-AzHost
```

<span data-ttu-id="9345b-112">Эта команда получает и удаляет данный хост.</span><span class="sxs-lookup"><span data-stu-id="9345b-112">This command gets and removes the given host.</span></span>

### <span data-ttu-id="9345b-113">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9345b-113">Example 2</span></span>
```
PS C:\> Remove-AzHost -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName -Name $hostName
```

<span data-ttu-id="9345b-114">Эта команда удаляет данный хост.</span><span class="sxs-lookup"><span data-stu-id="9345b-114">This command removes the given host.</span></span>

## <span data-ttu-id="9345b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9345b-115">PARAMETERS</span></span>

### <span data-ttu-id="9345b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9345b-116">-AsJob</span></span>
<span data-ttu-id="9345b-117">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9345b-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9345b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9345b-118">-DefaultProfile</span></span>
<span data-ttu-id="9345b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9345b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9345b-120">-HostGroupName</span><span class="sxs-lookup"><span data-stu-id="9345b-120">-HostGroupName</span></span>
<span data-ttu-id="9345b-121">Имя группы хостов.</span><span class="sxs-lookup"><span data-stu-id="9345b-121">The name of the host group.</span></span>

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

### <span data-ttu-id="9345b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9345b-122">-InputObject</span></span>
<span data-ttu-id="9345b-123">Локальный объект хоста.</span><span class="sxs-lookup"><span data-stu-id="9345b-123">The local object of the host.</span></span>

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

### <span data-ttu-id="9345b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9345b-124">-Name</span></span>
<span data-ttu-id="9345b-125">Имя хоста.</span><span class="sxs-lookup"><span data-stu-id="9345b-125">The name of the host.</span></span>

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

### <span data-ttu-id="9345b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9345b-126">-ResourceGroupName</span></span>
<span data-ttu-id="9345b-127">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9345b-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="9345b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9345b-128">-ResourceId</span></span>
<span data-ttu-id="9345b-129">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="9345b-129">The ID of the resource.</span></span>

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

### <span data-ttu-id="9345b-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9345b-130">-Confirm</span></span>
<span data-ttu-id="9345b-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9345b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9345b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9345b-132">-WhatIf</span></span>
<span data-ttu-id="9345b-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9345b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9345b-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9345b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9345b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9345b-135">CommonParameters</span></span>
<span data-ttu-id="9345b-136">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9345b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9345b-137">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9345b-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9345b-138">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9345b-138">INPUTS</span></span>

### <span data-ttu-id="9345b-139">System.String</span><span class="sxs-lookup"><span data-stu-id="9345b-139">System.String</span></span>

### <span data-ttu-id="9345b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span><span class="sxs-lookup"><span data-stu-id="9345b-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSHost</span></span>

## <span data-ttu-id="9345b-141">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9345b-141">OUTPUTS</span></span>

### <span data-ttu-id="9345b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="9345b-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="9345b-143">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9345b-143">NOTES</span></span>

## <span data-ttu-id="9345b-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9345b-144">RELATED LINKS</span></span>
