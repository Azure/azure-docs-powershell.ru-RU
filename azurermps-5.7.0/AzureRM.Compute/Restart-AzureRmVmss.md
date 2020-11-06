---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 47F0EE55-78C0-4C71-BD32-C7CB7B200DC3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Restart-AzureRmVmss.md
ms.openlocfilehash: 1bc6b2b3ceb7ed7f991c92e4b8f8b034c78d54d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568624"
---
# <span data-ttu-id="931b1-101">Restart-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="931b1-101">Restart-AzureRmVmss</span></span>

## <span data-ttu-id="931b1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="931b1-102">SYNOPSIS</span></span>
<span data-ttu-id="931b1-103">Перезапуск VMSS или виртуальной машины в VMSS.</span><span class="sxs-lookup"><span data-stu-id="931b1-103">Restarts the VMSS or a virtual machine within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="931b1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="931b1-104">SYNTAX</span></span>

```
Restart-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="931b1-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="931b1-105">DESCRIPTION</span></span>
<span data-ttu-id="931b1-106">Командлет **restarting-AzureRmVmss** перезапустит установленный для виртуальной машины (VMSS).</span><span class="sxs-lookup"><span data-stu-id="931b1-106">The **Restart-AzureRmVmss** cmdlet restarts the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="931b1-107">Этот командлет также можно использовать для перезапуска определенной виртуальной машины внутри VMSS с помощью параметра *InstanceId* .</span><span class="sxs-lookup"><span data-stu-id="931b1-107">This cmdlet can also be used to restart a specific virtual machine inside the VMSS by using the *InstanceId* parameter.</span></span>

## <span data-ttu-id="931b1-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="931b1-108">EXAMPLES</span></span>

### <span data-ttu-id="931b1-109">Пример 1: перезапуск VMSS</span><span class="sxs-lookup"><span data-stu-id="931b1-109">Example 1: Restart the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group001" -VMScaleSetName "VMSS001";
```

<span data-ttu-id="931b1-110">Эта команда перезапускает VMSS с именем VMSS001, который относится к группе ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="931b1-110">This command restarts the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

### <span data-ttu-id="931b1-111">Пример 2: перезагрузка определенной виртуальной машины в VMSS</span><span class="sxs-lookup"><span data-stu-id="931b1-111">Example 2: Restart a specific virtual machine within the VMSS</span></span>
```
PS C:\> Restart-AzureRmVmss -ResourceGroupName "Group004" -VMScaleSetName "VMSS001" -InstanceId "1"
```

<span data-ttu-id="931b1-112">Эта команда перезапускает виртуальную машину с ИДЕНТИФИКАТОРом 1 в VMSS с именем VMSS001, которая входит в группу ресурсов с именем Group001.</span><span class="sxs-lookup"><span data-stu-id="931b1-112">This command restarts a virtual machine that has the instance ID of 1 in the VMSS named VMSS001 that belongs to the resource group named Group001.</span></span>

## <span data-ttu-id="931b1-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="931b1-113">PARAMETERS</span></span>

### <span data-ttu-id="931b1-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="931b1-114">-InstanceId</span></span>
<span data-ttu-id="931b1-115">Задает в качестве строкового массива ИДЕНТИФИКАТОРы экземпляров, которые необходимо перезапустить.</span><span class="sxs-lookup"><span data-stu-id="931b1-115">Specifies, as a string array, the ID of the instances that need restarted.</span></span>

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

### <span data-ttu-id="931b1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="931b1-116">-ResourceGroupName</span></span>
<span data-ttu-id="931b1-117">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="931b1-117">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="931b1-118">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="931b1-118">-VMScaleSetName</span></span>
<span data-ttu-id="931b1-119">Форель имя VMSS, перезапускаемого командлетом.</span><span class="sxs-lookup"><span data-stu-id="931b1-119">Species the name of the VMSS that this cmdlet restarts.</span></span>

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

### <span data-ttu-id="931b1-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="931b1-120">-Confirm</span></span>
<span data-ttu-id="931b1-121">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="931b1-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="931b1-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="931b1-122">-WhatIf</span></span>
<span data-ttu-id="931b1-123">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="931b1-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="931b1-124">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="931b1-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="931b1-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="931b1-125">CommonParameters</span></span>
<span data-ttu-id="931b1-126">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="931b1-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="931b1-127">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="931b1-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="931b1-128">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="931b1-128">INPUTS</span></span>

### <span data-ttu-id="931b1-129">Ничего</span><span class="sxs-lookup"><span data-stu-id="931b1-129">None</span></span>
<span data-ttu-id="931b1-130">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="931b1-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="931b1-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="931b1-131">OUTPUTS</span></span>

###  
<span data-ttu-id="931b1-132">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="931b1-132">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="931b1-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="931b1-133">NOTES</span></span>

## <span data-ttu-id="931b1-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="931b1-134">RELATED LINKS</span></span>

[<span data-ttu-id="931b1-135">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="931b1-135">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="931b1-136">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="931b1-136">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="931b1-137">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="931b1-137">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="931b1-138">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="931b1-138">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="931b1-139">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="931b1-139">Start-AzureRmVmss</span></span>](./Start-AzureRmVmss.md)

[<span data-ttu-id="931b1-140">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="931b1-140">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="931b1-141">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="931b1-141">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


