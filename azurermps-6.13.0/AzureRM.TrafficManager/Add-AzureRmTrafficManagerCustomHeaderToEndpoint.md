---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734583"
---
# <span data-ttu-id="4e5ac-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e5ac-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="4e5ac-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4e5ac-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5ac-103">Добавляет пользовательские данные заголовка в объект конечной точки диспетчера локальных данных.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e5ac-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4e5ac-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e5ac-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e5ac-105">DESCRIPTION</span></span>
<span data-ttu-id="4e5ac-106">Командлет **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** добавляет пользовательские данные заголовка в локальный объект конечной точки диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-106">The **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="4e5ac-107">Вы можете получить конечную точку с помощью командлетов New-AzureRmTrafficManagerEndpoint или Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="4e5ac-108">Этот командлет работает с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="4e5ac-109">Зафиксируйте изменения конечной точки для диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="4e5ac-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4e5ac-110">EXAMPLES</span></span>

### <span data-ttu-id="4e5ac-111">Пример 1: Добавление сведений о настраиваемых заголовках в конечную точку</span><span class="sxs-lookup"><span data-stu-id="4e5ac-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="4e5ac-112">Первая команда создает конечную точку диспетчера трафика Azure с помощью командлета **New-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="4e5ac-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="4e5ac-113">Команда хранит локальную конечную точку в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="4e5ac-114">Вторая команда добавляет сведения о настраиваемых заголовках в конечную точку, хранящуюся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="4e5ac-115">Последняя команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="4e5ac-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4e5ac-116">PARAMETERS</span></span>

### <span data-ttu-id="4e5ac-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e5ac-117">-DefaultProfile</span></span>
<span data-ttu-id="4e5ac-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e5ac-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4e5ac-119">-Name</span></span>
<span data-ttu-id="4e5ac-120">Задает имя добавляемых сведений о настраиваемых заголовках.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="4e5ac-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e5ac-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="4e5ac-122">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="4e5ac-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="4e5ac-123">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="4e5ac-124">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzureRmTrafficManagerEndpoint или New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="4e5ac-125">-Value (значение)</span><span class="sxs-lookup"><span data-stu-id="4e5ac-125">-Value</span></span>
<span data-ttu-id="4e5ac-126">Задает значение добавляемых сведений о настраиваемых заголовках.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="4e5ac-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e5ac-127">-Confirm</span></span>
<span data-ttu-id="4e5ac-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e5ac-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e5ac-129">-WhatIf</span></span>
<span data-ttu-id="4e5ac-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e5ac-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e5ac-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5ac-132">CommonParameters</span></span>
<span data-ttu-id="4e5ac-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5ac-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e5ac-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5ac-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4e5ac-135">INPUTS</span></span>

### <span data-ttu-id="4e5ac-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e5ac-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="4e5ac-137">Этот командлет принимает объект **TrafficManagerEndpoint** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="4e5ac-137">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="4e5ac-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4e5ac-138">OUTPUTS</span></span>

### <span data-ttu-id="4e5ac-139">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e5ac-139">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="4e5ac-140">Этот командлет возвращает модифицированный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="4e5ac-140">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="4e5ac-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="4e5ac-141">NOTES</span></span>

## <span data-ttu-id="4e5ac-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4e5ac-142">RELATED LINKS</span></span>

[<span data-ttu-id="4e5ac-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e5ac-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="4e5ac-144">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e5ac-144">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="4e5ac-145">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="4e5ac-145">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="4e5ac-146">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4e5ac-146">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
