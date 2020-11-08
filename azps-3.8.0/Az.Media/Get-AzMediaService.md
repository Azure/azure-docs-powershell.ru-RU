---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94074535"
---
# <span data-ttu-id="331e9-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="331e9-101">Get-AzMediaService</span></span>

## <span data-ttu-id="331e9-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="331e9-102">SYNOPSIS</span></span>
<span data-ttu-id="331e9-103">Получение сведений о службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="331e9-103">Gets information about a media service.</span></span>

## <span data-ttu-id="331e9-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="331e9-104">SYNTAX</span></span>

### <span data-ttu-id="331e9-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="331e9-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="331e9-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="331e9-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="331e9-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="331e9-107">DESCRIPTION</span></span>
<span data-ttu-id="331e9-108">Командлет **Get-AzMediaService** получает сведения о службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="331e9-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="331e9-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="331e9-109">EXAMPLES</span></span>

### <span data-ttu-id="331e9-110">Пример 1: получение всех служб мультимедиа в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="331e9-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="331e9-111">Эта команда получает свойства для всех служб мультимедиа в группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="331e9-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="331e9-112">Пример 2: получение свойств службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="331e9-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="331e9-113">Эта команда получает свойства службы мультимедиа с именем MediaService1, которая относится к группе ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="331e9-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="331e9-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="331e9-114">PARAMETERS</span></span>

### <span data-ttu-id="331e9-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="331e9-115">-AccountName</span></span>
<span data-ttu-id="331e9-116">Указывает имя службы мультимедиа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="331e9-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="331e9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="331e9-117">-DefaultProfile</span></span>
<span data-ttu-id="331e9-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="331e9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="331e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="331e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="331e9-120">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="331e9-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="331e9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="331e9-121">CommonParameters</span></span>
<span data-ttu-id="331e9-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="331e9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="331e9-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="331e9-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="331e9-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="331e9-124">INPUTS</span></span>

### <span data-ttu-id="331e9-125">System. String</span><span class="sxs-lookup"><span data-stu-id="331e9-125">System.String</span></span>

## <span data-ttu-id="331e9-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="331e9-126">OUTPUTS</span></span>

### <span data-ttu-id="331e9-127">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="331e9-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="331e9-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="331e9-128">NOTES</span></span>

## <span data-ttu-id="331e9-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="331e9-129">RELATED LINKS</span></span>

[<span data-ttu-id="331e9-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="331e9-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="331e9-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="331e9-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="331e9-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="331e9-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


