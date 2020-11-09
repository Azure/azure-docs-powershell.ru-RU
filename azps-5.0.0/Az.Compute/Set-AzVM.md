---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: 34c49bdd798e23e9c5d151ed3de577136fad5b03
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94312074"
---
# <span data-ttu-id="3e17c-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e17c-101">Set-AzVM</span></span>

## <span data-ttu-id="3e17c-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="3e17c-102">SYNOPSIS</span></span>
<span data-ttu-id="3e17c-103">Помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="3e17c-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="3e17c-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="3e17c-104">SYNTAX</span></span>

### <span data-ttu-id="3e17c-105">GeneralizeResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3e17c-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e17c-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e17c-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e17c-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e17c-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e17c-108">SimulateEvictionResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e17c-108">SimulateEvictionResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-SimulateEviction] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e17c-109">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e17c-109">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3e17c-110">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e17c-110">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e17c-111">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e17c-111">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3e17c-112">SimulateEvictionIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="3e17c-112">SimulateEvictionIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-SimulateEviction] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3e17c-113">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e17c-113">DESCRIPTION</span></span>
<span data-ttu-id="3e17c-114">Командлет **Set-AzVM** помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="3e17c-114">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="3e17c-115">Перед выполнением этого командлета Войдите в виртуальную машину и используйте Sysprep для подготовки жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="3e17c-115">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="3e17c-116">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="3e17c-116">EXAMPLES</span></span>

### <span data-ttu-id="3e17c-117">Пример 1: Пометка виртуальной машины как обобщенной</span><span class="sxs-lookup"><span data-stu-id="3e17c-117">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="3e17c-118">Эта команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="3e17c-118">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="3e17c-119">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="3e17c-119">PARAMETERS</span></span>

### <span data-ttu-id="3e17c-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e17c-120">-AsJob</span></span>
<span data-ttu-id="3e17c-121">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="3e17c-121">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="3e17c-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e17c-122">-DefaultProfile</span></span>
<span data-ttu-id="3e17c-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3e17c-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3e17c-124">-Обобщенный</span><span class="sxs-lookup"><span data-stu-id="3e17c-124">-Generalized</span></span>
<span data-ttu-id="3e17c-125">Указывает на то, что этот командлет помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="3e17c-125">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="3e17c-126">-ID</span><span class="sxs-lookup"><span data-stu-id="3e17c-126">-Id</span></span>
<span data-ttu-id="3e17c-127">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3e17c-127">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="3e17c-128">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="3e17c-128">-Name</span></span>
<span data-ttu-id="3e17c-129">Указывает имя виртуальной машины, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="3e17c-129">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="3e17c-130">-Wait</span><span class="sxs-lookup"><span data-stu-id="3e17c-130">-NoWait</span></span>
<span data-ttu-id="3e17c-131">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="3e17c-131">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="3e17c-132">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="3e17c-132">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="3e17c-133">-Повторное применение</span><span class="sxs-lookup"><span data-stu-id="3e17c-133">-Reapply</span></span>
<span data-ttu-id="3e17c-134">Для повторного применения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3e17c-134">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="3e17c-135">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="3e17c-135">-Redeploy</span></span>
<span data-ttu-id="3e17c-136">Указывает, что этот командлет вручную повторно выполняет развертывание виртуальной машины на другом узле Azure для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="3e17c-136">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="3e17c-137">Если вы переустанавливаете виртуальную машину, она перезапускается, что приводит к потере временных данных диска.</span><span class="sxs-lookup"><span data-stu-id="3e17c-137">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="3e17c-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e17c-138">-ResourceGroupName</span></span>
<span data-ttu-id="3e17c-139">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="3e17c-139">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="3e17c-140">-SimulateEviction</span><span class="sxs-lookup"><span data-stu-id="3e17c-140">-SimulateEviction</span></span>
<span data-ttu-id="3e17c-141">Указывает на то, что этот командлет имитирует вытеснение на плашечную виртуальную машину.</span><span class="sxs-lookup"><span data-stu-id="3e17c-141">Indicates that this cmdlet simulates the eviction of spot virtual machine.</span></span>
<span data-ttu-id="3e17c-142">Вытеснение будет происходить в течение 30 минут при вызове API.</span><span class="sxs-lookup"><span data-stu-id="3e17c-142">The eviction will occur within 30 minutes of calling the API.</span></span>

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

### <span data-ttu-id="3e17c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e17c-143">CommonParameters</span></span>
<span data-ttu-id="3e17c-144">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="3e17c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e17c-145">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e17c-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e17c-146">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="3e17c-146">INPUTS</span></span>

### <span data-ttu-id="3e17c-147">System. String</span><span class="sxs-lookup"><span data-stu-id="3e17c-147">System.String</span></span>

## <span data-ttu-id="3e17c-148">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="3e17c-148">OUTPUTS</span></span>

### <span data-ttu-id="3e17c-149">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="3e17c-149">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="3e17c-150">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="3e17c-150">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="3e17c-151">Пуск</span><span class="sxs-lookup"><span data-stu-id="3e17c-151">NOTES</span></span>

## <span data-ttu-id="3e17c-152">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3e17c-152">RELATED LINKS</span></span>

[<span data-ttu-id="3e17c-153">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="3e17c-153">Get-AzVM</span></span>](./Get-AzVM.md)


