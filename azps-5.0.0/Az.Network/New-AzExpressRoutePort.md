---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249664"
---
# <span data-ttu-id="d724d-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d724d-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="d724d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d724d-102">SYNOPSIS</span></span>
<span data-ttu-id="d724d-103">Создание Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d724d-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="d724d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d724d-104">SYNTAX</span></span>

### <span data-ttu-id="d724d-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="d724d-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d724d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d724d-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d724d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d724d-107">DESCRIPTION</span></span>
<span data-ttu-id="d724d-108">Командлет **New-AzExpressRoutePort** создает Azure ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d724d-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="d724d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d724d-109">EXAMPLES</span></span>

### <span data-ttu-id="d724d-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d724d-110">Example 1</span></span>
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

### <span data-ttu-id="d724d-111">Пример 2</span><span class="sxs-lookup"><span data-stu-id="d724d-111">Example 2</span></span>
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

## <span data-ttu-id="d724d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d724d-112">PARAMETERS</span></span>

### <span data-ttu-id="d724d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d724d-113">-AsJob</span></span>
<span data-ttu-id="d724d-114">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d724d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d724d-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="d724d-115">-BandwidthInGbps</span></span>
<span data-ttu-id="d724d-116">Пропускная способность приобретенных портов в Гбит/с</span><span class="sxs-lookup"><span data-stu-id="d724d-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="d724d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d724d-117">-DefaultProfile</span></span>
<span data-ttu-id="d724d-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d724d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d724d-119">-Инкапсуляция</span><span class="sxs-lookup"><span data-stu-id="d724d-119">-Encapsulation</span></span>
<span data-ttu-id="d724d-120">Метод инкапсуляции на физических портах.</span><span class="sxs-lookup"><span data-stu-id="d724d-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="d724d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="d724d-121">-Force</span></span>
<span data-ttu-id="d724d-122">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="d724d-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="d724d-123">-Identity</span><span class="sxs-lookup"><span data-stu-id="d724d-123">-Identity</span></span>
<span data-ttu-id="d724d-124">Идентификационные данные, назначенные пользователю для чтения MacSec конфигурации</span><span class="sxs-lookup"><span data-stu-id="d724d-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d724d-125">-Link</span><span class="sxs-lookup"><span data-stu-id="d724d-125">-Link</span></span>
<span data-ttu-id="d724d-126">Набор физических ссылок на ресурс ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d724d-126">The set of physical links of the ExpressRoutePort resource</span></span>

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

### <span data-ttu-id="d724d-127">-Location</span><span class="sxs-lookup"><span data-stu-id="d724d-127">-Location</span></span>
<span data-ttu-id="d724d-128">Расположение.</span><span class="sxs-lookup"><span data-stu-id="d724d-128">The location.</span></span>

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

### <span data-ttu-id="d724d-129">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d724d-129">-Name</span></span>
<span data-ttu-id="d724d-130">Имя ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d724d-130">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="d724d-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="d724d-131">-PeeringLocation</span></span>
<span data-ttu-id="d724d-132">Имя расположения пиринга, которое физически сопоставлено ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d724d-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="d724d-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d724d-133">-ResourceGroupName</span></span>
<span data-ttu-id="d724d-134">Имя группы ресурсов для ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="d724d-134">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="d724d-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d724d-135">-ResourceId</span></span>
<span data-ttu-id="d724d-136">ResourceId для порта Express Route.</span><span class="sxs-lookup"><span data-stu-id="d724d-136">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="d724d-137">-Тег</span><span class="sxs-lookup"><span data-stu-id="d724d-137">-Tag</span></span>
<span data-ttu-id="d724d-138">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d724d-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d724d-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d724d-139">-Confirm</span></span>
<span data-ttu-id="d724d-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d724d-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d724d-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d724d-141">-WhatIf</span></span>
<span data-ttu-id="d724d-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d724d-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d724d-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d724d-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d724d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d724d-144">CommonParameters</span></span>
<span data-ttu-id="d724d-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d724d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d724d-146">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d724d-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d724d-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d724d-147">INPUTS</span></span>

### <span data-ttu-id="d724d-148">System. String</span><span class="sxs-lookup"><span data-stu-id="d724d-148">System.String</span></span>

### <span data-ttu-id="d724d-149">System. Int32</span><span class="sxs-lookup"><span data-stu-id="d724d-149">System.Int32</span></span>

### <span data-ttu-id="d724d-150">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="d724d-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d724d-151">Microsoft. Azure. Commands. Network. Models. PSExpressRouteLink []</span><span class="sxs-lookup"><span data-stu-id="d724d-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="d724d-152">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d724d-152">OUTPUTS</span></span>

### <span data-ttu-id="d724d-153">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d724d-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="d724d-154">Пуск</span><span class="sxs-lookup"><span data-stu-id="d724d-154">NOTES</span></span>

## <span data-ttu-id="d724d-155">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d724d-155">RELATED LINKS</span></span>

[<span data-ttu-id="d724d-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d724d-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="d724d-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d724d-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="d724d-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d724d-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)