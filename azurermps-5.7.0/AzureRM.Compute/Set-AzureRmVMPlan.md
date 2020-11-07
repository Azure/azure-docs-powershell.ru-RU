---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: c6c17978840fd5c446d7d89350f1792091a5cffa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732158"
---
# <span data-ttu-id="0159f-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="0159f-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="0159f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0159f-102">SYNOPSIS</span></span>
<span data-ttu-id="0159f-103">Задает сведения о плане рынка на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="0159f-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0159f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0159f-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [<CommonParameters>]
```

## <span data-ttu-id="0159f-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0159f-105">DESCRIPTION</span></span>
<span data-ttu-id="0159f-106">Командлет **Set-AzureRmVMPlan** задает сведения о плане Azure Marketplace для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0159f-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="0159f-107">Прежде чем развертывать изображение Marketplace с помощью командной строки, необходимо включить программный доступ или выполнить развертывание виртуальной машины с помощью портала Azure.</span><span class="sxs-lookup"><span data-stu-id="0159f-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="0159f-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0159f-108">EXAMPLES</span></span>

## <span data-ttu-id="0159f-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0159f-109">PARAMETERS</span></span>

### <span data-ttu-id="0159f-110">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0159f-110">-Name</span></span>
<span data-ttu-id="0159f-111">Указывает имя изображения из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="0159f-111">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="0159f-112">Это то же значение, которое возвращает командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="0159f-112">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="0159f-113">Дополнительные сведения о том, как найти сведения о изображении, приведены в разделе [Навигация и выбор образов виртуальных машин Azure с помощью PowerShell и службы Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) в документации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="0159f-113">For more information about how to find image information, see [Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLI](https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="0159f-114">-Product</span><span class="sxs-lookup"><span data-stu-id="0159f-114">-Product</span></span>
<span data-ttu-id="0159f-115">Определяет произведение изображения на рынке.</span><span class="sxs-lookup"><span data-stu-id="0159f-115">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="0159f-116">Это та же информация, что и значение **предложения** элемента **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="0159f-116">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0159f-117">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="0159f-117">-PromotionCode</span></span>
<span data-ttu-id="0159f-118">Указывает код рекламной акции.</span><span class="sxs-lookup"><span data-stu-id="0159f-118">Specifies a promotion code.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0159f-119">-Publisher</span><span class="sxs-lookup"><span data-stu-id="0159f-119">-Publisher</span></span>
<span data-ttu-id="0159f-120">Указывает издателя изображения.</span><span class="sxs-lookup"><span data-stu-id="0159f-120">Specifies the publisher of the image.</span></span>
<span data-ttu-id="0159f-121">Эти сведения можно найти с помощью командлета Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="0159f-121">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0159f-122">-VM</span><span class="sxs-lookup"><span data-stu-id="0159f-122">-VM</span></span>
<span data-ttu-id="0159f-123">Указывает объект виртуальной машины, для которого нужно задать план Marketplace.</span><span class="sxs-lookup"><span data-stu-id="0159f-123">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="0159f-124">Вы можете использовать командлет Get-AzureRmVM для получения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0159f-124">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="0159f-125">Вы можете использовать командлет New-AzureRmVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="0159f-125">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0159f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0159f-126">CommonParameters</span></span>
<span data-ttu-id="0159f-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0159f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0159f-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0159f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0159f-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0159f-129">INPUTS</span></span>

### <span data-ttu-id="0159f-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="0159f-130">None</span></span>
<span data-ttu-id="0159f-131">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="0159f-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0159f-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0159f-132">OUTPUTS</span></span>

## <span data-ttu-id="0159f-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="0159f-133">NOTES</span></span>

## <span data-ttu-id="0159f-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0159f-134">RELATED LINKS</span></span>

[<span data-ttu-id="0159f-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0159f-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0159f-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="0159f-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="0159f-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="0159f-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="0159f-138">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="0159f-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
