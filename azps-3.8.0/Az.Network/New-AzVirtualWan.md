---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 75b729437599f66be567229a1899028e628079fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94073220"
---
# <span data-ttu-id="e5e5b-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5e5b-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="e5e5b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e5e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e5b-103">Создает виртуальную глобальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="e5e5b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e5e5b-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5e5b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5e5b-105">DESCRIPTION</span></span>
<span data-ttu-id="e5e5b-106">Создание нового ресурса Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="e5e5b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e5e5b-107">EXAMPLES</span></span>

### <span data-ttu-id="e5e5b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e5e5b-108">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US" -AllowBranchToBranchTraffic $true

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
VirtualWANType             : Standard
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="e5e5b-109">В описанном выше примере создается группа ресурсов "testRG" в регионе "Западная часть США" и Виртуальная глобальная сеть Azure с разделом трафика для филиалов, разрешенных в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="e5e5b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e5e5b-110">PARAMETERS</span></span>

### <span data-ttu-id="e5e5b-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="e5e5b-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="e5e5b-112">Разрешить переход к трафику ветвления для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="e5e5b-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="e5e5b-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="e5e5b-114">Разрешите трафик vnet на виртуальную сеть для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="e5e5b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e5e5b-115">-AsJob</span></span>
<span data-ttu-id="e5e5b-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e5e5b-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e5e5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e5b-117">-DefaultProfile</span></span>
<span data-ttu-id="e5e5b-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5e5b-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e5e5b-119">-Location</span></span>
<span data-ttu-id="e5e5b-120">Расположение ресурса VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="e5e5b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e5e5b-121">-Name</span></span>
<span data-ttu-id="e5e5b-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-122">The resource name.</span></span>

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

### <span data-ttu-id="e5e5b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e5b-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5e5b-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-124">The resource group name.</span></span>

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

### <span data-ttu-id="e5e5b-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="e5e5b-125">-Tag</span></span>
<span data-ttu-id="e5e5b-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="e5e5b-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="e5e5b-127">-VirtualWANType</span></span>
<span data-ttu-id="e5e5b-128">Тип виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="e5e5b-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e5e5b-129">-Confirm</span></span>
<span data-ttu-id="e5e5b-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5e5b-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5e5b-131">-WhatIf</span></span>
<span data-ttu-id="e5e5b-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5e5b-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5e5b-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e5b-134">CommonParameters</span></span>
<span data-ttu-id="e5e5b-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e5e5b-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e5b-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e5e5b-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e5b-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e5e5b-137">INPUTS</span></span>

### <span data-ttu-id="e5e5b-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="e5e5b-138">None</span></span>

## <span data-ttu-id="e5e5b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e5e5b-139">OUTPUTS</span></span>

### <span data-ttu-id="e5e5b-140">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5e5b-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="e5e5b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="e5e5b-141">NOTES</span></span>

## <span data-ttu-id="e5e5b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e5e5b-142">RELATED LINKS</span></span>

[<span data-ttu-id="e5e5b-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5e5b-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="e5e5b-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5e5b-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="e5e5b-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e5e5b-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
