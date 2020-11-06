---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvmss
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 131fec8efa9075640d367726e5178caa54b9402a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93556763"
---
# <span data-ttu-id="a5c87-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a5c87-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="a5c87-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a5c87-102">SYNOPSIS</span></span>
<span data-ttu-id="a5c87-103">Запускает VMSS или набор виртуальных машин в VMSS.</span><span class="sxs-lookup"><span data-stu-id="a5c87-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5c87-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a5c87-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5c87-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5c87-105">DESCRIPTION</span></span>
<span data-ttu-id="a5c87-106">Командлет **Start-AzureRmVmss** запускает все виртуальные машины в наборе масштабов виртуальных машин (VMSS) или наборе виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="a5c87-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="a5c87-107">Вы можете использовать параметр *InstanceId* для выбора набора виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="a5c87-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="a5c87-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a5c87-108">EXAMPLES</span></span>

### <span data-ttu-id="a5c87-109">Пример 1: запуск определенного набора виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="a5c87-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="a5c87-110">Эта команда запускает определенный набор виртуальных машин, указанный в массиве строк с ИД экземпляра, который принадлежит к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="a5c87-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="a5c87-111">Пример 2: запуск всех виртуальных машин в VMSS</span><span class="sxs-lookup"><span data-stu-id="a5c87-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="a5c87-112">Эта команда запускает все виртуальные машины, которые принадлежат к VMSS с именем ContosoVMSS.</span><span class="sxs-lookup"><span data-stu-id="a5c87-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="a5c87-113">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a5c87-113">PARAMETERS</span></span>

### <span data-ttu-id="a5c87-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5c87-114">-AsJob</span></span>
<span data-ttu-id="a5c87-115">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="a5c87-115">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a5c87-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5c87-116">-DefaultProfile</span></span>
<span data-ttu-id="a5c87-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a5c87-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5c87-118">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="a5c87-118">-InstanceId</span></span>
<span data-ttu-id="a5c87-119">Задает в качестве массива строк идентификатор или идентификаторы экземпляров, с которых начинается командлет.</span><span class="sxs-lookup"><span data-stu-id="a5c87-119">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="a5c87-120">Например: `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="a5c87-120">For instance: `-InstanceId "0", "3"`</span></span>

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

### <span data-ttu-id="a5c87-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5c87-121">-ResourceGroupName</span></span>
<span data-ttu-id="a5c87-122">Указывает имя группы ресурсов для VMSS.</span><span class="sxs-lookup"><span data-stu-id="a5c87-122">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="a5c87-123">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="a5c87-123">-VMScaleSetName</span></span>
<span data-ttu-id="a5c87-124">Указывает имя VMSS, который запускается этим командлетом для виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="a5c87-124">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

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

### <span data-ttu-id="a5c87-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5c87-125">-Confirm</span></span>
<span data-ttu-id="a5c87-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="a5c87-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5c87-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5c87-127">-WhatIf</span></span>
<span data-ttu-id="a5c87-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="a5c87-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5c87-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="a5c87-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5c87-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5c87-130">CommonParameters</span></span>
<span data-ttu-id="a5c87-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a5c87-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5c87-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5c87-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5c87-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a5c87-133">INPUTS</span></span>

### <span data-ttu-id="a5c87-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a5c87-134">System.String</span></span>

### <span data-ttu-id="a5c87-135">System. String []</span><span class="sxs-lookup"><span data-stu-id="a5c87-135">System.String[]</span></span>

## <span data-ttu-id="a5c87-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a5c87-136">OUTPUTS</span></span>

### <span data-ttu-id="a5c87-137">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="a5c87-137">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="a5c87-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="a5c87-138">NOTES</span></span>

## <span data-ttu-id="a5c87-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a5c87-139">RELATED LINKS</span></span>

[<span data-ttu-id="a5c87-140">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a5c87-140">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="a5c87-141">New-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a5c87-141">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="a5c87-142">Remove-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a5c87-142">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="a5c87-143">Restarting-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a5c87-143">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="a5c87-144">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a5c87-144">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="a5c87-145">Остановить-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a5c87-145">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="a5c87-146">Update-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="a5c87-146">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


