---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmVMImagePublisher.md
ms.openlocfilehash: 109f55c1afc1c00d26c47d0131d098158010bd70
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "93570520"
---
# <span data-ttu-id="fd139-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fd139-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="fd139-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="fd139-102">SYNOPSIS</span></span>
<span data-ttu-id="fd139-103">Получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="fd139-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fd139-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="fd139-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fd139-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd139-105">DESCRIPTION</span></span>
<span data-ttu-id="fd139-106">Командлет **Get-AzureRmVMImagePublisher** получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="fd139-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="fd139-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="fd139-107">EXAMPLES</span></span>

### <span data-ttu-id="fd139-108">Пример 1: получение VMImageных издателей для региона</span><span class="sxs-lookup"><span data-stu-id="fd139-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="fd139-109">Эта команда получает издателей экземпляров VMImage для Центральной области США в вашем профиле Azure.</span><span class="sxs-lookup"><span data-stu-id="fd139-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="fd139-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="fd139-110">PARAMETERS</span></span>

### <span data-ttu-id="fd139-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd139-111">-DefaultProfile</span></span>
<span data-ttu-id="fd139-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="fd139-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fd139-113">-Location</span><span class="sxs-lookup"><span data-stu-id="fd139-113">-Location</span></span>
<span data-ttu-id="fd139-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="fd139-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="fd139-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd139-115">CommonParameters</span></span>
<span data-ttu-id="fd139-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="fd139-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd139-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fd139-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd139-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="fd139-118">INPUTS</span></span>

### <span data-ttu-id="fd139-119">System. String</span><span class="sxs-lookup"><span data-stu-id="fd139-119">System.String</span></span>

## <span data-ttu-id="fd139-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="fd139-120">OUTPUTS</span></span>

### <span data-ttu-id="fd139-121">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="fd139-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="fd139-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="fd139-122">NOTES</span></span>

## <span data-ttu-id="fd139-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="fd139-123">RELATED LINKS</span></span>

[<span data-ttu-id="fd139-124">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fd139-124">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="fd139-125">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="fd139-125">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="fd139-126">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="fd139-126">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="fd139-127">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="fd139-127">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


