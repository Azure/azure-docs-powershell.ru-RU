---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94078875"
---
# <span data-ttu-id="3dc45-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3dc45-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="3dc45-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3dc45-102">SYNOPSIS</span></span>
<span data-ttu-id="3dc45-103">Удалите ресурс с таблицей виртуального маршрутизатора, связанный с виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="3dc45-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="3dc45-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3dc45-104">SYNTAX</span></span>

### <span data-ttu-id="3dc45-105">ByVirtualHubRouteTableName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3dc45-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dc45-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="3dc45-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dc45-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="3dc45-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3dc45-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="3dc45-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3dc45-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dc45-109">DESCRIPTION</span></span>
<span data-ttu-id="3dc45-110">Удаляет указанную таблицу маршрутов, связанную с указанным виртуальным концентратором.</span><span class="sxs-lookup"><span data-stu-id="3dc45-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="3dc45-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3dc45-111">EXAMPLES</span></span>

### <span data-ttu-id="3dc45-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3dc45-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="3dc45-113">Эта команда удаляет routeTable1 виртуального центра westushub.</span><span class="sxs-lookup"><span data-stu-id="3dc45-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="3dc45-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3dc45-114">PARAMETERS</span></span>

### <span data-ttu-id="3dc45-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3dc45-115">-AsJob</span></span>
<span data-ttu-id="3dc45-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="3dc45-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3dc45-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3dc45-117">-DefaultProfile</span></span>
<span data-ttu-id="3dc45-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3dc45-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3dc45-119">-Force</span><span class="sxs-lookup"><span data-stu-id="3dc45-119">-Force</span></span>
<span data-ttu-id="3dc45-120">Не запрашивать подтверждение, если вы хотите перезаписать ресурс</span><span class="sxs-lookup"><span data-stu-id="3dc45-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="3dc45-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="3dc45-121">-HubName</span></span>
<span data-ttu-id="3dc45-122">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="3dc45-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc45-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3dc45-123">-InputObject</span></span>
<span data-ttu-id="3dc45-124">Ресурс virtualhubroutetable, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3dc45-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc45-125">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3dc45-125">-Name</span></span>
<span data-ttu-id="3dc45-126">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="3dc45-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc45-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3dc45-127">-PassThru</span></span>
<span data-ttu-id="3dc45-128">Возвращает объект, представляющий элемент, для которого выполняется операция.</span><span class="sxs-lookup"><span data-stu-id="3dc45-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="3dc45-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3dc45-129">-ResourceGroupName</span></span>
<span data-ttu-id="3dc45-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="3dc45-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3dc45-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3dc45-131">-ResourceId</span></span>
<span data-ttu-id="3dc45-132">Идентификатор ресурса для ресурса virtualhubroutetable, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="3dc45-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc45-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="3dc45-133">-VirtualHub</span></span>
<span data-ttu-id="3dc45-134">{{Fill VirtualHub Description}}</span><span class="sxs-lookup"><span data-stu-id="3dc45-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3dc45-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3dc45-135">-Confirm</span></span>
<span data-ttu-id="3dc45-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="3dc45-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3dc45-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3dc45-137">-WhatIf</span></span>
<span data-ttu-id="3dc45-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="3dc45-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3dc45-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="3dc45-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3dc45-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3dc45-140">CommonParameters</span></span>
<span data-ttu-id="3dc45-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3dc45-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3dc45-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3dc45-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3dc45-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3dc45-143">INPUTS</span></span>

### <span data-ttu-id="3dc45-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="3dc45-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="3dc45-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="3dc45-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="3dc45-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3dc45-146">System.String</span></span>

## <span data-ttu-id="3dc45-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3dc45-147">OUTPUTS</span></span>

### <span data-ttu-id="3dc45-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3dc45-148">System.Boolean</span></span>

## <span data-ttu-id="3dc45-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="3dc45-149">NOTES</span></span>

## <span data-ttu-id="3dc45-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3dc45-150">RELATED LINKS</span></span>
