---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94087993"
---
# <span data-ttu-id="29dbb-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="29dbb-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="29dbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="29dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="29dbb-103">Настройте параметры восходящего потока в службе SignalR.</span><span class="sxs-lookup"><span data-stu-id="29dbb-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="29dbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="29dbb-104">SYNTAX</span></span>

### <span data-ttu-id="29dbb-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="29dbb-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="29dbb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="29dbb-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29dbb-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="29dbb-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29dbb-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="29dbb-108">DESCRIPTION</span></span>
<span data-ttu-id="29dbb-109">Настройте параметры восходящего потока в службе SignalR.</span><span class="sxs-lookup"><span data-stu-id="29dbb-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="29dbb-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="29dbb-110">EXAMPLES</span></span>

### <span data-ttu-id="29dbb-111">Установка двух упорядоченных шаблонов восходящего потока</span><span class="sxs-lookup"><span data-stu-id="29dbb-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="29dbb-112">Следующий JSON представляет наборы реальных шаблонов.</span><span class="sxs-lookup"><span data-stu-id="29dbb-112">The following JSON represents the actual templates set.</span></span> 

 `
{
    "hubPattern": "chat",
    "eventPattern": "broadcast",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections1.com"
},
{
    "hubPattern": "*",
    "eventPattern": "*",
    "categoryPattern": "*",
    "urlTemplate": "http://host-connections2.com"
}
`

### <span data-ttu-id="29dbb-113">Удаление всех параметров восходящего потока</span><span class="sxs-lookup"><span data-stu-id="29dbb-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="29dbb-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="29dbb-114">PARAMETERS</span></span>

### <span data-ttu-id="29dbb-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="29dbb-115">-AsJob</span></span>
<span data-ttu-id="29dbb-116">Запустите командлет в фоновом задании.</span><span class="sxs-lookup"><span data-stu-id="29dbb-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="29dbb-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="29dbb-117">-Clear</span></span>
<span data-ttu-id="29dbb-118">Удалите все параметры восходящего потока.</span><span class="sxs-lookup"><span data-stu-id="29dbb-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="29dbb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29dbb-119">-DefaultProfile</span></span>
<span data-ttu-id="29dbb-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="29dbb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29dbb-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="29dbb-121">-InputObject</span></span>
<span data-ttu-id="29dbb-122">Объект Resource SignalR.</span><span class="sxs-lookup"><span data-stu-id="29dbb-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="29dbb-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="29dbb-123">-Name</span></span>
<span data-ttu-id="29dbb-124">Название службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="29dbb-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="29dbb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29dbb-125">-ResourceGroupName</span></span>
<span data-ttu-id="29dbb-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="29dbb-126">The resource group name.</span></span>
<span data-ttu-id="29dbb-127">Значение по умолчанию будет использоваться, если оно не указано.</span><span class="sxs-lookup"><span data-stu-id="29dbb-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="29dbb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29dbb-128">-ResourceId</span></span>
<span data-ttu-id="29dbb-129">Идентификатор ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="29dbb-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="29dbb-130">-Template</span><span class="sxs-lookup"><span data-stu-id="29dbb-130">-Template</span></span>
<span data-ttu-id="29dbb-131">Элементы шаблона (-ов) для параметров восходящего потока.</span><span class="sxs-lookup"><span data-stu-id="29dbb-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="29dbb-132">Обязательный ключ: UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="29dbb-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="29dbb-133">Необязательные клавиши: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="29dbb-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="29dbb-134">Пример использования синтаксиса splatting для передачи параметра Templates: @ {UrlTemplate = ' http://host-connections1.com ', HubPattern = ' chat '; EventPattern = "Broadcast"}, @ {UrlTemplate = ' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="29dbb-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29dbb-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="29dbb-135">-Confirm</span></span>
<span data-ttu-id="29dbb-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="29dbb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29dbb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29dbb-137">-WhatIf</span></span>
<span data-ttu-id="29dbb-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="29dbb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="29dbb-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="29dbb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29dbb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29dbb-140">CommonParameters</span></span>
<span data-ttu-id="29dbb-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="29dbb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29dbb-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="29dbb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29dbb-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="29dbb-143">INPUTS</span></span>

### <span data-ttu-id="29dbb-144">System. String</span><span class="sxs-lookup"><span data-stu-id="29dbb-144">System.String</span></span>

## <span data-ttu-id="29dbb-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="29dbb-145">OUTPUTS</span></span>

### <span data-ttu-id="29dbb-146">Microsoft. Azure. Commands. SignalR. Models. PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="29dbb-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="29dbb-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="29dbb-147">NOTES</span></span>

## <span data-ttu-id="29dbb-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="29dbb-148">RELATED LINKS</span></span>

[<span data-ttu-id="29dbb-149">Использование splatting для передачи параметров командам в PowerShell</span><span class="sxs-lookup"><span data-stu-id="29dbb-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)