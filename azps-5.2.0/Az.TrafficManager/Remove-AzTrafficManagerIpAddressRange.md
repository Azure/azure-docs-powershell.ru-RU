---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: bfeef76b700eb408da89561464bc5457f94cdd4a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402079"
---
# <span data-ttu-id="afd4e-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="afd4e-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="afd4e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afd4e-102">SYNOPSIS</span></span>
<span data-ttu-id="afd4e-103">Удаляет диапазон адресов или подсеть из локального объекта конечной точки Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="afd4e-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="afd4e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="afd4e-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="afd4e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="afd4e-105">DESCRIPTION</span></span>
<span data-ttu-id="afd4e-106">С **помощью командылета Remove-AzTrafficManagerIpAddressRange** можно удалить диапазон IP-адресов из локального объекта конечной точки Диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="afd4e-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="afd4e-107">Конечную точку можно получить с помощью New-AzTrafficManagerEndpoint или Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="afd4e-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="afd4e-108">Этот cmdlet выполняется с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="afd4e-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="afd4e-109">Зафиксировать изменения в конечной точке диспетчера трафика с помощью Set-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="afd4e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="afd4e-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="afd4e-110">EXAMPLES</span></span>

### <span data-ttu-id="afd4e-111">Пример 1. Удаление диапазонов IP-адресов из конечной точки</span><span class="sxs-lookup"><span data-stu-id="afd4e-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="afd4e-112">Первая команда получает конечную точку Azure contoso из профиля ContosoProfile в группе ресурсов ResourceGroup11, а затем сохраняет объект в переменной $TrafficManagerEndpoint ресурса.</span><span class="sxs-lookup"><span data-stu-id="afd4e-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="afd4e-113">Вторая команда удаляет диапазон IP-адресов из конечной точки, $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="afd4e-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="afd4e-114">Конечная команда обновляет конечную точку диспетчера трафика в соответствие с локальным значением в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="afd4e-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="afd4e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="afd4e-115">PARAMETERS</span></span>

### <span data-ttu-id="afd4e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afd4e-116">-DefaultProfile</span></span>
<span data-ttu-id="afd4e-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="afd4e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afd4e-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afd4e-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="afd4e-119">Определяет локальный **объект TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="afd4e-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="afd4e-120">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="afd4e-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="afd4e-121">Чтобы получить объект **TrafficManagerEndpoint,** воспользуйтесь Get-AzTrafficManagerEndpoint или New-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="afd4e-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="afd4e-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="afd4e-122">-Confirm</span></span>
<span data-ttu-id="afd4e-123">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="afd4e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="afd4e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="afd4e-124">-WhatIf</span></span>
<span data-ttu-id="afd4e-125">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="afd4e-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="afd4e-126">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="afd4e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="afd4e-127">-First</span><span class="sxs-lookup"><span data-stu-id="afd4e-127">-First</span></span>
<span data-ttu-id="afd4e-128">Указывает первый IP-адрес в диапазоне, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="afd4e-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="afd4e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afd4e-129">CommonParameters</span></span>
<span data-ttu-id="afd4e-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afd4e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afd4e-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afd4e-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afd4e-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="afd4e-132">INPUTS</span></span>

### <span data-ttu-id="afd4e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afd4e-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="afd4e-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="afd4e-134">OUTPUTS</span></span>

### <span data-ttu-id="afd4e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afd4e-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="afd4e-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="afd4e-136">NOTES</span></span>

## <span data-ttu-id="afd4e-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="afd4e-137">RELATED LINKS</span></span>

[<span data-ttu-id="afd4e-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="afd4e-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="afd4e-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="afd4e-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afd4e-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afd4e-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="afd4e-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="afd4e-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
