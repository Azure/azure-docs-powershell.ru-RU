---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: c9b7ce0c55ff917839ff8047454dcced42653b3d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065389"
---
# <span data-ttu-id="a4e31-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="a4e31-101">Set-AzVM</span></span>

## <span data-ttu-id="a4e31-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="a4e31-102">SYNOPSIS</span></span>
<span data-ttu-id="a4e31-103">Помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="a4e31-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="a4e31-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="a4e31-104">SYNTAX</span></span>

### <span data-ttu-id="a4e31-105">GeneralizeResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="a4e31-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4e31-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a4e31-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4e31-107">ReapplyResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a4e31-107">ReapplyResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Reapply] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4e31-108">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a4e31-108">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a4e31-109">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a4e31-109">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a4e31-110">ReapplyIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="a4e31-110">ReapplyIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Reapply] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4e31-111">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4e31-111">DESCRIPTION</span></span>
<span data-ttu-id="a4e31-112">Командлет **Set-AzVM** помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="a4e31-112">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="a4e31-113">Перед выполнением этого командлета Войдите в виртуальную машину и используйте Sysprep для подготовки жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="a4e31-113">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="a4e31-114">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="a4e31-114">EXAMPLES</span></span>

### <span data-ttu-id="a4e31-115">Пример 1: Пометка виртуальной машины как обобщенной</span><span class="sxs-lookup"><span data-stu-id="a4e31-115">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="a4e31-116">Эта команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="a4e31-116">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="a4e31-117">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="a4e31-117">PARAMETERS</span></span>

### <span data-ttu-id="a4e31-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a4e31-118">-AsJob</span></span>
<span data-ttu-id="a4e31-119">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="a4e31-119">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a4e31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4e31-120">-DefaultProfile</span></span>
<span data-ttu-id="a4e31-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a4e31-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4e31-122">-Обобщенный</span><span class="sxs-lookup"><span data-stu-id="a4e31-122">-Generalized</span></span>
<span data-ttu-id="a4e31-123">Указывает на то, что этот командлет помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="a4e31-123">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="a4e31-124">-ID</span><span class="sxs-lookup"><span data-stu-id="a4e31-124">-Id</span></span>
<span data-ttu-id="a4e31-125">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a4e31-125">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName, ReapplyIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e31-126">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="a4e31-126">-Name</span></span>
<span data-ttu-id="a4e31-127">Указывает имя виртуальной машины, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="a4e31-127">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e31-128">-Wait</span><span class="sxs-lookup"><span data-stu-id="a4e31-128">-NoWait</span></span>
<span data-ttu-id="a4e31-129">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="a4e31-129">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="a4e31-130">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="a4e31-130">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="a4e31-131">-Повторное применение</span><span class="sxs-lookup"><span data-stu-id="a4e31-131">-Reapply</span></span>
<span data-ttu-id="a4e31-132">Для повторного применения виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a4e31-132">To reapply virtual machine.</span></span>

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

### <span data-ttu-id="a4e31-133">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="a4e31-133">-Redeploy</span></span>
<span data-ttu-id="a4e31-134">Указывает, что этот командлет вручную повторно выполняет развертывание виртуальной машины на другом узле Azure для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="a4e31-134">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="a4e31-135">Если вы переустанавливаете виртуальную машину, она перезапускается, что приводит к потере временных данных диска.</span><span class="sxs-lookup"><span data-stu-id="a4e31-135">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="a4e31-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4e31-136">-ResourceGroupName</span></span>
<span data-ttu-id="a4e31-137">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="a4e31-137">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName, ReapplyResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a4e31-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4e31-138">CommonParameters</span></span>
<span data-ttu-id="a4e31-139">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="a4e31-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4e31-140">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4e31-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4e31-141">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="a4e31-141">INPUTS</span></span>

### <span data-ttu-id="a4e31-142">System. String</span><span class="sxs-lookup"><span data-stu-id="a4e31-142">System.String</span></span>

## <span data-ttu-id="a4e31-143">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="a4e31-143">OUTPUTS</span></span>

### <span data-ttu-id="a4e31-144">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="a4e31-144">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="a4e31-145">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="a4e31-145">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a4e31-146">Пуск</span><span class="sxs-lookup"><span data-stu-id="a4e31-146">NOTES</span></span>

## <span data-ttu-id="a4e31-147">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a4e31-147">RELATED LINKS</span></span>

[<span data-ttu-id="a4e31-148">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="a4e31-148">Get-AzVM</span></span>](./Get-AzVM.md)


