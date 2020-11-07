---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/remove-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Remove-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: ea69e8d07278be2c9f122d179090e63b9153128d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93728385"
---
# <span data-ttu-id="15f70-101">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="15f70-101">Remove-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="15f70-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="15f70-102">SYNOPSIS</span></span>
<span data-ttu-id="15f70-103">Удаление диапазона адресов или подсети из объекта конечной точки диспетчера локальных данных.</span><span class="sxs-lookup"><span data-stu-id="15f70-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="15f70-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="15f70-104">SYNTAX</span></span>

```
Remove-AzTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15f70-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="15f70-105">DESCRIPTION</span></span>
<span data-ttu-id="15f70-106">Командлет **Remove-AzTrafficManagerIpAddressRange** удаляет диапазон IP-адресов из локального объекта конечной точки диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="15f70-106">The **Remove-AzTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="15f70-107">Вы можете получить конечную точку с помощью командлетов New-AzTrafficManagerEndpoint или Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="15f70-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="15f70-108">Этот командлет работает с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="15f70-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="15f70-109">Зафиксируйте изменения конечной точки для диспетчера трафика с помощью командлета Set-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="15f70-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="15f70-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="15f70-110">EXAMPLES</span></span>

### <span data-ttu-id="15f70-111">Пример 1: удаление диапазонов IP-адресов из конечной точки</span><span class="sxs-lookup"><span data-stu-id="15f70-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="15f70-112">Первая команда получает конечную точку Azure с именем Contoso из профиля с именем ContosoProfile в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="15f70-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="15f70-113">Вторая команда удаляет диапазон IP-адресов из конечной точки, хранящейся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="15f70-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="15f70-114">Последняя команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="15f70-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="15f70-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="15f70-115">PARAMETERS</span></span>

### <span data-ttu-id="15f70-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15f70-116">-DefaultProfile</span></span>
<span data-ttu-id="15f70-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="15f70-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15f70-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15f70-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="15f70-119">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="15f70-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="15f70-120">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="15f70-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="15f70-121">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzTrafficManagerEndpoint или New-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="15f70-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="15f70-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="15f70-122">-Confirm</span></span>
<span data-ttu-id="15f70-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="15f70-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15f70-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15f70-124">-WhatIf</span></span>
<span data-ttu-id="15f70-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="15f70-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15f70-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="15f70-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15f70-127">-First</span><span class="sxs-lookup"><span data-stu-id="15f70-127">-First</span></span>
<span data-ttu-id="15f70-128">Задает первый IP-адрес удаляемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="15f70-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="15f70-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15f70-129">CommonParameters</span></span>
<span data-ttu-id="15f70-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="15f70-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15f70-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15f70-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15f70-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="15f70-132">INPUTS</span></span>

### <span data-ttu-id="15f70-133">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15f70-133">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="15f70-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="15f70-134">OUTPUTS</span></span>

### <span data-ttu-id="15f70-135">Microsoft. Azure. Commands. TrafficManager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15f70-135">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="15f70-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="15f70-136">NOTES</span></span>

## <span data-ttu-id="15f70-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="15f70-137">RELATED LINKS</span></span>

[<span data-ttu-id="15f70-138">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="15f70-138">Add-AzTrafficManagerIpAddressRange</span></span>](./Add-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="15f70-139">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="15f70-139">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15f70-140">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15f70-140">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="15f70-141">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="15f70-141">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
