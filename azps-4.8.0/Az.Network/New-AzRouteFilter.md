---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 8be04cd9e483e990d73130866779710bbed879bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244117"
---
# <span data-ttu-id="4ee74-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4ee74-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="4ee74-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4ee74-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee74-103">Создание фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="4ee74-103">Creates a route filter.</span></span>

## <span data-ttu-id="4ee74-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4ee74-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4ee74-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ee74-105">DESCRIPTION</span></span>
<span data-ttu-id="4ee74-106">Командлет New-AzRouteFilter создаст фильтр маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee74-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="4ee74-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4ee74-107">EXAMPLES</span></span>

### <span data-ttu-id="4ee74-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4ee74-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="4ee74-109">Команда создает новый фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="4ee74-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="4ee74-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4ee74-110">PARAMETERS</span></span>

### <span data-ttu-id="4ee74-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ee74-111">-AsJob</span></span>
<span data-ttu-id="4ee74-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4ee74-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4ee74-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee74-113">-DefaultProfile</span></span>
<span data-ttu-id="4ee74-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4ee74-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee74-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4ee74-115">-Force</span></span>
<span data-ttu-id="4ee74-116">Указывает на то, что этот командлет создает таблицу маршрутов, даже если фильтр маршрутов с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="4ee74-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="4ee74-117">-Location</span><span class="sxs-lookup"><span data-stu-id="4ee74-117">-Location</span></span>
<span data-ttu-id="4ee74-118">Указывает область Azure, в которой этот командлет создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="4ee74-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="4ee74-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4ee74-119">-Name</span></span>
<span data-ttu-id="4ee74-120">Задает имя фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="4ee74-120">Specifies a name for the route filter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee74-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee74-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ee74-122">Указывает имя группы ресурсов, в которой этот командлет создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="4ee74-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="4ee74-123">-Правило</span><span class="sxs-lookup"><span data-stu-id="4ee74-123">-Rule</span></span>
<span data-ttu-id="4ee74-124">Указывает массив объектов правил фильтра маршрутов, которые нужно связать с фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="4ee74-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee74-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="4ee74-125">-Tag</span></span>
<span data-ttu-id="4ee74-126">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="4ee74-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="4ee74-127">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="4ee74-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="4ee74-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ee74-128">-Confirm</span></span>
<span data-ttu-id="4ee74-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4ee74-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ee74-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ee74-130">-WhatIf</span></span>
<span data-ttu-id="4ee74-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4ee74-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4ee74-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4ee74-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ee74-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee74-133">CommonParameters</span></span>
<span data-ttu-id="4ee74-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4ee74-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee74-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee74-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee74-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4ee74-136">INPUTS</span></span>

### <span data-ttu-id="4ee74-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4ee74-137">System.String</span></span>

### <span data-ttu-id="4ee74-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule []</span><span class="sxs-lookup"><span data-stu-id="4ee74-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="4ee74-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4ee74-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4ee74-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4ee74-140">OUTPUTS</span></span>

### <span data-ttu-id="4ee74-141">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4ee74-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4ee74-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="4ee74-142">NOTES</span></span>
<span data-ttu-id="4ee74-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="4ee74-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="4ee74-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4ee74-144">RELATED LINKS</span></span>

[<span data-ttu-id="4ee74-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4ee74-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="4ee74-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4ee74-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="4ee74-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4ee74-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="4ee74-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ee74-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4ee74-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ee74-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4ee74-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ee74-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4ee74-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ee74-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="4ee74-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4ee74-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
