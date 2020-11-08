---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 6d879357a71e18d9f1b6beb25044bd5d4394a497
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073969"
---
# <span data-ttu-id="5c4f3-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5c4f3-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="5c4f3-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="5c4f3-102">SYNOPSIS</span></span>
<span data-ttu-id="5c4f3-103">Удаление VirtualRouter Azure.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="5c4f3-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="5c4f3-104">SYNTAX</span></span>

### <span data-ttu-id="5c4f3-105">VirtualRouterNameParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="5c4f3-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c4f3-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c4f3-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c4f3-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c4f3-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c4f3-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c4f3-108">DESCRIPTION</span></span>
<span data-ttu-id="5c4f3-109">Командлет **Remove-AzVirtualRouter** удаляет Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5c4f3-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="5c4f3-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="5c4f3-110">EXAMPLES</span></span>

### <span data-ttu-id="5c4f3-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="5c4f3-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter 
```

### <span data-ttu-id="5c4f3-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="5c4f3-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="5c4f3-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="5c4f3-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="5c4f3-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="5c4f3-114">PARAMETERS</span></span>

### <span data-ttu-id="5c4f3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c4f3-115">-AsJob</span></span>
<span data-ttu-id="5c4f3-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="5c4f3-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c4f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c4f3-117">-DefaultProfile</span></span>
<span data-ttu-id="5c4f3-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c4f3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="5c4f3-119">-Force</span></span>
<span data-ttu-id="5c4f3-120">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="5c4f3-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="5c4f3-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c4f3-121">-InputObject</span></span>
<span data-ttu-id="5c4f3-122">Входной объект виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-122">The virtual router input object.</span></span>

```yaml
Type: PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4f3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c4f3-123">-PassThru</span></span>
<span data-ttu-id="5c4f3-124">Возвращает объект, представляющий элемент, для которого выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="5c4f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c4f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="5c4f3-126">Имя группы ресурсов виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-126">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4f3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c4f3-127">-ResourceId</span></span>
<span data-ttu-id="5c4f3-128">Идентификатор ресурса виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-128">The virtual router resource Id.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4f3-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="5c4f3-129">-RouterName</span></span>
<span data-ttu-id="5c4f3-130">Имя виртуального маршрутизатора.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-130">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c4f3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c4f3-131">-Confirm</span></span>
<span data-ttu-id="5c4f3-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c4f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c4f3-133">-WhatIf</span></span>
<span data-ttu-id="5c4f3-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c4f3-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c4f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c4f3-136">CommonParameters</span></span>
<span data-ttu-id="5c4f3-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="5c4f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c4f3-138">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c4f3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c4f3-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="5c4f3-139">INPUTS</span></span>

### <span data-ttu-id="5c4f3-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5c4f3-140">System.String</span></span>

### <span data-ttu-id="5c4f3-141">Microsoft. Azure. Commands. Network. Models. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="5c4f3-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="5c4f3-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="5c4f3-142">OUTPUTS</span></span>

### <span data-ttu-id="5c4f3-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c4f3-143">System.Boolean</span></span>

## <span data-ttu-id="5c4f3-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="5c4f3-144">NOTES</span></span>

## <span data-ttu-id="5c4f3-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="5c4f3-145">RELATED LINKS</span></span>
