---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100236537"
---
# <span data-ttu-id="8183c-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8183c-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="8183c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8183c-102">SYNOPSIS</span></span>
<span data-ttu-id="8183c-103">Удалите сайт виртуального устройства из ресурса сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="8183c-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8183c-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="8183c-104">SYNTAX</span></span>

### <span data-ttu-id="8183c-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8183c-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8183c-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8183c-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8183c-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8183c-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8183c-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8183c-108">DESCRIPTION</span></span>
<span data-ttu-id="8183c-109">Команда Remove-AzVirtualApplianceSite удаляет сайт виртуального устройства из ресурса сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="8183c-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="8183c-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="8183c-110">EXAMPLES</span></span>

### <span data-ttu-id="8183c-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="8183c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="8183c-112">Удаление ресурса сайта виртуальной устройства.</span><span class="sxs-lookup"><span data-stu-id="8183c-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="8183c-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8183c-113">PARAMETERS</span></span>

### <span data-ttu-id="8183c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8183c-114">-AsJob</span></span>
<span data-ttu-id="8183c-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="8183c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8183c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8183c-116">-DefaultProfile</span></span>
<span data-ttu-id="8183c-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8183c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8183c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8183c-118">-Force</span></span>
<span data-ttu-id="8183c-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="8183c-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="8183c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="8183c-120">-Name</span></span>
<span data-ttu-id="8183c-121">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="8183c-121">The resource name.</span></span>

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

### <span data-ttu-id="8183c-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="8183c-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="8183c-123">ИД ресурса сетевого виртуального устройства, связанного с этим сайтом.</span><span class="sxs-lookup"><span data-stu-id="8183c-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="8183c-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8183c-124">-PassThru</span></span>
<span data-ttu-id="8183c-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="8183c-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8183c-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="8183c-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8183c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8183c-127">-ResourceGroupName</span></span>
<span data-ttu-id="8183c-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8183c-128">The resource group name.</span></span>

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

### <span data-ttu-id="8183c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8183c-129">-ResourceId</span></span>
<span data-ttu-id="8183c-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="8183c-130">The resource id.</span></span>

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

### <span data-ttu-id="8183c-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8183c-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="8183c-132">Объект сайта виртуальной устройства.</span><span class="sxs-lookup"><span data-stu-id="8183c-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="8183c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8183c-133">-Confirm</span></span>
<span data-ttu-id="8183c-134">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="8183c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8183c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8183c-135">-WhatIf</span></span>
<span data-ttu-id="8183c-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8183c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8183c-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="8183c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8183c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8183c-138">CommonParameters</span></span>
<span data-ttu-id="8183c-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8183c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8183c-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8183c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8183c-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8183c-141">INPUTS</span></span>

### <span data-ttu-id="8183c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="8183c-142">System.String</span></span>

### <span data-ttu-id="8183c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="8183c-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="8183c-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="8183c-144">OUTPUTS</span></span>

### <span data-ttu-id="8183c-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8183c-145">System.Boolean</span></span>

## <span data-ttu-id="8183c-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="8183c-146">NOTES</span></span>

## <span data-ttu-id="8183c-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8183c-147">RELATED LINKS</span></span>
