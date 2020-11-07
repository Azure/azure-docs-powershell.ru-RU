---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 7f6b68b02644b8244459398028680c9872fffa84
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93730346"
---
# <span data-ttu-id="0b2a4-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b2a4-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="0b2a4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0b2a4-102">SYNOPSIS</span></span>
<span data-ttu-id="0b2a4-103">Создание Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="0b2a4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0b2a4-104">SYNTAX</span></span>

### <span data-ttu-id="0b2a4-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0b2a4-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b2a4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b2a4-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b2a4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b2a4-107">DESCRIPTION</span></span>
<span data-ttu-id="0b2a4-108">Командлет **New-AzExpressRoutePort** создает Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b2a4-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="0b2a4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0b2a4-109">EXAMPLES</span></span>

### <span data-ttu-id="0b2a4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0b2a4-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="0b2a4-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0b2a4-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="0b2a4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0b2a4-112">PARAMETERS</span></span>

### <span data-ttu-id="0b2a4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0b2a4-113">-AsJob</span></span>
<span data-ttu-id="0b2a4-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0b2a4-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="0b2a4-115">-BandwidthInGbps</span></span>
<span data-ttu-id="0b2a4-116">Пропускная способность приобретенных портов в Гбит/с</span><span class="sxs-lookup"><span data-stu-id="0b2a4-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b2a4-117">-DefaultProfile</span></span>
<span data-ttu-id="0b2a4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b2a4-119">-Инкапсуляция</span><span class="sxs-lookup"><span data-stu-id="0b2a4-119">-Encapsulation</span></span>
<span data-ttu-id="0b2a4-120">Метод инкапсуляции на физических портах.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-120">Encapsulation method on physical ports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="0b2a4-121">-Force</span></span>
<span data-ttu-id="0b2a4-122">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="0b2a4-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-123">-Link</span><span class="sxs-lookup"><span data-stu-id="0b2a4-123">-Link</span></span>
<span data-ttu-id="0b2a4-124">Набор физических ссылок на ресурс ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b2a4-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-125">-Location</span><span class="sxs-lookup"><span data-stu-id="0b2a4-125">-Location</span></span>
<span data-ttu-id="0b2a4-126">Расположение.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-126">The location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0b2a4-127">-Name</span></span>
<span data-ttu-id="0b2a4-128">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-128">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="0b2a4-129">-PeeringLocation</span></span>
<span data-ttu-id="0b2a4-130">Имя расположения пиринга, которое физически сопоставлено ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b2a4-131">-ResourceGroupName</span></span>
<span data-ttu-id="0b2a4-132">Имя группы ресурсов для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b2a4-133">-ResourceId</span></span>
<span data-ttu-id="0b2a4-134">ResourceId для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-134">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="0b2a4-135">-Tag</span></span>
<span data-ttu-id="0b2a4-136">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-136">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b2a4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0b2a4-137">-Confirm</span></span>
<span data-ttu-id="0b2a4-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b2a4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b2a4-139">-WhatIf</span></span>
<span data-ttu-id="0b2a4-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b2a4-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b2a4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b2a4-142">CommonParameters</span></span>
<span data-ttu-id="0b2a4-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0b2a4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b2a4-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b2a4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b2a4-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0b2a4-145">INPUTS</span></span>

### <span data-ttu-id="0b2a4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0b2a4-146">System.String</span></span>

### <span data-ttu-id="0b2a4-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="0b2a4-147">System.Int32</span></span>

### <span data-ttu-id="0b2a4-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0b2a4-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0b2a4-149">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="0b2a4-149">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="0b2a4-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0b2a4-150">OUTPUTS</span></span>

### <span data-ttu-id="0b2a4-151">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b2a4-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="0b2a4-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="0b2a4-152">NOTES</span></span>

## <span data-ttu-id="0b2a4-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0b2a4-153">RELATED LINKS</span></span>

[<span data-ttu-id="0b2a4-154">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b2a4-154">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="0b2a4-155">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b2a4-155">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="0b2a4-156">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0b2a4-156">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
