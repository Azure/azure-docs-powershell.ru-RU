---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceNameAvailability.md
ms.openlocfilehash: be459183e47982fef8dbd2376ddd5110251bb001
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733701"
---
# <span data-ttu-id="62f1e-101">Get-AzureRmMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="62f1e-101">Get-AzureRmMediaServiceNameAvailability</span></span>

## <span data-ttu-id="62f1e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="62f1e-102">SYNOPSIS</span></span>
<span data-ttu-id="62f1e-103">Проверяет, доступно ли имя службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="62f1e-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="62f1e-104">Имена служб мультимедиа глобально уникальны.</span><span class="sxs-lookup"><span data-stu-id="62f1e-104">Media service names are globally unique.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62f1e-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="62f1e-105">SYNTAX</span></span>

```
Get-AzureRmMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="62f1e-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="62f1e-106">DESCRIPTION</span></span>
<span data-ttu-id="62f1e-107">Командлет **Get-AzureRmMediaServiceNameAvailability** проверяет, доступно ли имя службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="62f1e-107">The **Get-AzureRmMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="62f1e-108">Имена служб мультимедиа глобально уникальны.</span><span class="sxs-lookup"><span data-stu-id="62f1e-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="62f1e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="62f1e-109">EXAMPLES</span></span>

### <span data-ttu-id="62f1e-110">Пример 1: Проверка наличия имени службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="62f1e-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzureRmMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="62f1e-111">Эта команда проверяет, доступно ли имя MediaService1.</span><span class="sxs-lookup"><span data-stu-id="62f1e-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="62f1e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="62f1e-112">PARAMETERS</span></span>

### <span data-ttu-id="62f1e-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="62f1e-113">-AccountName</span></span>
<span data-ttu-id="62f1e-114">Указывает имя службы мультимедиа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="62f1e-114">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62f1e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f1e-115">-DefaultProfile</span></span>
<span data-ttu-id="62f1e-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="62f1e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62f1e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f1e-117">CommonParameters</span></span>
<span data-ttu-id="62f1e-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="62f1e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f1e-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62f1e-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f1e-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="62f1e-120">INPUTS</span></span>

## <span data-ttu-id="62f1e-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="62f1e-121">OUTPUTS</span></span>

### <span data-ttu-id="62f1e-122">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="62f1e-122">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="62f1e-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="62f1e-123">NOTES</span></span>

## <span data-ttu-id="62f1e-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="62f1e-124">RELATED LINKS</span></span>

[<span data-ttu-id="62f1e-125">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="62f1e-125">Get-AzureRmMediaService</span></span>](./Get-AzureRmMediaService.md)

[<span data-ttu-id="62f1e-126">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="62f1e-126">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="62f1e-127">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="62f1e-127">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="62f1e-128">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="62f1e-128">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


