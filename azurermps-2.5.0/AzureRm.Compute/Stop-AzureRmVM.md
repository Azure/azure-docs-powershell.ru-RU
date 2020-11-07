---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/stop-azurermvm
schema: 2.0.0
ms.openlocfilehash: 4bf5ec5ccdbe79f5557cb2f400fbcc0b9baf5e5a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915370"
---
# <span data-ttu-id="38e0b-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="38e0b-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="38e0b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="38e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="38e0b-103">Остановка виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="38e0b-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38e0b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="38e0b-104">SYNTAX</span></span>

### <span data-ttu-id="38e0b-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="38e0b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="38e0b-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="38e0b-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38e0b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="38e0b-107">DESCRIPTION</span></span>
<span data-ttu-id="38e0b-108">Командлет **Stop-AzureRmVM** останавливает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="38e0b-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="38e0b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="38e0b-109">EXAMPLES</span></span>

### <span data-ttu-id="38e0b-110">Пример 1: остановка виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="38e0b-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="38e0b-111">Эта команда останавливает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="38e0b-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="38e0b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="38e0b-112">PARAMETERS</span></span>

### <span data-ttu-id="38e0b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="38e0b-113">-AsJob</span></span>
<span data-ttu-id="38e0b-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="38e0b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="38e0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38e0b-115">-DefaultProfile</span></span>
<span data-ttu-id="38e0b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="38e0b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38e0b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="38e0b-117">-Force</span></span>
<span data-ttu-id="38e0b-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="38e0b-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="38e0b-119">-ID</span><span class="sxs-lookup"><span data-stu-id="38e0b-119">-Id</span></span>
<span data-ttu-id="38e0b-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="38e0b-120">The resource group name.</span></span>

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

### <span data-ttu-id="38e0b-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="38e0b-121">-Name</span></span>
<span data-ttu-id="38e0b-122">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="38e0b-122">The virtual machine name.</span></span>

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

### <span data-ttu-id="38e0b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38e0b-123">-ResourceGroupName</span></span>
<span data-ttu-id="38e0b-124">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="38e0b-124">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="38e0b-125">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="38e0b-125">-StayProvisioned</span></span>
<span data-ttu-id="38e0b-126">Командлет останавливает все виртуальные машины в VMSS, но не освобождает их.</span><span class="sxs-lookup"><span data-stu-id="38e0b-126">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="38e0b-127">Учетная запись оплачивается для остановленных виртуальных машин.</span><span class="sxs-lookup"><span data-stu-id="38e0b-127">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="38e0b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="38e0b-128">-Confirm</span></span>
<span data-ttu-id="38e0b-129">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="38e0b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38e0b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38e0b-130">-WhatIf</span></span>
<span data-ttu-id="38e0b-131">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="38e0b-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38e0b-132">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="38e0b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38e0b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38e0b-133">CommonParameters</span></span>
<span data-ttu-id="38e0b-134">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="38e0b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38e0b-135">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38e0b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38e0b-136">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="38e0b-136">INPUTS</span></span>

### <span data-ttu-id="38e0b-137">Ничего</span><span class="sxs-lookup"><span data-stu-id="38e0b-137">None</span></span>
<span data-ttu-id="38e0b-138">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="38e0b-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38e0b-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="38e0b-139">OUTPUTS</span></span>

### <span data-ttu-id="38e0b-140">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="38e0b-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="38e0b-141">Пуск</span><span class="sxs-lookup"><span data-stu-id="38e0b-141">NOTES</span></span>

## <span data-ttu-id="38e0b-142">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="38e0b-142">RELATED LINKS</span></span>

[<span data-ttu-id="38e0b-143">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="38e0b-143">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="38e0b-144">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="38e0b-144">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="38e0b-145">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="38e0b-145">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="38e0b-146">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="38e0b-146">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="38e0b-147">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="38e0b-147">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="38e0b-148">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="38e0b-148">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


