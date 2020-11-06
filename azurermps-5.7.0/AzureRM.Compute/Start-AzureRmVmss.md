---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 4c1bc282b4a5aa0bf8c324ec523b5c823ce3cd14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93565542"
---
# <span data-ttu-id="c19d6-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c19d6-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="c19d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c19d6-102">SYNOPSIS</span></span>
<span data-ttu-id="c19d6-103">Запускает VMSS или набор виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="c19d6-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c19d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c19d6-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c19d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c19d6-105">DESCRIPTION</span></span>
<span data-ttu-id="c19d6-106">Командлет **Start-AzureRmVmss** запускает все виртуальные машины в наборе масштабов виртуальных машин (VMSS) или наборе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c19d6-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="c19d6-107">Вы можете использовать параметр *InstanceId* для выбора набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c19d6-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="c19d6-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c19d6-108">EXAMPLES</span></span>

### <span data-ttu-id="c19d6-109">Пример 1: запуск определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="c19d6-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="c19d6-110">Эта команда запускает определенный набор виртуальных машин, указанный в массиве строк с ИД экземпляра, который принадлежит к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="c19d6-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="c19d6-111">Пример 2: запуск всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="c19d6-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="c19d6-112">Эта команда запускает все виртуальные машины, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="c19d6-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="c19d6-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c19d6-113">PARAMETERS</span></span>

### <span data-ttu-id="c19d6-114">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="c19d6-114">-InstanceId</span></span>
<span data-ttu-id="c19d6-115">Задает в качестве массива строк идентификатор или идентификаторы экземпляров, с которых начинается командлет.</span><span class="sxs-lookup"><span data-stu-id="c19d6-115">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="c19d6-116">Например: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="c19d6-116">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="c19d6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c19d6-117">-ResourceGroupName</span></span>
<span data-ttu-id="c19d6-118">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="c19d6-118">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="c19d6-119">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="c19d6-119">-VMScaleSetName</span></span>
<span data-ttu-id="c19d6-120">Указывает имя VMSS, который запускается этим командлетом для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="c19d6-120">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="c19d6-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c19d6-121">-Confirm</span></span>
<span data-ttu-id="c19d6-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c19d6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c19d6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c19d6-123">-WhatIf</span></span>
<span data-ttu-id="c19d6-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c19d6-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c19d6-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c19d6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c19d6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c19d6-126">CommonParameters</span></span>
<span data-ttu-id="c19d6-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c19d6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c19d6-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c19d6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c19d6-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c19d6-129">INPUTS</span></span>

### <span data-ttu-id="c19d6-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="c19d6-130">None</span></span>
<span data-ttu-id="c19d6-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c19d6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c19d6-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c19d6-132">OUTPUTS</span></span>

###  
<span data-ttu-id="c19d6-133">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="c19d6-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="c19d6-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="c19d6-134">NOTES</span></span>

## <span data-ttu-id="c19d6-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c19d6-135">RELATED LINKS</span></span>

[<span data-ttu-id="c19d6-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c19d6-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="c19d6-137">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c19d6-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="c19d6-138">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c19d6-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="c19d6-139">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c19d6-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="c19d6-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c19d6-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="c19d6-141">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c19d6-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="c19d6-142">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="c19d6-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


