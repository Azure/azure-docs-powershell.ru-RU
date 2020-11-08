---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: 7fde60c0bd1f400dd332782b6fbb9a92fefae4a1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065793"
---
# <span data-ttu-id="38187-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="38187-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="38187-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38187-102">SYNOPSIS</span></span>
<span data-ttu-id="38187-103">Перезапустите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="38187-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="38187-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38187-104">SYNTAX</span></span>

### <span data-ttu-id="38187-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38187-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38187-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="38187-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38187-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="38187-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38187-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38187-108">DESCRIPTION</span></span>
<span data-ttu-id="38187-109">Перезапустите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="38187-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="38187-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38187-110">EXAMPLES</span></span>

### <span data-ttu-id="38187-111">Перезапуск специфической службы сигнала</span><span class="sxs-lookup"><span data-stu-id="38187-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="38187-112">Группа ресурсов по умолчанию может быть установлена с помощью \` Set-AzDefault-ResourceGroupName myResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="38187-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="38187-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38187-113">PARAMETERS</span></span>

### <span data-ttu-id="38187-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38187-114">-AsJob</span></span>
<span data-ttu-id="38187-115">Запустите командлет в фоновом задании.</span><span class="sxs-lookup"><span data-stu-id="38187-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="38187-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38187-116">-DefaultProfile</span></span>
<span data-ttu-id="38187-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38187-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38187-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38187-118">-InputObject</span></span>
<span data-ttu-id="38187-119">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="38187-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="38187-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38187-120">-Name</span></span>
<span data-ttu-id="38187-121">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="38187-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="38187-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="38187-122">-PassThru</span></span>
<span data-ttu-id="38187-123">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="38187-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="38187-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38187-124">-ResourceGroupName</span></span>
<span data-ttu-id="38187-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38187-125">The resource group name.</span></span>
<span data-ttu-id="38187-126">Значение по умолчанию будет использоваться, если оно не указано.</span><span class="sxs-lookup"><span data-stu-id="38187-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="38187-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38187-127">-ResourceId</span></span>
<span data-ttu-id="38187-128">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="38187-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="38187-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38187-129">-Confirm</span></span>
<span data-ttu-id="38187-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38187-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38187-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38187-131">-WhatIf</span></span>
<span data-ttu-id="38187-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38187-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="38187-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38187-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38187-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38187-134">CommonParameters</span></span>
<span data-ttu-id="38187-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38187-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38187-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38187-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38187-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38187-137">INPUTS</span></span>

### <span data-ttu-id="38187-138">System. String</span><span class="sxs-lookup"><span data-stu-id="38187-138">System.String</span></span>

### <span data-ttu-id="38187-139">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="38187-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="38187-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38187-140">OUTPUTS</span></span>

### <span data-ttu-id="38187-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="38187-141">System.Boolean</span></span>

## <span data-ttu-id="38187-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="38187-142">NOTES</span></span>

## <span data-ttu-id="38187-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38187-143">RELATED LINKS</span></span>
