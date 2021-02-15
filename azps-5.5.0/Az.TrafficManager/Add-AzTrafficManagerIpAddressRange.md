---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100232385"
---
# <span data-ttu-id="a4f62-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="a4f62-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="a4f62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4f62-102">SYNOPSIS</span></span>
<span data-ttu-id="a4f62-103">Добавляет диапазон адреса или подсеть в локальный объект конечной точки Диспетчера трафика.</span><span class="sxs-lookup"><span data-stu-id="a4f62-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="a4f62-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a4f62-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4f62-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4f62-105">DESCRIPTION</span></span>
<span data-ttu-id="a4f62-106">С **помощью cmdlet Add-AzTrafficManagerIpAddressRange** можно добавить диапазон IP-адресов в локальный объект конечной точки Диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f62-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="a4f62-107">Конечную точку можно получить с помощью New-AzTrafficManagerEndpoint или Get-AzTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a4f62-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="a4f62-108">Этот cmdlet выполняется с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="a4f62-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="a4f62-109">Зафиксировать изменения в конечной точке диспетчера трафика с помощью Set-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="a4f62-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="a4f62-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a4f62-110">EXAMPLES</span></span>

### <span data-ttu-id="a4f62-111">Пример 1. Добавление диапазонов IP-адресов на конечную точку</span><span class="sxs-lookup"><span data-stu-id="a4f62-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="a4f62-112">Первая команда создает конечную точку Диспетчера трафика Azure с помощью командлета **New-AzTrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="a4f62-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="a4f62-113">При этом локализованная конечная точка хранится в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a4f62-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="a4f62-114">Вторая команда добавляет диапазон IP-адресов 1.2.3.4 к 5.6.7.8 к конечной точке, $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a4f62-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="a4f62-115">Третья команда добавляет диапазон IP-адресов 9.10.11.0 к 9.10.11.255 к конечной точке, $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a4f62-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="a4f62-116">Четвертая команда проверяет, совпадает ли область с размером диапазона, а затем добавляет диапазон IP-адресов 12.13.14.0 к 12.13.14.31 к конечной точке, храняной в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a4f62-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="a4f62-117">Пятая команда добавляет диапазон IP-адресов 15.16.17.18 к 15.16.17.18 к конечной точке, $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a4f62-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="a4f62-118">Конечная команда обновляет конечную точку диспетчера трафика в соответствие с локальным значением в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="a4f62-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="a4f62-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4f62-119">PARAMETERS</span></span>

### <span data-ttu-id="a4f62-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4f62-120">-DefaultProfile</span></span>
<span data-ttu-id="a4f62-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4f62-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4f62-122">-Last</span><span class="sxs-lookup"><span data-stu-id="a4f62-122">-Last</span></span>
<span data-ttu-id="a4f62-123">Указывает последний IP-адрес в добавляемом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="a4f62-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="a4f62-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="a4f62-124">-Scope</span></span>
<span data-ttu-id="a4f62-125">Определяет область добавляемого диапазона IP-адресов.</span><span class="sxs-lookup"><span data-stu-id="a4f62-125">Specifies the scope of the IP address range to be added.</span></span>

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

### <span data-ttu-id="a4f62-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a4f62-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="a4f62-127">Определяет локальный **объект TrafficManagerEndpoint.**</span><span class="sxs-lookup"><span data-stu-id="a4f62-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="a4f62-128">Этот cmdlet изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="a4f62-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="a4f62-129">Чтобы получить объект **TrafficManagerEndpoint,** воспользуйтесь Get-AzTrafficManagerEndpoint или New-AzTrafficManagerEndpoint управления.</span><span class="sxs-lookup"><span data-stu-id="a4f62-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="a4f62-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a4f62-130">-Confirm</span></span>
<span data-ttu-id="a4f62-131">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="a4f62-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4f62-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4f62-132">-WhatIf</span></span>
<span data-ttu-id="a4f62-133">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4f62-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a4f62-134">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="a4f62-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4f62-135">-First</span><span class="sxs-lookup"><span data-stu-id="a4f62-135">-First</span></span>
<span data-ttu-id="a4f62-136">Указывает первый IP-адрес в добавляемом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="a4f62-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="a4f62-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4f62-137">CommonParameters</span></span>
<span data-ttu-id="a4f62-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4f62-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4f62-139">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4f62-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4f62-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a4f62-140">INPUTS</span></span>

### <span data-ttu-id="a4f62-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a4f62-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a4f62-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a4f62-142">OUTPUTS</span></span>

### <span data-ttu-id="a4f62-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a4f62-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="a4f62-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a4f62-144">NOTES</span></span>

## <span data-ttu-id="a4f62-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4f62-145">RELATED LINKS</span></span>

[<span data-ttu-id="a4f62-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="a4f62-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="a4f62-147">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a4f62-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a4f62-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="a4f62-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="a4f62-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a4f62-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
