---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/update-azurermvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Update-AzureRmVirtualWan.md
ms.openlocfilehash: 3f62cf755ac06efe9ed5f04a6657a36cfe612abe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93560847"
---
# <span data-ttu-id="e6986-101">Update-AzureRmVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e6986-101">Update-AzureRmVirtualWan</span></span>

## <span data-ttu-id="e6986-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e6986-102">SYNOPSIS</span></span>
<span data-ttu-id="e6986-103">Обновляет виртуальную глобальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="e6986-103">Updates an Azure Virtual WAN.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6986-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e6986-104">SYNTAX</span></span>

### <span data-ttu-id="e6986-105">ByVirtualWanName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e6986-105">ByVirtualWanName (Default)</span></span>
```
Update-AzureRmVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6986-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="e6986-106">ByVirtualWanObject</span></span>
```
Update-AzureRmVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6986-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="e6986-107">ByVirtualWanResourceId</span></span>
```
Update-AzureRmVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6986-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6986-108">DESCRIPTION</span></span>
<span data-ttu-id="e6986-109">Обновляет виртуальную глобальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="e6986-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="e6986-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e6986-110">EXAMPLES</span></span>

### <span data-ttu-id="e6986-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e6986-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="e6986-112">В примере выше будет создана группа ресурсов "testRG" в регионе "Западная часть США" и виртуальная сеть Azure в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="e6986-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="e6986-113">VirtualWan обновляется новыми свойствами.</span><span class="sxs-lookup"><span data-stu-id="e6986-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="e6986-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e6986-114">PARAMETERS</span></span>

### <span data-ttu-id="e6986-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="e6986-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="e6986-116">Разрешить переход к трафику ветвления для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e6986-116">Allow branch to branch traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="e6986-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="e6986-118">Разрешите трафик vnet на виртуальную сеть для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="e6986-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6986-119">-AsJob</span></span>
<span data-ttu-id="e6986-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="e6986-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6986-121">-DefaultProfile</span></span>
<span data-ttu-id="e6986-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e6986-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e6986-123">-Force</span></span>
<span data-ttu-id="e6986-124">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="e6986-124">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e6986-125">-InputObject</span></span>
<span data-ttu-id="e6986-126">Объект виртуальной глобальной сети, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="e6986-126">The virtual wan object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObject
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e6986-127">-Name</span></span>
<span data-ttu-id="e6986-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="e6986-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e6986-129">-ResourceGroupName</span></span>
<span data-ttu-id="e6986-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6986-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e6986-131">-ResourceId</span></span>
<span data-ttu-id="e6986-132">Идентификатор ресурса Azure для виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="e6986-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="e6986-133">-Tag</span></span>
<span data-ttu-id="e6986-134">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="e6986-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e6986-135">-Confirm</span></span>
<span data-ttu-id="e6986-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e6986-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6986-137">-WhatIf</span></span>
<span data-ttu-id="e6986-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e6986-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6986-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e6986-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6986-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6986-140">CommonParameters</span></span>
<span data-ttu-id="e6986-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e6986-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6986-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6986-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6986-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e6986-143">INPUTS</span></span>

### <span data-ttu-id="e6986-144">System. String</span><span class="sxs-lookup"><span data-stu-id="e6986-144">System.String</span></span>

### <span data-ttu-id="e6986-145">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e6986-145">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="e6986-146">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e6986-146">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e6986-147">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e6986-147">OUTPUTS</span></span>

### <span data-ttu-id="e6986-148">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="e6986-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="e6986-149">Пуск</span><span class="sxs-lookup"><span data-stu-id="e6986-149">NOTES</span></span>

## <span data-ttu-id="e6986-150">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e6986-150">RELATED LINKS</span></span>
