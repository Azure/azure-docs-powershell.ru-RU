---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: d0895fc436f4f7d59a4d9f5b6cfc18574d7e8d9b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721646"
---
# <span data-ttu-id="2d99f-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d99f-101">Stop-AzVM</span></span>

## <span data-ttu-id="2d99f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d99f-102">SYNOPSIS</span></span>
<span data-ttu-id="2d99f-103">Остановка виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="2d99f-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="2d99f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d99f-104">SYNTAX</span></span>

### <span data-ttu-id="2d99f-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d99f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d99f-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2d99f-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d99f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d99f-107">DESCRIPTION</span></span>
<span data-ttu-id="2d99f-108">Командлет **Stop-AzVM** останавливает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="2d99f-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="2d99f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d99f-109">EXAMPLES</span></span>

### <span data-ttu-id="2d99f-110">Пример 1: остановка виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="2d99f-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2d99f-111">Эта команда останавливает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2d99f-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="2d99f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d99f-112">PARAMETERS</span></span>

### <span data-ttu-id="2d99f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d99f-113">-AsJob</span></span>
<span data-ttu-id="2d99f-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="2d99f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2d99f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d99f-115">-DefaultProfile</span></span>
<span data-ttu-id="2d99f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d99f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d99f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2d99f-117">-Force</span></span>
<span data-ttu-id="2d99f-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="2d99f-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2d99f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="2d99f-119">-Id</span></span>
<span data-ttu-id="2d99f-120">ИДЕНТИФИКАТОР виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d99f-120">The ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d99f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d99f-121">-Name</span></span>
<span data-ttu-id="2d99f-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d99f-122">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d99f-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="2d99f-123">-NoWait</span></span>
<span data-ttu-id="2d99f-124">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="2d99f-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2d99f-125">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="2d99f-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="2d99f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d99f-126">-ResourceGroupName</span></span>
<span data-ttu-id="2d99f-127">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d99f-127">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d99f-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="2d99f-128">-SkipShutdown</span></span>
<span data-ttu-id="2d99f-129">Чтобы запросить отключение от некорректной виртуальной машины при сохранении подготовки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d99f-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="2d99f-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="2d99f-130">-StayProvisioned</span></span>
<span data-ttu-id="2d99f-131">Командлет останавливает все виртуальные машины в VMSS, но не освобождает их.</span><span class="sxs-lookup"><span data-stu-id="2d99f-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="2d99f-132">Учетная запись оплачивается для остановленных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="2d99f-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="2d99f-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d99f-133">-Confirm</span></span>
<span data-ttu-id="2d99f-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d99f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d99f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d99f-135">-WhatIf</span></span>
<span data-ttu-id="2d99f-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d99f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d99f-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d99f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d99f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d99f-138">CommonParameters</span></span>
<span data-ttu-id="2d99f-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d99f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d99f-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d99f-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d99f-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d99f-141">INPUTS</span></span>

### <span data-ttu-id="2d99f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="2d99f-142">System.String</span></span>

## <span data-ttu-id="2d99f-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d99f-143">OUTPUTS</span></span>

### <span data-ttu-id="2d99f-144">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2d99f-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="2d99f-145">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2d99f-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2d99f-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d99f-146">NOTES</span></span>

## <span data-ttu-id="2d99f-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d99f-147">RELATED LINKS</span></span>

[<span data-ttu-id="2d99f-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d99f-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2d99f-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d99f-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="2d99f-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d99f-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="2d99f-151">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d99f-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="2d99f-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d99f-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="2d99f-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="2d99f-153">Update-AzVM</span></span>](./Update-AzVM.md)


