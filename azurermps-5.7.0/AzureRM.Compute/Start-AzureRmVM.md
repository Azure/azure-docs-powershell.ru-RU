---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 7b9e6aa5a9879e0f7abb281810d80a6900198ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732745"
---
# <span data-ttu-id="20f29-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="20f29-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="20f29-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20f29-102">SYNOPSIS</span></span>
<span data-ttu-id="20f29-103">Запуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="20f29-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20f29-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20f29-104">SYNTAX</span></span>

### <span data-ttu-id="20f29-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="20f29-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20f29-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="20f29-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20f29-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20f29-107">DESCRIPTION</span></span>
<span data-ttu-id="20f29-108">Командлет **Start-AzureRmVM** запускает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="20f29-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="20f29-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20f29-109">EXAMPLES</span></span>

### <span data-ttu-id="20f29-110">Пример 1: Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="20f29-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="20f29-111">Эта команда запускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="20f29-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="20f29-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20f29-112">PARAMETERS</span></span>

### <span data-ttu-id="20f29-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20f29-113">-AsJob</span></span>
<span data-ttu-id="20f29-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="20f29-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="20f29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20f29-115">-DefaultProfile</span></span>
<span data-ttu-id="20f29-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20f29-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20f29-117">-ID</span><span class="sxs-lookup"><span data-stu-id="20f29-117">-Id</span></span>
<span data-ttu-id="20f29-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="20f29-118">The resource group name.</span></span>

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

### <span data-ttu-id="20f29-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20f29-119">-Name</span></span>
<span data-ttu-id="20f29-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="20f29-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="20f29-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20f29-121">-ResourceGroupName</span></span>
<span data-ttu-id="20f29-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="20f29-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="20f29-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="20f29-123">-Confirm</span></span>
<span data-ttu-id="20f29-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="20f29-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20f29-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20f29-125">-WhatIf</span></span>
<span data-ttu-id="20f29-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="20f29-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20f29-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="20f29-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20f29-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20f29-128">CommonParameters</span></span>
<span data-ttu-id="20f29-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20f29-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20f29-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20f29-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20f29-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20f29-131">INPUTS</span></span>

### <span data-ttu-id="20f29-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="20f29-132">None</span></span>
<span data-ttu-id="20f29-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="20f29-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20f29-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20f29-134">OUTPUTS</span></span>

### <span data-ttu-id="20f29-135">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="20f29-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="20f29-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="20f29-136">NOTES</span></span>

## <span data-ttu-id="20f29-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20f29-137">RELATED LINKS</span></span>

[<span data-ttu-id="20f29-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="20f29-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="20f29-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="20f29-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="20f29-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="20f29-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="20f29-141">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="20f29-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="20f29-142">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="20f29-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="20f29-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="20f29-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


