---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/restart-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Restart-AzVM.md
ms.openlocfilehash: f7965e43c7a294d50d6f0774f76504a90c9d7148
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911393"
---
# <span data-ttu-id="0fab1-101">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="0fab1-101">Restart-AzVM</span></span>

## <span data-ttu-id="0fab1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fab1-102">SYNOPSIS</span></span>
<span data-ttu-id="0fab1-103">Перезапуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="0fab1-103">Restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="0fab1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fab1-104">SYNTAX</span></span>

### <span data-ttu-id="0fab1-105">RestartResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0fab1-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fab1-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0fab1-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fab1-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0fab1-107">RestartIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fab1-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0fab1-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fab1-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fab1-109">DESCRIPTION</span></span>
<span data-ttu-id="0fab1-110">Командлет **restart-AzVM** перезапустит виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="0fab1-110">The **Restart-AzVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="0fab1-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fab1-111">EXAMPLES</span></span>

### <span data-ttu-id="0fab1-112">Пример 1: перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="0fab1-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="0fab1-113">Эта команда перезапускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0fab1-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="0fab1-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fab1-114">PARAMETERS</span></span>

### <span data-ttu-id="0fab1-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fab1-115">-AsJob</span></span>
<span data-ttu-id="0fab1-116">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0fab1-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0fab1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fab1-117">-DefaultProfile</span></span>
<span data-ttu-id="0fab1-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fab1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fab1-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0fab1-119">-Id</span></span>
<span data-ttu-id="0fab1-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="0fab1-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: RestartIdParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fab1-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0fab1-121">-Name</span></span>
<span data-ttu-id="0fab1-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0fab1-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fab1-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="0fab1-123">-PerformMaintenance</span></span>
<span data-ttu-id="0fab1-124">Для выполнения обслуживания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0fab1-124">To perform the maintenance of virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PerformMaintenanceResourceGroupNameParameterSetName, PerformMaintenanceIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fab1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fab1-125">-ResourceGroupName</span></span>
<span data-ttu-id="0fab1-126">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0fab1-126">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: RestartResourceGroupNameParameterSetName, PerformMaintenanceResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fab1-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fab1-127">-Confirm</span></span>
<span data-ttu-id="0fab1-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0fab1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fab1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fab1-129">-WhatIf</span></span>
<span data-ttu-id="0fab1-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0fab1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fab1-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0fab1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fab1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fab1-132">CommonParameters</span></span>
<span data-ttu-id="0fab1-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fab1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fab1-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fab1-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fab1-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fab1-135">INPUTS</span></span>

### <span data-ttu-id="0fab1-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="0fab1-136">None</span></span>
<span data-ttu-id="0fab1-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0fab1-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0fab1-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fab1-138">OUTPUTS</span></span>

### <span data-ttu-id="0fab1-139">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="0fab1-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="0fab1-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fab1-140">NOTES</span></span>

## <span data-ttu-id="0fab1-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fab1-141">RELATED LINKS</span></span>

[<span data-ttu-id="0fab1-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0fab1-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="0fab1-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0fab1-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="0fab1-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="0fab1-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="0fab1-145">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="0fab1-145">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="0fab1-146">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="0fab1-146">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="0fab1-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0fab1-147">Update-AzVM</span></span>](./Update-AzVM.md)


