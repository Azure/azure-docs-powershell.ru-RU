---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: d54314686edafba9e72872411c678905adc55f47
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734817"
---
# <span data-ttu-id="644f7-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="644f7-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="644f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="644f7-102">SYNOPSIS</span></span>
<span data-ttu-id="644f7-103">Получение сведений о службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="644f7-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="644f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="644f7-104">SYNTAX</span></span>

### <span data-ttu-id="644f7-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="644f7-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="644f7-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="644f7-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="644f7-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="644f7-107">DESCRIPTION</span></span>
<span data-ttu-id="644f7-108">Командлет **Get-AzureRmMediaService** получает сведения о службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="644f7-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="644f7-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="644f7-109">EXAMPLES</span></span>

### <span data-ttu-id="644f7-110">Пример 1: получение всех служб мультимедиа в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="644f7-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="644f7-111">Эта команда получает свойства для всех служб мультимедиа в группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="644f7-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="644f7-112">Пример 2: получение свойств службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="644f7-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="644f7-113">Эта команда получает свойства службы мультимедиа с именем MediaService1, которая относится к группе ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="644f7-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="644f7-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="644f7-114">PARAMETERS</span></span>

### <span data-ttu-id="644f7-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="644f7-115">-AccountName</span></span>
<span data-ttu-id="644f7-116">Указывает имя службы мультимедиа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="644f7-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644f7-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="644f7-117">-ResourceGroupName</span></span>
<span data-ttu-id="644f7-118">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="644f7-118">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="644f7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="644f7-119">-DefaultProfile</span></span>
<span data-ttu-id="644f7-120">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="644f7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="644f7-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="644f7-121">CommonParameters</span></span>
<span data-ttu-id="644f7-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="644f7-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="644f7-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="644f7-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="644f7-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="644f7-124">INPUTS</span></span>

## <span data-ttu-id="644f7-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="644f7-125">OUTPUTS</span></span>

### <span data-ttu-id="644f7-126">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="644f7-126">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="644f7-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="644f7-127">NOTES</span></span>

## <span data-ttu-id="644f7-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="644f7-128">RELATED LINKS</span></span>

[<span data-ttu-id="644f7-129">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="644f7-129">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="644f7-130">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="644f7-130">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="644f7-131">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="644f7-131">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


