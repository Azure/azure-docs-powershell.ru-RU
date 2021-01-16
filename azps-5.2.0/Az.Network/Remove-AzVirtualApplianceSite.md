---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98394388"
---
# <span data-ttu-id="5b85f-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5b85f-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="5b85f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b85f-102">SYNOPSIS</span></span>
<span data-ttu-id="5b85f-103">Удалите сайт виртуального устройства из ресурса сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="5b85f-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5b85f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="5b85f-104">SYNTAX</span></span>

### <span data-ttu-id="5b85f-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5b85f-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5b85f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b85f-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5b85f-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5b85f-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5b85f-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5b85f-108">DESCRIPTION</span></span>
<span data-ttu-id="5b85f-109">Команда Remove-AzVirtualApplianceSite удаляет сайт виртуального устройства из ресурса сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="5b85f-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="5b85f-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="5b85f-110">EXAMPLES</span></span>

### <span data-ttu-id="5b85f-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5b85f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="5b85f-112">Удаление ресурса сайта виртуальной устройства.</span><span class="sxs-lookup"><span data-stu-id="5b85f-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="5b85f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5b85f-113">PARAMETERS</span></span>

### <span data-ttu-id="5b85f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5b85f-114">-AsJob</span></span>
<span data-ttu-id="5b85f-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5b85f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5b85f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b85f-116">-DefaultProfile</span></span>
<span data-ttu-id="5b85f-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5b85f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b85f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5b85f-118">-Force</span></span>
<span data-ttu-id="5b85f-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="5b85f-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5b85f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5b85f-120">-Name</span></span>
<span data-ttu-id="5b85f-121">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="5b85f-121">The resource name.</span></span>

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

### <span data-ttu-id="5b85f-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="5b85f-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="5b85f-123">ИД ресурса сетевого виртуального устройства, связанного с этим сайтом.</span><span class="sxs-lookup"><span data-stu-id="5b85f-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="5b85f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b85f-124">-PassThru</span></span>
<span data-ttu-id="5b85f-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="5b85f-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="5b85f-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="5b85f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5b85f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b85f-127">-ResourceGroupName</span></span>
<span data-ttu-id="5b85f-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="5b85f-128">The resource group name.</span></span>

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

### <span data-ttu-id="5b85f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5b85f-129">-ResourceId</span></span>
<span data-ttu-id="5b85f-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="5b85f-130">The resource id.</span></span>

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

### <span data-ttu-id="5b85f-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5b85f-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="5b85f-132">Объект сайта виртуальной устройства.</span><span class="sxs-lookup"><span data-stu-id="5b85f-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="5b85f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5b85f-133">-Confirm</span></span>
<span data-ttu-id="5b85f-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b85f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5b85f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5b85f-135">-WhatIf</span></span>
<span data-ttu-id="5b85f-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5b85f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5b85f-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="5b85f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5b85f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b85f-138">CommonParameters</span></span>
<span data-ttu-id="5b85f-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b85f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b85f-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b85f-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b85f-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b85f-141">INPUTS</span></span>

### <span data-ttu-id="5b85f-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5b85f-142">System.String</span></span>

### <span data-ttu-id="5b85f-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="5b85f-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="5b85f-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="5b85f-144">OUTPUTS</span></span>

### <span data-ttu-id="5b85f-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5b85f-145">System.Boolean</span></span>

## <span data-ttu-id="5b85f-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="5b85f-146">NOTES</span></span>

## <span data-ttu-id="5b85f-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5b85f-147">RELATED LINKS</span></span>
