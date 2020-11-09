---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244102"
---
# <span data-ttu-id="e703d-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="e703d-101">Remove-AzBastion</span></span>

## <span data-ttu-id="e703d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e703d-102">SYNOPSIS</span></span>
<span data-ttu-id="e703d-103">Удаляет ресурс Bastion.</span><span class="sxs-lookup"><span data-stu-id="e703d-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="e703d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e703d-104">SYNTAX</span></span>

### <span data-ttu-id="e703d-105">ByResourceGroupName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e703d-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e703d-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e703d-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e703d-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="e703d-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e703d-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e703d-108">DESCRIPTION</span></span>
<span data-ttu-id="e703d-109">Удаляет ресурс Bastion. Example1 удаляет Bastion с помощью ResourceGroupName и ResourceName.</span><span class="sxs-lookup"><span data-stu-id="e703d-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="e703d-110">Example2 удаляет Bastion с помощью объекта конвейера.</span><span class="sxs-lookup"><span data-stu-id="e703d-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="e703d-111">Example3 удаляет Bastion с помощью объекта.</span><span class="sxs-lookup"><span data-stu-id="e703d-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="e703d-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e703d-112">EXAMPLES</span></span>

### <span data-ttu-id="e703d-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e703d-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="e703d-114">Пример 2</span><span class="sxs-lookup"><span data-stu-id="e703d-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="e703d-115">Пример 3</span><span class="sxs-lookup"><span data-stu-id="e703d-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="e703d-116">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e703d-116">PARAMETERS</span></span>

### <span data-ttu-id="e703d-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e703d-117">-Confirm</span></span>
<span data-ttu-id="e703d-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e703d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e703d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e703d-119">-DefaultProfile</span></span>
<span data-ttu-id="e703d-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e703d-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e703d-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e703d-121">-Force</span></span>
<span data-ttu-id="e703d-122">Не запрашивать подтверждение.</span><span class="sxs-lookup"><span data-stu-id="e703d-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="e703d-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e703d-123">-InputObject</span></span>
<span data-ttu-id="e703d-124">Объект Bastion, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e703d-124">The Bastion object to be deleted.</span></span>

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

### <span data-ttu-id="e703d-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e703d-125">-Name</span></span>
<span data-ttu-id="e703d-126">Имя ресурса Bastion, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e703d-126">The bastion resource name to be deleted.</span></span>

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

### <span data-ttu-id="e703d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e703d-127">-PassThru</span></span>
<span data-ttu-id="e703d-128">Возвращает объект, представляющий элемент, для которого выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="e703d-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="e703d-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e703d-129">-ResourceGroupName</span></span>
<span data-ttu-id="e703d-130">Имя группы ресурсов, в которой Bastion существует.</span><span class="sxs-lookup"><span data-stu-id="e703d-130">The resource group name where bastion exists.</span></span>

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

### <span data-ttu-id="e703d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e703d-131">-ResourceId</span></span>
<span data-ttu-id="e703d-132">Идентификатор ресурса Azure для Bastion, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="e703d-132">The Azure resource ID for the Bastion to be deleted.</span></span>

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

### <span data-ttu-id="e703d-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e703d-133">-WhatIf</span></span>
<span data-ttu-id="e703d-134">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e703d-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e703d-135">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e703d-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e703d-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e703d-136">CommonParameters</span></span>
<span data-ttu-id="e703d-137">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e703d-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e703d-138">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e703d-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e703d-139">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e703d-139">INPUTS</span></span>

### <span data-ttu-id="e703d-140">Microsoft. Azure. Commands. Network. Models. PSBastion</span><span class="sxs-lookup"><span data-stu-id="e703d-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="e703d-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e703d-141">System.String</span></span>

## <span data-ttu-id="e703d-142">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e703d-142">OUTPUTS</span></span>

### <span data-ttu-id="e703d-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e703d-143">System.Boolean</span></span>

## <span data-ttu-id="e703d-144">Пуск</span><span class="sxs-lookup"><span data-stu-id="e703d-144">NOTES</span></span>

## <span data-ttu-id="e703d-145">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e703d-145">RELATED LINKS</span></span>
[<span data-ttu-id="e703d-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="e703d-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="e703d-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="e703d-147">New-AzBastion</span></span>](./New-AzBastion.md)