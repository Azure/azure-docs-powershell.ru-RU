---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: EF155949-5766-4BC4-9C8A-2B97E8EA032D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/restart-azurermvm
schema: 2.0.0
ms.openlocfilehash: 86fb5997c93aecbaa5aabd07255ae6bde840e91f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914913"
---
# <span data-ttu-id="35cfd-101">Restart-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35cfd-101">Restart-AzureRmVM</span></span>

## <span data-ttu-id="35cfd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="35cfd-102">SYNOPSIS</span></span>
<span data-ttu-id="35cfd-103">Перезапуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="35cfd-103">Restarts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="35cfd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="35cfd-104">SYNTAX</span></span>

### <span data-ttu-id="35cfd-105">RestartResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="35cfd-105">RestartResourceGroupNameParameterSetName (Default)</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35cfd-106">PerformMaintenanceResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="35cfd-106">PerformMaintenanceResourceGroupNameParameterSetName</span></span>
```
Restart-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35cfd-107">RestartIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="35cfd-107">RestartIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35cfd-108">PerformMaintenanceIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="35cfd-108">PerformMaintenanceIdParameterSetName</span></span>
```
Restart-AzureRmVM [-Id] <String> [-Name] <String> [-PerformMaintenance] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35cfd-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="35cfd-109">DESCRIPTION</span></span>
<span data-ttu-id="35cfd-110">Командлет **restart-AzureRmVM** перезапустит виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="35cfd-110">The **Restart-AzureRmVM** cmdlet restarts an Azure virtual machine.</span></span>

## <span data-ttu-id="35cfd-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="35cfd-111">EXAMPLES</span></span>

### <span data-ttu-id="35cfd-112">Пример 1: перезапуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="35cfd-112">Example 1: Restart a virtual machine</span></span>
```
PS C:\> Restart-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="35cfd-113">Эта команда перезапускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="35cfd-113">This command restarts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="35cfd-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="35cfd-114">PARAMETERS</span></span>

### <span data-ttu-id="35cfd-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="35cfd-115">-AsJob</span></span>
<span data-ttu-id="35cfd-116">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="35cfd-116">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="35cfd-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35cfd-117">-DefaultProfile</span></span>
<span data-ttu-id="35cfd-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="35cfd-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="35cfd-119">-ID</span><span class="sxs-lookup"><span data-stu-id="35cfd-119">-Id</span></span>
<span data-ttu-id="35cfd-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="35cfd-120">The resource group name.</span></span>

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

### <span data-ttu-id="35cfd-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="35cfd-121">-Name</span></span>
<span data-ttu-id="35cfd-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="35cfd-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="35cfd-123">-PerformMaintenance</span><span class="sxs-lookup"><span data-stu-id="35cfd-123">-PerformMaintenance</span></span>
<span data-ttu-id="35cfd-124">Для выполнения обслуживания виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="35cfd-124">To perform the maintenance of virtual machine.</span></span>

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

### <span data-ttu-id="35cfd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35cfd-125">-ResourceGroupName</span></span>
<span data-ttu-id="35cfd-126">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="35cfd-126">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="35cfd-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35cfd-127">-Confirm</span></span>
<span data-ttu-id="35cfd-128">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="35cfd-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35cfd-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35cfd-129">-WhatIf</span></span>
<span data-ttu-id="35cfd-130">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="35cfd-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35cfd-131">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="35cfd-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35cfd-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35cfd-132">CommonParameters</span></span>
<span data-ttu-id="35cfd-133">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="35cfd-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35cfd-134">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35cfd-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35cfd-135">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="35cfd-135">INPUTS</span></span>

### <span data-ttu-id="35cfd-136">Ничего</span><span class="sxs-lookup"><span data-stu-id="35cfd-136">None</span></span>
<span data-ttu-id="35cfd-137">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="35cfd-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="35cfd-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="35cfd-138">OUTPUTS</span></span>

### <span data-ttu-id="35cfd-139">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="35cfd-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="35cfd-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="35cfd-140">NOTES</span></span>

## <span data-ttu-id="35cfd-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="35cfd-141">RELATED LINKS</span></span>

[<span data-ttu-id="35cfd-142">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35cfd-142">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="35cfd-143">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35cfd-143">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="35cfd-144">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35cfd-144">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="35cfd-145">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35cfd-145">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="35cfd-146">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35cfd-146">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="35cfd-147">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="35cfd-147">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


