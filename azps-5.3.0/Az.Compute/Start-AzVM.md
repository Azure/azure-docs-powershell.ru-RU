---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 32e633d1f9fea877ef81b6c6e7ef5e8bb09da81a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98509009"
---
# <span data-ttu-id="bf2dd-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf2dd-101">Start-AzVM</span></span>

## <span data-ttu-id="bf2dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf2dd-102">SYNOPSIS</span></span>
<span data-ttu-id="bf2dd-103">Запускает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="bf2dd-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="bf2dd-104">SYNTAX</span></span>

### <span data-ttu-id="bf2dd-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="bf2dd-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-NoWait] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf2dd-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="bf2dd-106">IdParameterSetName</span></span>
```
Start-AzVM [-NoWait] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf2dd-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bf2dd-107">DESCRIPTION</span></span>
<span data-ttu-id="bf2dd-108">Для запуска виртуальной машины Запускается клиент **Start-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="bf2dd-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="bf2dd-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="bf2dd-109">EXAMPLES</span></span>

### <span data-ttu-id="bf2dd-110">Пример 1. Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="bf2dd-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="bf2dd-111">Эта команда запускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="bf2dd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf2dd-112">PARAMETERS</span></span>

### <span data-ttu-id="bf2dd-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf2dd-113">-AsJob</span></span>
<span data-ttu-id="bf2dd-114">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="bf2dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf2dd-115">-DefaultProfile</span></span>
<span data-ttu-id="bf2dd-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf2dd-117">-Id</span><span class="sxs-lookup"><span data-stu-id="bf2dd-117">-Id</span></span>
<span data-ttu-id="bf2dd-118">ИД виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="bf2dd-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bf2dd-119">-Name</span></span>
<span data-ttu-id="bf2dd-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="bf2dd-121">-NoWait</span><span class="sxs-lookup"><span data-stu-id="bf2dd-121">-NoWait</span></span>
<span data-ttu-id="bf2dd-122">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-122">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="bf2dd-123">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-123">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="bf2dd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf2dd-124">-ResourceGroupName</span></span>
<span data-ttu-id="bf2dd-125">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-125">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="bf2dd-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf2dd-126">-Confirm</span></span>
<span data-ttu-id="bf2dd-127">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf2dd-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf2dd-128">-WhatIf</span></span>
<span data-ttu-id="bf2dd-129">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bf2dd-130">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf2dd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf2dd-131">CommonParameters</span></span>
<span data-ttu-id="bf2dd-132">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf2dd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf2dd-133">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bf2dd-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf2dd-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="bf2dd-134">INPUTS</span></span>

### <span data-ttu-id="bf2dd-135">System.String</span><span class="sxs-lookup"><span data-stu-id="bf2dd-135">System.String</span></span>

## <span data-ttu-id="bf2dd-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="bf2dd-136">OUTPUTS</span></span>

### <span data-ttu-id="bf2dd-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="bf2dd-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="bf2dd-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="bf2dd-138">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="bf2dd-139">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="bf2dd-139">NOTES</span></span>

## <span data-ttu-id="bf2dd-140">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bf2dd-140">RELATED LINKS</span></span>

[<span data-ttu-id="bf2dd-141">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf2dd-141">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="bf2dd-142">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf2dd-142">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="bf2dd-143">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf2dd-143">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="bf2dd-144">Restart-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf2dd-144">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="bf2dd-145">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf2dd-145">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="bf2dd-146">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="bf2dd-146">Update-AzVM</span></span>](./Update-AzVM.md)


