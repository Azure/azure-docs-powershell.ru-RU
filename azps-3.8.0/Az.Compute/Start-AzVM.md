---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074605"
---
# <span data-ttu-id="8caa2-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="8caa2-101">Start-AzVM</span></span>

## <span data-ttu-id="8caa2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8caa2-102">SYNOPSIS</span></span>
<span data-ttu-id="8caa2-103">Запуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="8caa2-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="8caa2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8caa2-104">SYNTAX</span></span>

### <span data-ttu-id="8caa2-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8caa2-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8caa2-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8caa2-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8caa2-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8caa2-107">DESCRIPTION</span></span>
<span data-ttu-id="8caa2-108">Командлет **Start-AzVM** запускает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="8caa2-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="8caa2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8caa2-109">EXAMPLES</span></span>

### <span data-ttu-id="8caa2-110">Пример 1: Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="8caa2-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8caa2-111">Эта команда запускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8caa2-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8caa2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8caa2-112">PARAMETERS</span></span>

### <span data-ttu-id="8caa2-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8caa2-113">-AsJob</span></span>
<span data-ttu-id="8caa2-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="8caa2-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="8caa2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8caa2-115">-DefaultProfile</span></span>
<span data-ttu-id="8caa2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8caa2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8caa2-117">-ID</span><span class="sxs-lookup"><span data-stu-id="8caa2-117">-Id</span></span>
<span data-ttu-id="8caa2-118">ИДЕНТИФИКАТОР виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8caa2-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="8caa2-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8caa2-119">-Name</span></span>
<span data-ttu-id="8caa2-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8caa2-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="8caa2-121">-Wait</span><span class="sxs-lookup"><span data-stu-id="8caa2-121">-NoWait</span></span>
<span data-ttu-id="8caa2-122">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="8caa2-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="8caa2-123">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="8caa2-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="8caa2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8caa2-124">-ResourceGroupName</span></span>
<span data-ttu-id="8caa2-125">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8caa2-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8caa2-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8caa2-126">-Confirm</span></span>
<span data-ttu-id="8caa2-127">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8caa2-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8caa2-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8caa2-128">-WhatIf</span></span>
<span data-ttu-id="8caa2-129">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8caa2-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8caa2-130">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8caa2-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8caa2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8caa2-131">CommonParameters</span></span>
<span data-ttu-id="8caa2-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8caa2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8caa2-133">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8caa2-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8caa2-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8caa2-134">INPUTS</span></span>

### <span data-ttu-id="8caa2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8caa2-135">System.String</span></span>

## <span data-ttu-id="8caa2-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8caa2-136">OUTPUTS</span></span>

### <span data-ttu-id="8caa2-137">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8caa2-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="8caa2-138">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8caa2-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8caa2-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="8caa2-139">NOTES</span></span>

## <span data-ttu-id="8caa2-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8caa2-140">RELATED LINKS</span></span>

[<span data-ttu-id="8caa2-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8caa2-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8caa2-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8caa2-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="8caa2-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="8caa2-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="8caa2-144">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="8caa2-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="8caa2-145">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="8caa2-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="8caa2-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8caa2-146">Update-AzVM</span></span>](./Update-AzVM.md)


