---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: 393f2a75217b95b6c1c5366326735ac0f78ac294
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901085"
---
# <span data-ttu-id="baaed-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="baaed-101">Stop-AzVM</span></span>

## <span data-ttu-id="baaed-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="baaed-102">SYNOPSIS</span></span>
<span data-ttu-id="baaed-103">Остановка виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="baaed-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="baaed-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="baaed-104">SYNTAX</span></span>

### <span data-ttu-id="baaed-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="baaed-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="baaed-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="baaed-106">IdParameterSetName</span></span>
```
Stop-AzVM [[-Name] <String>] [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="baaed-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="baaed-107">DESCRIPTION</span></span>
<span data-ttu-id="baaed-108">Командлет **Stop-AzVM** останавливает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="baaed-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="baaed-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="baaed-109">EXAMPLES</span></span>

### <span data-ttu-id="baaed-110">Пример 1: остановка виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="baaed-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="baaed-111">Эта команда останавливает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="baaed-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="baaed-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="baaed-112">PARAMETERS</span></span>

### <span data-ttu-id="baaed-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="baaed-113">-AsJob</span></span>
<span data-ttu-id="baaed-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="baaed-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="baaed-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="baaed-115">-DefaultProfile</span></span>
<span data-ttu-id="baaed-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="baaed-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="baaed-117">-Force</span><span class="sxs-lookup"><span data-stu-id="baaed-117">-Force</span></span>
<span data-ttu-id="baaed-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="baaed-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="baaed-119">-ID</span><span class="sxs-lookup"><span data-stu-id="baaed-119">-Id</span></span>
<span data-ttu-id="baaed-120">ИДЕНТИФИКАТОР виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="baaed-120">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="baaed-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="baaed-121">-Name</span></span>
<span data-ttu-id="baaed-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="baaed-122">The virtual machine name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="baaed-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="baaed-123">-ResourceGroupName</span></span>
<span data-ttu-id="baaed-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="baaed-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="baaed-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="baaed-125">-StayProvisioned</span></span>
<span data-ttu-id="baaed-126">Командлет останавливает все виртуальные машины в VMSS, но не освобождает их.</span><span class="sxs-lookup"><span data-stu-id="baaed-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="baaed-127">Учетная запись оплачивается для остановленных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="baaed-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="baaed-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="baaed-128">-Confirm</span></span>
<span data-ttu-id="baaed-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="baaed-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="baaed-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="baaed-130">-WhatIf</span></span>
<span data-ttu-id="baaed-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="baaed-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="baaed-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="baaed-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="baaed-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="baaed-133">CommonParameters</span></span>
<span data-ttu-id="baaed-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="baaed-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="baaed-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="baaed-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="baaed-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="baaed-136">INPUTS</span></span>

### <span data-ttu-id="baaed-137">System. String</span><span class="sxs-lookup"><span data-stu-id="baaed-137">System.String</span></span>

## <span data-ttu-id="baaed-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="baaed-138">OUTPUTS</span></span>

### <span data-ttu-id="baaed-139">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="baaed-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="baaed-140">Пуск</span><span class="sxs-lookup"><span data-stu-id="baaed-140">NOTES</span></span>

## <span data-ttu-id="baaed-141">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="baaed-141">RELATED LINKS</span></span>

[<span data-ttu-id="baaed-142">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="baaed-142">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="baaed-143">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="baaed-143">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="baaed-144">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="baaed-144">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="baaed-145">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="baaed-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="baaed-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="baaed-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="baaed-147">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="baaed-147">Update-AzVM</span></span>](./Update-AzVM.md)


