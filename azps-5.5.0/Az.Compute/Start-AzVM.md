---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100234724"
---
# <span data-ttu-id="fd102-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd102-101">Start-AzVM</span></span>

## <span data-ttu-id="fd102-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd102-102">SYNOPSIS</span></span>
<span data-ttu-id="fd102-103">Запускает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="fd102-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="fd102-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="fd102-104">SYNTAX</span></span>

### <span data-ttu-id="fd102-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="fd102-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd102-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="fd102-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd102-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd102-107">DESCRIPTION</span></span>
<span data-ttu-id="fd102-108">С **его использованием запускается** виртуальная машина Azure.</span><span class="sxs-lookup"><span data-stu-id="fd102-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="fd102-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="fd102-109">EXAMPLES</span></span>

### <span data-ttu-id="fd102-110">Пример 1. Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="fd102-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="fd102-111">Эта команда запускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="fd102-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="fd102-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd102-112">PARAMETERS</span></span>

### <span data-ttu-id="fd102-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fd102-113">-AsJob</span></span>
<span data-ttu-id="fd102-114">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="fd102-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="fd102-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd102-115">-DefaultProfile</span></span>
<span data-ttu-id="fd102-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd102-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd102-117">-Id</span><span class="sxs-lookup"><span data-stu-id="fd102-117">-Id</span></span>
<span data-ttu-id="fd102-118">ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd102-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="fd102-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fd102-119">-Name</span></span>
<span data-ttu-id="fd102-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd102-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="fd102-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fd102-121">-NoWait</span></span>
<span data-ttu-id="fd102-122">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="fd102-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="fd102-123">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="fd102-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="fd102-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd102-124">-ResourceGroupName</span></span>
<span data-ttu-id="fd102-125">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="fd102-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fd102-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd102-126">-Confirm</span></span>
<span data-ttu-id="fd102-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd102-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd102-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd102-128">-WhatIf</span></span>
<span data-ttu-id="fd102-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fd102-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd102-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="fd102-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd102-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd102-131">CommonParameters</span></span>
<span data-ttu-id="fd102-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fd102-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd102-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fd102-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd102-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="fd102-134">INPUTS</span></span>

### <span data-ttu-id="fd102-135">System.String</span><span class="sxs-lookup"><span data-stu-id="fd102-135">System.String</span></span>

## <span data-ttu-id="fd102-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="fd102-136">OUTPUTS</span></span>

### <span data-ttu-id="fd102-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="fd102-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="fd102-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="fd102-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="fd102-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="fd102-139">NOTES</span></span>

## <span data-ttu-id="fd102-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd102-140">RELATED LINKS</span></span>

[<span data-ttu-id="fd102-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd102-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="fd102-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd102-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="fd102-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd102-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="fd102-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd102-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="fd102-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd102-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="fd102-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="fd102-146">Update-AzVM</span></span>](./Update-AzVM.md)


