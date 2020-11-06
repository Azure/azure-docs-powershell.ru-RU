---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D342
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/remove-azurermtrafficmanagercustomheaderfromendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md
ms.openlocfilehash: 452e252b7bf9368ea89e81f2d37fd5a80ab079b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558159"
---
# <span data-ttu-id="f4b2a-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4b2a-101">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>

## <span data-ttu-id="f4b2a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f4b2a-102">SYNOPSIS</span></span>
<span data-ttu-id="f4b2a-103">Удаляет данные настраиваемого заголовка из объекта конечной точки диспетчера локальных данных.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-103">Removes custom header information from a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4b2a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f4b2a-104">SYNTAX</span></span>

```
Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -Name <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4b2a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4b2a-105">DESCRIPTION</span></span>
<span data-ttu-id="f4b2a-106">Командлет **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** удаляет данные настраиваемого заголовка из локального объекта конечной точки диспетчера трафика Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-106">The **Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint** cmdlet removes custom header information from a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="f4b2a-107">Вы можете получить конечную точку с помощью командлетов New-AzureRmTrafficManagerEndpoint или Get-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="f4b2a-108">Этот командлет работает с объектом локальной конечной точки.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="f4b2a-109">Зафиксируйте изменения конечной точки для диспетчера трафика с помощью командлета Set-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="f4b2a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f4b2a-110">EXAMPLES</span></span>

### <span data-ttu-id="f4b2a-111">Пример 1: удаление настраиваемых сведений о подсети из конечной точки</span><span class="sxs-lookup"><span data-stu-id="f4b2a-111">Example 1: Remove custom subnet information from an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = Get-AzureRmTrafficManagerEndpoint -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints
PS C:\> Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="f4b2a-112">Первая команда получает конечную точку Azure с именем Contoso из профиля с именем ContosoProfile в группе ресурсов с именем ResourceGroup11 и сохраняет этот объект в переменной $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-112">The first command gets the Azure endpoint named contoso from the profile named ContosoProfile in the resource group named ResourceGroup11, and then stores that object in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="f4b2a-113">Вторая команда удаляет данные настраиваемого заголовка из конечной точки, хранящейся в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-113">The second command removes custom header information from the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="f4b2a-114">Последняя команда обновляет конечную точку в диспетчере трафика таким образом, чтобы она соответствовала локальному значению в $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-114">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="f4b2a-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f4b2a-115">PARAMETERS</span></span>

### <span data-ttu-id="f4b2a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4b2a-116">-DefaultProfile</span></span>
<span data-ttu-id="f4b2a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4b2a-118">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f4b2a-118">-Name</span></span>
<span data-ttu-id="f4b2a-119">Указывает имя удаляемых настраиваемых данных заголовка.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-119">Specifies the name of the custom header information to be removed.</span></span>

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

### <span data-ttu-id="f4b2a-120">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4b2a-120">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="f4b2a-121">Указывает локальный объект **TrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="f4b2a-121">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="f4b2a-122">Этот командлет изменяет этот локальный объект.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-122">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="f4b2a-123">Чтобы получить объект **TrafficManagerEndpoint** , используйте командлет Get-AzureRmTrafficManagerEndpoint или New-AzureRmTrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-123">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="f4b2a-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f4b2a-124">-Confirm</span></span>
<span data-ttu-id="f4b2a-125">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4b2a-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4b2a-126">-WhatIf</span></span>
<span data-ttu-id="f4b2a-127">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4b2a-128">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4b2a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4b2a-129">CommonParameters</span></span>
<span data-ttu-id="f4b2a-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4b2a-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4b2a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4b2a-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f4b2a-132">INPUTS</span></span>

### <span data-ttu-id="f4b2a-133">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4b2a-133">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="f4b2a-134">Этот командлет принимает объект **TrafficManagerEndpoint** для этого командлета.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-134">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="f4b2a-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f4b2a-135">OUTPUTS</span></span>

### <span data-ttu-id="f4b2a-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4b2a-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="f4b2a-137">Этот командлет возвращает модифицированный объект TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="f4b2a-137">This cmdlet returns a modified TrafficManagerEndpoint object.</span></span>

## <span data-ttu-id="f4b2a-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="f4b2a-138">NOTES</span></span>

## <span data-ttu-id="f4b2a-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f4b2a-139">RELATED LINKS</span></span>

[<span data-ttu-id="f4b2a-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4b2a-140">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>](./Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md)

[<span data-ttu-id="f4b2a-141">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="f4b2a-141">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f4b2a-142">New-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4b2a-142">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="f4b2a-143">Set-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f4b2a-143">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
