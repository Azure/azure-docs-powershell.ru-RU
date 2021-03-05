---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 4a24953dd763c54cba7454bf9e46bb9373b0f450
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987409"
---
# <span data-ttu-id="9d42f-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d42f-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="9d42f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d42f-102">SYNOPSIS</span></span>
<span data-ttu-id="9d42f-103">Добавляет пользовательские сведения о заглавной точке в локальный объект конечной точки Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="9d42f-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="9d42f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d42f-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d42f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d42f-105">DESCRIPTION</span></span>
<span data-ttu-id="9d42f-106">Cmdlet **Add-AzTrafficManagerCustomHeaderToEndpoint** добавляет пользовательские данные заголовок к локальному объекту конечной точки Диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="9d42f-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="9d42f-107">Конечную точку можно получить с помощью New-AzTrafficManagerEndpoint или Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9d42f-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="9d42f-108">Этот cmdlet выполняется с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="9d42f-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="9d42f-109">Зафиксировать изменения в конечной точке диспетчера трафика с помощью Set-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="9d42f-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="9d42f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d42f-110">EXAMPLES</span></span>

### <span data-ttu-id="9d42f-111">Пример 1. Добавление пользовательских данных в конечную точку</span><span class="sxs-lookup"><span data-stu-id="9d42f-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="9d42f-112">Первая команда создает конечную точку Диспетчера трафика Azure с помощью командлета **New-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="9d42f-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="9d42f-113">При этом локализованная конечная точка хранится в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9d42f-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="9d42f-114">Вторая команда добавляет настраиваемые сведения о заглавных точках в конечную точку, $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9d42f-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="9d42f-115">Конечная команда обновляет конечную точку диспетчера трафика в соответствие с локальным значением в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9d42f-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="9d42f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d42f-116">PARAMETERS</span></span>

### <span data-ttu-id="9d42f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d42f-117">-DefaultProfile</span></span>
<span data-ttu-id="9d42f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d42f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d42f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9d42f-119">-Name</span></span>
<span data-ttu-id="9d42f-120">Определяет имя добавляемой настраиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="9d42f-120">Specifies the name of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d42f-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d42f-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="9d42f-122">Определяет локальный **объект TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="9d42f-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="9d42f-123">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="9d42f-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="9d42f-124">Чтобы получить объект **TrafficManagerEndpoint,** воспользуйтесь Get-AzTrafficManagerEndpoint или New-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="9d42f-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d42f-125">-Значение</span><span class="sxs-lookup"><span data-stu-id="9d42f-125">-Value</span></span>
<span data-ttu-id="9d42f-126">Определяет значение добавляемой настраиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="9d42f-126">Specifies the value of the custom header information to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9d42f-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d42f-127">-Confirm</span></span>
<span data-ttu-id="9d42f-128">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="9d42f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d42f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d42f-129">-WhatIf</span></span>
<span data-ttu-id="9d42f-130">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d42f-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d42f-131">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d42f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d42f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d42f-132">CommonParameters</span></span>
<span data-ttu-id="9d42f-133">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d42f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d42f-134">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d42f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d42f-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d42f-135">INPUTS</span></span>

### <span data-ttu-id="9d42f-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d42f-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9d42f-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d42f-137">OUTPUTS</span></span>

### <span data-ttu-id="9d42f-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d42f-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="9d42f-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d42f-139">NOTES</span></span>

## <span data-ttu-id="9d42f-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d42f-140">RELATED LINKS</span></span>

[<span data-ttu-id="9d42f-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d42f-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="9d42f-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d42f-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9d42f-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="9d42f-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="9d42f-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="9d42f-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
