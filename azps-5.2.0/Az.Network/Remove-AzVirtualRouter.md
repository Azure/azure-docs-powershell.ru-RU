---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98413916"
---
# <span data-ttu-id="0d775-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="0d775-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="0d775-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d775-102">SYNOPSIS</span></span>
<span data-ttu-id="0d775-103">Удаляет Azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="0d775-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="0d775-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="0d775-104">SYNTAX</span></span>

### <span data-ttu-id="0d775-105">VirtualRouterNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d775-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d775-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d775-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d775-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d775-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d775-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d775-108">DESCRIPTION</span></span>
<span data-ttu-id="0d775-109">**Cmdlet Remove-AzVirtualRouter** удаляет azure VirtualRouter.</span><span class="sxs-lookup"><span data-stu-id="0d775-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="0d775-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="0d775-110">EXAMPLES</span></span>

### <span data-ttu-id="0d775-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0d775-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="0d775-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="0d775-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="0d775-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="0d775-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="0d775-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0d775-114">PARAMETERS</span></span>

### <span data-ttu-id="0d775-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d775-115">-AsJob</span></span>
<span data-ttu-id="0d775-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="0d775-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d775-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d775-117">-DefaultProfile</span></span>
<span data-ttu-id="0d775-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d775-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d775-119">-Force</span><span class="sxs-lookup"><span data-stu-id="0d775-119">-Force</span></span>
<span data-ttu-id="0d775-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="0d775-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="0d775-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d775-121">-InputObject</span></span>
<span data-ttu-id="0d775-122">Виртуальный объект ввода маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="0d775-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d775-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d775-123">-PassThru</span></span>
<span data-ttu-id="0d775-124">Возвращает объект, представляющий элемент, с которым выполняется данной операция.</span><span class="sxs-lookup"><span data-stu-id="0d775-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="0d775-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d775-125">-ResourceGroupName</span></span>
<span data-ttu-id="0d775-126">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="0d775-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d775-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d775-127">-ResourceId</span></span>
<span data-ttu-id="0d775-128">Виртуальный маршрутизатор, ид ресурса.</span><span class="sxs-lookup"><span data-stu-id="0d775-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d775-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="0d775-129">-RouterName</span></span>
<span data-ttu-id="0d775-130">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="0d775-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d775-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0d775-131">-Confirm</span></span>
<span data-ttu-id="0d775-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d775-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d775-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d775-133">-WhatIf</span></span>
<span data-ttu-id="0d775-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d775-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d775-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="0d775-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d775-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d775-136">CommonParameters</span></span>
<span data-ttu-id="0d775-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d775-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d775-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0d775-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d775-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="0d775-139">INPUTS</span></span>

### <span data-ttu-id="0d775-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0d775-140">System.String</span></span>

### <span data-ttu-id="0d775-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="0d775-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="0d775-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="0d775-142">OUTPUTS</span></span>

### <span data-ttu-id="0d775-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0d775-143">System.Boolean</span></span>

## <span data-ttu-id="0d775-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="0d775-144">NOTES</span></span>

## <span data-ttu-id="0d775-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d775-145">RELATED LINKS</span></span>
