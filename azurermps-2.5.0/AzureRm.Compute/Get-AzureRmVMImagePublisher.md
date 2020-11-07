---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmimagepublisher
schema: 2.0.0
ms.openlocfilehash: 1faae0848a96595e71ba96c20f2df9df59cd7ef0
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/15/2020
ms.locfileid: "93914625"
---
# <span data-ttu-id="266dc-101">Get-AzureRmVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="266dc-101">Get-AzureRmVMImagePublisher</span></span>

## <span data-ttu-id="266dc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="266dc-102">SYNOPSIS</span></span>
<span data-ttu-id="266dc-103">Получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="266dc-103">Gets the VMImage publishers.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="266dc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="266dc-104">SYNTAX</span></span>

```
Get-AzureRmVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="266dc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="266dc-105">DESCRIPTION</span></span>
<span data-ttu-id="266dc-106">Командлет **Get-AzureRmVMImagePublisher** получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="266dc-106">The **Get-AzureRmVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="266dc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="266dc-107">EXAMPLES</span></span>

### <span data-ttu-id="266dc-108">Пример 1: получение VMImageных издателей для региона</span><span class="sxs-lookup"><span data-stu-id="266dc-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzureRmVMImagePublisher -Location "Central US"
```

<span data-ttu-id="266dc-109">Эта команда получает издателей экземпляров VMImage для Центральной области США в вашем профиле Azure.</span><span class="sxs-lookup"><span data-stu-id="266dc-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="266dc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="266dc-110">PARAMETERS</span></span>

### <span data-ttu-id="266dc-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="266dc-111">-DefaultProfile</span></span>
<span data-ttu-id="266dc-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="266dc-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="266dc-113">-Location</span><span class="sxs-lookup"><span data-stu-id="266dc-113">-Location</span></span>
<span data-ttu-id="266dc-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="266dc-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="266dc-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="266dc-115">CommonParameters</span></span>
<span data-ttu-id="266dc-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="266dc-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="266dc-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="266dc-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="266dc-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="266dc-118">INPUTS</span></span>

### <span data-ttu-id="266dc-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="266dc-119">None</span></span>
<span data-ttu-id="266dc-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="266dc-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="266dc-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="266dc-121">OUTPUTS</span></span>

### <span data-ttu-id="266dc-122">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="266dc-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="266dc-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="266dc-123">NOTES</span></span>

## <span data-ttu-id="266dc-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="266dc-124">RELATED LINKS</span></span>

[<span data-ttu-id="266dc-125">Get-AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="266dc-125">Get-AzureRmVMImage</span></span>](./Get-AzureRmVMImage.md)

[<span data-ttu-id="266dc-126">Get-AzureRmVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="266dc-126">Get-AzureRmVMImageOffer</span></span>](./Get-AzureRmVMImageOffer.md)

[<span data-ttu-id="266dc-127">Get-AzureRmVMImageSku</span><span class="sxs-lookup"><span data-stu-id="266dc-127">Get-AzureRmVMImageSku</span></span>](./Get-AzureRmVMImageSku.md)

[<span data-ttu-id="266dc-128">Сохранить — AzureRmVMImage</span><span class="sxs-lookup"><span data-stu-id="266dc-128">Save-AzureRmVMImage</span></span>](./Save-AzureRmVMImage.md)


