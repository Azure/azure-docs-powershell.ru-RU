---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 939320CB-2595-4150-AFDD-500CEA78559C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVM.md
ms.openlocfilehash: 6fa67a039599ab066b82ad923f5a2f896b0db519
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734078"
---
# <span data-ttu-id="1a53b-101">Set-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1a53b-101">Set-AzureRmVM</span></span>

## <span data-ttu-id="1a53b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="1a53b-102">SYNOPSIS</span></span>
<span data-ttu-id="1a53b-103">Помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="1a53b-103">Marks a virtual machine as generalized.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a53b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="1a53b-104">SYNTAX</span></span>

### <span data-ttu-id="1a53b-105">GeneralizeResourceGroupNameParameterSetName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="1a53b-105">GeneralizeResourceGroupNameParameterSetName (Default)</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Generalized]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a53b-106">RedeployResourceGroupNameParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1a53b-106">RedeployResourceGroupNameParameterSetName</span></span>
```
Set-AzureRmVM [-ResourceGroupName] <String> [-Name] <String> [-Redeploy]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1a53b-107">GeneralizeIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1a53b-107">GeneralizeIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Generalized] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1a53b-108">RedeployIdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="1a53b-108">RedeployIdParameterSetName</span></span>
```
Set-AzureRmVM [-Id] <String> [-Name] <String> [-Redeploy] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a53b-109">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a53b-109">DESCRIPTION</span></span>
<span data-ttu-id="1a53b-110">Командлет **Set-AzureRmVM** помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="1a53b-110">The **Set-AzureRmVM** cmdlet marks a virtual machine as generalized.</span></span>
<span data-ttu-id="1a53b-111">Перед выполнением этого командлета Войдите в виртуальную машину и используйте Sysprep для подготовки жесткого диска.</span><span class="sxs-lookup"><span data-stu-id="1a53b-111">Before you run this cmdlet, log on to the virtual machine and use Sysprep to prepare the hard disk.</span></span>

## <span data-ttu-id="1a53b-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="1a53b-112">EXAMPLES</span></span>

### <span data-ttu-id="1a53b-113">Пример 1: Пометка виртуальной машины как обобщенной</span><span class="sxs-lookup"><span data-stu-id="1a53b-113">Example 1: Mark a virtual machine as generalized</span></span>
```
PS C:\> Set-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -Generalized
```

<span data-ttu-id="1a53b-114">Эта команда помечает виртуальную машину с именем VirtualMachine07 как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="1a53b-114">This command marks the virtual machine named VirtualMachine07 as generalized.</span></span>

## <span data-ttu-id="1a53b-115">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="1a53b-115">PARAMETERS</span></span>

### <span data-ttu-id="1a53b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a53b-116">-DefaultProfile</span></span>
<span data-ttu-id="1a53b-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1a53b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a53b-118">-Обобщенный</span><span class="sxs-lookup"><span data-stu-id="1a53b-118">-Generalized</span></span>
<span data-ttu-id="1a53b-119">Указывает на то, что этот командлет помечает виртуальную машину как обобщенную.</span><span class="sxs-lookup"><span data-stu-id="1a53b-119">Indicates that this cmdlet marks a virtual machine as generalized.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GeneralizeResourceGroupNameParameterSetName, GeneralizeIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a53b-120">-ID</span><span class="sxs-lookup"><span data-stu-id="1a53b-120">-Id</span></span>
<span data-ttu-id="1a53b-121">Указывает идентификатор ресурса виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1a53b-121">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="1a53b-122">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="1a53b-122">-Name</span></span>
<span data-ttu-id="1a53b-123">Указывает имя виртуальной машины, на которой работает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="1a53b-123">Specifies the name of the virtual machine on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="1a53b-124">-Повторное развертывание</span><span class="sxs-lookup"><span data-stu-id="1a53b-124">-Redeploy</span></span>
<span data-ttu-id="1a53b-125">Указывает, что этот командлет вручную повторно выполняет развертывание виртуальной машины на другом узле Azure для устранения проблем.</span><span class="sxs-lookup"><span data-stu-id="1a53b-125">Indicates that this cmdlet manually redeploys the virtual machine to a different Azure host to fix any problems.</span></span>

<span data-ttu-id="1a53b-126">Если вы переустанавливаете виртуальную машину, она перезапускается, что приводит к потере временных данных диска.</span><span class="sxs-lookup"><span data-stu-id="1a53b-126">If you redeploy a virtual machine, it restarts, which results in the loss of ephemeral drive data.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RedeployResourceGroupNameParameterSetName, RedeployIdParameterSetName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a53b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a53b-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a53b-128">Указывает имя группы ресурсов виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="1a53b-128">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="1a53b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a53b-129">CommonParameters</span></span>
<span data-ttu-id="1a53b-130">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="1a53b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a53b-131">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a53b-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a53b-132">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="1a53b-132">INPUTS</span></span>

## <span data-ttu-id="1a53b-133">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="1a53b-133">OUTPUTS</span></span>

## <span data-ttu-id="1a53b-134">Пуск</span><span class="sxs-lookup"><span data-stu-id="1a53b-134">NOTES</span></span>

## <span data-ttu-id="1a53b-135">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1a53b-135">RELATED LINKS</span></span>

[<span data-ttu-id="1a53b-136">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="1a53b-136">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)


