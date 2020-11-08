---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94248102"
---
# <span data-ttu-id="fdcf6-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fdcf6-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="fdcf6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fdcf6-102">SYNOPSIS</span></span>
<span data-ttu-id="fdcf6-103">Удаление ресурса таблицы узлового маршрута, связанного с VirtualHub.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="fdcf6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fdcf6-104">SYNTAX</span></span>

### <span data-ttu-id="fdcf6-105">ByVHubRouteTableName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fdcf6-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdcf6-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="fdcf6-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdcf6-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="fdcf6-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdcf6-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="fdcf6-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdcf6-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdcf6-109">DESCRIPTION</span></span>
<span data-ttu-id="fdcf6-110">Удаляет указанную таблицу маршрутов Hub, связанную с указанным виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="fdcf6-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fdcf6-111">EXAMPLES</span></span>

### <span data-ttu-id="fdcf6-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="fdcf6-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="fdcf6-113">Эта команда удаляет таблицу "разветвитель маршрута" виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="fdcf6-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fdcf6-114">PARAMETERS</span></span>

### <span data-ttu-id="fdcf6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdcf6-115">-AsJob</span></span>
<span data-ttu-id="fdcf6-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="fdcf6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdcf6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdcf6-117">-DefaultProfile</span></span>
<span data-ttu-id="fdcf6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdcf6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="fdcf6-119">-Force</span></span>
<span data-ttu-id="fdcf6-120">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="fdcf6-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fdcf6-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdcf6-121">-InputObject</span></span>
<span data-ttu-id="fdcf6-122">Ресурс vhubroutetable, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdcf6-123">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="fdcf6-123">-Name</span></span>
<span data-ttu-id="fdcf6-124">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdcf6-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="fdcf6-125">-ParentObject</span></span>
<span data-ttu-id="fdcf6-126">Родительский объект виртуального концентратора для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdcf6-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="fdcf6-127">-ParentResourceName</span></span>
<span data-ttu-id="fdcf6-128">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdcf6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdcf6-129">-PassThru</span></span>
<span data-ttu-id="fdcf6-130">Возвращает объект, представляющий элемент, для которого выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="fdcf6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdcf6-131">-ResourceGroupName</span></span>
<span data-ttu-id="fdcf6-132">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fdcf6-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdcf6-133">-ResourceId</span></span>
<span data-ttu-id="fdcf6-134">Идентификатор ресурса для ресурса vhubroutetable, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdcf6-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fdcf6-135">-Confirm</span></span>
<span data-ttu-id="fdcf6-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdcf6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdcf6-137">-WhatIf</span></span>
<span data-ttu-id="fdcf6-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdcf6-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdcf6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdcf6-140">CommonParameters</span></span>
<span data-ttu-id="fdcf6-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fdcf6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdcf6-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdcf6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdcf6-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fdcf6-143">INPUTS</span></span>

### <span data-ttu-id="fdcf6-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fdcf6-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="fdcf6-145">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fdcf6-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="fdcf6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fdcf6-146">System.String</span></span>

## <span data-ttu-id="fdcf6-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fdcf6-147">OUTPUTS</span></span>

### <span data-ttu-id="fdcf6-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fdcf6-148">System.Boolean</span></span>

## <span data-ttu-id="fdcf6-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="fdcf6-149">NOTES</span></span>

## <span data-ttu-id="fdcf6-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fdcf6-150">RELATED LINKS</span></span>

[<span data-ttu-id="fdcf6-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fdcf6-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="fdcf6-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="fdcf6-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="fdcf6-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fdcf6-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="fdcf6-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="fdcf6-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)