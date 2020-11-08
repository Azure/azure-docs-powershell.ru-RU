---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078877"
---
# <span data-ttu-id="063f1-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="063f1-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="063f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="063f1-102">SYNOPSIS</span></span>
<span data-ttu-id="063f1-103">Удалите сайт виртуального устройства из ресурса виртуального сетевого устройства.</span><span class="sxs-lookup"><span data-stu-id="063f1-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="063f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="063f1-104">SYNTAX</span></span>

### <span data-ttu-id="063f1-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="063f1-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="063f1-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="063f1-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="063f1-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="063f1-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="063f1-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="063f1-108">DESCRIPTION</span></span>
<span data-ttu-id="063f1-109">Команда Remove-AzVirtualApplianceSite удаляет сайт виртуального устройства из ресурса виртуального сетевого устройства.</span><span class="sxs-lookup"><span data-stu-id="063f1-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="063f1-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="063f1-110">EXAMPLES</span></span>

### <span data-ttu-id="063f1-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="063f1-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="063f1-112">Удалите ресурс сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="063f1-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="063f1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="063f1-113">PARAMETERS</span></span>

### <span data-ttu-id="063f1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="063f1-114">-AsJob</span></span>
<span data-ttu-id="063f1-115">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="063f1-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="063f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="063f1-116">-DefaultProfile</span></span>
<span data-ttu-id="063f1-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="063f1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="063f1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="063f1-118">-Force</span></span>
<span data-ttu-id="063f1-119">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="063f1-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="063f1-120">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="063f1-120">-Name</span></span>
<span data-ttu-id="063f1-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="063f1-121">The resource name.</span></span>

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

### <span data-ttu-id="063f1-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="063f1-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="063f1-123">Идентификатор ресурса сетевого виртуального устройства, связанного с этим сайтом.</span><span class="sxs-lookup"><span data-stu-id="063f1-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="063f1-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="063f1-124">-PassThru</span></span>
<span data-ttu-id="063f1-125">Возвращает объект, который представляет собой элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="063f1-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="063f1-126">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="063f1-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="063f1-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="063f1-127">-ResourceGroupName</span></span>
<span data-ttu-id="063f1-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="063f1-128">The resource group name.</span></span>

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

### <span data-ttu-id="063f1-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="063f1-129">-ResourceId</span></span>
<span data-ttu-id="063f1-130">Идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="063f1-130">The resource id.</span></span>

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

### <span data-ttu-id="063f1-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="063f1-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="063f1-132">Объект сайта виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="063f1-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="063f1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="063f1-133">-Confirm</span></span>
<span data-ttu-id="063f1-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="063f1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="063f1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="063f1-135">-WhatIf</span></span>
<span data-ttu-id="063f1-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="063f1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="063f1-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="063f1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="063f1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="063f1-138">CommonParameters</span></span>
<span data-ttu-id="063f1-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="063f1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="063f1-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="063f1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="063f1-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="063f1-141">INPUTS</span></span>

### <span data-ttu-id="063f1-142">System. String</span><span class="sxs-lookup"><span data-stu-id="063f1-142">System.String</span></span>

### <span data-ttu-id="063f1-143">Microsoft. Azure. Commands. Network. Models. PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="063f1-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="063f1-144">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="063f1-144">OUTPUTS</span></span>

### <span data-ttu-id="063f1-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="063f1-145">System.Boolean</span></span>

## <span data-ttu-id="063f1-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="063f1-146">NOTES</span></span>

## <span data-ttu-id="063f1-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="063f1-147">RELATED LINKS</span></span>
