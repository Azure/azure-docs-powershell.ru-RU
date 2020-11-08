---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMPlan.md
ms.openlocfilehash: 93837ff6618523f71fdd2b0a3b933b50892af429
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074623"
---
# <span data-ttu-id="8d968-101">Set-AzVMPlan</span><span class="sxs-lookup"><span data-stu-id="8d968-101">Set-AzVMPlan</span></span>

## <span data-ttu-id="8d968-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="8d968-102">SYNOPSIS</span></span>
<span data-ttu-id="8d968-103">Задает сведения о плане рынка на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="8d968-103">Sets the Marketplace plan information on a virtual machine.</span></span>

## <span data-ttu-id="8d968-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="8d968-104">SYNTAX</span></span>

```
Set-AzVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8d968-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d968-105">DESCRIPTION</span></span>
<span data-ttu-id="8d968-106">Командлет **Set-AzVMPlan** задает сведения о плане Azure Marketplace для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d968-106">The **Set-AzVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>
<span data-ttu-id="8d968-107">Прежде чем развертывать изображение Marketplace с помощью командной строки, необходимо включить программный доступ или выполнить развертывание виртуальной машины с помощью портала Azure.</span><span class="sxs-lookup"><span data-stu-id="8d968-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="8d968-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="8d968-108">EXAMPLES</span></span>

## <span data-ttu-id="8d968-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="8d968-109">PARAMETERS</span></span>

### <span data-ttu-id="8d968-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d968-110">-DefaultProfile</span></span>
<span data-ttu-id="8d968-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="8d968-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8d968-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="8d968-112">-Name</span></span>
<span data-ttu-id="8d968-113">Указывает имя изображения из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="8d968-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="8d968-114">Это то же значение, которое возвращает командлет Get-AzVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="8d968-114">This is the same value that is returned by the Get-AzVMImageSku cmdlet.</span></span>
<span data-ttu-id="8d968-115">Дополнительные сведения о поиске изображений можно найти в разделе Навигация и выбор образов виртуальных машин Azure с помощью PowerShell и инфраструктуры Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) в документации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8d968-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="8d968-116">-Product</span><span class="sxs-lookup"><span data-stu-id="8d968-116">-Product</span></span>
<span data-ttu-id="8d968-117">Определяет произведение изображения на рынке.</span><span class="sxs-lookup"><span data-stu-id="8d968-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="8d968-118">Это та же информация, что и значение **предложения** элемента **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="8d968-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="8d968-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="8d968-119">-PromotionCode</span></span>
<span data-ttu-id="8d968-120">Указывает код рекламной акции.</span><span class="sxs-lookup"><span data-stu-id="8d968-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="8d968-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8d968-121">-Publisher</span></span>
<span data-ttu-id="8d968-122">Указывает издателя изображения.</span><span class="sxs-lookup"><span data-stu-id="8d968-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="8d968-123">Эти сведения можно найти с помощью командлета Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="8d968-123">You can find this information by using the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="8d968-124">-VM</span><span class="sxs-lookup"><span data-stu-id="8d968-124">-VM</span></span>
<span data-ttu-id="8d968-125">Указывает объект виртуальной машины, для которого нужно задать план Marketplace.</span><span class="sxs-lookup"><span data-stu-id="8d968-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="8d968-126">Вы можете использовать командлет Get-AzVM для получения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d968-126">You can use the Get-AzVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="8d968-127">Вы можете использовать командлет New-AzVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="8d968-127">You can use the New-AzVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="8d968-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d968-128">CommonParameters</span></span>
<span data-ttu-id="8d968-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="8d968-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d968-130">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d968-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d968-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="8d968-131">INPUTS</span></span>

### <span data-ttu-id="8d968-132">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8d968-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="8d968-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8d968-133">System.String</span></span>

## <span data-ttu-id="8d968-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="8d968-134">OUTPUTS</span></span>

### <span data-ttu-id="8d968-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="8d968-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="8d968-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="8d968-136">NOTES</span></span>

## <span data-ttu-id="8d968-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="8d968-137">RELATED LINKS</span></span>

[<span data-ttu-id="8d968-138">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8d968-138">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8d968-139">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="8d968-139">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="8d968-140">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="8d968-140">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="8d968-141">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="8d968-141">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
