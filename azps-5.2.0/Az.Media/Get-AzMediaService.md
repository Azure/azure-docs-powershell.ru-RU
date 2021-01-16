---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: bd1f3f2d202e21f12ba7bd111853473094d042e0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98410348"
---
# <span data-ttu-id="c2c42-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c2c42-101">Get-AzMediaService</span></span>

## <span data-ttu-id="c2c42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2c42-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c42-103">Получает сведения о службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c2c42-103">Gets information about a media service.</span></span>

## <span data-ttu-id="c2c42-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2c42-104">SYNTAX</span></span>

### <span data-ttu-id="c2c42-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2c42-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c2c42-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2c42-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2c42-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2c42-107">DESCRIPTION</span></span>
<span data-ttu-id="c2c42-108">Для **получения сведений о** службе мультимедиа вы можете получить сведения о его службе.</span><span class="sxs-lookup"><span data-stu-id="c2c42-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="c2c42-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2c42-109">EXAMPLES</span></span>

### <span data-ttu-id="c2c42-110">Пример 1. Получить все службы мультимедиа в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="c2c42-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="c2c42-111">Эта команда получает свойства для всех служб мультимедиа в группе ресурсов ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="c2c42-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="c2c42-112">Пример 2. Свойства службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="c2c42-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="c2c42-113">Эта команда получает свойства службы мультимедиа MediaService1, которая принадлежит к группе ресурсов ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="c2c42-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="c2c42-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2c42-114">PARAMETERS</span></span>

### <span data-ttu-id="c2c42-115">-AccountName</span><span class="sxs-lookup"><span data-stu-id="c2c42-115">-AccountName</span></span>
<span data-ttu-id="c2c42-116">Указывает имя службы мультимедиа, которую получает этот cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2c42-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="c2c42-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c42-117">-DefaultProfile</span></span>
<span data-ttu-id="c2c42-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="c2c42-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2c42-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2c42-119">-ResourceGroupName</span></span>
<span data-ttu-id="c2c42-120">Имя группы ресурсов, которая содержит службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="c2c42-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="c2c42-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c42-121">CommonParameters</span></span>
<span data-ttu-id="c2c42-122">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2c42-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c42-123">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c42-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c42-124">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2c42-124">INPUTS</span></span>

### <span data-ttu-id="c2c42-125">System.String</span><span class="sxs-lookup"><span data-stu-id="c2c42-125">System.String</span></span>

## <span data-ttu-id="c2c42-126">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2c42-126">OUTPUTS</span></span>

### <span data-ttu-id="c2c42-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span><span class="sxs-lookup"><span data-stu-id="c2c42-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="c2c42-128">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2c42-128">NOTES</span></span>

## <span data-ttu-id="c2c42-129">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2c42-129">RELATED LINKS</span></span>

[<span data-ttu-id="c2c42-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c2c42-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="c2c42-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c2c42-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="c2c42-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="c2c42-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


