---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d7718ffafd6383e0873e61955cd231ca8b6a409d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94243502"
---
# <span data-ttu-id="f10a2-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="f10a2-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="f10a2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f10a2-102">SYNOPSIS</span></span>
<span data-ttu-id="f10a2-103">Проверяет, доступно ли имя службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f10a2-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="f10a2-104">Имена служб мультимедиа глобально уникальны.</span><span class="sxs-lookup"><span data-stu-id="f10a2-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="f10a2-105">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f10a2-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="f10a2-106">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f10a2-106">DESCRIPTION</span></span>
<span data-ttu-id="f10a2-107">Командлет **Get-AzMediaServiceNameAvailability** проверяет, доступно ли имя службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f10a2-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="f10a2-108">Имена служб мультимедиа глобально уникальны.</span><span class="sxs-lookup"><span data-stu-id="f10a2-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="f10a2-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f10a2-109">EXAMPLES</span></span>

### <span data-ttu-id="f10a2-110">Пример 1: Проверка наличия имени службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f10a2-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="f10a2-111">Эта команда проверяет, доступно ли имя MediaService1.</span><span class="sxs-lookup"><span data-stu-id="f10a2-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="f10a2-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f10a2-112">PARAMETERS</span></span>

### <span data-ttu-id="f10a2-113">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f10a2-113">-AccountName</span></span>
<span data-ttu-id="f10a2-114">Указывает имя службы мультимедиа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="f10a2-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="f10a2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f10a2-115">-DefaultProfile</span></span>
<span data-ttu-id="f10a2-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="f10a2-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f10a2-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f10a2-117">CommonParameters</span></span>
<span data-ttu-id="f10a2-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f10a2-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f10a2-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f10a2-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f10a2-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f10a2-120">INPUTS</span></span>

### <span data-ttu-id="f10a2-121">Ничего</span><span class="sxs-lookup"><span data-stu-id="f10a2-121">None</span></span>

## <span data-ttu-id="f10a2-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f10a2-122">OUTPUTS</span></span>

### <span data-ttu-id="f10a2-123">Microsoft. Azure. Commands. Media. Models. PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="f10a2-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="f10a2-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="f10a2-124">NOTES</span></span>

## <span data-ttu-id="f10a2-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f10a2-125">RELATED LINKS</span></span>

[<span data-ttu-id="f10a2-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f10a2-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="f10a2-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f10a2-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="f10a2-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f10a2-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="f10a2-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="f10a2-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


