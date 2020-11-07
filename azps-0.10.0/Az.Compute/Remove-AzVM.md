---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: A16C2084-30A4-4AB8-AE22-28CC6E74FD48
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Remove-AzVM.md
ms.openlocfilehash: 4cdf61c8a5afca78f1701314476d9eacb862cdfb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911428"
---
# <span data-ttu-id="ad725-101">Remove-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad725-101">Remove-AzVM</span></span>

## <span data-ttu-id="ad725-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ad725-102">SYNOPSIS</span></span>
<span data-ttu-id="ad725-103">Удаление виртуальной машины из Azure.</span><span class="sxs-lookup"><span data-stu-id="ad725-103">Removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="ad725-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ad725-104">SYNTAX</span></span>

### <span data-ttu-id="ad725-105">ResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="ad725-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-ResourceGroupName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad725-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="ad725-106">IdParameterSetName</span></span>
```
Remove-AzVM [-Name] <String> [-Force] [-Id] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad725-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad725-107">DESCRIPTION</span></span>
<span data-ttu-id="ad725-108">Командлет **Remove-AzVM** удаляет виртуальную машину из Azure.</span><span class="sxs-lookup"><span data-stu-id="ad725-108">The **Remove-AzVM** cmdlet removes a virtual machine from Azure.</span></span>

## <span data-ttu-id="ad725-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ad725-109">EXAMPLES</span></span>

### <span data-ttu-id="ad725-110">Пример 1: Удаление виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="ad725-110">Example 1: Remove a virtual machine</span></span>
```
PS C:\> Remove-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="ad725-111">Эта команда удаляет виртуальную машину с именем VirtualMachine07 в группе ресурсов ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="ad725-111">This command removes the virtual machine named VirtualMachine07 in the resource group ResourceGroup11.</span></span>

## <span data-ttu-id="ad725-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ad725-112">PARAMETERS</span></span>

### <span data-ttu-id="ad725-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ad725-113">-AsJob</span></span>
<span data-ttu-id="ad725-114">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="ad725-114">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="ad725-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad725-115">-DefaultProfile</span></span>
<span data-ttu-id="ad725-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ad725-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad725-117">-Force</span><span class="sxs-lookup"><span data-stu-id="ad725-117">-Force</span></span>
<span data-ttu-id="ad725-118">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="ad725-118">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ad725-119">-ID</span><span class="sxs-lookup"><span data-stu-id="ad725-119">-Id</span></span>
<span data-ttu-id="ad725-120">Имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad725-120">The resource group name.</span></span>

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

### <span data-ttu-id="ad725-121">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ad725-121">-Name</span></span>
<span data-ttu-id="ad725-122">Название ресурса.</span><span class="sxs-lookup"><span data-stu-id="ad725-122">The resource name.</span></span>

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

### <span data-ttu-id="ad725-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad725-123">-ResourceGroupName</span></span>
<span data-ttu-id="ad725-124">Указывает имя группы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="ad725-124">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ad725-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ad725-125">-Confirm</span></span>
<span data-ttu-id="ad725-126">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="ad725-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad725-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad725-127">-WhatIf</span></span>
<span data-ttu-id="ad725-128">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="ad725-128">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="ad725-129">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="ad725-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad725-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad725-130">CommonParameters</span></span>
<span data-ttu-id="ad725-131">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ad725-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad725-132">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad725-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad725-133">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ad725-133">INPUTS</span></span>

### <span data-ttu-id="ad725-134">Ничего</span><span class="sxs-lookup"><span data-stu-id="ad725-134">None</span></span>
<span data-ttu-id="ad725-135">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="ad725-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad725-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ad725-136">OUTPUTS</span></span>

### <span data-ttu-id="ad725-137">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="ad725-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="ad725-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="ad725-138">NOTES</span></span>

## <span data-ttu-id="ad725-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ad725-139">RELATED LINKS</span></span>

[<span data-ttu-id="ad725-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad725-140">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ad725-141">New-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad725-141">New-AzVM</span></span>](./New-AzVM.md)

[<span data-ttu-id="ad725-142">Restarting-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad725-142">Restart-AzVM</span></span>](./Restart-AzVM.md)

[<span data-ttu-id="ad725-143">Start-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad725-143">Start-AzVM</span></span>](./Start-AzVM.md)

[<span data-ttu-id="ad725-144">Остановить-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad725-144">Stop-AzVM</span></span>](./Stop-AzVM.md)

[<span data-ttu-id="ad725-145">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ad725-145">Update-AzVM</span></span>](./Update-AzVM.md)


