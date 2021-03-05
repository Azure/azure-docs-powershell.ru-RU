---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b42f456b45de0e78b9d9e0c371dca950ada88ded
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977496"
---
# <span data-ttu-id="2f540-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="2f540-101">Set-AzVM</span></span>

## <span data-ttu-id="2f540-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f540-102">SYNOPSIS</span></span>
<span data-ttu-id="2f540-103">Пометка виртуальной машины как обобщенной.</span><span class="sxs-lookup"><span data-stu-id="2f540-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="2f540-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2f540-104">SYNTAX</span></span>

### <span data-ttu-id="2f540-105">GeneralizeResourceGroupNameParameterSetName (Default)</span><span class="sxs-lookup"><span data-stu-id="2f540-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f540-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2f540-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f540-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2f540-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f540-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2f540-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f540-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2f540-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2f540-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2f540-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f540-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2f540-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2f540-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="2f540-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2f540-113">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2f540-113">DESCRIPTION</span></span>
<span data-ttu-id="2f540-114">Для виртуальной машины в качестве обобщенного можно пометить cmdlet **Set-AzVM.**</span><span class="sxs-lookup"><span data-stu-id="2f540-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="2f540-115">Перед запуском этого cmdlet войдите на виртуальную машину и подготовьте жесткий диск с помощью Sysprep.</span><span class="sxs-lookup"><span data-stu-id="2f540-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="2f540-116">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2f540-116">EXAMPLES</span></span>

### <span data-ttu-id="2f540-117">Пример 1. Пометка виртуальной машины как обобщенной</span><span class="sxs-lookup"><span data-stu-id="2f540-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="2f540-118">Эта команда пометит виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="2f540-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="2f540-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f540-119">PARAMETERS</span></span>

### <span data-ttu-id="2f540-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f540-120">-AsJob</span></span>
<span data-ttu-id="2f540-121">Запустите его в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="2f540-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="2f540-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f540-122">-DefaultProfile</span></span>
<span data-ttu-id="2f540-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2f540-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2f540-124">-Обобщено</span><span class="sxs-lookup"><span data-stu-id="2f540-124">-Generalized</span></span>
<span data-ttu-id="2f540-125">Указывает на то, что этот cmdlet помещает виртуальную машину как общую.</span><span class="sxs-lookup"><span data-stu-id="2f540-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f540-126">-Id</span><span class="sxs-lookup"><span data-stu-id="2f540-126">-Id</span></span>
<span data-ttu-id="2f540-127">Определяет ИД ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2f540-127">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f540-128">-Name</span><span class="sxs-lookup"><span data-stu-id="2f540-128">-Name</span></span>
<span data-ttu-id="2f540-129">Указывает имя виртуальной машины, на которой выполняется этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f540-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f540-130">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2f540-130">-NoWait</span></span>
<span data-ttu-id="2f540-131">Начинает операцию и возвращает ее немедленно до ее завершения.</span><span class="sxs-lookup"><span data-stu-id="2f540-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="2f540-132">Чтобы определить успешное завершение операции, используйте другой механизм.</span><span class="sxs-lookup"><span data-stu-id="2f540-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f540-133">-Reapply</span><span class="sxs-lookup"><span data-stu-id="2f540-133">-Reapply</span></span>
<span data-ttu-id="2f540-134">Чтобы повторно прибавить виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="2f540-134">To reapply virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ReapplyResourceGroupNameParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f540-135">-Redeploy</span><span class="sxs-lookup"><span data-stu-id="2f540-135">-Redeploy</span></span>
<span data-ttu-id="2f540-136">Указывает на то, что этот cmdlet вручную перенаправит виртуальную машину на другой хост Azure для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="2f540-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="2f540-137">При перезапуске виртуальной машины она перезапускится, что приводит к потере данных эпозитерального диска.</span><span class="sxs-lookup"><span data-stu-id="2f540-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f540-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f540-138">-ResourceGroupName</span></span>
<span data-ttu-id="2f540-139">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="2f540-139">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName, SimulateEvictionResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f540-140">-Simulateeviction</span><span class="sxs-lookup"><span data-stu-id="2f540-140">-SimulateEviction</span></span>
<span data-ttu-id="2f540-141">Указывает на то, что этот cmdlet имитация работы spot virtual machine.</span><span class="sxs-lookup"><span data-stu-id="2f540-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="2f540-142">Это произойдет в течение 30 минут после вызова API.</span><span class="sxs-lookup"><span data-stu-id="2f540-142">The eviction will occur within 30 minutes of calling the API.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimulateEvictionResourceGroupNameParameterSetName, SimulateEvictionIdParameterSetName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f540-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f540-143">CommonParameters</span></span>
<span data-ttu-id="2f540-144">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f540-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f540-145">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f540-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f540-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2f540-146">INPUTS</span></span>

### <span data-ttu-id="2f540-147">System.String</span><span class="sxs-lookup"><span data-stu-id="2f540-147">System.String</span></span>

## <span data-ttu-id="2f540-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f540-148">OUTPUTS</span></span>

### <span data-ttu-id="2f540-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="2f540-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="2f540-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2f540-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="2f540-151">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2f540-151">NOTES</span></span>

## <span data-ttu-id="2f540-152">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2f540-152">RELATED LINKS</span></span>

[<span data-ttu-id="2f540-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2f540-153">Get-AzVM</span></span>](./Get-AzVM.md)


