---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualWan.md
ms.openlocfilehash: 9969ee8009e1a0cd3cf5e071f01bd03035455bde
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316628"
---
# <span data-ttu-id="d8adf-101">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d8adf-101">New-AzVirtualWan</span></span>

## <span data-ttu-id="d8adf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d8adf-102">SYNOPSIS</span></span>
<span data-ttu-id="d8adf-103">Создает виртуальную глобальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="d8adf-103">Creates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="d8adf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d8adf-104">SYNTAX</span></span>

```
New-AzVirtualWan -ResourceGroupName <String> -Name <String> -Location <String> [-AllowVnetToVnetTraffic]
 [-AllowBranchToBranchTraffic] [-Tag <Hashtable>] [-VirtualWANType <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8adf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8adf-105">DESCRIPTION</span></span>
<span data-ttu-id="d8adf-106">Создание нового ресурса Azure VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="d8adf-106">Creates a new Azure VirtualWAN resource.</span></span>

## <span data-ttu-id="d8adf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d8adf-107">EXAMPLES</span></span>

### <span data-ttu-id="d8adf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d8adf-108">Example 1</span></span>

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

<span data-ttu-id="d8adf-109">В описанном выше примере создается группа ресурсов "testRG" в регионе "Западная часть США" и Виртуальная глобальная сеть Azure с разделом трафика для филиалов, разрешенных в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="d8adf-109">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN with branch to branch traffic allowed in that resource group in Azure.</span></span>

## <span data-ttu-id="d8adf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d8adf-110">PARAMETERS</span></span>

### <span data-ttu-id="d8adf-111">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="d8adf-111">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="d8adf-112">Разрешить переход к трафику ветвления для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d8adf-112">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="d8adf-113">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="d8adf-113">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="d8adf-114">Разрешите трафик vnet на виртуальную сеть для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="d8adf-114">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="d8adf-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8adf-115">-AsJob</span></span>
<span data-ttu-id="d8adf-116">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="d8adf-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8adf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8adf-117">-DefaultProfile</span></span>
<span data-ttu-id="d8adf-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d8adf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8adf-119">-Location</span><span class="sxs-lookup"><span data-stu-id="d8adf-119">-Location</span></span>
<span data-ttu-id="d8adf-120">Расположение ресурса VirtualWAN.</span><span class="sxs-lookup"><span data-stu-id="d8adf-120">The location of the VirtualWAN resource.</span></span>

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

### <span data-ttu-id="d8adf-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="d8adf-121">-Name</span></span>
<span data-ttu-id="d8adf-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="d8adf-122">The resource name.</span></span>

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

### <span data-ttu-id="d8adf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8adf-123">-ResourceGroupName</span></span>
<span data-ttu-id="d8adf-124">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8adf-124">The resource group name.</span></span>

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

### <span data-ttu-id="d8adf-125">-Тег</span><span class="sxs-lookup"><span data-stu-id="d8adf-125">-Tag</span></span>
<span data-ttu-id="d8adf-126">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="d8adf-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="d8adf-127">-VirtualWANType</span><span class="sxs-lookup"><span data-stu-id="d8adf-127">-VirtualWANType</span></span>
<span data-ttu-id="d8adf-128">Тип виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="d8adf-128">The type of the Virtual Wan.</span></span>

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

### <span data-ttu-id="d8adf-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8adf-129">-Confirm</span></span>
<span data-ttu-id="d8adf-130">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="d8adf-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8adf-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8adf-131">-WhatIf</span></span>
<span data-ttu-id="d8adf-132">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="d8adf-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8adf-133">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="d8adf-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8adf-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8adf-134">CommonParameters</span></span>
<span data-ttu-id="d8adf-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d8adf-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8adf-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8adf-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8adf-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d8adf-137">INPUTS</span></span>

### <span data-ttu-id="d8adf-138">Ничего</span><span class="sxs-lookup"><span data-stu-id="d8adf-138">None</span></span>

## <span data-ttu-id="d8adf-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d8adf-139">OUTPUTS</span></span>

### <span data-ttu-id="d8adf-140">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d8adf-140">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="d8adf-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="d8adf-141">NOTES</span></span>

## <span data-ttu-id="d8adf-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d8adf-142">RELATED LINKS</span></span>

[<span data-ttu-id="d8adf-143">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d8adf-143">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="d8adf-144">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d8adf-144">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)

[<span data-ttu-id="d8adf-145">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="d8adf-145">Update-AzVirtualWan</span></span>](./Update-AzVirtualWan.md)
