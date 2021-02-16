---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217481"
---
# <span data-ttu-id="ee794-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="ee794-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="ee794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee794-102">SYNOPSIS</span></span>
<span data-ttu-id="ee794-103">Удаление службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="ee794-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="ee794-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ee794-104">SYNTAX</span></span>

### <span data-ttu-id="ee794-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ee794-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee794-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee794-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee794-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee794-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee794-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ee794-108">DESCRIPTION</span></span>
<span data-ttu-id="ee794-109">Удаление службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="ee794-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="ee794-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ee794-110">EXAMPLES</span></span>

### <span data-ttu-id="ee794-111">Удаление службы SignalR</span><span class="sxs-lookup"><span data-stu-id="ee794-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="ee794-112">Удаление всей службы SignalR из канала</span><span class="sxs-lookup"><span data-stu-id="ee794-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="ee794-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee794-113">PARAMETERS</span></span>

### <span data-ttu-id="ee794-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee794-114">-AsJob</span></span>
<span data-ttu-id="ee794-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="ee794-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee794-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee794-116">-DefaultProfile</span></span>
<span data-ttu-id="ee794-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ee794-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee794-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee794-118">-InputObject</span></span>
<span data-ttu-id="ee794-119">Объект ресурса SignalR.</span><span class="sxs-lookup"><span data-stu-id="ee794-119">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee794-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ee794-120">-Name</span></span>
<span data-ttu-id="ee794-121">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="ee794-121">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee794-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee794-122">-PassThru</span></span>
<span data-ttu-id="ee794-123">Если удаление успешно завершено, возвращается истина.</span><span class="sxs-lookup"><span data-stu-id="ee794-123">Returns true if the removal was completed successfully.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee794-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee794-124">-ResourceGroupName</span></span>
<span data-ttu-id="ee794-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ee794-125">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee794-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee794-126">-ResourceId</span></span>
<span data-ttu-id="ee794-127">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="ee794-127">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee794-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee794-128">-Confirm</span></span>
<span data-ttu-id="ee794-129">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ee794-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee794-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee794-130">-WhatIf</span></span>
<span data-ttu-id="ee794-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee794-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee794-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ee794-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee794-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee794-133">CommonParameters</span></span>
<span data-ttu-id="ee794-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee794-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee794-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ee794-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee794-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ee794-136">INPUTS</span></span>

### <span data-ttu-id="ee794-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ee794-137">System.String</span></span>
### <span data-ttu-id="ee794-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="ee794-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="ee794-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ee794-139">OUTPUTS</span></span>

### <span data-ttu-id="ee794-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ee794-140">System.Boolean</span></span>
## <span data-ttu-id="ee794-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ee794-141">NOTES</span></span>

## <span data-ttu-id="ee794-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ee794-142">RELATED LINKS</span></span>
