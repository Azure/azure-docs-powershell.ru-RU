---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: c98b716f37fcf9aafafacdefad4c51b0451cf12d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955459"
---
# <span data-ttu-id="ff104-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="ff104-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="ff104-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff104-102">SYNOPSIS</span></span>
<span data-ttu-id="ff104-103">Перезапустите службу SignalR.</span><span class="sxs-lookup"><span data-stu-id="ff104-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="ff104-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ff104-104">SYNTAX</span></span>

### <span data-ttu-id="ff104-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ff104-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff104-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff104-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ff104-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ff104-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ff104-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff104-108">DESCRIPTION</span></span>
<span data-ttu-id="ff104-109">Перезапустите службу SignalR.</span><span class="sxs-lookup"><span data-stu-id="ff104-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="ff104-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ff104-110">EXAMPLES</span></span>

### <span data-ttu-id="ff104-111">Перезапуск определенной службы SignalR</span><span class="sxs-lookup"><span data-stu-id="ff104-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="ff104-112">Группу ресурсов по умолчанию может установить \` Set-AzDefault -ResourceGroupName myResourceGroup. \`</span><span class="sxs-lookup"><span data-stu-id="ff104-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="ff104-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff104-113">PARAMETERS</span></span>

### <span data-ttu-id="ff104-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ff104-114">-AsJob</span></span>
<span data-ttu-id="ff104-115">Запустите его в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="ff104-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="ff104-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff104-116">-DefaultProfile</span></span>
<span data-ttu-id="ff104-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff104-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff104-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ff104-118">-InputObject</span></span>
<span data-ttu-id="ff104-119">Объект ресурса SignalR.</span><span class="sxs-lookup"><span data-stu-id="ff104-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="ff104-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ff104-120">-Name</span></span>
<span data-ttu-id="ff104-121">Имя службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="ff104-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="ff104-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ff104-122">-PassThru</span></span>
<span data-ttu-id="ff104-123">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="ff104-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="ff104-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff104-124">-ResourceGroupName</span></span>
<span data-ttu-id="ff104-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ff104-125">The resource group name.</span></span>
<span data-ttu-id="ff104-126">Значение по умолчанию будет использоваться, если не указано.</span><span class="sxs-lookup"><span data-stu-id="ff104-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="ff104-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ff104-127">-ResourceId</span></span>
<span data-ttu-id="ff104-128">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="ff104-128">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff104-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ff104-129">-Confirm</span></span>
<span data-ttu-id="ff104-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="ff104-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff104-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff104-131">-WhatIf</span></span>
<span data-ttu-id="ff104-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff104-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff104-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ff104-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff104-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff104-134">CommonParameters</span></span>
<span data-ttu-id="ff104-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff104-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff104-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ff104-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff104-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ff104-137">INPUTS</span></span>

### <span data-ttu-id="ff104-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ff104-138">System.String</span></span>

### <span data-ttu-id="ff104-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="ff104-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="ff104-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ff104-140">OUTPUTS</span></span>

### <span data-ttu-id="ff104-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="ff104-141">System.Boolean</span></span>

## <span data-ttu-id="ff104-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ff104-142">NOTES</span></span>

## <span data-ttu-id="ff104-143">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff104-143">RELATED LINKS</span></span>
