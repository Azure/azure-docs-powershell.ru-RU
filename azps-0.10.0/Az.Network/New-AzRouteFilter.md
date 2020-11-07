---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 0b02c1bfbeee6fa3a628ea6ffacd04c15e96a440
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93909629"
---
# <span data-ttu-id="54671-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="54671-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="54671-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="54671-102">SYNOPSIS</span></span>
<span data-ttu-id="54671-103">Создание фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="54671-103">Creates a route filter.</span></span>

## <span data-ttu-id="54671-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="54671-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String>
 [-Rule <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54671-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54671-105">DESCRIPTION</span></span>
<span data-ttu-id="54671-106">Командлет New-AzRouteFilter создаст фильтр маршрута Azure.</span><span class="sxs-lookup"><span data-stu-id="54671-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="54671-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="54671-107">EXAMPLES</span></span>

### <span data-ttu-id="54671-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="54671-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

 
<span data-ttu-id="54671-109">{{Добавить пример описания}}</span><span class="sxs-lookup"><span data-stu-id="54671-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="54671-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="54671-110">PARAMETERS</span></span>

### <span data-ttu-id="54671-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54671-111">-AsJob</span></span>
<span data-ttu-id="54671-112">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="54671-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54671-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54671-113">-DefaultProfile</span></span>
<span data-ttu-id="54671-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54671-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54671-115">-Force</span><span class="sxs-lookup"><span data-stu-id="54671-115">-Force</span></span>
<span data-ttu-id="54671-116">Указывает на то, что этот командлет создает таблицу маршрутов, даже если фильтр маршрутов с таким именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="54671-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54671-117">-Location</span><span class="sxs-lookup"><span data-stu-id="54671-117">-Location</span></span>
<span data-ttu-id="54671-118">Указывает область Azure, в которой этот командлет создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="54671-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54671-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="54671-119">-Name</span></span>
<span data-ttu-id="54671-120">Задает имя фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="54671-120">Specifies a name for the route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54671-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54671-121">-ResourceGroupName</span></span>
<span data-ttu-id="54671-122">Указывает имя группы ресурсов, в которой этот командлет создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="54671-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54671-123">-Правило</span><span class="sxs-lookup"><span data-stu-id="54671-123">-Rule</span></span>
<span data-ttu-id="54671-124">Указывает массив объектов правил фильтра маршрутов, которые нужно связать с фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="54671-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="54671-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="54671-125">-Tag</span></span>
<span data-ttu-id="54671-126">Пары "ключ-значение" в виде хэш-таблицы.</span><span class="sxs-lookup"><span data-stu-id="54671-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="54671-127">Например:</span><span class="sxs-lookup"><span data-stu-id="54671-127">For example:</span></span>

<span data-ttu-id="54671-128">@ {Key0 = "value0"; key1 = $null; key2 = "значение2"}</span><span class="sxs-lookup"><span data-stu-id="54671-128">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54671-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54671-129">-Confirm</span></span>
<span data-ttu-id="54671-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="54671-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54671-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54671-131">-WhatIf</span></span>
<span data-ttu-id="54671-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="54671-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54671-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="54671-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54671-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54671-134">CommonParameters</span></span>
<span data-ttu-id="54671-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="54671-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54671-136">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54671-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54671-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="54671-137">INPUTS</span></span>

## <span data-ttu-id="54671-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="54671-138">OUTPUTS</span></span>

### <span data-ttu-id="54671-139">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="54671-139">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="54671-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="54671-140">NOTES</span></span>
<span data-ttu-id="54671-141">Ключевые слова: Azure, azurerm, ARM, Resource, Management, Manager, Network, Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="54671-141">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="54671-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54671-142">RELATED LINKS</span></span>

[<span data-ttu-id="54671-143">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="54671-143">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="54671-144">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="54671-144">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="54671-145">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="54671-145">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="54671-146">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="54671-146">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)
