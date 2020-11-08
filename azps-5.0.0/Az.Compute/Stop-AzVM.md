---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94246772"
---
# <span data-ttu-id="70a2d-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="70a2d-101">Stop-AzVM</span></span>

## <span data-ttu-id="70a2d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="70a2d-102">SYNOPSIS</span></span>
<span data-ttu-id="70a2d-103">Остановка виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="70a2d-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="70a2d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="70a2d-104">SYNTAX</span></span>

### <span data-ttu-id="70a2d-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="70a2d-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="70a2d-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="70a2d-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="70a2d-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="70a2d-107">DESCRIPTION</span></span>
<span data-ttu-id="70a2d-108">Командлет **Stop-AzVM** останавливает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="70a2d-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="70a2d-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="70a2d-109">EXAMPLES</span></span>

### <span data-ttu-id="70a2d-110">Пример 1: остановка виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="70a2d-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="70a2d-111">Эта команда останавливает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="70a2d-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="70a2d-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="70a2d-112">PARAMETERS</span></span>

### <span data-ttu-id="70a2d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="70a2d-113">-AsJob</span></span>
<span data-ttu-id="70a2d-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="70a2d-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="70a2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70a2d-115">-DefaultProfile</span></span>
<span data-ttu-id="70a2d-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="70a2d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70a2d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="70a2d-117">-Force</span></span>
<span data-ttu-id="70a2d-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="70a2d-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="70a2d-119">-ID</span><span class="sxs-lookup"><span data-stu-id="70a2d-119">-Id</span></span>
<span data-ttu-id="70a2d-120">ИДЕНТИФИКАТОР виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="70a2d-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="70a2d-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="70a2d-121">-Name</span></span>
<span data-ttu-id="70a2d-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="70a2d-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="70a2d-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="70a2d-123">-NoWait</span></span>
<span data-ttu-id="70a2d-124">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="70a2d-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="70a2d-125">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="70a2d-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="70a2d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="70a2d-126">-ResourceGroupName</span></span>
<span data-ttu-id="70a2d-127">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="70a2d-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="70a2d-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="70a2d-128">-SkipShutdown</span></span>
<span data-ttu-id="70a2d-129">Чтобы запросить отключение от некорректной виртуальной машины при сохранении подготовки виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="70a2d-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="70a2d-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="70a2d-130">-StayProvisioned</span></span>
<span data-ttu-id="70a2d-131">Командлет останавливает все виртуальные машины в VMSS, но не освобождает их.</span><span class="sxs-lookup"><span data-stu-id="70a2d-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="70a2d-132">Учетная запись оплачивается для остановленных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="70a2d-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="70a2d-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="70a2d-133">-Confirm</span></span>
<span data-ttu-id="70a2d-134">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="70a2d-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="70a2d-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="70a2d-135">-WhatIf</span></span>
<span data-ttu-id="70a2d-136">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="70a2d-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="70a2d-137">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="70a2d-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="70a2d-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70a2d-138">CommonParameters</span></span>
<span data-ttu-id="70a2d-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="70a2d-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70a2d-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="70a2d-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70a2d-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="70a2d-141">INPUTS</span></span>

### <span data-ttu-id="70a2d-142">System. String</span><span class="sxs-lookup"><span data-stu-id="70a2d-142">System.String</span></span>

## <span data-ttu-id="70a2d-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="70a2d-143">OUTPUTS</span></span>

### <span data-ttu-id="70a2d-144">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="70a2d-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="70a2d-145">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="70a2d-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="70a2d-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="70a2d-146">NOTES</span></span>

## <span data-ttu-id="70a2d-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="70a2d-147">RELATED LINKS</span></span>

[<span data-ttu-id="70a2d-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="70a2d-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="70a2d-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="70a2d-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="70a2d-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="70a2d-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="70a2d-151">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="70a2d-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="70a2d-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="70a2d-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="70a2d-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="70a2d-153">Update-AzVM</span></span>](./Update-AzVM.md)


