---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: b75eb7e9bbac3efddc49bcccf384f288c01960a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996218"
---
# <span data-ttu-id="b7574-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="b7574-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="b7574-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7574-102">SYNOPSIS</span></span>
<span data-ttu-id="b7574-103">Удалите ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="b7574-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b7574-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b7574-104">SYNTAX</span></span>

### <span data-ttu-id="b7574-105">ResourceNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b7574-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7574-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7574-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b7574-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7574-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7574-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b7574-108">DESCRIPTION</span></span>
<span data-ttu-id="b7574-109">Команда Remove-AzNetworkVirtualAppliance удаляет ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="b7574-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b7574-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b7574-110">EXAMPLES</span></span>

### <span data-ttu-id="b7574-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b7574-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="b7574-112">Удалите ресурс сетевого виртуального устройства.</span><span class="sxs-lookup"><span data-stu-id="b7574-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="b7574-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7574-113">PARAMETERS</span></span>

### <span data-ttu-id="b7574-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7574-114">-AsJob</span></span>
<span data-ttu-id="b7574-115">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b7574-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7574-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7574-116">-DefaultProfile</span></span>
<span data-ttu-id="b7574-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b7574-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7574-118">-Force</span><span class="sxs-lookup"><span data-stu-id="b7574-118">-Force</span></span>
<span data-ttu-id="b7574-119">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="b7574-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b7574-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b7574-120">-Name</span></span>
<span data-ttu-id="b7574-121">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="b7574-121">The resource name.</span></span>

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

### <span data-ttu-id="b7574-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="b7574-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="b7574-123">Объект ресурса.</span><span class="sxs-lookup"><span data-stu-id="b7574-123">The resource object.</span></span>

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

### <span data-ttu-id="b7574-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7574-124">-PassThru</span></span>
<span data-ttu-id="b7574-125">Возвращает объект, представляющий элемент, с которым вы работаете.</span><span class="sxs-lookup"><span data-stu-id="b7574-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b7574-126">По умолчанию этот cmdlet не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="b7574-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b7574-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7574-127">-ResourceGroupName</span></span>
<span data-ttu-id="b7574-128">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b7574-128">The resource group name.</span></span>

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

### <span data-ttu-id="b7574-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7574-129">-ResourceId</span></span>
<span data-ttu-id="b7574-130">ИД ресурса.</span><span class="sxs-lookup"><span data-stu-id="b7574-130">The Resource Id.</span></span>

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

### <span data-ttu-id="b7574-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b7574-131">-Confirm</span></span>
<span data-ttu-id="b7574-132">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="b7574-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7574-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7574-133">-WhatIf</span></span>
<span data-ttu-id="b7574-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7574-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7574-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b7574-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7574-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7574-136">CommonParameters</span></span>
<span data-ttu-id="b7574-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7574-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7574-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7574-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7574-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b7574-139">INPUTS</span></span>

### <span data-ttu-id="b7574-140">System.String</span><span class="sxs-lookup"><span data-stu-id="b7574-140">System.String</span></span>

### <span data-ttu-id="b7574-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="b7574-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="b7574-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7574-142">OUTPUTS</span></span>

### <span data-ttu-id="b7574-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b7574-143">System.Boolean</span></span>

## <span data-ttu-id="b7574-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b7574-144">NOTES</span></span>

## <span data-ttu-id="b7574-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b7574-145">RELATED LINKS</span></span>
