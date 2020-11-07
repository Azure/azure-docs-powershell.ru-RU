---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 7311F66C-3370-4436-8030-6D98D42C3112
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimagepublisher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImagePublisher.md
ms.openlocfilehash: f2b0cd955cd63eb6066da43e8b468ab4ea9bb0bd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93721900"
---
# <span data-ttu-id="d220b-101">Get-AzVMImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d220b-101">Get-AzVMImagePublisher</span></span>

## <span data-ttu-id="d220b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="d220b-102">SYNOPSIS</span></span>
<span data-ttu-id="d220b-103">Получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="d220b-103">Gets the VMImage publishers.</span></span>

## <span data-ttu-id="d220b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="d220b-104">SYNTAX</span></span>

```
Get-AzVMImagePublisher -Location <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d220b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d220b-105">DESCRIPTION</span></span>
<span data-ttu-id="d220b-106">Командлет **Get-AzVMImagePublisher** получает издатели VMImage.</span><span class="sxs-lookup"><span data-stu-id="d220b-106">The **Get-AzVMImagePublisher** cmdlet gets the VMImage publishers.</span></span>

## <span data-ttu-id="d220b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="d220b-107">EXAMPLES</span></span>

### <span data-ttu-id="d220b-108">Пример 1: получение VMImageных издателей для региона</span><span class="sxs-lookup"><span data-stu-id="d220b-108">Example 1: Get VMImage publishers for a region</span></span>
```
PS C:\> Get-AzVMImagePublisher -Location "Central US"
```

<span data-ttu-id="d220b-109">Эта команда получает издателей экземпляров VMImage для Центральной области США в вашем профиле Azure.</span><span class="sxs-lookup"><span data-stu-id="d220b-109">This command gets the publishers of VMImage instances for the Central US region within your Azure profile.</span></span>

## <span data-ttu-id="d220b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="d220b-110">PARAMETERS</span></span>

### <span data-ttu-id="d220b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d220b-111">-DefaultProfile</span></span>
<span data-ttu-id="d220b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d220b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d220b-113">-Location</span><span class="sxs-lookup"><span data-stu-id="d220b-113">-Location</span></span>
<span data-ttu-id="d220b-114">Указывает расположение VMImage.</span><span class="sxs-lookup"><span data-stu-id="d220b-114">Specifies the location of the VMImage.</span></span>

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

### <span data-ttu-id="d220b-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d220b-115">CommonParameters</span></span>
<span data-ttu-id="d220b-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="d220b-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d220b-117">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d220b-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d220b-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="d220b-118">INPUTS</span></span>

### <span data-ttu-id="d220b-119">System. String</span><span class="sxs-lookup"><span data-stu-id="d220b-119">System.String</span></span>

## <span data-ttu-id="d220b-120">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="d220b-120">OUTPUTS</span></span>

### <span data-ttu-id="d220b-121">Microsoft. Azure. Commands. COMPUTE. Models. PSVirtualMachineImagePublisher</span><span class="sxs-lookup"><span data-stu-id="d220b-121">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImagePublisher</span></span>

## <span data-ttu-id="d220b-122">Пуск</span><span class="sxs-lookup"><span data-stu-id="d220b-122">NOTES</span></span>

## <span data-ttu-id="d220b-123">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d220b-123">RELATED LINKS</span></span>

[<span data-ttu-id="d220b-124">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d220b-124">Get-AzVMImage</span></span>](./Get-AzVMImage.md)

[<span data-ttu-id="d220b-125">Get-AzVMImageOffer</span><span class="sxs-lookup"><span data-stu-id="d220b-125">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="d220b-126">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="d220b-126">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="d220b-127">Сохранить — AzVMImage</span><span class="sxs-lookup"><span data-stu-id="d220b-127">Save-AzVMImage</span></span>](./Save-AzVMImage.md)


