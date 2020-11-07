---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVM.md
ms.openlocfilehash: a147565a61bc75d71083c69766138c3a5a4659db
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93901134"
---
# <span data-ttu-id="07691-101">Set-AzVM</span><span class="sxs-lookup"><span data-stu-id="07691-101">Set-AzVM</span></span>

## <span data-ttu-id="07691-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="07691-102">SYNOPSIS</span></span>
<span data-ttu-id="07691-103">Помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="07691-103">Marks a virtual machine as generalized.</span></span>

## <span data-ttu-id="07691-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="07691-104">SYNTAX</span></span>

### <span data-ttu-id="07691-105">GeneralizeResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="07691-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07691-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="07691-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07691-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="07691-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Generalized] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="07691-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="07691-108">RedeployIdParameterSetName</span></span>
```
Set-AzVM [-Id] <String> [[-Name] <String>] [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="07691-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="07691-109">DESCRIPTION</span></span>
<span data-ttu-id="07691-110">Командлет **Set-AzVM** помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="07691-110">The **Set-AzVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="07691-111">Перед выполнением этого командлета Войдите в виртуальную машину и используйте Sysprep для подготовки жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="07691-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="07691-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="07691-112">EXAMPLES</span></span>

### <span data-ttu-id="07691-113">Пример 1: Пометка виртуальной машины как обобщенной</span><span class="sxs-lookup"><span data-stu-id="07691-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="07691-114">Эта команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="07691-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="07691-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="07691-115">PARAMETERS</span></span>

### <span data-ttu-id="07691-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07691-116">-AsJob</span></span>
<span data-ttu-id="07691-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="07691-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="07691-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07691-118">-DefaultProfile</span></span>
<span data-ttu-id="07691-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="07691-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07691-120">-Обобщенный</span><span class="sxs-lookup"><span data-stu-id="07691-120">-Generalized</span></span>
<span data-ttu-id="07691-121">Указывает на то, что этот командлет помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="07691-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="07691-122">-ID</span><span class="sxs-lookup"><span data-stu-id="07691-122">-Id</span></span>
<span data-ttu-id="07691-123">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="07691-123">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="07691-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="07691-124">-Name</span></span>
<span data-ttu-id="07691-125">Указывает имя виртуальной машины, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="07691-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

```yaml
Type: System.String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07691-126">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="07691-126">-Redeploy</span></span>
<span data-ttu-id="07691-127">Указывает, что этот командлет вручную повторно выполняет развертывание виртуальной машины на другом узле Azure для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="07691-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="07691-128">Если вы переустанавливаете виртуальную машину, она перезапускается, что приводит к потере временных данных диска.</span><span class="sxs-lookup"><span data-stu-id="07691-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="07691-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07691-129">-ResourceGroupName</span></span>
<span data-ttu-id="07691-130">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="07691-130">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="07691-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07691-131">CommonParameters</span></span>
<span data-ttu-id="07691-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="07691-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07691-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07691-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07691-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="07691-134">INPUTS</span></span>

### <span data-ttu-id="07691-135">System. String</span><span class="sxs-lookup"><span data-stu-id="07691-135">System.String</span></span>

## <span data-ttu-id="07691-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="07691-136">OUTPUTS</span></span>

### <span data-ttu-id="07691-137">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="07691-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="07691-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="07691-138">NOTES</span></span>

## <span data-ttu-id="07691-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="07691-139">RELATED LINKS</span></span>

[<span data-ttu-id="07691-140">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="07691-140">Get-AzVM</span></span>](./Get-AzVM.md)


