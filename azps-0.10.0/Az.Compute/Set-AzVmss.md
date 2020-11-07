---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVmss.md
ms.openlocfilehash: 5ceb420f30525817ebccd6d3f38a53e6c1cad66e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911316"
---
# <span data-ttu-id="f59ab-101">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f59ab-101">Set-AzVmss</span></span>

## <span data-ttu-id="f59ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f59ab-102">SYNOPSIS</span></span>
<span data-ttu-id="f59ab-103">Задает определенные действия в указанном VMSS.</span><span class="sxs-lookup"><span data-stu-id="f59ab-103">Sets specific actions on a specified VMSS.</span></span>

## <span data-ttu-id="f59ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f59ab-104">SYNTAX</span></span>

### <span data-ttu-id="f59ab-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f59ab-105">DefaultParameter (Default)</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f59ab-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="f59ab-106">FriendMethod</span></span>
```
Set-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f59ab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f59ab-107">DESCRIPTION</span></span>
<span data-ttu-id="f59ab-108">Командлет **Set-AzVmss** задает определенные действия в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="f59ab-108">The **Set-AzVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="f59ab-109">Единственным действием, поддерживаемым этим командлетом, является переобраз.</span><span class="sxs-lookup"><span data-stu-id="f59ab-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="f59ab-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f59ab-110">EXAMPLES</span></span>

### <span data-ttu-id="f59ab-111">Пример 1: переизображение VMSS</span><span class="sxs-lookup"><span data-stu-id="f59ab-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="f59ab-112">Эта команда позволяет переобразировать VMSS с именем ContosoVMSS, которое принадлежит группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="f59ab-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="f59ab-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f59ab-113">PARAMETERS</span></span>

### <span data-ttu-id="f59ab-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f59ab-114">-AsJob</span></span>
<span data-ttu-id="f59ab-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="f59ab-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="f59ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f59ab-116">-DefaultProfile</span></span>
<span data-ttu-id="f59ab-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f59ab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f59ab-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="f59ab-118">-InstanceId</span></span>
<span data-ttu-id="f59ab-119">Идентификатор экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="f59ab-119">The instance ID of the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59ab-120">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="f59ab-120">-Reimage</span></span>
<span data-ttu-id="f59ab-121">Указывает на то, что командлет переобразует VMSS.</span><span class="sxs-lookup"><span data-stu-id="f59ab-121">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59ab-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="f59ab-122">-ReimageAll</span></span>
<span data-ttu-id="f59ab-123">Указывает на то, что командлет переобразовать все диски в VMSS.</span><span class="sxs-lookup"><span data-stu-id="f59ab-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f59ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f59ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="f59ab-125">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="f59ab-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="f59ab-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="f59ab-126">-VMScaleSetName</span></span>
<span data-ttu-id="f59ab-127">Форель имя VMSS, для которого этот командлет задает действия.</span><span class="sxs-lookup"><span data-stu-id="f59ab-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f59ab-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f59ab-128">-Confirm</span></span>
<span data-ttu-id="f59ab-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f59ab-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f59ab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f59ab-130">-WhatIf</span></span>
<span data-ttu-id="f59ab-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f59ab-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f59ab-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f59ab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f59ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f59ab-133">CommonParameters</span></span>
<span data-ttu-id="f59ab-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f59ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f59ab-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f59ab-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f59ab-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f59ab-136">INPUTS</span></span>

### <span data-ttu-id="f59ab-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="f59ab-137">None</span></span>
<span data-ttu-id="f59ab-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="f59ab-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f59ab-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f59ab-139">OUTPUTS</span></span>

### <span data-ttu-id="f59ab-140">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="f59ab-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="f59ab-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="f59ab-141">NOTES</span></span>

## <span data-ttu-id="f59ab-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f59ab-142">RELATED LINKS</span></span>

[<span data-ttu-id="f59ab-143">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f59ab-143">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="f59ab-144">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f59ab-144">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="f59ab-145">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f59ab-145">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="f59ab-146">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f59ab-146">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="f59ab-147">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f59ab-147">Start-AzVmss</span></span>](./Start-AzVmss.md)

[<span data-ttu-id="f59ab-148">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f59ab-148">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="f59ab-149">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="f59ab-149">Update-AzVmss</span></span>](./Update-AzVmss.md)


