---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/start-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 121d9353baaa10058e101d3f8a7d398f345052ff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733884"
---
# <span data-ttu-id="2d76b-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d76b-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="2d76b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="2d76b-102">SYNOPSIS</span></span>
<span data-ttu-id="2d76b-103">Запуск виртуальной машины Azure.</span><span class="sxs-lookup"><span data-stu-id="2d76b-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2d76b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="2d76b-104">SYNTAX</span></span>

### <span data-ttu-id="2d76b-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="2d76b-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2d76b-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2d76b-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d76b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d76b-107">DESCRIPTION</span></span>
<span data-ttu-id="2d76b-108">Командлет **Start-AzureRmVM** запускает виртуальную машину Azure.</span><span class="sxs-lookup"><span data-stu-id="2d76b-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="2d76b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="2d76b-109">EXAMPLES</span></span>

### <span data-ttu-id="2d76b-110">Пример 1: Запуск виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="2d76b-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="2d76b-111">Эта команда запускает виртуальную машину с именем VirtualMachine07 в ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="2d76b-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="2d76b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="2d76b-112">PARAMETERS</span></span>

### <span data-ttu-id="2d76b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d76b-113">-AsJob</span></span>
<span data-ttu-id="2d76b-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="2d76b-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2d76b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d76b-115">-DefaultProfile</span></span>
<span data-ttu-id="2d76b-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2d76b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d76b-117">-ID</span><span class="sxs-lookup"><span data-stu-id="2d76b-117">-Id</span></span>
<span data-ttu-id="2d76b-118">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="2d76b-118">The resource group name.</span></span>

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

### <span data-ttu-id="2d76b-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="2d76b-119">-Name</span></span>
<span data-ttu-id="2d76b-120">Имя виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d76b-120">The virtual machine name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2d76b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d76b-121">-ResourceGroupName</span></span>
<span data-ttu-id="2d76b-122">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2d76b-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="2d76b-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2d76b-123">-Confirm</span></span>
<span data-ttu-id="2d76b-124">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="2d76b-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d76b-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d76b-125">-WhatIf</span></span>
<span data-ttu-id="2d76b-126">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="2d76b-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2d76b-127">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="2d76b-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d76b-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d76b-128">CommonParameters</span></span>
<span data-ttu-id="2d76b-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="2d76b-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d76b-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d76b-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d76b-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="2d76b-131">INPUTS</span></span>

### <span data-ttu-id="2d76b-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2d76b-132">System.String</span></span>

## <span data-ttu-id="2d76b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="2d76b-133">OUTPUTS</span></span>

### <span data-ttu-id="2d76b-134">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2d76b-134">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="2d76b-135">Пуск</span><span class="sxs-lookup"><span data-stu-id="2d76b-135">NOTES</span></span>

## <span data-ttu-id="2d76b-136">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2d76b-136">RELATED LINKS</span></span>

[<span data-ttu-id="2d76b-137">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d76b-137">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="2d76b-138">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d76b-138">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="2d76b-139">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d76b-139">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="2d76b-140">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d76b-140">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="2d76b-141">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d76b-141">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="2d76b-142">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="2d76b-142">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


