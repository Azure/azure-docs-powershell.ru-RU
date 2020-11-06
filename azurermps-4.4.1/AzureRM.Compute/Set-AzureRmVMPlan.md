---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMPlan.md
ms.openlocfilehash: 9fc5da6afd281f68329274ae62a67d888aa13260
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93570072"
---
# <span data-ttu-id="95f98-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="95f98-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="95f98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="95f98-102">SYNOPSIS</span></span>
<span data-ttu-id="95f98-103">Задает сведения о плане рынка на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="95f98-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95f98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="95f98-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95f98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f98-105">DESCRIPTION</span></span>
<span data-ttu-id="95f98-106">Командлет **Set-AzureRmVMPlan** задает сведения о плане Azure Marketplace для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95f98-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="95f98-107">Прежде чем развертывать изображение Marketplace с помощью командной строки, необходимо включить программный доступ или выполнить развертывание виртуальной машины с помощью портала Azure.</span><span class="sxs-lookup"><span data-stu-id="95f98-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="95f98-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="95f98-108">EXAMPLES</span></span>

## <span data-ttu-id="95f98-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="95f98-109">PARAMETERS</span></span>

### <span data-ttu-id="95f98-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95f98-110">-DefaultProfile</span></span>
<span data-ttu-id="95f98-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="95f98-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95f98-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="95f98-112">-Name</span></span>
<span data-ttu-id="95f98-113">Указывает имя изображения из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="95f98-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="95f98-114">Это то же значение, которое возвращает командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="95f98-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="95f98-115">Дополнительные сведения о поиске изображений можно найти в разделе Навигация и выбор образов виртуальных машин Azure с помощью PowerShell и инфраструктуры Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) в документации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="95f98-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="95f98-116">-Product</span><span class="sxs-lookup"><span data-stu-id="95f98-116">-Product</span></span>
<span data-ttu-id="95f98-117">Определяет произведение изображения на рынке.</span><span class="sxs-lookup"><span data-stu-id="95f98-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="95f98-118">Это та же информация, что и значение **предложения** элемента **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="95f98-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="95f98-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="95f98-119">-PromotionCode</span></span>
<span data-ttu-id="95f98-120">Указывает код рекламной акции.</span><span class="sxs-lookup"><span data-stu-id="95f98-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="95f98-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="95f98-121">-Publisher</span></span>
<span data-ttu-id="95f98-122">Указывает издателя изображения.</span><span class="sxs-lookup"><span data-stu-id="95f98-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="95f98-123">Эти сведения можно найти с помощью командлета Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="95f98-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="95f98-124">-VM</span><span class="sxs-lookup"><span data-stu-id="95f98-124">-VM</span></span>
<span data-ttu-id="95f98-125">Указывает объект виртуальной машины, для которого нужно задать план Marketplace.</span><span class="sxs-lookup"><span data-stu-id="95f98-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="95f98-126">Вы можете использовать командлет Get-AzureRmVM для получения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95f98-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="95f98-127">Вы можете использовать командлет New-AzureRmVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="95f98-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="95f98-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95f98-128">CommonParameters</span></span>
<span data-ttu-id="95f98-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="95f98-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95f98-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95f98-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95f98-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="95f98-131">INPUTS</span></span>

## <span data-ttu-id="95f98-132">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="95f98-132">OUTPUTS</span></span>

## <span data-ttu-id="95f98-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="95f98-133">NOTES</span></span>

## <span data-ttu-id="95f98-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="95f98-134">RELATED LINKS</span></span>

[<span data-ttu-id="95f98-135">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="95f98-135">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="95f98-136">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="95f98-136">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="95f98-137">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="95f98-137">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="95f98-138">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="95f98-138">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
