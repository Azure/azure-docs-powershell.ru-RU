---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558184"
---
# <span data-ttu-id="51f6e-101">Add-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="51f6e-101">Add-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="51f6e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="51f6e-102">SYNOPSIS</span></span>
<span data-ttu-id="51f6e-103">Добавляет диапазон адресов или подсеть к объекту конечной точки диспетчера локальных данных.</span><span class="sxs-lookup"><span data-stu-id="51f6e-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="51f6e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="51f6e-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51f6e-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="51f6e-105">DESCRIPTION</span></span>
<span data-ttu-id="51f6e-106">Командлет **Add-AzureRmTrafficManagerIpAddressRange** добавляет диапазон IP-адресов в локальный объект конечной точки диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="51f6e-106">The **Add-AzureRmTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="51f6e-107">Вы можете получить конечную точку с помощью командлетов New-AzureRmTrafficManagerEndpoint или Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51f6e-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="51f6e-108">Этот командлет работает с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="51f6e-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="51f6e-109">Зафиксируйте изменения конечной точки для диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51f6e-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="51f6e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="51f6e-110">EXAMPLES</span></span>

### <span data-ttu-id="51f6e-111">Пример 1: Добавление диапазонов IP-адресов в конечную точку</span><span class="sxs-lookup"><span data-stu-id="51f6e-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="51f6e-112">Первая команда создает конечную точку диспетчера трафика Azure с помощью командлета **New-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="51f6e-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="51f6e-113">Команда хранит локальную конечную точку в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51f6e-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="51f6e-114">Вторая команда добавляет диапазон IP-адресов 1.2.3.4 в 5.6.7.8 в конечную точку, хранящуюся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51f6e-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="51f6e-115">Третья команда добавляет диапазон IP-адресов 9.10.11.0 в 9.10.11.255 в конечную точку, хранящуюся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51f6e-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="51f6e-116">Четвертая команда удостоверяет, что область соответствует размеру диапазона, а затем добавляет диапазон IP-адресов 12.13.14.0 в 12.13.14.31 в конечную точку, хранящуюся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51f6e-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="51f6e-117">Пятая команда добавляет диапазон IP-адресов 15.16.17.18 в 15.16.17.18 в конечную точку, хранящуюся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51f6e-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="51f6e-118">Последняя команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51f6e-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="51f6e-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="51f6e-119">PARAMETERS</span></span>

### <span data-ttu-id="51f6e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51f6e-120">-DefaultProfile</span></span>
<span data-ttu-id="51f6e-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="51f6e-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="51f6e-122">-Last</span><span class="sxs-lookup"><span data-stu-id="51f6e-122">-Last</span></span>
<span data-ttu-id="51f6e-123">Задает последний IP-адрес добавляемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="51f6e-123">Specifies the last IP address in the range to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f6e-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="51f6e-124">-Scope</span></span>
<span data-ttu-id="51f6e-125">Задает область, в которую нужно добавить диапазон IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="51f6e-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51f6e-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="51f6e-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="51f6e-127">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="51f6e-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="51f6e-128">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="51f6e-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="51f6e-129">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzureRmTrafficManagerEndpoint или New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="51f6e-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="51f6e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51f6e-130">-Confirm</span></span>
<span data-ttu-id="51f6e-131">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="51f6e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51f6e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51f6e-132">-WhatIf</span></span>
<span data-ttu-id="51f6e-133">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="51f6e-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51f6e-134">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="51f6e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51f6e-135">-First</span><span class="sxs-lookup"><span data-stu-id="51f6e-135">-First</span></span>
<span data-ttu-id="51f6e-136">Задает первый IP-адрес добавляемого диапазона.</span><span class="sxs-lookup"><span data-stu-id="51f6e-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="51f6e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51f6e-137">CommonParameters</span></span>
<span data-ttu-id="51f6e-138">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="51f6e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51f6e-139">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="51f6e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51f6e-140">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="51f6e-140">INPUTS</span></span>

### <span data-ttu-id="51f6e-141">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="51f6e-141">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="51f6e-142">Этот командлет принимает объект **TrafficManagerEndpoint** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="51f6e-142">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="51f6e-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="51f6e-143">OUTPUTS</span></span>

### <span data-ttu-id="51f6e-144">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="51f6e-144">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="51f6e-145">Этот командлет возвращает модифицированный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="51f6e-145">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="51f6e-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="51f6e-146">NOTES</span></span>

## <span data-ttu-id="51f6e-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="51f6e-147">RELATED LINKS</span></span>

[<span data-ttu-id="51f6e-148">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="51f6e-148">Remove-AzureRmTrafficManagerIpAddressRange</span></span>](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="51f6e-149">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="51f6e-149">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="51f6e-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="51f6e-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="51f6e-151">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="51f6e-151">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
