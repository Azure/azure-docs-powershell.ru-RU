---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94072884"
---
# <span data-ttu-id="9858a-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="9858a-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="9858a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9858a-102">SYNOPSIS</span></span>
<span data-ttu-id="9858a-103">Возвращает VMImage типы предложения.</span><span class="sxs-lookup"><span data-stu-id="9858a-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="9858a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9858a-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9858a-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9858a-105">DESCRIPTION</span></span>
<span data-ttu-id="9858a-106">Командлет **Get-AzVMImageOffer** получает типы предложений VMImage.</span><span class="sxs-lookup"><span data-stu-id="9858a-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="9858a-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9858a-107">EXAMPLES</span></span>

### <span data-ttu-id="9858a-108">Пример 1: получение типов предложений для издателя</span><span class="sxs-lookup"><span data-stu-id="9858a-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="9858a-109">Эта команда получает типы предложений для указанного издателя в центральном регионе США.</span><span class="sxs-lookup"><span data-stu-id="9858a-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="9858a-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9858a-110">PARAMETERS</span></span>

### <span data-ttu-id="9858a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9858a-111">-DefaultProfile</span></span>
<span data-ttu-id="9858a-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9858a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9858a-113">-Location</span><span class="sxs-lookup"><span data-stu-id="9858a-113">-Location</span></span>
<span data-ttu-id="9858a-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="9858a-114">Specifies the location of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9858a-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="9858a-115">-PublisherName</span></span>
<span data-ttu-id="9858a-116">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="9858a-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="9858a-117">Чтобы получить издатель, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="9858a-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9858a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9858a-118">CommonParameters</span></span>
<span data-ttu-id="9858a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9858a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9858a-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9858a-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9858a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9858a-121">INPUTS</span></span>

### <span data-ttu-id="9858a-122">System. String</span><span class="sxs-lookup"><span data-stu-id="9858a-122">System.String</span></span>

## <span data-ttu-id="9858a-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9858a-123">OUTPUTS</span></span>

### <span data-ttu-id="9858a-124">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="9858a-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="9858a-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="9858a-125">NOTES</span></span>

## <span data-ttu-id="9858a-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9858a-126">RELATED LINKS</span></span>

[<span data-ttu-id="9858a-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9858a-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="9858a-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="9858a-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="9858a-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="9858a-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="9858a-130">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="9858a-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


