---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
ms.openlocfilehash: 8d3b204815fc273f97a549582a193002f5f4a48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562879"
---
# <span data-ttu-id="501b4-101">New-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="501b4-101">New-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="501b4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="501b4-102">SYNOPSIS</span></span>
<span data-ttu-id="501b4-103">Создание Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="501b4-103">Creates an Azure ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="501b4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="501b4-104">SYNTAX</span></span>

### <span data-ttu-id="501b4-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="501b4-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="501b4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="501b4-106">ResourceIdParameterSet</span></span>
```
New-AzureRmExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="501b4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="501b4-107">DESCRIPTION</span></span>
<span data-ttu-id="501b4-108">Командлет **New-AzureRmExpressRoutePort** создает Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="501b4-108">The **New-AzureRmExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="501b4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="501b4-109">EXAMPLES</span></span>

### <span data-ttu-id="501b4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="501b4-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

### <span data-ttu-id="501b4-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="501b4-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

## <span data-ttu-id="501b4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="501b4-112">PARAMETERS</span></span>

### <span data-ttu-id="501b4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="501b4-113">-AsJob</span></span>
<span data-ttu-id="501b4-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="501b4-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="501b4-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="501b4-115">-BandwidthInGbps</span></span>
<span data-ttu-id="501b4-116">Пропускная способность приобретенных портов в Гбит/с</span><span class="sxs-lookup"><span data-stu-id="501b4-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="501b4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="501b4-117">-DefaultProfile</span></span>
<span data-ttu-id="501b4-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="501b4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="501b4-119">-Инкапсуляция</span><span class="sxs-lookup"><span data-stu-id="501b4-119">-Encapsulation</span></span>
<span data-ttu-id="501b4-120">Метод инкапсуляции на физических портах.</span><span class="sxs-lookup"><span data-stu-id="501b4-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="501b4-121">-Force</span><span class="sxs-lookup"><span data-stu-id="501b4-121">-Force</span></span>
<span data-ttu-id="501b4-122">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="501b4-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="501b4-123">-Link</span><span class="sxs-lookup"><span data-stu-id="501b4-123">-Link</span></span>
<span data-ttu-id="501b4-124">Набор физических ссылок на ресурс ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="501b4-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="501b4-125">-Location</span><span class="sxs-lookup"><span data-stu-id="501b4-125">-Location</span></span>
<span data-ttu-id="501b4-126">Расположение.</span><span class="sxs-lookup"><span data-stu-id="501b4-126">The location.</span></span>

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

### <span data-ttu-id="501b4-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="501b4-127">-Name</span></span>
<span data-ttu-id="501b4-128">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="501b4-128">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="501b4-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="501b4-129">-PeeringLocation</span></span>
<span data-ttu-id="501b4-130">Имя расположения пиринга, которое физически сопоставлено ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="501b4-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="501b4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="501b4-131">-ResourceGroupName</span></span>
<span data-ttu-id="501b4-132">Имя группы ресурсов для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="501b4-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="501b4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="501b4-133">-ResourceId</span></span>
<span data-ttu-id="501b4-134">ResourceId для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="501b4-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="501b4-135">-Тег</span><span class="sxs-lookup"><span data-stu-id="501b4-135">-Tag</span></span>
<span data-ttu-id="501b4-136">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="501b4-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="501b4-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="501b4-137">-Confirm</span></span>
<span data-ttu-id="501b4-138">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="501b4-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="501b4-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="501b4-139">-WhatIf</span></span>
<span data-ttu-id="501b4-140">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="501b4-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="501b4-141">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="501b4-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="501b4-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="501b4-142">CommonParameters</span></span>
<span data-ttu-id="501b4-143">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="501b4-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="501b4-144">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="501b4-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="501b4-145">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="501b4-145">INPUTS</span></span>

### <span data-ttu-id="501b4-146">System. String</span><span class="sxs-lookup"><span data-stu-id="501b4-146">System.String</span></span>

### <span data-ttu-id="501b4-147">System. Int32</span><span class="sxs-lookup"><span data-stu-id="501b4-147">System.Int32</span></span>

### <span data-ttu-id="501b4-148">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="501b4-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="501b4-149">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink, Microsoft. Azure. Commands. Network, Version = 6.3.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="501b4-149">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink, Microsoft.Azure.Commands.Network, Version=6.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="501b4-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="501b4-150">OUTPUTS</span></span>

### <span data-ttu-id="501b4-151">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="501b4-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="501b4-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="501b4-152">NOTES</span></span>

## <span data-ttu-id="501b4-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="501b4-153">RELATED LINKS</span></span>
