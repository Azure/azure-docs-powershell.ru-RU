---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualwan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualWan.md
ms.openlocfilehash: 3a1d30f3ae44b0e6893682cf0c1d700207682803
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729923"
---
# <span data-ttu-id="bcb93-101">Update-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bcb93-101">Update-AzVirtualWan</span></span>

## <span data-ttu-id="bcb93-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bcb93-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb93-103">Обновляет виртуальную глобальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb93-103">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="bcb93-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bcb93-104">SYNTAX</span></span>

### <span data-ttu-id="bcb93-105">ByVirtualWanName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bcb93-105">ByVirtualWanName (Default)</span></span>
```
Update-AzVirtualWan -ResourceGroupName <String> -Name <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcb93-106">ByVirtualWanObject</span><span class="sxs-lookup"><span data-stu-id="bcb93-106">ByVirtualWanObject</span></span>
```
Update-AzVirtualWan -InputObject <PSVirtualWan> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bcb93-107">ByVirtualWanResourceId</span><span class="sxs-lookup"><span data-stu-id="bcb93-107">ByVirtualWanResourceId</span></span>
```
Update-AzVirtualWan -ResourceId <String> [-AllowVnetToVnetTraffic <Boolean>]
 [-AllowBranchToBranchTraffic <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcb93-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcb93-108">DESCRIPTION</span></span>
<span data-ttu-id="bcb93-109">Обновляет виртуальную глобальную сеть Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb93-109">Updates an Azure Virtual WAN.</span></span>

## <span data-ttu-id="bcb93-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bcb93-110">EXAMPLES</span></span>

### <span data-ttu-id="bcb93-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bcb93-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG" 
PS C:\> New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> Update-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -AllowBranchToBranchTraffic $true -AllowVnetToVnetTraffic $false

Name                       : testRG
Id                         : /subscriptions/{SubscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AllowVnetToVnetTraffic     : False
AllowBranchToBranchTraffic : True
Location                   : West US
Type                       : Microsoft.Network/virtualWans
ProvisioningState          : Succeeded
```

<span data-ttu-id="bcb93-112">В примере выше будет создана группа ресурсов "testRG" в регионе "Западная часть США" и виртуальная сеть Azure в этой группе ресурсов в Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb93-112">The above will create a resource group "testRG" in region "West US" and an Azure Virtual WAN in that resource group in Azure.</span></span> <span data-ttu-id="bcb93-113">VirtualWan обновляется новыми свойствами.</span><span class="sxs-lookup"><span data-stu-id="bcb93-113">VirtualWan is updated with new properties.</span></span>

## <span data-ttu-id="bcb93-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bcb93-114">PARAMETERS</span></span>

### <span data-ttu-id="bcb93-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="bcb93-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="bcb93-116">Разрешить переход к трафику ветвления для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="bcb93-116">Allow branch to branch traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="bcb93-117">-AllowVnetToVnetTraffic</span><span class="sxs-lookup"><span data-stu-id="bcb93-117">-AllowVnetToVnetTraffic</span></span>
<span data-ttu-id="bcb93-118">Разрешите трафик vnet на виртуальную сеть для VirtualWan.</span><span class="sxs-lookup"><span data-stu-id="bcb93-118">Allow vnet to vnet traffic for VirtualWan.</span></span>

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

### <span data-ttu-id="bcb93-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bcb93-119">-AsJob</span></span>
<span data-ttu-id="bcb93-120">Выполнить командлет в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="bcb93-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bcb93-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb93-121">-DefaultProfile</span></span>
<span data-ttu-id="bcb93-122">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb93-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb93-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bcb93-123">-Force</span></span>
<span data-ttu-id="bcb93-124">Не запрашивать подтверждение, если вы хотите переделать ресурс</span><span class="sxs-lookup"><span data-stu-id="bcb93-124">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="bcb93-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bcb93-125">-InputObject</span></span>
<span data-ttu-id="bcb93-126">Объект виртуальной глобальной сети, который нужно изменить.</span><span class="sxs-lookup"><span data-stu-id="bcb93-126">The virtual wan object to be modified</span></span>

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

### <span data-ttu-id="bcb93-127">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="bcb93-127">-Name</span></span>
<span data-ttu-id="bcb93-128">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="bcb93-128">The resource name.</span></span>

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

### <span data-ttu-id="bcb93-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb93-129">-ResourceGroupName</span></span>
<span data-ttu-id="bcb93-130">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bcb93-130">The resource group name.</span></span>

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

### <span data-ttu-id="bcb93-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bcb93-131">-ResourceId</span></span>
<span data-ttu-id="bcb93-132">Идентификатор ресурса Azure для виртуальной глобальной сети.</span><span class="sxs-lookup"><span data-stu-id="bcb93-132">The Azure resource ID for the virtual wan.</span></span>

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

### <span data-ttu-id="bcb93-133">-Тег</span><span class="sxs-lookup"><span data-stu-id="bcb93-133">-Tag</span></span>
<span data-ttu-id="bcb93-134">Хэш-таблица, представляющая Теги ресурсов.</span><span class="sxs-lookup"><span data-stu-id="bcb93-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb93-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bcb93-135">-Confirm</span></span>
<span data-ttu-id="bcb93-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bcb93-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bcb93-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb93-137">-WhatIf</span></span>
<span data-ttu-id="bcb93-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bcb93-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb93-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bcb93-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bcb93-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb93-140">CommonParameters</span></span>
<span data-ttu-id="bcb93-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bcb93-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb93-142">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb93-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb93-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bcb93-143">INPUTS</span></span>

### <span data-ttu-id="bcb93-144">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bcb93-144">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="bcb93-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bcb93-145">System.String</span></span>

## <span data-ttu-id="bcb93-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bcb93-146">OUTPUTS</span></span>

### <span data-ttu-id="bcb93-147">Microsoft. Azure. Commands. Network. Models. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bcb93-147">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

## <span data-ttu-id="bcb93-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="bcb93-148">NOTES</span></span>

## <span data-ttu-id="bcb93-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bcb93-149">RELATED LINKS</span></span>

[<span data-ttu-id="bcb93-150">Get-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bcb93-150">Get-AzVirtualWan</span></span>](./Get-AzVirtualWan.md)

[<span data-ttu-id="bcb93-151">New-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bcb93-151">New-AzVirtualWan</span></span>](./New-AzVirtualWan.md)

[<span data-ttu-id="bcb93-152">Remove-AzVirtualWan</span><span class="sxs-lookup"><span data-stu-id="bcb93-152">Remove-AzVirtualWan</span></span>](./Remove-AzVirtualWan.md)
