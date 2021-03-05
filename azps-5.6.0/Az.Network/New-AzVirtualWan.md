---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 3bb2a2d7c8e53cc7ba336234e3c5b24ad58e2faa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995333"
---
# <span data-ttu-id="dbee6-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="dbee6-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="dbee6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbee6-102">SYNOPSIS</span></span>
<span data-ttu-id="dbee6-103">Создает виртуальную WAN Azure.</span><span class="sxs-lookup"><span data-stu-id="dbee6-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="dbee6-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dbee6-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbee6-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dbee6-105">DESCRIPTION</span></span>
<span data-ttu-id="dbee6-106">Создает новый ресурс виртуальной wan Azure.</span><span class="sxs-lookup"><span data-stu-id="dbee6-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="dbee6-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dbee6-107">EXAMPLES</span></span>

### <span data-ttu-id="dbee6-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dbee6-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="dbee6-109">Выше будет создаваться группа ресурсов testRG в регионе "West US" и виртуальная сеть Azure с ветвью на ветвь трафика, разрешенным в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="dbee6-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="dbee6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbee6-110">PARAMETERS</span></span>

### <span data-ttu-id="dbee6-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="dbee6-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="dbee6-112">Разрешить ветвь-трафик для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="dbee6-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="dbee6-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="dbee6-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="dbee6-114">Разрешить VNET-трафик vnet для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="dbee6-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="dbee6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dbee6-115">-AsJob</span></span>
<span data-ttu-id="dbee6-116">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="dbee6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dbee6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbee6-117">-DefaultProfile</span></span>
<span data-ttu-id="dbee6-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dbee6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbee6-119">-Location</span><span class="sxs-lookup"><span data-stu-id="dbee6-119">-Location</span></span>
<span data-ttu-id="dbee6-120">Расположение ресурса VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="dbee6-120">The location of the VirtualWAN resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbee6-121">-Name</span><span class="sxs-lookup"><span data-stu-id="dbee6-121">-Name</span></span>
<span data-ttu-id="dbee6-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="dbee6-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbee6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbee6-123">-ResourceGroupName</span></span>
<span data-ttu-id="dbee6-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="dbee6-124">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbee6-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="dbee6-125">-Tag</span></span>
<span data-ttu-id="dbee6-126">A hashtable which represents resource tags.</span><span class="sxs-lookup"><span data-stu-id="dbee6-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbee6-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="dbee6-127">-VirtualWANType</span></span>
<span data-ttu-id="dbee6-128">Тип виртуальной wan.</span><span class="sxs-lookup"><span data-stu-id="dbee6-128">The type of the Virtual Wan.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbee6-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbee6-129">-Confirm</span></span>
<span data-ttu-id="dbee6-130">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="dbee6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbee6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbee6-131">-WhatIf</span></span>
<span data-ttu-id="dbee6-132">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbee6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbee6-133">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dbee6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbee6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbee6-134">CommonParameters</span></span>
<span data-ttu-id="dbee6-135">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbee6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbee6-136">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dbee6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbee6-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dbee6-137">INPUTS</span></span>

### <span data-ttu-id="dbee6-138">Нет</span><span class="sxs-lookup"><span data-stu-id="dbee6-138">None</span></span>

## <span data-ttu-id="dbee6-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dbee6-139">OUTPUTS</span></span>

### <span data-ttu-id="dbee6-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="dbee6-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="dbee6-141">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dbee6-141">NOTES</span></span>

## <span data-ttu-id="dbee6-142">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dbee6-142">RELATED LINKS</span></span>

[<span data-ttu-id="dbee6-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="dbee6-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="dbee6-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="dbee6-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="dbee6-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="dbee6-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
