---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaService.md
ms.openlocfilehash: 8b1f4a10ab974f50a01ba0725285ccd7a3b7dffc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733043"
---
# <span data-ttu-id="69f2f-101">Get-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="69f2f-101">Get-AzureRmMediaService</span></span>

## <span data-ttu-id="69f2f-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="69f2f-102">SYNOPSIS</span></span>
<span data-ttu-id="69f2f-103">Получение сведений о службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="69f2f-103">Gets information about a media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69f2f-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="69f2f-104">SYNTAX</span></span>

### <span data-ttu-id="69f2f-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="69f2f-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="69f2f-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="69f2f-106">AccountNameParameterSet</span></span>
```
Get-AzureRmMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="69f2f-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="69f2f-107">DESCRIPTION</span></span>
<span data-ttu-id="69f2f-108">Командлет **Get-AzureRmMediaService** получает сведения о службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="69f2f-108">The **Get-AzureRmMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="69f2f-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="69f2f-109">EXAMPLES</span></span>

### <span data-ttu-id="69f2f-110">Пример 1: получение всех служб мультимедиа в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="69f2f-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="69f2f-111">Эта команда получает свойства для всех служб мультимедиа в группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="69f2f-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="69f2f-112">Пример 2: получение свойств службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="69f2f-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzureRmMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="69f2f-113">Эта команда получает свойства службы мультимедиа с именем MediaService1, которая относится к группе ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="69f2f-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="69f2f-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="69f2f-114">PARAMETERS</span></span>

### <span data-ttu-id="69f2f-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="69f2f-115">-AccountName</span></span>
<span data-ttu-id="69f2f-116">Указывает имя службы мультимедиа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="69f2f-116">Specifies the name of the media service that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: AccountNameParameterSet
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69f2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69f2f-117">-DefaultProfile</span></span>
<span data-ttu-id="69f2f-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="69f2f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="69f2f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69f2f-119">-ResourceGroupName</span></span>
<span data-ttu-id="69f2f-120">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="69f2f-120">Specifies the name of the resource group that contains the media service.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69f2f-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69f2f-121">CommonParameters</span></span>
<span data-ttu-id="69f2f-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="69f2f-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69f2f-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69f2f-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69f2f-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="69f2f-124">INPUTS</span></span>

### <span data-ttu-id="69f2f-125">Ничего</span><span class="sxs-lookup"><span data-stu-id="69f2f-125">None</span></span>
<span data-ttu-id="69f2f-126">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="69f2f-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="69f2f-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="69f2f-127">OUTPUTS</span></span>

### <span data-ttu-id="69f2f-128">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="69f2f-128">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="69f2f-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="69f2f-129">NOTES</span></span>

## <span data-ttu-id="69f2f-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="69f2f-130">RELATED LINKS</span></span>

[<span data-ttu-id="69f2f-131">New-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="69f2f-131">New-AzureRmMediaService</span></span>](./New-AzureRmMediaService.md)

[<span data-ttu-id="69f2f-132">Remove-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="69f2f-132">Remove-AzureRmMediaService</span></span>](./Remove-AzureRmMediaService.md)

[<span data-ttu-id="69f2f-133">Set-AzureRmMediaService</span><span class="sxs-lookup"><span data-stu-id="69f2f-133">Set-AzureRmMediaService</span></span>](./Set-AzureRmMediaService.md)


