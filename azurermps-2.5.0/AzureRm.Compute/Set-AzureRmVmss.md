---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmss
schema: 2.0.0
ms.openlocfilehash: 2d33f111928d0b022c7836d0b5c86fb5ec6f203e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913910"
---
# <span data-ttu-id="0fbb8-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0fbb8-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="0fbb8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0fbb8-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbb8-103">Задает определенные действия в указанном VMSS.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0fbb8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0fbb8-104">SYNTAX</span></span>

### <span data-ttu-id="0fbb8-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0fbb8-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fbb8-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="0fbb8-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fbb8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fbb8-107">DESCRIPTION</span></span>
<span data-ttu-id="0fbb8-108">Командлет **Set-AzureRmVmss** задает определенные действия в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="0fbb8-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0fbb8-109">Единственным действием, поддерживаемым этим командлетом, является переобраз.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="0fbb8-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0fbb8-110">EXAMPLES</span></span>

### <span data-ttu-id="0fbb8-111">Пример 1: переизображение VMSS</span><span class="sxs-lookup"><span data-stu-id="0fbb8-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="0fbb8-112">Эта команда позволяет переобразировать VMSS с именем ContosoVMSS, которое принадлежит группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="0fbb8-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0fbb8-113">PARAMETERS</span></span>

### <span data-ttu-id="0fbb8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fbb8-114">-AsJob</span></span>
<span data-ttu-id="0fbb8-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0fbb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbb8-116">-DefaultProfile</span></span>
<span data-ttu-id="0fbb8-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fbb8-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="0fbb8-118">-InstanceId</span></span>
<span data-ttu-id="0fbb8-119">Идентификатор экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-119">The instance ID of the virtual machine.</span></span>

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

### <span data-ttu-id="0fbb8-120">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="0fbb8-120">-Reimage</span></span>
<span data-ttu-id="0fbb8-121">Указывает на то, что командлет переобразует VMSS.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-121">Indicates that the cmdlet reimages the VMSS.</span></span>

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

### <span data-ttu-id="0fbb8-122">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="0fbb8-122">-ReimageAll</span></span>
<span data-ttu-id="0fbb8-123">Указывает на то, что командлет переобразовать все диски в VMSS.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-123">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

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

### <span data-ttu-id="0fbb8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbb8-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fbb8-125">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-125">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="0fbb8-126">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="0fbb8-126">-VMScaleSetName</span></span>
<span data-ttu-id="0fbb8-127">Форель имя VMSS, для которого этот командлет задает действия.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-127">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

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

### <span data-ttu-id="0fbb8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fbb8-128">-Confirm</span></span>
<span data-ttu-id="0fbb8-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fbb8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fbb8-130">-WhatIf</span></span>
<span data-ttu-id="0fbb8-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fbb8-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fbb8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbb8-133">CommonParameters</span></span>
<span data-ttu-id="0fbb8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbb8-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fbb8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbb8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0fbb8-136">INPUTS</span></span>

### <span data-ttu-id="0fbb8-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="0fbb8-137">None</span></span>
<span data-ttu-id="0fbb8-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0fbb8-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0fbb8-139">OUTPUTS</span></span>

### <span data-ttu-id="0fbb8-140">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="0fbb8-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0fbb8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="0fbb8-141">NOTES</span></span>

## <span data-ttu-id="0fbb8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0fbb8-142">RELATED LINKS</span></span>

[<span data-ttu-id="0fbb8-143">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0fbb8-143">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="0fbb8-144">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0fbb8-144">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="0fbb8-145">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0fbb8-145">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="0fbb8-146">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0fbb8-146">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="0fbb8-147">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0fbb8-147">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="0fbb8-148">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0fbb8-148">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="0fbb8-149">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="0fbb8-149">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


