---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: b3e060680ee5df25708f153b239ec6c13b4e8a35
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721704"
---
# <span data-ttu-id="58648-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="58648-101">Set-AzVM</span></span>

## <span data-ttu-id="58648-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="58648-102">SYNOPSIS</span></span>
<span data-ttu-id="58648-103">Помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="58648-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="58648-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="58648-104">SYNTAX</span></span>

### <span data-ttu-id="58648-105">GeneralizeResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="58648-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58648-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="58648-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58648-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="58648-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58648-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="58648-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [-Redeploy] [-AsJob] [-NoWait] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="58648-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="58648-109">DESCRIPTION</span></span>
<span data-ttu-id="58648-110">Командлет **Set-AzVM** помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="58648-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="58648-111">Перед выполнением этого командлета Войдите в виртуальную машину и используйте Sysprep для подготовки жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="58648-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="58648-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="58648-112">EXAMPLES</span></span>

### <span data-ttu-id="58648-113">Пример 1: Пометка виртуальной машины как обобщенной</span><span class="sxs-lookup"><span data-stu-id="58648-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="58648-114">Эта команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="58648-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="58648-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="58648-115">PARAMETERS</span></span>

### <span data-ttu-id="58648-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58648-116">-AsJob</span></span>
<span data-ttu-id="58648-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="58648-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="58648-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58648-118">-DefaultProfile</span></span>
<span data-ttu-id="58648-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="58648-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="58648-120">-Обобщенный</span><span class="sxs-lookup"><span data-stu-id="58648-120">-Generalized</span></span>
<span data-ttu-id="58648-121">Указывает на то, что этот командлет помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="58648-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="58648-122">-ID</span><span class="sxs-lookup"><span data-stu-id="58648-122">-Id</span></span>
<span data-ttu-id="58648-123">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="58648-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58648-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="58648-124">-Name</span></span>
<span data-ttu-id="58648-125">Указывает имя виртуальной машины, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="58648-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58648-126">-Wait</span><span class="sxs-lookup"><span data-stu-id="58648-126">-NoWait</span></span>
<span data-ttu-id="58648-127">Запускает операцию и возвращает значение немедленно, прежде чем операция завершится.</span><span class="sxs-lookup"><span data-stu-id="58648-127">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="58648-128">Для определения того, успешно ли завершилась операция, используйте какой – то другой механизм.</span><span class="sxs-lookup"><span data-stu-id="58648-128">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58648-129">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="58648-129">-Redeploy</span></span>
<span data-ttu-id="58648-130">Указывает, что этот командлет вручную повторно выполняет развертывание виртуальной машины на другом узле Azure для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="58648-130">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="58648-131">Если вы переустанавливаете виртуальную машину, она перезапускается, что приводит к потере временных данных диска.</span><span class="sxs-lookup"><span data-stu-id="58648-131">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="58648-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58648-132">-ResourceGroupName</span></span>
<span data-ttu-id="58648-133">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="58648-133">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58648-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58648-134">CommonParameters</span></span>
<span data-ttu-id="58648-135">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="58648-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58648-136">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="58648-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58648-137">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="58648-137">INPUTS</span></span>

### <span data-ttu-id="58648-138">System. String</span><span class="sxs-lookup"><span data-stu-id="58648-138">System.String</span></span>

## <span data-ttu-id="58648-139">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="58648-139">OUTPUTS</span></span>

### <span data-ttu-id="58648-140">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="58648-140">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

### <span data-ttu-id="58648-141">Microsoft. Azure. Commands. COMPUTE. Models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="58648-141">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="58648-142">Пуск</span><span class="sxs-lookup"><span data-stu-id="58648-142">NOTES</span></span>

## <span data-ttu-id="58648-143">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="58648-143">RELATED LINKS</span></span>

[<span data-ttu-id="58648-144">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="58648-144">Get-AzVM</span></span>](./Get-AzVM.md)


