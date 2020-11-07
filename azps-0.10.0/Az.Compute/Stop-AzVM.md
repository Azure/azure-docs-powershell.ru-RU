---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/stop-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Stop-AzVM.md
ms.openlocfilehash: c35326449678578492b5b8a7d4a3f5b8bff5a41d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910458"
---
# <span data-ttu-id="8a01a-101">Stop-AzVM</span><span class="sxs-lookup"><span data-stu-id="8a01a-101">Stop-AzVM</span></span>

## <span data-ttu-id="8a01a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8a01a-102">SYNOPSIS</span></span>
<span data-ttu-id="8a01a-103">Остановка виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="8a01a-103">Stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8a01a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8a01a-104">SYNTAX</span></span>

### <span data-ttu-id="8a01a-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="8a01a-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8a01a-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="8a01a-106">IdParameterSetName</span></span>
```
Stop-AzVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a01a-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a01a-107">DESCRIPTION</span></span>
<span data-ttu-id="8a01a-108">Командлет **Stop-AzVM** останавливает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="8a01a-108">The **Stop-AzVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="8a01a-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8a01a-109">EXAMPLES</span></span>

### <span data-ttu-id="8a01a-110">Пример 1: остановка виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="8a01a-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="8a01a-111">Эта команда останавливает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="8a01a-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="8a01a-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8a01a-112">PARAMETERS</span></span>

### <span data-ttu-id="8a01a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8a01a-113">-AsJob</span></span>
<span data-ttu-id="8a01a-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="8a01a-114">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a01a-115">-DefaultProfile</span></span>
<span data-ttu-id="8a01a-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8a01a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="8a01a-117">-Force</span></span>
<span data-ttu-id="8a01a-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="8a01a-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01a-119">-ID</span><span class="sxs-lookup"><span data-stu-id="8a01a-119">-Id</span></span>
<span data-ttu-id="8a01a-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="8a01a-120">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01a-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8a01a-121">-Name</span></span>
<span data-ttu-id="8a01a-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8a01a-122">The virtual machine name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a01a-123">-ResourceGroupName</span></span>
<span data-ttu-id="8a01a-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8a01a-124">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a01a-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="8a01a-125">-StayProvisioned</span></span>
<span data-ttu-id="8a01a-126">Командлет останавливает все виртуальные машины в VMSS, но не освобождает их.</span><span class="sxs-lookup"><span data-stu-id="8a01a-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="8a01a-127">Учетная запись оплачивается для остановленных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="8a01a-127">The account is charged for the stopped virtual machines.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8a01a-128">-Confirm</span></span>
<span data-ttu-id="8a01a-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="8a01a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a01a-130">-WhatIf</span></span>
<span data-ttu-id="8a01a-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="8a01a-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a01a-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="8a01a-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a01a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a01a-133">CommonParameters</span></span>
<span data-ttu-id="8a01a-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8a01a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a01a-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a01a-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a01a-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8a01a-136">INPUTS</span></span>

### <span data-ttu-id="8a01a-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="8a01a-137">None</span></span>
<span data-ttu-id="8a01a-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="8a01a-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8a01a-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8a01a-139">OUTPUTS</span></span>

### <span data-ttu-id="8a01a-140">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="8a01a-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="8a01a-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="8a01a-141">NOTES</span></span>

## <span data-ttu-id="8a01a-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8a01a-142">RELATED LINKS</span></span>

[<span data-ttu-id="8a01a-143">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8a01a-143">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8a01a-144">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="8a01a-144">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="8a01a-145">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="8a01a-145">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="8a01a-146">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="8a01a-146">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="8a01a-147">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="8a01a-147">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="8a01a-148">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8a01a-148">Update-AzVM</span></span>](./Update-AzVM.md)


