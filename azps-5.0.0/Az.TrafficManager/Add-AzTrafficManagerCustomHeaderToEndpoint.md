---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249422"
---
# <span data-ttu-id="2dcb2-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dcb2-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="2dcb2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2dcb2-102">SYNOPSIS</span></span>
<span data-ttu-id="2dcb2-103">Добавляет пользовательские данные заголовка в объект конечной точки диспетчера локальных данных.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="2dcb2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2dcb2-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2dcb2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dcb2-105">DESCRIPTION</span></span>
<span data-ttu-id="2dcb2-106">Командлет **Add-AzTrafficManagerCustomHeaderToEndpoint** добавляет пользовательские данные заголовка в локальный объект конечной точки диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="2dcb2-107">Вы можете получить конечную точку с помощью командлетов New-AzTrafficManagerEndpoint или Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="2dcb2-108">Этот командлет работает с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="2dcb2-109">Зафиксируйте изменения конечной точки для диспетчера трафика с помощью командлета Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="2dcb2-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2dcb2-110">EXAMPLES</span></span>

### <span data-ttu-id="2dcb2-111">Пример 1: Добавление сведений о настраиваемых заголовках в конечную точку</span><span class="sxs-lookup"><span data-stu-id="2dcb2-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="2dcb2-112">Первая команда создает конечную точку диспетчера трафика Azure с помощью командлета **New-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="2dcb2-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="2dcb2-113">Команда хранит локальную конечную точку в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="2dcb2-114">Вторая команда добавляет сведения о настраиваемых заголовках в конечную точку, хранящуюся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="2dcb2-115">Последняя команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="2dcb2-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2dcb2-116">PARAMETERS</span></span>

### <span data-ttu-id="2dcb2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dcb2-117">-DefaultProfile</span></span>
<span data-ttu-id="2dcb2-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dcb2-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2dcb2-119">-Name</span></span>
<span data-ttu-id="2dcb2-120">Задает имя добавляемых сведений о настраиваемых заголовках.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="2dcb2-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dcb2-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="2dcb2-122">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="2dcb2-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="2dcb2-123">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="2dcb2-124">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzTrafficManagerEndpoint или New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="2dcb2-125">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="2dcb2-125">-Value</span></span>
<span data-ttu-id="2dcb2-126">Задает значение добавляемых сведений о настраиваемых заголовках.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="2dcb2-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2dcb2-127">-Confirm</span></span>
<span data-ttu-id="2dcb2-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2dcb2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2dcb2-129">-WhatIf</span></span>
<span data-ttu-id="2dcb2-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2dcb2-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2dcb2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dcb2-132">CommonParameters</span></span>
<span data-ttu-id="2dcb2-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2dcb2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dcb2-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dcb2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dcb2-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2dcb2-135">INPUTS</span></span>

### <span data-ttu-id="2dcb2-136">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dcb2-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2dcb2-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2dcb2-137">OUTPUTS</span></span>

### <span data-ttu-id="2dcb2-138">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dcb2-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="2dcb2-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="2dcb2-139">NOTES</span></span>

## <span data-ttu-id="2dcb2-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2dcb2-140">RELATED LINKS</span></span>

[<span data-ttu-id="2dcb2-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dcb2-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="2dcb2-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dcb2-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2dcb2-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="2dcb2-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="2dcb2-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="2dcb2-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)