---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 46e6e29b9a79fb5a8273fb3872d09e2cd290accd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98402612"
---
# <span data-ttu-id="54340-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="54340-101">Stop-AzVM</span></span>

## <span data-ttu-id="54340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54340-102">SYNOPSIS</span></span>
<span data-ttu-id="54340-103">Остановка виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="54340-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="54340-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="54340-104">SYNTAX</span></span>

### <span data-ttu-id="54340-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="54340-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-ResourceGroupName] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="54340-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="54340-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Force] [-StayProvisioned] [-NoWait] [-SkipShutdown] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54340-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="54340-107">DESCRIPTION</span></span>
<span data-ttu-id="54340-108">Для остановки виртуальной машины Azure будет останавливаться **cmdlet Stop-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="54340-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="54340-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="54340-109">EXAMPLES</span></span>

### <span data-ttu-id="54340-110">Пример 1. Остановка виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="54340-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="54340-111">Эта команда останавливает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="54340-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="54340-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54340-112">PARAMETERS</span></span>

### <span data-ttu-id="54340-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54340-113">-AsJob</span></span>
<span data-ttu-id="54340-114">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="54340-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="54340-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54340-115">-DefaultProfile</span></span>
<span data-ttu-id="54340-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="54340-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54340-117">-Force</span><span class="sxs-lookup"><span data-stu-id="54340-117">-Force</span></span>
<span data-ttu-id="54340-118">Запуск команды без запроса подтверждения.</span><span class="sxs-lookup"><span data-stu-id="54340-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="54340-119">-Id</span><span class="sxs-lookup"><span data-stu-id="54340-119">-Id</span></span>
<span data-ttu-id="54340-120">ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="54340-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="54340-121">-Name</span><span class="sxs-lookup"><span data-stu-id="54340-121">-Name</span></span>
<span data-ttu-id="54340-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="54340-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="54340-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="54340-123">-NoWait</span></span>
<span data-ttu-id="54340-124">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="54340-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="54340-125">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="54340-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="54340-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54340-126">-ResourceGroupName</span></span>
<span data-ttu-id="54340-127">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="54340-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="54340-128">-SkipShutdown</span><span class="sxs-lookup"><span data-stu-id="54340-128">-SkipShutdown</span></span>
<span data-ttu-id="54340-129">Чтобы запросить неявное завершение работы VM при его условии,</span><span class="sxs-lookup"><span data-stu-id="54340-129">To request non-graceful VM shutdown when keeping the VM provisioned.</span></span>

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

### <span data-ttu-id="54340-130">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="54340-130">-StayProvisioned</span></span>
<span data-ttu-id="54340-131">Он останавливает все виртуальные машины в VMSS, но не занимается их поиском.</span><span class="sxs-lookup"><span data-stu-id="54340-131">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="54340-132">С учетной записи взимается плата за остановленные виртуальные машины.</span><span class="sxs-lookup"><span data-stu-id="54340-132">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="54340-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="54340-133">-Confirm</span></span>
<span data-ttu-id="54340-134">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54340-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54340-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54340-135">-WhatIf</span></span>
<span data-ttu-id="54340-136">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54340-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="54340-137">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="54340-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54340-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54340-138">CommonParameters</span></span>
<span data-ttu-id="54340-139">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54340-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54340-140">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="54340-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54340-141">INPUTS</span><span class="sxs-lookup"><span data-stu-id="54340-141">INPUTS</span></span>

### <span data-ttu-id="54340-142">System.String</span><span class="sxs-lookup"><span data-stu-id="54340-142">System.String</span></span>

## <span data-ttu-id="54340-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="54340-143">OUTPUTS</span></span>

### <span data-ttu-id="54340-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="54340-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="54340-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="54340-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="54340-146">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="54340-146">NOTES</span></span>

## <span data-ttu-id="54340-147">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="54340-147">RELATED LINKS</span></span>

[<span data-ttu-id="54340-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="54340-148">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="54340-149">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="54340-149">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="54340-150">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="54340-150">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="54340-151">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="54340-151">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="54340-152">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="54340-152">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="54340-153">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="54340-153">Update-AzVM</span></span>](./Update-AzVM.md)


