---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94234927"
---
# <span data-ttu-id="e3589-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="e3589-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="e3589-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e3589-102">SYNOPSIS</span></span>
<span data-ttu-id="e3589-103">Удалите ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="e3589-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="e3589-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e3589-104">SYNTAX</span></span>

### <span data-ttu-id="e3589-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e3589-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3589-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3589-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3589-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e3589-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3589-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3589-108">DESCRIPTION</span></span>
<span data-ttu-id="e3589-109">Команда Remove-AzNetworkVirtualAppliance удаляет ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="e3589-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="e3589-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e3589-110">EXAMPLES</span></span>

### <span data-ttu-id="e3589-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e3589-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="e3589-112">Удалите ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="e3589-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="e3589-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e3589-113">PARAMETERS</span></span>

### <span data-ttu-id="e3589-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3589-114">-AsJob</span></span>
<span data-ttu-id="e3589-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e3589-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e3589-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3589-116">-DefaultProfile</span></span>
<span data-ttu-id="e3589-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e3589-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3589-118">-Force</span><span class="sxs-lookup"><span data-stu-id="e3589-118">-Force</span></span>
<span data-ttu-id="e3589-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e3589-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e3589-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e3589-120">-Name</span></span>
<span data-ttu-id="e3589-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e3589-121">The resource name.</span></span>

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

### <span data-ttu-id="e3589-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="e3589-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="e3589-123">Объект ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3589-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e3589-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e3589-124">-PassThru</span></span>
<span data-ttu-id="e3589-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="e3589-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="e3589-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e3589-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e3589-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3589-127">-ResourceGroupName</span></span>
<span data-ttu-id="e3589-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e3589-128">The resource group name.</span></span>

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

### <span data-ttu-id="e3589-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3589-129">-ResourceId</span></span>
<span data-ttu-id="e3589-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="e3589-130">The Resource Id.</span></span>

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

### <span data-ttu-id="e3589-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3589-131">-Confirm</span></span>
<span data-ttu-id="e3589-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e3589-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3589-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3589-133">-WhatIf</span></span>
<span data-ttu-id="e3589-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e3589-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3589-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e3589-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3589-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3589-136">CommonParameters</span></span>
<span data-ttu-id="e3589-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e3589-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3589-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e3589-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3589-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e3589-139">INPUTS</span></span>

### <span data-ttu-id="e3589-140">System. String</span><span class="sxs-lookup"><span data-stu-id="e3589-140">System.String</span></span>

### <span data-ttu-id="e3589-141">Microsoft. Azure. Commands. Network. Models. PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="e3589-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="e3589-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e3589-142">OUTPUTS</span></span>

### <span data-ttu-id="e3589-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e3589-143">System.Boolean</span></span>

## <span data-ttu-id="e3589-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e3589-144">NOTES</span></span>

## <span data-ttu-id="e3589-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e3589-145">RELATED LINKS</span></span>
