---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98519452"
---
# <span data-ttu-id="2496e-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="2496e-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="2496e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2496e-102">SYNOPSIS</span></span>
<span data-ttu-id="2496e-103">Задает сведения о плане Marketplace на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="2496e-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="2496e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="2496e-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2496e-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="2496e-105">DESCRIPTION</span></span>
<span data-ttu-id="2496e-106">Для виртуальной машины задаются сведения о плане Azure Marketplace с использованием **cmdlet Set-AzVMPlan.**</span><span class="sxs-lookup"><span data-stu-id="2496e-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="2496e-107">Прежде чем развернуть изображение Marketplace с помощью командной строки, необходимо включить программный доступ или развернуть виртуальную машину на портале Azure.</span><span class="sxs-lookup"><span data-stu-id="2496e-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="2496e-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="2496e-108">EXAMPLES</span></span>

## <span data-ttu-id="2496e-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2496e-109">PARAMETERS</span></span>

### <span data-ttu-id="2496e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2496e-110">-DefaultProfile</span></span>
<span data-ttu-id="2496e-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="2496e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2496e-112">-Name</span><span class="sxs-lookup"><span data-stu-id="2496e-112">-Name</span></span>
<span data-ttu-id="2496e-113">Указывает имя изображения из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2496e-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="2496e-114">Это то же значение, которое возвращается Get-AzVMImageSku..</span><span class="sxs-lookup"><span data-stu-id="2496e-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="2496e-115">Дополнительные сведения о поиске изображений см. в документации Microsoft Azure для поиска изображений виртуальной машины Azure с помощью PowerShell и Azure https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) CLI.</span><span class="sxs-lookup"><span data-stu-id="2496e-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="2496e-116">-Product</span><span class="sxs-lookup"><span data-stu-id="2496e-116">-Product</span></span>
<span data-ttu-id="2496e-117">Определяет продукт изображения из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2496e-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="2496e-118">Это те же сведения, что и **значение предложения** элемента **imageReference.**</span><span class="sxs-lookup"><span data-stu-id="2496e-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2496e-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="2496e-119">-PromotionCode</span></span>
<span data-ttu-id="2496e-120">Указывает рекламный код.</span><span class="sxs-lookup"><span data-stu-id="2496e-120">Specifies a promotion code.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2496e-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="2496e-121">-Publisher</span></span>
<span data-ttu-id="2496e-122">Указывает издателя изображения.</span><span class="sxs-lookup"><span data-stu-id="2496e-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="2496e-123">Эти сведения можно найти с помощью Get-AzVMImagePublisher управления.</span><span class="sxs-lookup"><span data-stu-id="2496e-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2496e-124">-VM</span><span class="sxs-lookup"><span data-stu-id="2496e-124">-VM</span></span>
<span data-ttu-id="2496e-125">Определяет объект виртуальной машины, для которого нужно установить план Marketplace.</span><span class="sxs-lookup"><span data-stu-id="2496e-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="2496e-126">Для получения объекта Get-AzVM машин можно использовать Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="2496e-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="2496e-127">Для создания объекта New-AzVMConfig машин можно использовать New-AzVMConfig.</span><span class="sxs-lookup"><span data-stu-id="2496e-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2496e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2496e-128">CommonParameters</span></span>
<span data-ttu-id="2496e-129">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2496e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2496e-130">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2496e-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2496e-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="2496e-131">INPUTS</span></span>

### <span data-ttu-id="2496e-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="2496e-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="2496e-133">System.String</span><span class="sxs-lookup"><span data-stu-id="2496e-133">System.String</span></span>

## <span data-ttu-id="2496e-134">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2496e-134">OUTPUTS</span></span>

### <span data-ttu-id="2496e-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMa modelse</span><span class="sxs-lookup"><span data-stu-id="2496e-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="2496e-136">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="2496e-136">NOTES</span></span>

## <span data-ttu-id="2496e-137">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="2496e-137">RELATED LINKS</span></span>

[<span data-ttu-id="2496e-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="2496e-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="2496e-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="2496e-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="2496e-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="2496e-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="2496e-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="2496e-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
