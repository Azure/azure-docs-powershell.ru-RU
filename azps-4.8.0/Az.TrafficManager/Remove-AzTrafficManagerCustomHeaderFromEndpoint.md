---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 35ab92add873e603101400f77e813fb115386fd4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94079317"
---
# <span data-ttu-id="96da4-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="96da4-101">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="96da4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="96da4-102">SYNOPSIS</span></span>
<span data-ttu-id="96da4-103">Удаляет данные настраиваемого заголовка из объекта конечной точки диспетчера локальных данных.</span><span class="sxs-lookup"><span data-stu-id="96da4-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="96da4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="96da4-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerCustomHeaderFromEndpoint -Name <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96da4-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="96da4-105">DESCRIPTION</span></span>
<span data-ttu-id="96da4-106">Командлет **Remove-AzTrafficManagerCustomHeaderFromEndpoint** удаляет данные настраиваемого заголовка из локального объекта конечной точки диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="96da4-106">The **Remove-AzTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="96da4-107">Вы можете получить конечную точку с помощью командлетов New-AzTrafficManagerEndpoint или Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="96da4-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="96da4-108">Этот командлет работает с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="96da4-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="96da4-109">Зафиксируйте изменения конечной точки для диспетчера трафика с помощью командлета Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="96da4-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="96da4-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="96da4-110">EXAMPLES</span></span>

### <span data-ttu-id="96da4-111">Пример 1: удаление настраиваемых сведений о подсети из конечной точки</span><span class="sxs-lookup"><span data-stu-id="96da4-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="96da4-112">Первая команда получает конечную точку Azure с именем Contoso из профиля с именем ContosoProfile в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="96da4-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="96da4-113">Вторая команда удаляет данные настраиваемого заголовка из конечной точки, хранящейся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="96da4-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="96da4-114">Последняя команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="96da4-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="96da4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="96da4-115">PARAMETERS</span></span>

### <span data-ttu-id="96da4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96da4-116">-DefaultProfile</span></span>
<span data-ttu-id="96da4-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="96da4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96da4-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="96da4-118">-Name</span></span>
<span data-ttu-id="96da4-119">Указывает имя удаляемых настраиваемых данных заголовка.</span><span class="sxs-lookup"><span data-stu-id="96da4-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="96da4-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96da4-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="96da4-121">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="96da4-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="96da4-122">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="96da4-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="96da4-123">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzTrafficManagerEndpoint или New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="96da4-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="96da4-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96da4-124">-Confirm</span></span>
<span data-ttu-id="96da4-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="96da4-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96da4-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96da4-126">-WhatIf</span></span>
<span data-ttu-id="96da4-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="96da4-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96da4-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="96da4-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96da4-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96da4-129">CommonParameters</span></span>
<span data-ttu-id="96da4-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="96da4-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96da4-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96da4-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96da4-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="96da4-132">INPUTS</span></span>

### <span data-ttu-id="96da4-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96da4-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="96da4-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="96da4-134">OUTPUTS</span></span>

### <span data-ttu-id="96da4-135">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96da4-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="96da4-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="96da4-136">NOTES</span></span>

## <span data-ttu-id="96da4-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="96da4-137">RELATED LINKS</span></span>

[<span data-ttu-id="96da4-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="96da4-138">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="96da4-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="96da4-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="96da4-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96da4-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="96da4-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="96da4-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
