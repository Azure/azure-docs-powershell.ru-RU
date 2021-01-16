---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/set-azsignalrupstream
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/Set-AzSignalRUpstream.md
ms.openlocfilehash: e04e87067f86f529117512e7443118f308b20547
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98397092"
---
# <span data-ttu-id="59504-101">Set-AzSignalRUpstream</span><span class="sxs-lookup"><span data-stu-id="59504-101">Set-AzSignalRUpstream</span></span>

## <span data-ttu-id="59504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59504-102">SYNOPSIS</span></span>
<span data-ttu-id="59504-103">Настройка upstream параметров службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="59504-103">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="59504-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="59504-104">SYNTAX</span></span>

### <span data-ttu-id="59504-105">ResourceGroupParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="59504-105">ResourceGroupParameterSet (Default)</span></span>
```
Set-AzSignalRUpstream [-ResourceGroupName <String>] [-Name] <String> [-AsJob]
 [-Template <PSUpstreamTemplate[]>] [-Clear] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="59504-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59504-106">ResourceIdParameterSet</span></span>
```
Set-AzSignalRUpstream -ResourceId <String> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59504-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59504-107">InputObjectParameterSet</span></span>
```
Set-AzSignalRUpstream -InputObject <PSSignalRResource> [-AsJob] [-Template <PSUpstreamTemplate[]>] [-Clear]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59504-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59504-108">DESCRIPTION</span></span>
<span data-ttu-id="59504-109">Настройка upstream параметров службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="59504-109">Set the upstream settings of a SignalR service.</span></span>

## <span data-ttu-id="59504-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="59504-110">EXAMPLES</span></span>

### <span data-ttu-id="59504-111">Настройка двух упорядоченных вверх шаблонов</span><span class="sxs-lookup"><span data-stu-id="59504-111">Set two ordered upstream templates</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Template @{UrlTemplate='http://host-connections1.com'; HubPattern='chat';EventPattern='broadcast' }, @{UrlTemplate='http://host-connections2.com'}

Templates
---------
{Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplate, Microsoft.Azure.Commands.SignalR.Models.PSUpstreamTemplat…
```

<span data-ttu-id="59504-112">Следующая версия JSON представляет собой фактический набор шаблонов.</span><span class="sxs-lookup"><span data-stu-id="59504-112">The following JSON represents the actual templates set.</span></span> 

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

### <span data-ttu-id="59504-113">Очистка всех параметров в потоках</span><span class="sxs-lookup"><span data-stu-id="59504-113">Clear all the upstream settings</span></span>
```powershell
PS C:\>  Set-AzSignalRUpstream -name pssignalr -ResourceGroupName test_resource_group -Clear

Templates
---------
{}
```

## <span data-ttu-id="59504-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59504-114">PARAMETERS</span></span>

### <span data-ttu-id="59504-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59504-115">-AsJob</span></span>
<span data-ttu-id="59504-116">Запустите проектлет в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="59504-116">Run the cmdlet in background job.</span></span>

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

### <span data-ttu-id="59504-117">-Clear</span><span class="sxs-lookup"><span data-stu-id="59504-117">-Clear</span></span>
<span data-ttu-id="59504-118">Очистка всех параметров в потоках.</span><span class="sxs-lookup"><span data-stu-id="59504-118">Clear all the upstream settings.</span></span>

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

### <span data-ttu-id="59504-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59504-119">-DefaultProfile</span></span>
<span data-ttu-id="59504-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="59504-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59504-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="59504-121">-InputObject</span></span>
<span data-ttu-id="59504-122">Объект ресурса SignalR.</span><span class="sxs-lookup"><span data-stu-id="59504-122">The SignalR resource object.</span></span>

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

### <span data-ttu-id="59504-123">-Name</span><span class="sxs-lookup"><span data-stu-id="59504-123">-Name</span></span>
<span data-ttu-id="59504-124">Имя службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="59504-124">The SignalR service name.</span></span>

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

### <span data-ttu-id="59504-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59504-125">-ResourceGroupName</span></span>
<span data-ttu-id="59504-126">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="59504-126">The resource group name.</span></span>
<span data-ttu-id="59504-127">Значение по умолчанию будет использоваться, если не указано.</span><span class="sxs-lookup"><span data-stu-id="59504-127">The default one will be used if not specified.</span></span>

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

### <span data-ttu-id="59504-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59504-128">-ResourceId</span></span>
<span data-ttu-id="59504-129">ИД ресурса службы SignalR.</span><span class="sxs-lookup"><span data-stu-id="59504-129">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="59504-130">-Template</span><span class="sxs-lookup"><span data-stu-id="59504-130">-Template</span></span>
<span data-ttu-id="59504-131">Пункты шаблона для параметров в потоках вверх.</span><span class="sxs-lookup"><span data-stu-id="59504-131">Template item(s) for upstream settings.</span></span>
<span data-ttu-id="59504-132">Требуемая клавиша: URLTemplate.</span><span class="sxs-lookup"><span data-stu-id="59504-132">Required key: UrlTemplate.</span></span>
<span data-ttu-id="59504-133">Необязательные клавиши: HubPattern, EventPattern, CategoryPattern.</span><span class="sxs-lookup"><span data-stu-id="59504-133">Optional keys: HubPattern, EventPattern, CategoryPattern.</span></span>
<span data-ttu-id="59504-134">Пример использования синтаксиса с splatting для параметра шаблонов: @{UrlTemplate=' http://host-connections1.com ', HubPattern= 'chat'; EventPattern='broadcast' },@{UrlTemplate=' http://host-connections2.com '}</span><span class="sxs-lookup"><span data-stu-id="59504-134">Example using splatting syntax to pass templates parameter: @{UrlTemplate='http://host-connections1.com', HubPattern= 'chat';EventPattern='broadcast' },@{UrlTemplate='http://host-connections2.com'}</span></span>

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

### <span data-ttu-id="59504-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59504-135">-Confirm</span></span>
<span data-ttu-id="59504-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59504-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59504-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59504-137">-WhatIf</span></span>
<span data-ttu-id="59504-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59504-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59504-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="59504-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59504-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59504-140">CommonParameters</span></span>
<span data-ttu-id="59504-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59504-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59504-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59504-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59504-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="59504-143">INPUTS</span></span>

### <span data-ttu-id="59504-144">System.String</span><span class="sxs-lookup"><span data-stu-id="59504-144">System.String</span></span>

## <span data-ttu-id="59504-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="59504-145">OUTPUTS</span></span>

### <span data-ttu-id="59504-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span><span class="sxs-lookup"><span data-stu-id="59504-146">Microsoft.Azure.Commands.SignalR.Models.PSServerlessUpstreamSettings</span></span>

## <span data-ttu-id="59504-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="59504-147">NOTES</span></span>

## <span data-ttu-id="59504-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59504-148">RELATED LINKS</span></span>

[<span data-ttu-id="59504-149">Использование параметра splatting для управления параметрами в командах PowerShell</span><span class="sxs-lookup"><span data-stu-id="59504-149">How to use splatting to pass parameters to commands in PowerShell</span></span>](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.core/about/about_splatting?view=powershell-7)