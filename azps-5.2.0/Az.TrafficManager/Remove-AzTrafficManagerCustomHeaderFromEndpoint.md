---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98391423"
---
# <span data-ttu-id="0c594-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c594-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="0c594-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c594-102">SYNOPSIS</span></span>
<span data-ttu-id="0c594-103">Удаляет пользовательские данные загона из локального объекта конечной точки Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="0c594-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="0c594-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0c594-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c594-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0c594-105">DESCRIPTION</span></span>
<span data-ttu-id="0c594-106">Cmdlet **Remove-AzTrafficManagerCustomHeaderFromEndpoint** удаляет пользовательские данные заголовок из локального объекта конечной точки Диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="0c594-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="0c594-107">Конечную точку можно получить с помощью New-AzTrafficManagerEndpoint или Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0c594-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="0c594-108">Этот cmdlet выполняется с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="0c594-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="0c594-109">Зафиксировать изменения в конечной точке диспетчера трафика с помощью Set-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="0c594-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="0c594-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0c594-110">EXAMPLES</span></span>

### <span data-ttu-id="0c594-111">Пример 1. Удаление сведений настраиваемой подсети из конечной точки</span><span class="sxs-lookup"><span data-stu-id="0c594-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="0c594-112">Первая команда получает конечную точку Azure contoso из профиля ContosoProfile в группе ресурсов ResourceGroup11, а затем сохраняет объект в переменной $TrafficManagerEndpoint ресурса.</span><span class="sxs-lookup"><span data-stu-id="0c594-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="0c594-113">Вторая команда удаляет настраиваемые данные загона из конечной точки, храняной в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0c594-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="0c594-114">Конечная команда обновляет конечную точку диспетчера трафика в соответствие с локальным значением в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0c594-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="0c594-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c594-115">PARAMETERS</span></span>

### <span data-ttu-id="0c594-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c594-116">-DefaultProfile</span></span>
<span data-ttu-id="0c594-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0c594-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c594-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0c594-118">-Name</span></span>
<span data-ttu-id="0c594-119">Указывает имя удаляемой настраиваемой информации.</span><span class="sxs-lookup"><span data-stu-id="0c594-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="0c594-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c594-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="0c594-121">Определяет локальный **объект TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="0c594-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="0c594-122">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="0c594-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="0c594-123">Чтобы получить объект **TrafficManagerEndpoint,** воспользуйтесь Get-AzTrafficManagerEndpoint или New-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="0c594-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="0c594-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c594-124">-Confirm</span></span>
<span data-ttu-id="0c594-125">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="0c594-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c594-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c594-126">-WhatIf</span></span>
<span data-ttu-id="0c594-127">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c594-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c594-128">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0c594-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c594-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c594-129">CommonParameters</span></span>
<span data-ttu-id="0c594-130">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c594-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c594-131">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c594-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c594-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0c594-132">INPUTS</span></span>

### <span data-ttu-id="0c594-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c594-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0c594-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0c594-134">OUTPUTS</span></span>

### <span data-ttu-id="0c594-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c594-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="0c594-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0c594-136">NOTES</span></span>

## <span data-ttu-id="0c594-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0c594-137">RELATED LINKS</span></span>

[<span data-ttu-id="0c594-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c594-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="0c594-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="0c594-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0c594-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c594-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="0c594-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0c594-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
