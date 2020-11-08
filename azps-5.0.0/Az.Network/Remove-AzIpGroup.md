---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: 35cf06e23a533970b14b439be5d55a64476330be
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246084"
---
# <span data-ttu-id="9ab5e-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="9ab5e-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="9ab5e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9ab5e-102">SYNOPSIS</span></span>
<span data-ttu-id="9ab5e-103">Удаление IpGroup Azure.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="9ab5e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9ab5e-104">SYNTAX</span></span>

### <span data-ttu-id="9ab5e-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ab5e-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab5e-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ab5e-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ab5e-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9ab5e-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ab5e-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ab5e-108">DESCRIPTION</span></span>
<span data-ttu-id="9ab5e-109">Командлет **Remove-AzIpGroup** удаляет Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="9ab5e-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="9ab5e-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9ab5e-110">EXAMPLES</span></span>

### <span data-ttu-id="9ab5e-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9ab5e-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="9ab5e-112">Пример 2</span><span class="sxs-lookup"><span data-stu-id="9ab5e-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="9ab5e-113">Пример 3</span><span class="sxs-lookup"><span data-stu-id="9ab5e-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="9ab5e-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9ab5e-114">PARAMETERS</span></span>

### <span data-ttu-id="9ab5e-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9ab5e-115">-AsJob</span></span>
<span data-ttu-id="9ab5e-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="9ab5e-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9ab5e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ab5e-117">-DefaultProfile</span></span>
<span data-ttu-id="9ab5e-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ab5e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="9ab5e-119">-Force</span></span>
<span data-ttu-id="9ab5e-120">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="9ab5e-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="9ab5e-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="9ab5e-121">-IpGroup</span></span>
<span data-ttu-id="9ab5e-122">Объект ввода ipGroup.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-122">The ipGroup input object.</span></span>

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

### <span data-ttu-id="9ab5e-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9ab5e-123">-Name</span></span>
<span data-ttu-id="9ab5e-124">Имя IPGroup.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-124">The name of the ipgroup.</span></span>

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

### <span data-ttu-id="9ab5e-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9ab5e-125">-PassThru</span></span>
<span data-ttu-id="9ab5e-126">Возвращает объект, представляющий элемент, для которого выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-126">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="9ab5e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ab5e-127">-ResourceGroupName</span></span>
<span data-ttu-id="9ab5e-128">Имя группы ресурсов для IPGroup.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-128">The resource group name of the ipgroup.</span></span>

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

### <span data-ttu-id="9ab5e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9ab5e-129">-ResourceId</span></span>
<span data-ttu-id="9ab5e-130">Идентификатор ресурса IPGroup.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-130">The ipgroup resource Id.</span></span>

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

### <span data-ttu-id="9ab5e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9ab5e-131">-Confirm</span></span>
<span data-ttu-id="9ab5e-132">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ab5e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ab5e-133">-WhatIf</span></span>
<span data-ttu-id="9ab5e-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9ab5e-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ab5e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ab5e-136">CommonParameters</span></span>
<span data-ttu-id="9ab5e-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9ab5e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ab5e-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9ab5e-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ab5e-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9ab5e-139">INPUTS</span></span>

### <span data-ttu-id="9ab5e-140">System. String</span><span class="sxs-lookup"><span data-stu-id="9ab5e-140">System.String</span></span>

### <span data-ttu-id="9ab5e-141">Microsoft. Azure. Commands. Network. Models. PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="9ab5e-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="9ab5e-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9ab5e-142">OUTPUTS</span></span>

### <span data-ttu-id="9ab5e-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9ab5e-143">System.Boolean</span></span>

## <span data-ttu-id="9ab5e-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="9ab5e-144">NOTES</span></span>

## <span data-ttu-id="9ab5e-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9ab5e-145">RELATED LINKS</span></span>
