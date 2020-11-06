---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: a28fe30424b5b1d29c3b671e5cec266fc75d9dbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567708"
---
# <span data-ttu-id="cfed9-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cfed9-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="cfed9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cfed9-102">SYNOPSIS</span></span>
<span data-ttu-id="cfed9-103">Создание фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="cfed9-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfed9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cfed9-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cfed9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfed9-105">DESCRIPTION</span></span>
<span data-ttu-id="cfed9-106">Командлет New-AzureRmRouteFilter создаст фильтр маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="cfed9-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="cfed9-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cfed9-107">EXAMPLES</span></span>

### <span data-ttu-id="cfed9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cfed9-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="cfed9-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="cfed9-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="cfed9-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cfed9-110">PARAMETERS</span></span>

### <span data-ttu-id="cfed9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cfed9-111">-AsJob</span></span>
<span data-ttu-id="cfed9-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="cfed9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cfed9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfed9-113">-DefaultProfile</span></span>
<span data-ttu-id="cfed9-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cfed9-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cfed9-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cfed9-115">-Force</span></span>
<span data-ttu-id="cfed9-116">Указывает на то, что этот командлет создает таблицу маршрутов, даже если фильтр маршрутов с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="cfed9-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="cfed9-117">-Location</span><span class="sxs-lookup"><span data-stu-id="cfed9-117">-Location</span></span>
<span data-ttu-id="cfed9-118">Указывает область Azure, в которой этот командлет создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="cfed9-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="cfed9-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cfed9-119">-Name</span></span>
<span data-ttu-id="cfed9-120">Задает имя фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="cfed9-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="cfed9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cfed9-121">-ResourceGroupName</span></span>
<span data-ttu-id="cfed9-122">Указывает имя группы ресурсов, в которой этот командлет создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="cfed9-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="cfed9-123">-Правило</span><span class="sxs-lookup"><span data-stu-id="cfed9-123">-Rule</span></span>
<span data-ttu-id="cfed9-124">Указывает массив объектов правил фильтра маршрутов, которые нужно связать с фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="cfed9-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cfed9-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="cfed9-125">-Tag</span></span>
<span data-ttu-id="cfed9-126">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="cfed9-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="cfed9-127">Например: @ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="cfed9-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="cfed9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cfed9-128">-Confirm</span></span>
<span data-ttu-id="cfed9-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cfed9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cfed9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cfed9-130">-WhatIf</span></span>
<span data-ttu-id="cfed9-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cfed9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cfed9-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cfed9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cfed9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfed9-133">CommonParameters</span></span>
<span data-ttu-id="cfed9-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cfed9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfed9-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfed9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfed9-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cfed9-136">INPUTS</span></span>

### <span data-ttu-id="cfed9-137">System. String</span><span class="sxs-lookup"><span data-stu-id="cfed9-137">System.String</span></span>

### <span data-ttu-id="cfed9-138">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule, Microsoft. Azure. Commands. Network, Version = 6.4.1.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="cfed9-138">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="cfed9-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="cfed9-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cfed9-140">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cfed9-140">OUTPUTS</span></span>

### <span data-ttu-id="cfed9-141">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cfed9-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="cfed9-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="cfed9-142">NOTES</span></span>
<span data-ttu-id="cfed9-143">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="cfed9-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="cfed9-144">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cfed9-144">RELATED LINKS</span></span>

[<span data-ttu-id="cfed9-145">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cfed9-145">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="cfed9-146">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="cfed9-146">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="cfed9-147">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cfed9-147">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="cfed9-148">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="cfed9-148">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
