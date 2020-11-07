---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: dcb5913176af352c39867f7029523765aca0d781
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2020
ms.locfileid: "93911518"
---
# <span data-ttu-id="75ab7-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="75ab7-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="75ab7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="75ab7-102">SYNOPSIS</span></span>
<span data-ttu-id="75ab7-103">Получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="75ab7-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="75ab7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="75ab7-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="75ab7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="75ab7-105">DESCRIPTION</span></span>
<span data-ttu-id="75ab7-106">Командлет **Get-AzVMImagePublisher** получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="75ab7-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="75ab7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="75ab7-107">EXAMPLES</span></span>

### <span data-ttu-id="75ab7-108">Пример 1: получение VMImageных издателей для региона</span><span class="sxs-lookup"><span data-stu-id="75ab7-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="75ab7-109">Эта команда получает издателей экземпляров VMImage для Центральной области США в вашем профиле Azure.</span><span class="sxs-lookup"><span data-stu-id="75ab7-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="75ab7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="75ab7-110">PARAMETERS</span></span>

### <span data-ttu-id="75ab7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75ab7-111">-DefaultProfile</span></span>
<span data-ttu-id="75ab7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="75ab7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75ab7-113">-Location</span><span class="sxs-lookup"><span data-stu-id="75ab7-113">-Location</span></span>
<span data-ttu-id="75ab7-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="75ab7-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="75ab7-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75ab7-115">CommonParameters</span></span>
<span data-ttu-id="75ab7-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="75ab7-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75ab7-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75ab7-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75ab7-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="75ab7-118">INPUTS</span></span>

### <span data-ttu-id="75ab7-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="75ab7-119">None</span></span>
<span data-ttu-id="75ab7-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="75ab7-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="75ab7-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="75ab7-121">OUTPUTS</span></span>

### <span data-ttu-id="75ab7-122">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="75ab7-122">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="75ab7-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="75ab7-123">NOTES</span></span>

## <span data-ttu-id="75ab7-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="75ab7-124">RELATED LINKS</span></span>

[<span data-ttu-id="75ab7-125">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="75ab7-125">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="75ab7-126">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="75ab7-126">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="75ab7-127">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="75ab7-127">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="75ab7-128">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="75ab7-128">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


