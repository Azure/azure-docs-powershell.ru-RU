---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240616"
---
# <span data-ttu-id="45890-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45890-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="45890-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45890-102">SYNOPSIS</span></span>
<span data-ttu-id="45890-103">Удаление связанного с виртуальным концентратором ресурса таблицы маршрутов виртуального концентратора.</span><span class="sxs-lookup"><span data-stu-id="45890-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="45890-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="45890-104">SYNTAX</span></span>

### <span data-ttu-id="45890-105">ByVirtualHubRouteTableName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="45890-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45890-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="45890-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45890-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="45890-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45890-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="45890-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45890-109">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="45890-109">DESCRIPTION</span></span>
<span data-ttu-id="45890-110">Удаляет указанную таблицу маршрутов, связанную с указанным виртуальным центром.</span><span class="sxs-lookup"><span data-stu-id="45890-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="45890-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="45890-111">EXAMPLES</span></span>

### <span data-ttu-id="45890-112">Пример 1</span><span class="sxs-lookup"><span data-stu-id="45890-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="45890-113">Эта команда удаляет маршрутTable1 виртуального концентратора westsub.</span><span class="sxs-lookup"><span data-stu-id="45890-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="45890-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45890-114">PARAMETERS</span></span>

### <span data-ttu-id="45890-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45890-115">-AsJob</span></span>
<span data-ttu-id="45890-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="45890-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="45890-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45890-117">-DefaultProfile</span></span>
<span data-ttu-id="45890-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="45890-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45890-119">-Force</span><span class="sxs-lookup"><span data-stu-id="45890-119">-Force</span></span>
<span data-ttu-id="45890-120">Не спрашивайте подтверждения при переописи ресурса</span><span class="sxs-lookup"><span data-stu-id="45890-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="45890-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="45890-121">-HubName</span></span>
<span data-ttu-id="45890-122">Имя родительского ресурса.</span><span class="sxs-lookup"><span data-stu-id="45890-122">The parent resource name.</span></span>

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

### <span data-ttu-id="45890-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45890-123">-InputObject</span></span>
<span data-ttu-id="45890-124">Удаляется виртуальный ресурс, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="45890-124">The virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="45890-125">-Name</span><span class="sxs-lookup"><span data-stu-id="45890-125">-Name</span></span>
<span data-ttu-id="45890-126">Имя ресурса.</span><span class="sxs-lookup"><span data-stu-id="45890-126">The resource name.</span></span>

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

### <span data-ttu-id="45890-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45890-127">-PassThru</span></span>
<span data-ttu-id="45890-128">Возвращает объект, представляющий элемент, для которого выполняется эта операция.</span><span class="sxs-lookup"><span data-stu-id="45890-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="45890-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45890-129">-ResourceGroupName</span></span>
<span data-ttu-id="45890-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="45890-130">The resource group name.</span></span>

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

### <span data-ttu-id="45890-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="45890-131">-ResourceId</span></span>
<span data-ttu-id="45890-132">ИД ресурса, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="45890-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="45890-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="45890-133">-VirtualHub</span></span>
<span data-ttu-id="45890-134">{{ Заполнить описание VirtualHub }}</span><span class="sxs-lookup"><span data-stu-id="45890-134">{{ Fill VirtualHub Description }}</span></span>

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

### <span data-ttu-id="45890-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45890-135">-Confirm</span></span>
<span data-ttu-id="45890-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45890-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45890-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45890-137">-WhatIf</span></span>
<span data-ttu-id="45890-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45890-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45890-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="45890-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45890-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45890-140">CommonParameters</span></span>
<span data-ttu-id="45890-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45890-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45890-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45890-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45890-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="45890-143">INPUTS</span></span>

### <span data-ttu-id="45890-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="45890-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="45890-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="45890-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="45890-146">System.String</span><span class="sxs-lookup"><span data-stu-id="45890-146">System.String</span></span>

## <span data-ttu-id="45890-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="45890-147">OUTPUTS</span></span>

### <span data-ttu-id="45890-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45890-148">System.Boolean</span></span>

## <span data-ttu-id="45890-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="45890-149">NOTES</span></span>

## <span data-ttu-id="45890-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="45890-150">RELATED LINKS</span></span>
