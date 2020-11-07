---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: A1EA7D34-A8B4-4FA0-BD8C-3E846715AFBA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/set-azurermvmplan
schema: 2.0.0
ms.openlocfilehash: ce0101140bc353eb52ee8d1af7f2878735da73db
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93915366"
---
# <span data-ttu-id="ea9c9-101">Set-AzureRmVMPlan</span><span class="sxs-lookup"><span data-stu-id="ea9c9-101">Set-AzureRmVMPlan</span></span>

## <span data-ttu-id="ea9c9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ea9c9-102">SYNOPSIS</span></span>
<span data-ttu-id="ea9c9-103">Задает сведения о плане рынка на виртуальной машине.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-103">Sets the Marketplace plan information on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ea9c9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ea9c9-104">SYNTAX</span></span>

```
Set-AzureRmVMPlan [-VM] <PSVirtualMachine> [-Name] <String> [[-Product] <String>] [[-PromotionCode] <String>]
 [[-Publisher] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ea9c9-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea9c9-105">DESCRIPTION</span></span>
<span data-ttu-id="ea9c9-106">Командлет **Set-AzureRmVMPlan** задает сведения о плане Azure Marketplace для виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-106">The **Set-AzureRmVMPlan** cmdlet sets the Azure Marketplace plan information for a virtual machine.</span></span>

<span data-ttu-id="ea9c9-107">Прежде чем развертывать изображение Marketplace с помощью командной строки, необходимо включить программный доступ или выполнить развертывание виртуальной машины с помощью портала Azure.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-107">Before being able to deploy a Marketplace image through the command-line, programmatic access must be enabled or the virtual machine must be deployed by using the Azure portal.</span></span>

## <span data-ttu-id="ea9c9-108">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ea9c9-108">EXAMPLES</span></span>

## <span data-ttu-id="ea9c9-109">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ea9c9-109">PARAMETERS</span></span>

### <span data-ttu-id="ea9c9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea9c9-110">-DefaultProfile</span></span>
<span data-ttu-id="ea9c9-111">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ea9c9-112">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="ea9c9-112">-Name</span></span>
<span data-ttu-id="ea9c9-113">Указывает имя изображения из Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-113">Specifies the name of the image from the Marketplace.</span></span>
<span data-ttu-id="ea9c9-114">Это то же значение, которое возвращает командлет Get-AzureRmVMImageSku.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-114">This is the same value that is returned by the Get-AzureRmVMImageSku cmdlet.</span></span>
<span data-ttu-id="ea9c9-115">Дополнительные сведения о поиске изображений можно найти в разделе Навигация и выбор образов виртуальных машин Azure с помощью PowerShell и инфраструктуры Azure CLI https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ ( https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) в документации Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-115">For more information about how to find image information, see Navigating and Selecting Azure Virtual Machine images with PowerShell and the Azure CLIhttps://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/ (https://azure.microsoft.com/documentation/articles/resource-groups-vm-searching/) in the Microsoft Azure documentation.</span></span>

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

### <span data-ttu-id="ea9c9-116">-Product</span><span class="sxs-lookup"><span data-stu-id="ea9c9-116">-Product</span></span>
<span data-ttu-id="ea9c9-117">Определяет произведение изображения на рынке.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-117">Specifies the product of the image from the Marketplace.</span></span>
<span data-ttu-id="ea9c9-118">Это та же информация, что и значение **предложения** элемента **imageReference** .</span><span class="sxs-lookup"><span data-stu-id="ea9c9-118">This is the same information as the **Offer** value of the **imageReference** element.</span></span>

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

### <span data-ttu-id="ea9c9-119">-PromotionCode</span><span class="sxs-lookup"><span data-stu-id="ea9c9-119">-PromotionCode</span></span>
<span data-ttu-id="ea9c9-120">Указывает код рекламной акции.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-120">Specifies a promotion code.</span></span>

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

### <span data-ttu-id="ea9c9-121">-Publisher</span><span class="sxs-lookup"><span data-stu-id="ea9c9-121">-Publisher</span></span>
<span data-ttu-id="ea9c9-122">Указывает издателя изображения.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-122">Specifies the publisher of the image.</span></span>
<span data-ttu-id="ea9c9-123">Эти сведения можно найти с помощью командлета Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-123">You can find this information by using the Get-AzureRmVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="ea9c9-124">-VM</span><span class="sxs-lookup"><span data-stu-id="ea9c9-124">-VM</span></span>
<span data-ttu-id="ea9c9-125">Указывает объект виртуальной машины, для которого нужно задать план Marketplace.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-125">Specifies the virtual machine object for which to set a Marketplace plan.</span></span>
<span data-ttu-id="ea9c9-126">Вы можете использовать командлет Get-AzureRmVM для получения объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-126">You can use the Get-AzureRmVM cmdlet to obtain a virtual machine object.</span></span>
<span data-ttu-id="ea9c9-127">Вы можете использовать командлет New-AzureRmVMConfig для создания объекта виртуальной машины.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-127">You can use the New-AzureRmVMConfig cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="ea9c9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea9c9-128">CommonParameters</span></span>
<span data-ttu-id="ea9c9-129">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea9c9-130">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea9c9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea9c9-131">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ea9c9-131">INPUTS</span></span>

### <span data-ttu-id="ea9c9-132">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ea9c9-132">PSVirtualMachine</span></span>
<span data-ttu-id="ea9c9-133">Параметр VM принимает значение типа "PSVirtualMachine" из конвейера.</span><span class="sxs-lookup"><span data-stu-id="ea9c9-133">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="ea9c9-134">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ea9c9-134">OUTPUTS</span></span>

### <span data-ttu-id="ea9c9-135">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="ea9c9-135">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="ea9c9-136">Пуск</span><span class="sxs-lookup"><span data-stu-id="ea9c9-136">NOTES</span></span>

## <span data-ttu-id="ea9c9-137">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ea9c9-137">RELATED LINKS</span></span>

[<span data-ttu-id="ea9c9-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="ea9c9-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="ea9c9-139">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="ea9c9-139">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="ea9c9-140">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="ea9c9-140">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="ea9c9-141">New-AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="ea9c9-141">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
