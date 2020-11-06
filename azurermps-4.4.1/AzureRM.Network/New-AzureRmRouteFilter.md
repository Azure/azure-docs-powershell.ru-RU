---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilter.md
ms.openlocfilehash: 6cc420ccb2ba2c7e555956d711fe0e30d02ef62f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562455"
---
# <span data-ttu-id="b245c-101">New-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b245c-101">New-AzureRmRouteFilter</span></span>

## <span data-ttu-id="b245c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b245c-102">SYNOPSIS</span></span>
<span data-ttu-id="b245c-103">Создание фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b245c-103">Creates a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b245c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b245c-104">SYNTAX</span></span>

```
New-AzureRmRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b245c-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b245c-105">DESCRIPTION</span></span>
<span data-ttu-id="b245c-106">Командлет New-AzureRmRouteFilter создаст фильтр маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="b245c-106">The New-AzureRmRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="b245c-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b245c-107">EXAMPLES</span></span>

### <span data-ttu-id="b245c-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b245c-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="b245c-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="b245c-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="b245c-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b245c-110">PARAMETERS</span></span>

### <span data-ttu-id="b245c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="b245c-111">-Force</span></span>
<span data-ttu-id="b245c-112">Указывает на то, что этот командлет создает таблицу маршрутов, даже если фильтр маршрутов с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="b245c-112">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="b245c-113">-Location</span><span class="sxs-lookup"><span data-stu-id="b245c-113">-Location</span></span>
<span data-ttu-id="b245c-114">Указывает область Azure, в которой этот командлет создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b245c-114">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="b245c-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b245c-115">-Name</span></span>
<span data-ttu-id="b245c-116">Задает имя фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b245c-116">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="b245c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b245c-117">-ResourceGroupName</span></span>
<span data-ttu-id="b245c-118">Указывает имя группы ресурсов, в которой этот командлет создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b245c-118">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="b245c-119">-Правило</span><span class="sxs-lookup"><span data-stu-id="b245c-119">-Rule</span></span>
<span data-ttu-id="b245c-120">Указывает массив объектов правил фильтра маршрутов, которые нужно связать с фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="b245c-120">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="b245c-121">-Тег</span><span class="sxs-lookup"><span data-stu-id="b245c-121">-Tag</span></span>
<span data-ttu-id="b245c-122">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="b245c-122">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b245c-123">Например:</span><span class="sxs-lookup"><span data-stu-id="b245c-123">For example:</span></span>

<span data-ttu-id="b245c-124">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="b245c-124">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b245c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b245c-125">-Confirm</span></span>
<span data-ttu-id="b245c-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b245c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b245c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b245c-127">-WhatIf</span></span>
<span data-ttu-id="b245c-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b245c-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b245c-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b245c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b245c-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b245c-130">-DefaultProfile</span></span>
<span data-ttu-id="b245c-131">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b245c-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b245c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b245c-132">CommonParameters</span></span>
<span data-ttu-id="b245c-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b245c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b245c-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b245c-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b245c-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b245c-135">INPUTS</span></span>

## <span data-ttu-id="b245c-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b245c-136">OUTPUTS</span></span>

### <span data-ttu-id="b245c-137">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b245c-137">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="b245c-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="b245c-138">NOTES</span></span>
<span data-ttu-id="b245c-139">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="b245c-139">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="b245c-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b245c-140">RELATED LINKS</span></span>

[<span data-ttu-id="b245c-141">Get-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b245c-141">Get-AzureRmRouteFilter</span></span>](./Get-AzureRmRouteFilter.md)

[<span data-ttu-id="b245c-142">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="b245c-142">New-AzureRmRouteFilterRuleConfig</span></span>](./New-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="b245c-143">Remove-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b245c-143">Remove-AzureRmRouteFilter</span></span>](./Remove-AzureRmRouteFilter.md)

[<span data-ttu-id="b245c-144">Set-AzureRmRouteFilter</span><span class="sxs-lookup"><span data-stu-id="b245c-144">Set-AzureRmRouteFilter</span></span>](./Set-AzureRmRouteFilter.md)
