---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/start-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Start-AzVM.md
ms.openlocfilehash: e343b9e16f793a760166736edcef6658bde34723
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93910465"
---
# <span data-ttu-id="df463-101">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="df463-101">Start-AzVM</span></span>

## <span data-ttu-id="df463-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="df463-102">SYNOPSIS</span></span>
<span data-ttu-id="df463-103">Запуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="df463-103">Starts an Azure virtual machine.</span></span>

## <span data-ttu-id="df463-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="df463-104">SYNTAX</span></span>

### <span data-ttu-id="df463-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="df463-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df463-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="df463-106">IdParameterSetName</span></span>
```
Start-AzVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df463-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="df463-107">DESCRIPTION</span></span>
<span data-ttu-id="df463-108">Командлет **Start-AzVM** запускает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="df463-108">The **Start-AzVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="df463-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="df463-109">EXAMPLES</span></span>

### <span data-ttu-id="df463-110">Пример 1: Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="df463-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="df463-111">Эта команда запускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="df463-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="df463-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="df463-112">PARAMETERS</span></span>

### <span data-ttu-id="df463-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="df463-113">-AsJob</span></span>
<span data-ttu-id="df463-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="df463-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="df463-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df463-115">-DefaultProfile</span></span>
<span data-ttu-id="df463-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="df463-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df463-117">-ID</span><span class="sxs-lookup"><span data-stu-id="df463-117">-Id</span></span>
<span data-ttu-id="df463-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="df463-118">The resource group name.</span></span>

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

### <span data-ttu-id="df463-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="df463-119">-Name</span></span>
<span data-ttu-id="df463-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="df463-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="df463-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df463-121">-ResourceGroupName</span></span>
<span data-ttu-id="df463-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="df463-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="df463-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df463-123">-Confirm</span></span>
<span data-ttu-id="df463-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="df463-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df463-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df463-125">-WhatIf</span></span>
<span data-ttu-id="df463-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="df463-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df463-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="df463-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df463-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df463-128">CommonParameters</span></span>
<span data-ttu-id="df463-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="df463-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df463-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df463-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df463-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="df463-131">INPUTS</span></span>

### <span data-ttu-id="df463-132">Ничего</span><span class="sxs-lookup"><span data-stu-id="df463-132">None</span></span>
<span data-ttu-id="df463-133">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="df463-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="df463-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="df463-134">OUTPUTS</span></span>

### <span data-ttu-id="df463-135">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="df463-135">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="df463-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="df463-136">NOTES</span></span>

## <span data-ttu-id="df463-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="df463-137">RELATED LINKS</span></span>

[<span data-ttu-id="df463-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="df463-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="df463-139">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="df463-139">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="df463-140">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="df463-140">Remove-AzVM</span></span>](./Remove-AzVM.md)

[<span data-ttu-id="df463-141">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="df463-141">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="df463-142">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="df463-142">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="df463-143">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="df463-143">Update-AzVM</span></span>](./Update-AzVM.md)


