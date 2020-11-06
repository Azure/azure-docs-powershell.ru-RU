---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D345
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 5bb661dbc5a65b9a245fcfa35cdc194bbcded1eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558151"
---
# <span data-ttu-id="56ff7-101">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="56ff7-101">Remove-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="56ff7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="56ff7-102">SYNOPSIS</span></span>
<span data-ttu-id="56ff7-103">Удаление диапазона адресов или подсети из объекта конечной точки диспетчера локальных данных.</span><span class="sxs-lookup"><span data-stu-id="56ff7-103">Removes an address range or subnet from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56ff7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="56ff7-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerIpAddressRange -First <String> -TrafficManagerEndpoint <TrafficManagerEndpoint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56ff7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="56ff7-105">DESCRIPTION</span></span>
<span data-ttu-id="56ff7-106">Командлет **Remove-AzureRmTrafficManagerIpAddressRange** удаляет диапазон IP-адресов из локального объекта конечной точки диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="56ff7-106">The **Remove-AzureRmTrafficManagerIpAddressRange** cmdlet removes an IP address range from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="56ff7-107">Вы можете получить конечную точку с помощью командлетов New-AzureRmTrafficManagerEndpoint или Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56ff7-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="56ff7-108">Этот командлет работает с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="56ff7-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="56ff7-109">Зафиксируйте изменения конечной точки для диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56ff7-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="56ff7-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="56ff7-110">EXAMPLES</span></span>

### <span data-ttu-id="56ff7-111">Пример 1: удаление диапазонов IP-адресов из конечной точки</span><span class="sxs-lookup"><span data-stu-id="56ff7-111">Example 1: Remove IP address ranges from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="56ff7-112">Первая команда получает конечную точку Azure с именем Contoso из профиля с именем ContosoProfile в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56ff7-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="56ff7-113">Вторая команда удаляет диапазон IP-адресов из конечной точки, хранящейся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56ff7-113">The second command removes an IP address range from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="56ff7-114">Последняя команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56ff7-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="56ff7-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="56ff7-115">PARAMETERS</span></span>

### <span data-ttu-id="56ff7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56ff7-116">-DefaultProfile</span></span>
<span data-ttu-id="56ff7-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="56ff7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="56ff7-118">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56ff7-118">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="56ff7-119">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="56ff7-119">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="56ff7-120">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="56ff7-120">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="56ff7-121">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzureRmTrafficManagerEndpoint или New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56ff7-121">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="56ff7-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="56ff7-122">-Confirm</span></span>
<span data-ttu-id="56ff7-123">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="56ff7-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56ff7-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56ff7-124">-WhatIf</span></span>
<span data-ttu-id="56ff7-125">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="56ff7-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="56ff7-126">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="56ff7-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56ff7-127">-First</span><span class="sxs-lookup"><span data-stu-id="56ff7-127">-First</span></span>
<span data-ttu-id="56ff7-128">Задает первый IP-адрес удаляемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="56ff7-128">Specifies the first IP address in the range to be removed.</span></span>

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

### <span data-ttu-id="56ff7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56ff7-129">CommonParameters</span></span>
<span data-ttu-id="56ff7-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="56ff7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56ff7-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56ff7-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56ff7-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="56ff7-132">INPUTS</span></span>

### <span data-ttu-id="56ff7-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56ff7-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="56ff7-134">Этот командлет принимает объект **TrafficManagerEndpoint** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="56ff7-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="56ff7-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="56ff7-135">OUTPUTS</span></span>

### <span data-ttu-id="56ff7-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56ff7-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="56ff7-137">Этот командлет возвращает модифицированный объект TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="56ff7-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="56ff7-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="56ff7-138">NOTES</span></span>

## <span data-ttu-id="56ff7-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="56ff7-139">RELATED LINKS</span></span>

[<span data-ttu-id="56ff7-140">Add-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="56ff7-140">Add-AzureRmTrafficManagerIpAddressRange</span></span>](./Add-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="56ff7-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="56ff7-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="56ff7-142">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56ff7-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="56ff7-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="56ff7-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
