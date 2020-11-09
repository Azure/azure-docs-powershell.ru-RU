---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D2CCAEB4-E43E-4075-9436-77F2C4FE9463
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimageoffer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImageOffer.md
ms.openlocfilehash: bd434bae36bc48d5c06bee1ed5fa77673ac426ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94247630"
---
# <span data-ttu-id="588f5-101">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="588f5-101">Get-AzVMImageOffer</span></span>

## <span data-ttu-id="588f5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="588f5-102">SYNOPSIS</span></span>
<span data-ttu-id="588f5-103">Возвращает VMImage типы предложения.</span><span class="sxs-lookup"><span data-stu-id="588f5-103">Gets VMImage offer types.</span></span>

## <span data-ttu-id="588f5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="588f5-104">SYNTAX</span></span>

```
Get-AzVMImageOffer -Location <String> -PublisherName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="588f5-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="588f5-105">DESCRIPTION</span></span>
<span data-ttu-id="588f5-106">Командлет **Get-AzVMImageOffer** получает типы предложений VMImage.</span><span class="sxs-lookup"><span data-stu-id="588f5-106">The **Get-AzVMImageOffer** cmdlet gets the VMImage offer types.</span></span>

## <span data-ttu-id="588f5-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="588f5-107">EXAMPLES</span></span>

### <span data-ttu-id="588f5-108">Пример 1: получение типов предложений для издателя</span><span class="sxs-lookup"><span data-stu-id="588f5-108">Example 1: Get offer types for a publisher</span></span>
```
PS C:\> Get-AzVMImageOffer -Location "Central US" -PublisherName "Fabrikam"
```

<span data-ttu-id="588f5-109">Эта команда получает типы предложений для указанного издателя в центральном регионе США.</span><span class="sxs-lookup"><span data-stu-id="588f5-109">This command gets the offer types for the specified publisher in the Central US region.</span></span>

## <span data-ttu-id="588f5-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="588f5-110">PARAMETERS</span></span>

### <span data-ttu-id="588f5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="588f5-111">-DefaultProfile</span></span>
<span data-ttu-id="588f5-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="588f5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="588f5-113">-Location</span><span class="sxs-lookup"><span data-stu-id="588f5-113">-Location</span></span>
<span data-ttu-id="588f5-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="588f5-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="588f5-115">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="588f5-115">-PublisherName</span></span>
<span data-ttu-id="588f5-116">Указывает имя издателя VMImage.</span><span class="sxs-lookup"><span data-stu-id="588f5-116">Specifies the name of a publisher of a VMImage.</span></span>
<span data-ttu-id="588f5-117">Чтобы получить издатель, используйте командлет Get-AzVMImagePublisher.</span><span class="sxs-lookup"><span data-stu-id="588f5-117">To obtain a publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

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

### <span data-ttu-id="588f5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="588f5-118">CommonParameters</span></span>
<span data-ttu-id="588f5-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="588f5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="588f5-120">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="588f5-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="588f5-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="588f5-121">INPUTS</span></span>

### <span data-ttu-id="588f5-122">System. String</span><span class="sxs-lookup"><span data-stu-id="588f5-122">System.String</span></span>

## <span data-ttu-id="588f5-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="588f5-123">OUTPUTS</span></span>

### <span data-ttu-id="588f5-124">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImageOffer</span><span class="sxs-lookup"><span data-stu-id="588f5-124">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageOffer</span></span>

## <span data-ttu-id="588f5-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="588f5-125">NOTES</span></span>

## <span data-ttu-id="588f5-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="588f5-126">RELATED LINKS</span></span>

[<span data-ttu-id="588f5-127">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="588f5-127">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="588f5-128">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="588f5-128">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="588f5-129">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="588f5-129">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="588f5-130">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="588f5-130">Save-AzVMImage</span></span>](./Save-AzVMImage.md)

