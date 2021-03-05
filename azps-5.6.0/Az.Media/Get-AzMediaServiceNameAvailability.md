---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 23C6C9D3-A745-46C8-AB2C-B874223FBFFF
online version: https://docs.microsoft.com/powershell/module/az.media/get-azmediaservicenameavailability
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceNameAvailability.md
ms.openlocfilehash: d8928aea539910751c61ad03f5e5a4d67188e371
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960467"
---
# <span data-ttu-id="61990-101">Get-AzMediaServiceNameAvailability</span><span class="sxs-lookup"><span data-stu-id="61990-101">Get-AzMediaServiceNameAvailability</span></span>

## <span data-ttu-id="61990-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61990-102">SYNOPSIS</span></span>
<span data-ttu-id="61990-103">Проверяет, доступно ли имя службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="61990-103">Checks whether a media service name is available.</span></span>
<span data-ttu-id="61990-104">Имена служб мультимедиа являются уникальными глобально.</span><span class="sxs-lookup"><span data-stu-id="61990-104">Media service names are globally unique.</span></span>

## <span data-ttu-id="61990-105">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="61990-105">SYNTAX</span></span>

```
Get-AzMediaServiceNameAvailability [-DefaultProfile <IAzureContextContainer>] [-AccountName] <String>
 [<CommonParameters>]
```

## <span data-ttu-id="61990-106">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="61990-106">DESCRIPTION</span></span>
<span data-ttu-id="61990-107">Для проверки доступности имени медиа-службы будет доступен ли такой служарныйлет **Get-AzMediaServiceNameAvailability.**</span><span class="sxs-lookup"><span data-stu-id="61990-107">The **Get-AzMediaServiceNameAvailability** cmdlet checks whether a media service name is available.</span></span>
<span data-ttu-id="61990-108">Имена служб мультимедиа являются уникальными глобально.</span><span class="sxs-lookup"><span data-stu-id="61990-108">Media service names are globally unique.</span></span>

## <span data-ttu-id="61990-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="61990-109">EXAMPLES</span></span>

### <span data-ttu-id="61990-110">Пример 1. Проверка на наличии имени службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="61990-110">Example 1: Check whether a Media Service name is available</span></span>
```
PS C:\>Get-AzMediaServiceNameAvailability -AccountName "MediaService1"
```

<span data-ttu-id="61990-111">Эта команда проверяет, доступно ли имя MediaService1.</span><span class="sxs-lookup"><span data-stu-id="61990-111">This command checks if the name MediaService1 is available.</span></span>

## <span data-ttu-id="61990-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61990-112">PARAMETERS</span></span>

### <span data-ttu-id="61990-113">-AccountName</span><span class="sxs-lookup"><span data-stu-id="61990-113">-AccountName</span></span>
<span data-ttu-id="61990-114">Указывает имя службы мультимедиа, которая получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="61990-114">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="61990-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61990-115">-DefaultProfile</span></span>
<span data-ttu-id="61990-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="61990-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61990-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61990-117">CommonParameters</span></span>
<span data-ttu-id="61990-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61990-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61990-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="61990-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61990-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="61990-120">INPUTS</span></span>

### <span data-ttu-id="61990-121">Нет</span><span class="sxs-lookup"><span data-stu-id="61990-121">None</span></span>

## <span data-ttu-id="61990-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="61990-122">OUTPUTS</span></span>

### <span data-ttu-id="61990-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span><span class="sxs-lookup"><span data-stu-id="61990-123">Microsoft.Azure.Commands.Media.Models.PSCheckNameAvailabilityOutput</span></span>

## <span data-ttu-id="61990-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="61990-124">NOTES</span></span>

## <span data-ttu-id="61990-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="61990-125">RELATED LINKS</span></span>

[<span data-ttu-id="61990-126">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="61990-126">Get-AzMediaService</span></span>](./Get-AzMediaService.md)

[<span data-ttu-id="61990-127">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="61990-127">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="61990-128">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="61990-128">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="61990-129">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="61990-129">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


