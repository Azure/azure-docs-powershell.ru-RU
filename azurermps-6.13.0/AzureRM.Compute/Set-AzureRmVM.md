---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 18fd719662fbbe46276927fb05fbff021d8bcb96
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734675"
---
# <span data-ttu-id="477c4-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="477c4-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="477c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="477c4-102">SYNOPSIS</span></span>
<span data-ttu-id="477c4-103">Помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="477c4-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="477c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="477c4-104">SYNTAX</span></span>

### <span data-ttu-id="477c4-105">GeneralizeResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="477c4-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="477c4-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="477c4-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="477c4-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="477c4-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="477c4-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="477c4-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="477c4-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="477c4-109">DESCRIPTION</span></span>
<span data-ttu-id="477c4-110">Командлет **Set-AzureRmVM** помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="477c4-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="477c4-111">Перед выполнением этого командлета Войдите в виртуальную машину и используйте Sysprep для подготовки жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="477c4-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="477c4-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="477c4-112">EXAMPLES</span></span>

### <span data-ttu-id="477c4-113">Пример 1: Пометка виртуальной машины как обобщенной</span><span class="sxs-lookup"><span data-stu-id="477c4-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="477c4-114">Эта команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="477c4-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="477c4-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="477c4-115">PARAMETERS</span></span>

### <span data-ttu-id="477c4-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="477c4-116">-AsJob</span></span>
<span data-ttu-id="477c4-117">Запустите командлет в фоновом режиме и верните задание для отслеживания хода выполнения.</span><span class="sxs-lookup"><span data-stu-id="477c4-117">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="477c4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="477c4-118">-DefaultProfile</span></span>
<span data-ttu-id="477c4-119">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="477c4-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="477c4-120">-Обобщенный</span><span class="sxs-lookup"><span data-stu-id="477c4-120">-Generalized</span></span>
<span data-ttu-id="477c4-121">Указывает на то, что этот командлет помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="477c4-121">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

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

### <span data-ttu-id="477c4-122">-ID</span><span class="sxs-lookup"><span data-stu-id="477c4-122">-Id</span></span>
<span data-ttu-id="477c4-123">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="477c4-123">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="477c4-124">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="477c4-124">-Name</span></span>
<span data-ttu-id="477c4-125">Указывает имя виртуальной машины, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="477c4-125">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="477c4-126">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="477c4-126">-Redeploy</span></span>
<span data-ttu-id="477c4-127">Указывает, что этот командлет вручную повторно выполняет развертывание виртуальной машины на другом узле Azure для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="477c4-127">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>
<span data-ttu-id="477c4-128">Если вы переустанавливаете виртуальную машину, она перезапускается, что приводит к потере временных данных диска.</span><span class="sxs-lookup"><span data-stu-id="477c4-128">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

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

### <span data-ttu-id="477c4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="477c4-129">-ResourceGroupName</span></span>
<span data-ttu-id="477c4-130">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="477c4-130">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="477c4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="477c4-131">CommonParameters</span></span>
<span data-ttu-id="477c4-132">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="477c4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="477c4-133">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="477c4-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="477c4-134">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="477c4-134">INPUTS</span></span>

### <span data-ttu-id="477c4-135">System. String</span><span class="sxs-lookup"><span data-stu-id="477c4-135">System.String</span></span>

## <span data-ttu-id="477c4-136">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="477c4-136">OUTPUTS</span></span>

### <span data-ttu-id="477c4-137">Microsoft. Azure. Commands. COMPUTE. Models. PSComputeLongRunningOperation</span><span class="sxs-lookup"><span data-stu-id="477c4-137">Microsoft.Azure.Commands.Compute.Models.PSComputeLongRunningOperation</span></span>

## <span data-ttu-id="477c4-138">Пуск</span><span class="sxs-lookup"><span data-stu-id="477c4-138">NOTES</span></span>

## <span data-ttu-id="477c4-139">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="477c4-139">RELATED LINKS</span></span>

[<span data-ttu-id="477c4-140">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="477c4-140">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


