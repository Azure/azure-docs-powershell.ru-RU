---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98406447"
---
# <span data-ttu-id="6adc0-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6adc0-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6adc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6adc0-102">SYNOPSIS</span></span>
<span data-ttu-id="6adc0-103">Удалите ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="6adc0-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6adc0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6adc0-104">SYNTAX</span></span>

### <span data-ttu-id="6adc0-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6adc0-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adc0-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6adc0-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6adc0-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6adc0-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6adc0-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6adc0-108">DESCRIPTION</span></span>
<span data-ttu-id="6adc0-109">Команда Remove-AzNetworkVirtualAppliance удаляет ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="6adc0-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6adc0-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6adc0-110">EXAMPLES</span></span>

### <span data-ttu-id="6adc0-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6adc0-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="6adc0-112">Удалите ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="6adc0-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="6adc0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6adc0-113">PARAMETERS</span></span>

### <span data-ttu-id="6adc0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6adc0-114">-AsJob</span></span>
<span data-ttu-id="6adc0-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="6adc0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6adc0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6adc0-116">-DefaultProfile</span></span>
<span data-ttu-id="6adc0-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6adc0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6adc0-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6adc0-118">-Force</span></span>
<span data-ttu-id="6adc0-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="6adc0-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6adc0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6adc0-120">-Name</span></span>
<span data-ttu-id="6adc0-121">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="6adc0-121">The resource name.</span></span>

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

### <span data-ttu-id="6adc0-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6adc0-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="6adc0-123">Объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="6adc0-123">The resource object.</span></span>

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

### <span data-ttu-id="6adc0-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6adc0-124">-PassThru</span></span>
<span data-ttu-id="6adc0-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="6adc0-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="6adc0-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="6adc0-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6adc0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6adc0-127">-ResourceGroupName</span></span>
<span data-ttu-id="6adc0-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6adc0-128">The resource group name.</span></span>

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

### <span data-ttu-id="6adc0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6adc0-129">-ResourceId</span></span>
<span data-ttu-id="6adc0-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="6adc0-130">The Resource Id.</span></span>

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

### <span data-ttu-id="6adc0-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6adc0-131">-Confirm</span></span>
<span data-ttu-id="6adc0-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6adc0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6adc0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6adc0-133">-WhatIf</span></span>
<span data-ttu-id="6adc0-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6adc0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6adc0-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6adc0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6adc0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6adc0-136">CommonParameters</span></span>
<span data-ttu-id="6adc0-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6adc0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6adc0-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6adc0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6adc0-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6adc0-139">INPUTS</span></span>

### <span data-ttu-id="6adc0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6adc0-140">System.String</span></span>

### <span data-ttu-id="6adc0-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="6adc0-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="6adc0-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6adc0-142">OUTPUTS</span></span>

### <span data-ttu-id="6adc0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6adc0-143">System.Boolean</span></span>

## <span data-ttu-id="6adc0-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6adc0-144">NOTES</span></span>

## <span data-ttu-id="6adc0-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6adc0-145">RELATED LINKS</span></span>
