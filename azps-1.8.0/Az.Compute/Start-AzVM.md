---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: 84e24bdcd69a3100e3030e6d1947240494aea8e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93731215"
---
# <span data-ttu-id="0a5f1-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a5f1-101">Start-AzVM</span></span>

## <span data-ttu-id="0a5f1-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0a5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="0a5f1-103">Запуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="0a5f1-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0a5f1-104">SYNTAX</span></span>

### <span data-ttu-id="0a5f1-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0a5f1-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a5f1-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0a5f1-106">IdParameterSetName</span></span>
```
Start-AzVM [[-Name] <String>] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a5f1-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a5f1-107">DESCRIPTION</span></span>
<span data-ttu-id="0a5f1-108">Командлет **Start-AzVM** запускает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="0a5f1-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0a5f1-109">EXAMPLES</span></span>

### <span data-ttu-id="0a5f1-110">Пример 1: Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="0a5f1-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="0a5f1-111">Эта команда запускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="0a5f1-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0a5f1-112">PARAMETERS</span></span>

### <span data-ttu-id="0a5f1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a5f1-113">-AsJob</span></span>
<span data-ttu-id="0a5f1-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="0a5f1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a5f1-115">-DefaultProfile</span></span>
<span data-ttu-id="0a5f1-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a5f1-117">-ID</span><span class="sxs-lookup"><span data-stu-id="0a5f1-117">-Id</span></span>
<span data-ttu-id="0a5f1-118">ИДЕНТИФИКАТОР виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-118">The ID of the virtual machine.</span></span>

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

### <span data-ttu-id="0a5f1-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0a5f1-119">-Name</span></span>
<span data-ttu-id="0a5f1-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="0a5f1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a5f1-121">-ResourceGroupName</span></span>
<span data-ttu-id="0a5f1-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="0a5f1-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a5f1-123">-Confirm</span></span>
<span data-ttu-id="0a5f1-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a5f1-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a5f1-125">-WhatIf</span></span>
<span data-ttu-id="0a5f1-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a5f1-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a5f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a5f1-128">CommonParameters</span></span>
<span data-ttu-id="0a5f1-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0a5f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a5f1-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a5f1-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a5f1-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0a5f1-131">INPUTS</span></span>

### <span data-ttu-id="0a5f1-132">System. String</span><span class="sxs-lookup"><span data-stu-id="0a5f1-132">System.String</span></span>

## <span data-ttu-id="0a5f1-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0a5f1-133">OUTPUTS</span></span>

### <span data-ttu-id="0a5f1-134">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="0a5f1-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="0a5f1-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="0a5f1-135">NOTES</span></span>

## <span data-ttu-id="0a5f1-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0a5f1-136">RELATED LINKS</span></span>

[<span data-ttu-id="0a5f1-137">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a5f1-137">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="0a5f1-138">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a5f1-138">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="0a5f1-139">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a5f1-139">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="0a5f1-140">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a5f1-140">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="0a5f1-141">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a5f1-141">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="0a5f1-142">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="0a5f1-142">Update-AzVM</span></span>](./Update-AzVM.md)


