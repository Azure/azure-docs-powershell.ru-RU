---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 6e733bfecea9a054bbab3794ca61778894c613fe
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94235645"
---
# <span data-ttu-id="ad6d8-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad6d8-101">Remove-AzVM</span></span>

## <span data-ttu-id="ad6d8-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ad6d8-103">Удаление виртуальной машины из Azure.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="ad6d8-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad6d8-104">SYNTAX</span></span>

### <span data-ttu-id="ad6d8-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad6d8-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad6d8-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ad6d8-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Force] [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad6d8-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad6d8-107">DESCRIPTION</span></span>
<span data-ttu-id="ad6d8-108">Командлет **Remove-AzVM** удаляет виртуальную машину из Azure.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="ad6d8-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad6d8-109">EXAMPLES</span></span>

### <span data-ttu-id="ad6d8-110">Пример 1: Удаление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="ad6d8-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ad6d8-111">Эта команда удаляет виртуальную машину с именем VirtualMachine07 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="ad6d8-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad6d8-112">PARAMETERS</span></span>

### <span data-ttu-id="ad6d8-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad6d8-113">-AsJob</span></span>
<span data-ttu-id="ad6d8-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ad6d8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad6d8-115">-DefaultProfile</span></span>
<span data-ttu-id="ad6d8-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad6d8-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ad6d8-117">-Force</span></span>
<span data-ttu-id="ad6d8-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d8-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ad6d8-119">-Id</span></span>
<span data-ttu-id="ad6d8-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-120">The resource group name.</span></span>

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

### <span data-ttu-id="ad6d8-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad6d8-121">-Name</span></span>
<span data-ttu-id="ad6d8-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d8-123">-Wait</span><span class="sxs-lookup"><span data-stu-id="ad6d8-123">-NoWait</span></span>
<span data-ttu-id="ad6d8-124">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-124">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="ad6d8-125">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-125">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="ad6d8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad6d8-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad6d8-127">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-127">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad6d8-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad6d8-128">-Confirm</span></span>
<span data-ttu-id="ad6d8-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad6d8-130">-WhatIf</span></span>
<span data-ttu-id="ad6d8-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad6d8-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad6d8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad6d8-133">CommonParameters</span></span>
<span data-ttu-id="ad6d8-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad6d8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad6d8-135">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ad6d8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad6d8-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad6d8-136">INPUTS</span></span>

### <span data-ttu-id="ad6d8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ad6d8-137">System.String</span></span>

## <span data-ttu-id="ad6d8-138">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad6d8-138">OUTPUTS</span></span>

### <span data-ttu-id="ad6d8-139">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ad6d8-139">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="ad6d8-140">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ad6d8-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ad6d8-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad6d8-141">NOTES</span></span>

## <span data-ttu-id="ad6d8-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad6d8-142">RELATED LINKS</span></span>

[<span data-ttu-id="ad6d8-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad6d8-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ad6d8-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad6d8-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="ad6d8-145">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad6d8-145">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="ad6d8-146">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad6d8-146">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="ad6d8-147">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad6d8-147">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="ad6d8-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad6d8-148">Update-AzVM</span></span>](./Update-AzVM.md)

