---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimageoffer
schema: 2.0.0
ms.openlocfilehash: 00169d833244ece2f697d2429f5e5db5ee0bf901
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93913914"
---
# <span data-ttu-id="c9214-101">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="c9214-101">Get-AzureRmVMImageOffer</span></span>

## <span data-ttu-id="c9214-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c9214-102">SYNOPSIS</span></span>
<span data-ttu-id="c9214-103">Возвращает VMImage типы предложения.</span><span class="sxs-lookup"><span data-stu-id="c9214-103">Gets VMImage offer types.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9214-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c9214-104">SYNTAX</span></span>

```
Get-AzureRmVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9214-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9214-105">DESCRIPTION</span></span>
<span data-ttu-id="c9214-106">Командлет **Get-AzureRmVMImageOffer** получает типы предложений VMImage.</span><span class="sxs-lookup"><span data-stu-id="c9214-106">The **Get-AzureRmVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="c9214-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c9214-107">EXAMPLES</span></span>

### <span data-ttu-id="c9214-108">Пример 1: получение типов предложений для издателя</span><span class="sxs-lookup"><span data-stu-id="c9214-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzureRmVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="c9214-109">Эта команда получает типы предложений для указанного издателя в центральном регионе США.</span><span class="sxs-lookup"><span data-stu-id="c9214-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="c9214-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c9214-110">PARAMETERS</span></span>

### <span data-ttu-id="c9214-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9214-111">-DefaultProfile</span></span>
<span data-ttu-id="c9214-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c9214-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c9214-113">-Location</span><span class="sxs-lookup"><span data-stu-id="c9214-113">-Location</span></span>
<span data-ttu-id="c9214-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="c9214-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9214-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="c9214-115">-PublisherName</span></span>
<span data-ttu-id="c9214-116">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="c9214-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="c9214-117">Чтобы получить издатель, используйте командлет Get-AzureRmVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="c9214-117">To obtain a publisher, use the Get-AzureRmVMImagePublisher cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9214-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9214-118">CommonParameters</span></span>
<span data-ttu-id="c9214-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c9214-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9214-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9214-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9214-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c9214-121">INPUTS</span></span>

### <span data-ttu-id="c9214-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="c9214-122">None</span></span>
<span data-ttu-id="c9214-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="c9214-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9214-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c9214-124">OUTPUTS</span></span>

### <span data-ttu-id="c9214-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="c9214-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="c9214-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="c9214-126">NOTES</span></span>

## <span data-ttu-id="c9214-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c9214-127">RELATED LINKS</span></span>

[<span data-ttu-id="c9214-128">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c9214-128">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="c9214-129">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="c9214-129">Get-AzureRmVMImagePublisher</span></span>](./Get-AzureRmVMImagePublisher.md)

[<span data-ttu-id="c9214-130">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="c9214-130">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="c9214-131">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="c9214-131">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


