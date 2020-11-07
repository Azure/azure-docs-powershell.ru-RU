---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvm
schema: 2.0.0
ms.openlocfilehash: 5f694ef2985ecc983932b2ff78705be8a08315f2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732161"
---
# <span data-ttu-id="cac1f-101">Remove-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cac1f-101">Remove-AzureRmVM</span></span>

## <span data-ttu-id="cac1f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cac1f-102">SYNOPSIS</span></span>
<span data-ttu-id="cac1f-103">Удаление виртуальной машины из Azure.</span><span class="sxs-lookup"><span data-stu-id="cac1f-103">Removes a virtual machine from Azure.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cac1f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cac1f-104">SYNTAX</span></span>

### <span data-ttu-id="cac1f-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cac1f-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cac1f-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="cac1f-106">IdParameterSetName</span></span>
```
Remove-AzureRmVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cac1f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cac1f-107">DESCRIPTION</span></span>
<span data-ttu-id="cac1f-108">Командлет **Remove-AzureRmVM** удаляет виртуальную машину из Azure.</span><span class="sxs-lookup"><span data-stu-id="cac1f-108">The **Remove-AzureRmVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="cac1f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cac1f-109">EXAMPLES</span></span>

### <span data-ttu-id="cac1f-110">Пример 1: Удаление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="cac1f-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="cac1f-111">Эта команда удаляет виртуальную машину с именем VirtualMachine07 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="cac1f-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="cac1f-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cac1f-112">PARAMETERS</span></span>

### <span data-ttu-id="cac1f-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cac1f-113">-AsJob</span></span>
<span data-ttu-id="cac1f-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="cac1f-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="cac1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cac1f-115">-DefaultProfile</span></span>
<span data-ttu-id="cac1f-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cac1f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cac1f-117">-Force</span><span class="sxs-lookup"><span data-stu-id="cac1f-117">-Force</span></span>
<span data-ttu-id="cac1f-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="cac1f-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac1f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="cac1f-119">-Id</span></span>
<span data-ttu-id="cac1f-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cac1f-120">The resource group name.</span></span>

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

### <span data-ttu-id="cac1f-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="cac1f-121">-Name</span></span>
<span data-ttu-id="cac1f-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="cac1f-122">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cac1f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cac1f-123">-ResourceGroupName</span></span>
<span data-ttu-id="cac1f-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="cac1f-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="cac1f-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cac1f-125">-Confirm</span></span>
<span data-ttu-id="cac1f-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="cac1f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac1f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cac1f-127">-WhatIf</span></span>
<span data-ttu-id="cac1f-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="cac1f-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="cac1f-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="cac1f-129">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cac1f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cac1f-130">CommonParameters</span></span>
<span data-ttu-id="cac1f-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cac1f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cac1f-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cac1f-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cac1f-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cac1f-133">INPUTS</span></span>

### <span data-ttu-id="cac1f-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="cac1f-134">None</span></span>
<span data-ttu-id="cac1f-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="cac1f-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cac1f-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cac1f-136">OUTPUTS</span></span>

### <span data-ttu-id="cac1f-137">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="cac1f-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="cac1f-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="cac1f-138">NOTES</span></span>

## <span data-ttu-id="cac1f-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cac1f-139">RELATED LINKS</span></span>

[<span data-ttu-id="cac1f-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cac1f-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="cac1f-141">New-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cac1f-141">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="cac1f-142">Restarting-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cac1f-142">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="cac1f-143">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cac1f-143">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="cac1f-144">Остановить-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cac1f-144">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="cac1f-145">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="cac1f-145">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


