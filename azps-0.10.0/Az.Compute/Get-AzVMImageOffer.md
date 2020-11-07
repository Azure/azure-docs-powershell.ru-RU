---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: eb56542d02498a0d4b8aa4176c77d75ab6ad4da6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911517"
---
# <span data-ttu-id="01bbb-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="01bbb-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="01bbb-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="01bbb-102">SYNOPSIS</span></span>
<span data-ttu-id="01bbb-103">Возвращает VMImage типы предложения.</span><span class="sxs-lookup"><span data-stu-id="01bbb-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="01bbb-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="01bbb-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="01bbb-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="01bbb-105">DESCRIPTION</span></span>
<span data-ttu-id="01bbb-106">Командлет **Get-AzVMImageOffer** получает типы предложений VMImage.</span><span class="sxs-lookup"><span data-stu-id="01bbb-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="01bbb-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="01bbb-107">EXAMPLES</span></span>

### <span data-ttu-id="01bbb-108">Пример 1: получение типов предложений для издателя</span><span class="sxs-lookup"><span data-stu-id="01bbb-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="01bbb-109">Эта команда получает типы предложений для указанного издателя в центральном регионе США.</span><span class="sxs-lookup"><span data-stu-id="01bbb-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="01bbb-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="01bbb-110">PARAMETERS</span></span>

### <span data-ttu-id="01bbb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01bbb-111">-DefaultProfile</span></span>
<span data-ttu-id="01bbb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="01bbb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="01bbb-113">-Location</span><span class="sxs-lookup"><span data-stu-id="01bbb-113">-Location</span></span>
<span data-ttu-id="01bbb-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="01bbb-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="01bbb-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="01bbb-115">-PublisherName</span></span>
<span data-ttu-id="01bbb-116">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="01bbb-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="01bbb-117">Чтобы получить издатель, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="01bbb-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="01bbb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bbb-118">CommonParameters</span></span>
<span data-ttu-id="01bbb-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="01bbb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bbb-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01bbb-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bbb-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="01bbb-121">INPUTS</span></span>

### <span data-ttu-id="01bbb-122">Ничего</span><span class="sxs-lookup"><span data-stu-id="01bbb-122">None</span></span>
<span data-ttu-id="01bbb-123">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="01bbb-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="01bbb-124">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="01bbb-124">OUTPUTS</span></span>

### <span data-ttu-id="01bbb-125">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="01bbb-125">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="01bbb-126">Пуск</span><span class="sxs-lookup"><span data-stu-id="01bbb-126">NOTES</span></span>

## <span data-ttu-id="01bbb-127">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="01bbb-127">RELATED LINKS</span></span>

[<span data-ttu-id="01bbb-128">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="01bbb-128">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="01bbb-129">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="01bbb-129">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="01bbb-130">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="01bbb-130">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="01bbb-131">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="01bbb-131">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


