---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249630"
---
# <span data-ttu-id="fe998-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="fe998-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="fe998-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fe998-102">SYNOPSIS</span></span>
<span data-ttu-id="fe998-103">Удалите сайт виртуального устройства из ресурса виртуального сетевого устройства.</span><span class="sxs-lookup"><span data-stu-id="fe998-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="fe998-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fe998-104">SYNTAX</span></span>

### <span data-ttu-id="fe998-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fe998-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fe998-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe998-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fe998-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fe998-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe998-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe998-108">DESCRIPTION</span></span>
<span data-ttu-id="fe998-109">Команда Remove-AzVirtualApplianceSite удаляет сайт виртуального устройства из ресурса виртуального сетевого устройства.</span><span class="sxs-lookup"><span data-stu-id="fe998-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="fe998-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fe998-110">EXAMPLES</span></span>

### <span data-ttu-id="fe998-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fe998-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="fe998-112">Удалите ресурс сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="fe998-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="fe998-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fe998-113">PARAMETERS</span></span>

### <span data-ttu-id="fe998-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fe998-114">-AsJob</span></span>
<span data-ttu-id="fe998-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fe998-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fe998-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe998-116">-DefaultProfile</span></span>
<span data-ttu-id="fe998-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fe998-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fe998-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fe998-118">-Force</span></span>
<span data-ttu-id="fe998-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="fe998-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="fe998-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fe998-120">-Name</span></span>
<span data-ttu-id="fe998-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe998-121">The resource name.</span></span>

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

### <span data-ttu-id="fe998-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="fe998-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="fe998-123">Идентификатор ресурса сетевого виртуального устройства, связанного с этим сайтом.</span><span class="sxs-lookup"><span data-stu-id="fe998-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="fe998-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe998-124">-PassThru</span></span>
<span data-ttu-id="fe998-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="fe998-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="fe998-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="fe998-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fe998-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe998-127">-ResourceGroupName</span></span>
<span data-ttu-id="fe998-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fe998-128">The resource group name.</span></span>

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

### <span data-ttu-id="fe998-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fe998-129">-ResourceId</span></span>
<span data-ttu-id="fe998-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="fe998-130">The resource id.</span></span>

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

### <span data-ttu-id="fe998-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="fe998-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="fe998-132">Объект сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="fe998-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe998-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe998-133">-Confirm</span></span>
<span data-ttu-id="fe998-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fe998-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe998-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe998-135">-WhatIf</span></span>
<span data-ttu-id="fe998-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fe998-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe998-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fe998-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe998-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe998-138">CommonParameters</span></span>
<span data-ttu-id="fe998-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fe998-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe998-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fe998-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe998-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fe998-141">INPUTS</span></span>

### <span data-ttu-id="fe998-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fe998-142">System.String</span></span>

### <span data-ttu-id="fe998-143">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="fe998-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="fe998-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fe998-144">OUTPUTS</span></span>

### <span data-ttu-id="fe998-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe998-145">System.Boolean</span></span>

## <span data-ttu-id="fe998-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="fe998-146">NOTES</span></span>

## <span data-ttu-id="fe998-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fe998-147">RELATED LINKS</span></span>
