---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98425228"
---
# <span data-ttu-id="dc617-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="dc617-101">Remove-AzBastion</span></span>

## <span data-ttu-id="dc617-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc617-102">SYNOPSIS</span></span>
<span data-ttu-id="dc617-103">Удаляет ресурс базы.</span><span class="sxs-lookup"><span data-stu-id="dc617-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="dc617-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc617-104">SYNTAX</span></span>

### <span data-ttu-id="dc617-105">ByResourceGroupName (Default)</span><span class="sxs-lookup"><span data-stu-id="dc617-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc617-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dc617-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc617-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc617-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc617-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc617-108">DESCRIPTION</span></span>
<span data-ttu-id="dc617-109">Удаляет ресурс базы. В примере1 название базы данных удаляется с помощью его названия ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="dc617-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="dc617-110">В примере 2 удаляется название, используя его объект с конвейером.</span><span class="sxs-lookup"><span data-stu-id="dc617-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="dc617-111">В примере 3 удаляется базовая подпись с использованием объекта.</span><span class="sxs-lookup"><span data-stu-id="dc617-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="dc617-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc617-112">EXAMPLES</span></span>

### <span data-ttu-id="dc617-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc617-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="dc617-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="dc617-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="dc617-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="dc617-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="dc617-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc617-116">PARAMETERS</span></span>

### <span data-ttu-id="dc617-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc617-117">-Confirm</span></span>
<span data-ttu-id="dc617-118">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc617-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc617-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc617-119">-DefaultProfile</span></span>
<span data-ttu-id="dc617-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc617-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc617-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dc617-121">-Force</span></span>
<span data-ttu-id="dc617-122">Не спрашивайте подтверждения.</span><span class="sxs-lookup"><span data-stu-id="dc617-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="dc617-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc617-123">-InputObject</span></span>
<span data-ttu-id="dc617-124">Удаляемый объект "Базовая".</span><span class="sxs-lookup"><span data-stu-id="dc617-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dc617-125">-Name</span><span class="sxs-lookup"><span data-stu-id="dc617-125">-Name</span></span>
<span data-ttu-id="dc617-126">Название удаляемой базы данных ресурса.</span><span class="sxs-lookup"><span data-stu-id="dc617-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc617-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc617-127">-PassThru</span></span>
<span data-ttu-id="dc617-128">Возвращает объект, представляющий элемент, с которым выполняется данной операция.</span><span class="sxs-lookup"><span data-stu-id="dc617-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="dc617-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc617-129">-ResourceGroupName</span></span>
<span data-ttu-id="dc617-130">Имя группы ресурсов, в которой есть базовая подпись.</span><span class="sxs-lookup"><span data-stu-id="dc617-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc617-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc617-131">-ResourceId</span></span>
<span data-ttu-id="dc617-132">ИД ресурса Azure для удаления базы данных.</span><span class="sxs-lookup"><span data-stu-id="dc617-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc617-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc617-133">-WhatIf</span></span>
<span data-ttu-id="dc617-134">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc617-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc617-135">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc617-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc617-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc617-136">CommonParameters</span></span>
<span data-ttu-id="dc617-137">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc617-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc617-138">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc617-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc617-139">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc617-139">INPUTS</span></span>

### <span data-ttu-id="dc617-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="dc617-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="dc617-141">System.String</span><span class="sxs-lookup"><span data-stu-id="dc617-141">System.String</span></span>

## <span data-ttu-id="dc617-142">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc617-142">OUTPUTS</span></span>

### <span data-ttu-id="dc617-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc617-143">System.Boolean</span></span>

## <span data-ttu-id="dc617-144">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc617-144">NOTES</span></span>

## <span data-ttu-id="dc617-145">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc617-145">RELATED LINKS</span></span>
[<span data-ttu-id="dc617-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="dc617-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="dc617-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="dc617-147">New-AzBastion</span></span>](./New-AzBastion.md)