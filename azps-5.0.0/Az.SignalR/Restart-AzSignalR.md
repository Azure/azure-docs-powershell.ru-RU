---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/restart-azsignalr
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Restart-AzSignalR.md
ms.openlocfilehash: ea5de8ddd36d315381d4f60ee0fa1ce7dc49adc2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247524"
---
# <span data-ttu-id="3638d-101">Restart-AzSignalR</span><span class="sxs-lookup"><span data-stu-id="3638d-101">Restart-AzSignalR</span></span>

## <span data-ttu-id="3638d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3638d-102">SYNOPSIS</span></span>
<span data-ttu-id="3638d-103">Перезапустите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="3638d-103">Restart a SignalR service.</span></span>

## <span data-ttu-id="3638d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3638d-104">SYNTAX</span></span>

### <span data-ttu-id="3638d-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3638d-105">ResourceGroupParameterSet (Default)</span></span>
```
Restart-AzSignalR [-ResourceGroupName <String>] [-Name] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3638d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3638d-106">ResourceIdParameterSet</span></span>
```
Restart-AzSignalR -ResourceId <String> [-AsJob] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3638d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3638d-107">InputObjectParameterSet</span></span>
```
Restart-AzSignalR -InputObject <PSSignalRResource> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3638d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3638d-108">DESCRIPTION</span></span>
<span data-ttu-id="3638d-109">Перезапустите службу сигнала.</span><span class="sxs-lookup"><span data-stu-id="3638d-109">Restart a SignalR service.</span></span>

## <span data-ttu-id="3638d-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3638d-110">EXAMPLES</span></span>

### <span data-ttu-id="3638d-111">Перезапуск специфической службы сигнала</span><span class="sxs-lookup"><span data-stu-id="3638d-111">Restart a specific SignalR service</span></span>
```powershell
PS C:\> Restart-AzSignalR -ResourceGroupName myResourceGroup -Name mysignalr1 -PassThru

True
```

<span data-ttu-id="3638d-112">Группа ресурсов по умолчанию может быть установлена с помощью \` Set-AzDefault-ResourceGroupName myResourceGroup \` .</span><span class="sxs-lookup"><span data-stu-id="3638d-112">The default resource group can be set by \`Set-AzDefault -ResourceGroupName myResourceGroup\`.</span></span>

## <span data-ttu-id="3638d-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3638d-113">PARAMETERS</span></span>

### <span data-ttu-id="3638d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3638d-114">-AsJob</span></span>
<span data-ttu-id="3638d-115">Запустите командлет в фоновом задании.</span><span class="sxs-lookup"><span data-stu-id="3638d-115">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="3638d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3638d-116">-DefaultProfile</span></span>
<span data-ttu-id="3638d-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3638d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3638d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3638d-118">-InputObject</span></span>
<span data-ttu-id="3638d-119">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="3638d-119">The SignalR resource object.</span></span>

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

### <span data-ttu-id="3638d-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3638d-120">-Name</span></span>
<span data-ttu-id="3638d-121">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="3638d-121">The SignalR service name.</span></span>

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

### <span data-ttu-id="3638d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3638d-122">-PassThru</span></span>
<span data-ttu-id="3638d-123">{{Fill описание пропускания}}</span><span class="sxs-lookup"><span data-stu-id="3638d-123">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="3638d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3638d-124">-ResourceGroupName</span></span>
<span data-ttu-id="3638d-125">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3638d-125">The resource group name.</span></span>
<span data-ttu-id="3638d-126">Значение по умолчанию будет использоваться, если оно не указано.</span><span class="sxs-lookup"><span data-stu-id="3638d-126">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="3638d-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3638d-127">-ResourceId</span></span>
<span data-ttu-id="3638d-128">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="3638d-128">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="3638d-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3638d-129">-Confirm</span></span>
<span data-ttu-id="3638d-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3638d-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3638d-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3638d-131">-WhatIf</span></span>
<span data-ttu-id="3638d-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3638d-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3638d-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3638d-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3638d-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3638d-134">CommonParameters</span></span>
<span data-ttu-id="3638d-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3638d-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3638d-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3638d-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3638d-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3638d-137">INPUTS</span></span>

### <span data-ttu-id="3638d-138">System. String</span><span class="sxs-lookup"><span data-stu-id="3638d-138">System.String</span></span>

### <span data-ttu-id="3638d-139">Microsoft. Azure. Commands. SignalR. Models. PSSignalRResource</span><span class="sxs-lookup"><span data-stu-id="3638d-139">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>

## <span data-ttu-id="3638d-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3638d-140">OUTPUTS</span></span>

### <span data-ttu-id="3638d-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3638d-141">System.Boolean</span></span>

## <span data-ttu-id="3638d-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="3638d-142">NOTES</span></span>

## <span data-ttu-id="3638d-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3638d-143">RELATED LINKS</span></span>