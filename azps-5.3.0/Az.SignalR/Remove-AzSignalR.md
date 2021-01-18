---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/remove-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Remove-AzSignalR.md
ms.openlocfilehash: 89df3c19b34ee7175e6fe65269f8df5f218a49f3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505938"
---
# <span data-ttu-id="79554-101">Remove-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="79554-101">Remove-AzSignalR</span></span>

## <span data-ttu-id="79554-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79554-102">SYNOPSIS</span></span>
<span data-ttu-id="79554-103">Удаление службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="79554-103">Remove a SignalR service.</span></span>

## <span data-ttu-id="79554-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="79554-104">SYNTAX</span></span>

### <span data-ttu-id="79554-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="79554-105">ResourceGroupParameterSet (Default)</span></span>
```
Remove-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79554-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="79554-106">ResourceIdParameterSet</span></span>
```
Remove-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79554-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79554-107">InputObjectParameterSet</span></span>
```
Remove-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79554-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="79554-108">DESCRIPTION</span></span>
<span data-ttu-id="79554-109">Удаление службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="79554-109">Remove a SignalR service.</span></span>

## <span data-ttu-id="79554-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="79554-110">EXAMPLES</span></span>

### <span data-ttu-id="79554-111">Удаление службы SignalR</span><span class="sxs-lookup"><span data-stu-id="79554-111">Remove a SignalR service</span></span>
```
PS C:\> Remove-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

### <span data-ttu-id="79554-112">Удаление всей службы SignalR из канала</span><span class="sxs-lookup"><span data-stu-id="79554-112">Remove all SignalR service from pipe</span></span>
```
PS C:\> Get-AzSignalR -ResourceGroupName myResourceGroup | Remove-AzSignalR
```

## <span data-ttu-id="79554-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79554-113">PARAMETERS</span></span>

### <span data-ttu-id="79554-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="79554-114">-AsJob</span></span>
<span data-ttu-id="79554-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="79554-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="79554-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79554-116">-DefaultProfile</span></span>
<span data-ttu-id="79554-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="79554-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79554-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79554-118">-InputObject</span></span>
<span data-ttu-id="79554-119">Объект ресурса SignalR.</span><span class="sxs-lookup"><span data-stu-id="79554-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="79554-120">-Name</span><span class="sxs-lookup"><span data-stu-id="79554-120">-Name</span></span>
<span data-ttu-id="79554-121">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="79554-121">SignalR service name.</span></span>

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

### <span data-ttu-id="79554-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="79554-122">-PassThru</span></span>
<span data-ttu-id="79554-123">Если удаление успешно завершено, возвращается истина.</span><span class="sxs-lookup"><span data-stu-id="79554-123">Returns true if the removal was completed successfully.</span></span>

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

### <span data-ttu-id="79554-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79554-124">-ResourceGroupName</span></span>
<span data-ttu-id="79554-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="79554-125">Resource group name.</span></span>

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

### <span data-ttu-id="79554-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79554-126">-ResourceId</span></span>
<span data-ttu-id="79554-127">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="79554-127">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="79554-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79554-128">-Confirm</span></span>
<span data-ttu-id="79554-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79554-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79554-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79554-130">-WhatIf</span></span>
<span data-ttu-id="79554-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79554-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79554-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="79554-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79554-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79554-133">CommonParameters</span></span>
<span data-ttu-id="79554-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79554-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79554-135">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79554-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79554-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="79554-136">INPUTS</span></span>

### <span data-ttu-id="79554-137">System.String</span><span class="sxs-lookup"><span data-stu-id="79554-137">System.String</span></span>
### <span data-ttu-id="79554-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="79554-138">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="79554-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="79554-139">OUTPUTS</span></span>

### <span data-ttu-id="79554-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="79554-140">System.Boolean</span></span>
## <span data-ttu-id="79554-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="79554-141">NOTES</span></span>

## <span data-ttu-id="79554-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="79554-142">RELATED LINKS</span></span>
