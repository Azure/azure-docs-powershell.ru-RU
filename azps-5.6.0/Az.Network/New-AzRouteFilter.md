---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azroutefilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzRouteFilter.md
ms.openlocfilehash: 9a262bd5680a9d5cd89d5ec32e3a57edbdaf60f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982339"
---
# <span data-ttu-id="46064-101">New-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="46064-101">New-AzRouteFilter</span></span>

## <span data-ttu-id="46064-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46064-102">SYNOPSIS</span></span>
<span data-ttu-id="46064-103">Создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="46064-103">Creates a route filter.</span></span>

## <span data-ttu-id="46064-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="46064-104">SYNTAX</span></span>

```
New-AzRouteFilter -Name <String> -ResourceGroupName <String> -Location <String> [-Rule <PSRouteFilterRule[]>]
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="46064-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="46064-105">DESCRIPTION</span></span>
<span data-ttu-id="46064-106">С New-AzRouteFilter создается фильтр маршрутов Azure.</span><span class="sxs-lookup"><span data-stu-id="46064-106">The New-AzRouteFilter cmdlet creates an Azure route filter.</span></span>

## <span data-ttu-id="46064-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="46064-107">EXAMPLES</span></span>

### <span data-ttu-id="46064-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="46064-108">Example 1</span></span>
```powershell
PS C:\> New-AzRouteFilter -Name "MyRouteFilter" -ResourceGroupName "MyResourceGroup" -Location "West US"
```

<span data-ttu-id="46064-109">Команда создает новый фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="46064-109">The command creates a new route filter.</span></span>

## <span data-ttu-id="46064-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46064-110">PARAMETERS</span></span>

### <span data-ttu-id="46064-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46064-111">-AsJob</span></span>
<span data-ttu-id="46064-112">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="46064-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="46064-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46064-113">-DefaultProfile</span></span>
<span data-ttu-id="46064-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="46064-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46064-115">-Force</span><span class="sxs-lookup"><span data-stu-id="46064-115">-Force</span></span>
<span data-ttu-id="46064-116">Указывает на то, что этот cmdlet создает таблицу маршрутов, даже если фильтр маршрутов с таким же именем уже существует.</span><span class="sxs-lookup"><span data-stu-id="46064-116">Indicates that this cmdlet creates a route table even if a route filter that has the same name already exists.</span></span>

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

### <span data-ttu-id="46064-117">-Location</span><span class="sxs-lookup"><span data-stu-id="46064-117">-Location</span></span>
<span data-ttu-id="46064-118">Определяет регион Azure, в котором этот cmdlet создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="46064-118">Specifies the Azure region in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="46064-119">-Name</span><span class="sxs-lookup"><span data-stu-id="46064-119">-Name</span></span>
<span data-ttu-id="46064-120">Имя фильтра маршрутов.</span><span class="sxs-lookup"><span data-stu-id="46064-120">Specifies a name for the route filter.</span></span>

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

### <span data-ttu-id="46064-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46064-121">-ResourceGroupName</span></span>
<span data-ttu-id="46064-122">Имя группы ресурсов, в которой этот cmdlet создает фильтр маршрутов.</span><span class="sxs-lookup"><span data-stu-id="46064-122">Specifies the name of the resource group in which this cmdlet creates a route filter.</span></span>

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

### <span data-ttu-id="46064-123">-Правило</span><span class="sxs-lookup"><span data-stu-id="46064-123">-Rule</span></span>
<span data-ttu-id="46064-124">Указывает массив объектов правила фильтра маршрутов, которые нужно связать с фильтром маршрутов.</span><span class="sxs-lookup"><span data-stu-id="46064-124">Specifies an array of Route Filter Rule objects to associate with the route filter.</span></span>

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

### <span data-ttu-id="46064-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="46064-125">-Tag</span></span>
<span data-ttu-id="46064-126">Пары "ключевое значение" в виде hash table.</span><span class="sxs-lookup"><span data-stu-id="46064-126">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="46064-127">Например: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="46064-127">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="46064-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46064-128">-Confirm</span></span>
<span data-ttu-id="46064-129">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46064-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46064-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46064-130">-WhatIf</span></span>
<span data-ttu-id="46064-131">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46064-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="46064-132">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="46064-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46064-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46064-133">CommonParameters</span></span>
<span data-ttu-id="46064-134">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46064-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46064-135">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46064-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46064-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="46064-136">INPUTS</span></span>

### <span data-ttu-id="46064-137">System.String</span><span class="sxs-lookup"><span data-stu-id="46064-137">System.String</span></span>

### <span data-ttu-id="46064-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span><span class="sxs-lookup"><span data-stu-id="46064-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule[]</span></span>

### <span data-ttu-id="46064-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="46064-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="46064-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46064-140">OUTPUTS</span></span>

### <span data-ttu-id="46064-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="46064-141">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="46064-142">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="46064-142">NOTES</span></span>
<span data-ttu-id="46064-143">Ключевые слова: azure, azurerm, arm, resource, management, manager, network, networking</span><span class="sxs-lookup"><span data-stu-id="46064-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="46064-144">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="46064-144">RELATED LINKS</span></span>

[<span data-ttu-id="46064-145">Get-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="46064-145">Get-AzRouteFilter</span></span>](./Get-AzRouteFilter.md)

[<span data-ttu-id="46064-146">Remove-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="46064-146">Remove-AzRouteFilter</span></span>](./Remove-AzRouteFilter.md)

[<span data-ttu-id="46064-147">Set-AzRouteFilter</span><span class="sxs-lookup"><span data-stu-id="46064-147">Set-AzRouteFilter</span></span>](./Set-AzRouteFilter.md)

[<span data-ttu-id="46064-148">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46064-148">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="46064-149">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46064-149">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="46064-150">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46064-150">New-AzRouteFilterRuleConfig</span></span>](./New-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="46064-151">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46064-151">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="46064-152">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="46064-152">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)
