---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: f1c8589663008b0ebc640a052199a11c82d3b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996302"
---
# <span data-ttu-id="4b837-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="4b837-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="4b837-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b837-102">SYNOPSIS</span></span>
<span data-ttu-id="4b837-103">Удаляет IpGroup в Azure.</span><span class="sxs-lookup"><span data-stu-id="4b837-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="4b837-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="4b837-104">SYNTAX</span></span>

### <span data-ttu-id="4b837-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b837-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b837-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b837-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b837-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4b837-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b837-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b837-108">DESCRIPTION</span></span>
<span data-ttu-id="4b837-109">При **этом удаляется ipGroup Azure.**</span><span class="sxs-lookup"><span data-stu-id="4b837-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="4b837-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="4b837-110">EXAMPLES</span></span>

### <span data-ttu-id="4b837-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b837-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="4b837-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="4b837-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="4b837-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="4b837-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="4b837-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b837-114">PARAMETERS</span></span>

### <span data-ttu-id="4b837-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4b837-115">-AsJob</span></span>
<span data-ttu-id="4b837-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="4b837-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4b837-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b837-117">-DefaultProfile</span></span>
<span data-ttu-id="4b837-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4b837-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b837-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4b837-119">-Force</span></span>
<span data-ttu-id="4b837-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="4b837-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="4b837-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="4b837-121">-IpGroup</span></span>
<span data-ttu-id="4b837-122">Объект ввода IPGroup.</span><span class="sxs-lookup"><span data-stu-id="4b837-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4b837-123">-Name</span><span class="sxs-lookup"><span data-stu-id="4b837-123">-Name</span></span>
<span data-ttu-id="4b837-124">Имя ipgroup.</span><span class="sxs-lookup"><span data-stu-id="4b837-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b837-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b837-125">-PassThru</span></span>
<span data-ttu-id="4b837-126">Возвращает объект, представляющий элемент, с которым выполняется данной операция.</span><span class="sxs-lookup"><span data-stu-id="4b837-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="4b837-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b837-127">-ResourceGroupName</span></span>
<span data-ttu-id="4b837-128">Имя группы ресурсов ipgroup.</span><span class="sxs-lookup"><span data-stu-id="4b837-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b837-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b837-129">-ResourceId</span></span>
<span data-ttu-id="4b837-130">The ipgroup resource Id.</span><span class="sxs-lookup"><span data-stu-id="4b837-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4b837-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b837-131">-Confirm</span></span>
<span data-ttu-id="4b837-132">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b837-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b837-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b837-133">-WhatIf</span></span>
<span data-ttu-id="4b837-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b837-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b837-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="4b837-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b837-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b837-136">CommonParameters</span></span>
<span data-ttu-id="4b837-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b837-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b837-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4b837-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b837-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="4b837-139">INPUTS</span></span>

### <span data-ttu-id="4b837-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4b837-140">System.String</span></span>

### <span data-ttu-id="4b837-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="4b837-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="4b837-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="4b837-142">OUTPUTS</span></span>

### <span data-ttu-id="4b837-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4b837-143">System.Boolean</span></span>

## <span data-ttu-id="4b837-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="4b837-144">NOTES</span></span>

## <span data-ttu-id="4b837-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b837-145">RELATED LINKS</span></span>
