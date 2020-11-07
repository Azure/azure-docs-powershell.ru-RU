---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
ms.openlocfilehash: 04110cb46d3f0ed0e5e09e6b12544b927cf6ae25
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914146"
---
# <span data-ttu-id="6d9f7-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d9f7-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="6d9f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d9f7-102">SYNOPSIS</span></span>
<span data-ttu-id="6d9f7-103">Запуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6d9f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d9f7-104">SYNTAX</span></span>

### <span data-ttu-id="6d9f7-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6d9f7-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d9f7-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="6d9f7-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d9f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d9f7-107">DESCRIPTION</span></span>
<span data-ttu-id="6d9f7-108">Командлет **Start-AzureRmVM** запускает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="6d9f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d9f7-109">EXAMPLES</span></span>

### <span data-ttu-id="6d9f7-110">Пример 1: Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6d9f7-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="6d9f7-111">Эта команда запускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="6d9f7-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d9f7-112">PARAMETERS</span></span>

### <span data-ttu-id="6d9f7-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d9f7-113">-AsJob</span></span>
<span data-ttu-id="6d9f7-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="6d9f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d9f7-115">-DefaultProfile</span></span>
<span data-ttu-id="6d9f7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d9f7-117">-ID</span><span class="sxs-lookup"><span data-stu-id="6d9f7-117">-Id</span></span>
<span data-ttu-id="6d9f7-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-118">The resource group name.</span></span>

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

### <span data-ttu-id="6d9f7-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6d9f7-119">-Name</span></span>
<span data-ttu-id="6d9f7-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="6d9f7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d9f7-121">-ResourceGroupName</span></span>
<span data-ttu-id="6d9f7-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6d9f7-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d9f7-123">-Confirm</span></span>
<span data-ttu-id="6d9f7-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d9f7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d9f7-125">-WhatIf</span></span>
<span data-ttu-id="6d9f7-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6d9f7-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d9f7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d9f7-128">CommonParameters</span></span>
<span data-ttu-id="6d9f7-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d9f7-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d9f7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d9f7-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d9f7-131">INPUTS</span></span>

### <span data-ttu-id="6d9f7-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="6d9f7-132">None</span></span>
<span data-ttu-id="6d9f7-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="6d9f7-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6d9f7-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d9f7-134">OUTPUTS</span></span>

### <span data-ttu-id="6d9f7-135">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="6d9f7-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="6d9f7-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d9f7-136">NOTES</span></span>

## <span data-ttu-id="6d9f7-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d9f7-137">RELATED LINKS</span></span>

[<span data-ttu-id="6d9f7-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d9f7-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="6d9f7-139">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d9f7-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="6d9f7-140">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d9f7-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="6d9f7-141">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d9f7-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="6d9f7-142">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d9f7-142">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="6d9f7-143">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6d9f7-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


