---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVmss.md
ms.openlocfilehash: d3677191bb3a196b97dcb8ff6c5b62b4aafd3a8b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910464"
---
# <span data-ttu-id="aa9c5-101">Start-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aa9c5-101">Start-AzVmss</span></span>

## <span data-ttu-id="aa9c5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="aa9c5-102">SYNOPSIS</span></span>
<span data-ttu-id="aa9c5-103">Запускает VMSS или набор виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

## <span data-ttu-id="aa9c5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="aa9c5-104">SYNTAX</span></span>

```
Start-AzVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa9c5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa9c5-105">DESCRIPTION</span></span>
<span data-ttu-id="aa9c5-106">Командлет **Start-AzVmss** запускает все виртуальные машины в наборе масштабов виртуальных машин (VMSS) или наборе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-106">The **Start-AzVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="aa9c5-107">Вы можете использовать параметр *InstanceId* для выбора набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="aa9c5-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="aa9c5-108">EXAMPLES</span></span>

### <span data-ttu-id="aa9c5-109">Пример 1: запуск определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="aa9c5-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="aa9c5-110">Эта команда запускает определенный набор виртуальных машин, указанный в массиве строк с ИД экземпляра, который принадлежит к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="aa9c5-111">Пример 2: запуск всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="aa9c5-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="aa9c5-112">Эта команда запускает все виртуальные машины, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="aa9c5-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="aa9c5-113">PARAMETERS</span></span>

### <span data-ttu-id="aa9c5-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa9c5-114">-AsJob</span></span>
<span data-ttu-id="aa9c5-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="aa9c5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa9c5-116">-DefaultProfile</span></span>
<span data-ttu-id="aa9c5-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aa9c5-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="aa9c5-118">-InstanceId</span></span>
<span data-ttu-id="aa9c5-119">Задает в качестве массива строк идентификатор или идентификаторы экземпляров, с которых начинается командлет.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="aa9c5-120">Например: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="aa9c5-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="aa9c5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa9c5-121">-ResourceGroupName</span></span>
<span data-ttu-id="aa9c5-122">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="aa9c5-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="aa9c5-123">-VMScaleSetName</span></span>
<span data-ttu-id="aa9c5-124">Указывает имя VMSS, который запускается этим командлетом для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="aa9c5-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aa9c5-125">-Confirm</span></span>
<span data-ttu-id="aa9c5-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa9c5-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa9c5-127">-WhatIf</span></span>
<span data-ttu-id="aa9c5-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa9c5-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa9c5-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa9c5-130">CommonParameters</span></span>
<span data-ttu-id="aa9c5-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa9c5-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa9c5-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa9c5-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="aa9c5-133">INPUTS</span></span>

### <span data-ttu-id="aa9c5-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="aa9c5-134">None</span></span>
<span data-ttu-id="aa9c5-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="aa9c5-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="aa9c5-136">OUTPUTS</span></span>

###  
<span data-ttu-id="aa9c5-137">Этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-137">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="aa9c5-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="aa9c5-138">NOTES</span></span>

## <span data-ttu-id="aa9c5-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="aa9c5-139">RELATED LINKS</span></span>

[<span data-ttu-id="aa9c5-140">Get-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aa9c5-140">Get-AzVmss</span></span>](./Get-AzVmss.md)

[<span data-ttu-id="aa9c5-141">New-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aa9c5-141">New-AzVmss</span></span>](./New-AzVmss.md)

[<span data-ttu-id="aa9c5-142">Remove-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aa9c5-142">Remove-AzVmss</span></span>](./Remove-AzVmss.md)

[<span data-ttu-id="aa9c5-143">Restarting-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aa9c5-143">Restart-AzVmss</span></span>](./Restart-AzVmss.md)

[<span data-ttu-id="aa9c5-144">Set-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aa9c5-144">Set-AzVmss</span></span>](./Set-AzVmss.md)

[<span data-ttu-id="aa9c5-145">Остановить-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aa9c5-145">Stop-AzVmss</span></span>](./Stop-AzVmss.md)

[<span data-ttu-id="aa9c5-146">Update-AzVmss</span><span class="sxs-lookup"><span data-stu-id="aa9c5-146">Update-AzVmss</span></span>](./Update-AzVmss.md)


