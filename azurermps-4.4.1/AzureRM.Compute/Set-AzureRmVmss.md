---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 6442E5BB-D59D-483B-8AC5-2586C6C1E925
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVmss.md
ms.openlocfilehash: efb24aa4f8770e1911b9bf85a1fbf4dd366ea34d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557796"
---
# <span data-ttu-id="e0958-101">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0958-101">Set-AzureRmVmss</span></span>

## <span data-ttu-id="e0958-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e0958-102">SYNOPSIS</span></span>
<span data-ttu-id="e0958-103">Задает определенные действия в указанном VMSS.</span><span class="sxs-lookup"><span data-stu-id="e0958-103">Sets specific actions on a specified VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0958-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e0958-104">SYNTAX</span></span>

### <span data-ttu-id="e0958-105">DefaultParameter (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e0958-105">DefaultParameter (Default)</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-Reimage]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e0958-106">FriendMethod</span><span class="sxs-lookup"><span data-stu-id="e0958-106">FriendMethod</span></span>
```
Set-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-ReimageAll] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0958-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0958-107">DESCRIPTION</span></span>
<span data-ttu-id="e0958-108">Командлет **Set-AzureRmVmss** задает определенные действия в наборе масштабов виртуальных машин (VMSS).</span><span class="sxs-lookup"><span data-stu-id="e0958-108">The **Set-AzureRmVmss** cmdlet sets specific actions on the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="e0958-109">Единственным действием, поддерживаемым этим командлетом, является переобраз.</span><span class="sxs-lookup"><span data-stu-id="e0958-109">The only action this cmdlet supports is Reimage.</span></span>

## <span data-ttu-id="e0958-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e0958-110">EXAMPLES</span></span>

### <span data-ttu-id="e0958-111">Пример 1: переизображение VMSS</span><span class="sxs-lookup"><span data-stu-id="e0958-111">Example 1: Reimage a VMSS</span></span>
```
PS C:\> Set-AzureRmVmss -Reimage -ResourceGroupName "ContosoGroup" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="e0958-112">Эта команда позволяет переобразировать VMSS с именем ContosoVMSS, которое принадлежит группе ресурсов с именем ContosoGroup.</span><span class="sxs-lookup"><span data-stu-id="e0958-112">This command reimages the VMSS named ContosoVMSS that belongs to the resource group named ContosoGroup.</span></span>

## <span data-ttu-id="e0958-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e0958-113">PARAMETERS</span></span>

### <span data-ttu-id="e0958-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0958-114">-DefaultProfile</span></span>
<span data-ttu-id="e0958-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e0958-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0958-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="e0958-116">-InstanceId</span></span>
<span data-ttu-id="e0958-117">Идентификатор экземпляра виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="e0958-117">The instance ID of the virtual machine.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-118">-Повторное изображение</span><span class="sxs-lookup"><span data-stu-id="e0958-118">-Reimage</span></span>
<span data-ttu-id="e0958-119">Указывает на то, что командлет переобразует VMSS.</span><span class="sxs-lookup"><span data-stu-id="e0958-119">Indicates that the cmdlet reimages the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DefaultParameter
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-120">-ReimageAll</span><span class="sxs-lookup"><span data-stu-id="e0958-120">-ReimageAll</span></span>
<span data-ttu-id="e0958-121">Указывает на то, что командлет переобразовать все диски в VMSS.</span><span class="sxs-lookup"><span data-stu-id="e0958-121">Indicates that the cmdlet reimages all the disks in the VMSS.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FriendMethod
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0958-122">-ResourceGroupName</span></span>
<span data-ttu-id="e0958-123">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="e0958-123">Specifies the name of the resource group of the VMSS.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-124">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="e0958-124">-VMScaleSetName</span></span>
<span data-ttu-id="e0958-125">Форель имя VMSS, для которого этот командлет задает действия.</span><span class="sxs-lookup"><span data-stu-id="e0958-125">Species the name of the VMSS for which this cmdlet sets actions on.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e0958-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0958-126">-Confirm</span></span>
<span data-ttu-id="e0958-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e0958-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0958-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0958-128">-WhatIf</span></span>
<span data-ttu-id="e0958-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e0958-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e0958-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e0958-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0958-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0958-131">CommonParameters</span></span>
<span data-ttu-id="e0958-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e0958-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0958-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0958-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0958-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e0958-134">INPUTS</span></span>

## <span data-ttu-id="e0958-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e0958-135">OUTPUTS</span></span>

### <span data-ttu-id="e0958-136">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="e0958-136">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="e0958-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="e0958-137">NOTES</span></span>

## <span data-ttu-id="e0958-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e0958-138">RELATED LINKS</span></span>

[<span data-ttu-id="e0958-139">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0958-139">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="e0958-140">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0958-140">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="e0958-141">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0958-141">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="e0958-142">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0958-142">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="e0958-143">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0958-143">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="e0958-144">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0958-144">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="e0958-145">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="e0958-145">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


