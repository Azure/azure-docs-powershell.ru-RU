---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
ms.openlocfilehash: 030e1dfc05354cded24ac76a379707edd0f07c34
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913472"
---
# <span data-ttu-id="4167b-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4167b-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="4167b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4167b-102">SYNOPSIS</span></span>
<span data-ttu-id="4167b-103">Помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="4167b-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4167b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4167b-104">SYNTAX</span></span>

### <span data-ttu-id="4167b-105">GeneralizeResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4167b-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4167b-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4167b-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4167b-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4167b-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4167b-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="4167b-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4167b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4167b-109">DESCRIPTION</span></span>
<span data-ttu-id="4167b-110">Командлет **Set-AzureRmVM** помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="4167b-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="4167b-111">Перед выполнением этого командлета Войдите в виртуальную машину и используйте Sysprep для подготовки жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="4167b-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="4167b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4167b-112">EXAMPLES</span></span>

### <span data-ttu-id="4167b-113">Пример 1: Пометка виртуальной машины как обобщенной</span><span class="sxs-lookup"><span data-stu-id="4167b-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="4167b-114">Эта команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="4167b-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="4167b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4167b-115">PARAMETERS</span></span>

### <span data-ttu-id="4167b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4167b-116">-AsJob</span></span>
<span data-ttu-id="4167b-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="4167b-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="4167b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4167b-118">-DefaultProfile</span></span>
<span data-ttu-id="4167b-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="4167b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4167b-120">-Обобщенный</span><span class="sxs-lookup"><span data-stu-id="4167b-120">-Generalized</span></span>
<span data-ttu-id="4167b-121">Указывает на то, что этот командлет помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="4167b-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4167b-122">-ID</span><span class="sxs-lookup"><span data-stu-id="4167b-122">-Id</span></span>
<span data-ttu-id="4167b-123">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4167b-123">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeIdParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4167b-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="4167b-124">-Name</span></span>
<span data-ttu-id="4167b-125">Указывает имя виртуальной машины, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="4167b-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="4167b-126">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="4167b-126">-Redeploy</span></span>
<span data-ttu-id="4167b-127">Указывает, что этот командлет вручную повторно выполняет развертывание виртуальной машины на другом узле Azure для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="4167b-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="4167b-128">Если вы переустанавливаете виртуальную машину, она перезапускается, что приводит к потере временных данных диска.</span><span class="sxs-lookup"><span data-stu-id="4167b-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4167b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4167b-129">-ResourceGroupName</span></span>
<span data-ttu-id="4167b-130">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="4167b-130">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, RedeployResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4167b-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4167b-131">CommonParameters</span></span>
<span data-ttu-id="4167b-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4167b-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4167b-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4167b-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4167b-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4167b-134">INPUTS</span></span>

### <span data-ttu-id="4167b-135">Ничего</span><span class="sxs-lookup"><span data-stu-id="4167b-135">None</span></span>
<span data-ttu-id="4167b-136">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="4167b-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4167b-137">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4167b-137">OUTPUTS</span></span>

### <span data-ttu-id="4167b-138">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="4167b-138">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="4167b-139">Пуск</span><span class="sxs-lookup"><span data-stu-id="4167b-139">NOTES</span></span>

## <span data-ttu-id="4167b-140">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4167b-140">RELATED LINKS</span></span>

[<span data-ttu-id="4167b-141">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="4167b-141">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


