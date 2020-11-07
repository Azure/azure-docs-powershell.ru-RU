---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 5a7f03cbd4fdac75743fed491697ac2bb4ff6dac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901205"
---
# <span data-ttu-id="9e17b-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e17b-101">Remove-AzVM</span></span>

## <span data-ttu-id="9e17b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9e17b-102">SYNOPSIS</span></span>
<span data-ttu-id="9e17b-103">Удаление виртуальной машины из Azure.</span><span class="sxs-lookup"><span data-stu-id="9e17b-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="9e17b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9e17b-104">SYNTAX</span></span>

### <span data-ttu-id="9e17b-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9e17b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9e17b-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="9e17b-106">IdParameterSetName</span></span>
```
Remove-AzVM [[-Name] <String>] [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9e17b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e17b-107">DESCRIPTION</span></span>
<span data-ttu-id="9e17b-108">Командлет **Remove-AzVM** удаляет виртуальную машину из Azure.</span><span class="sxs-lookup"><span data-stu-id="9e17b-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="9e17b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9e17b-109">EXAMPLES</span></span>

### <span data-ttu-id="9e17b-110">Пример 1: Удаление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="9e17b-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="9e17b-111">Эта команда удаляет виртуальную машину с именем VirtualMachine07 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="9e17b-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="9e17b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9e17b-112">PARAMETERS</span></span>

### <span data-ttu-id="9e17b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9e17b-113">-AsJob</span></span>
<span data-ttu-id="9e17b-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="9e17b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="9e17b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e17b-115">-DefaultProfile</span></span>
<span data-ttu-id="9e17b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9e17b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9e17b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9e17b-117">-Force</span></span>
<span data-ttu-id="9e17b-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="9e17b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9e17b-119">-ID</span><span class="sxs-lookup"><span data-stu-id="9e17b-119">-Id</span></span>
<span data-ttu-id="9e17b-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e17b-120">The resource group name.</span></span>

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

### <span data-ttu-id="9e17b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="9e17b-121">-Name</span></span>
<span data-ttu-id="9e17b-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="9e17b-122">The resource name.</span></span>

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

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: ResourceName, VMName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9e17b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9e17b-123">-ResourceGroupName</span></span>
<span data-ttu-id="9e17b-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="9e17b-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9e17b-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9e17b-125">-Confirm</span></span>
<span data-ttu-id="9e17b-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9e17b-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9e17b-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9e17b-127">-WhatIf</span></span>
<span data-ttu-id="9e17b-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9e17b-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9e17b-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9e17b-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9e17b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e17b-130">CommonParameters</span></span>
<span data-ttu-id="9e17b-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9e17b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e17b-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e17b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e17b-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9e17b-133">INPUTS</span></span>

### <span data-ttu-id="9e17b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="9e17b-134">System.String</span></span>

## <span data-ttu-id="9e17b-135">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9e17b-135">OUTPUTS</span></span>

### <span data-ttu-id="9e17b-136">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="9e17b-136">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="9e17b-137">Пуск</span><span class="sxs-lookup"><span data-stu-id="9e17b-137">NOTES</span></span>

## <span data-ttu-id="9e17b-138">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9e17b-138">RELATED LINKS</span></span>

[<span data-ttu-id="9e17b-139">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e17b-139">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9e17b-140">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e17b-140">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="9e17b-141">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e17b-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="9e17b-142">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e17b-142">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="9e17b-143">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e17b-143">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="9e17b-144">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="9e17b-144">Update-AzVM</span></span>](./Update-AzVM.md)


