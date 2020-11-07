---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 9843D191-CBC4-481A-BD36-D7B2D7917BD9
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaService.md
ms.openlocfilehash: a6d1ff6d169fab90fa866e94577ce9b3f9580a4b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93720379"
---
# <span data-ttu-id="59976-101">Get-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="59976-101">Get-AzMediaService</span></span>

## <span data-ttu-id="59976-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="59976-102">SYNOPSIS</span></span>
<span data-ttu-id="59976-103">Получение сведений о службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59976-103">Gets information about a media service.</span></span>

## <span data-ttu-id="59976-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="59976-104">SYNTAX</span></span>

### <span data-ttu-id="59976-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="59976-105">ResourceGroupParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59976-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59976-106">AccountNameParameterSet</span></span>
```
Get-AzMediaService [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59976-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="59976-107">DESCRIPTION</span></span>
<span data-ttu-id="59976-108">Командлет **Get-AzMediaService** получает сведения о службе мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59976-108">The **Get-AzMediaService** cmdlet gets information about a media service.</span></span>

## <span data-ttu-id="59976-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="59976-109">EXAMPLES</span></span>

### <span data-ttu-id="59976-110">Пример 1: получение всех служб мультимедиа в группе ресурсов</span><span class="sxs-lookup"><span data-stu-id="59976-110">Example 1: Get all media services in a resource group</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup001"
```

<span data-ttu-id="59976-111">Эта команда получает свойства для всех служб мультимедиа в группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="59976-111">This command gets properties for all media services in the resource group named ResourceGroup001.</span></span>

### <span data-ttu-id="59976-112">Пример 2: получение свойств службы мультимедиа</span><span class="sxs-lookup"><span data-stu-id="59976-112">Example 2: Get media service properties</span></span>
```
PS C:\>Get-AzMediaService -ResourceGroupName "ResourceGroup002" -AccountName "MediaService1"
```

<span data-ttu-id="59976-113">Эта команда получает свойства службы мультимедиа с именем MediaService1, которая относится к группе ресурсов с именем ResourceGroup002.</span><span class="sxs-lookup"><span data-stu-id="59976-113">This command gets the properties of the media service named MediaService1 that belongs to the resource group named ResourceGroup002.</span></span>

## <span data-ttu-id="59976-114">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="59976-114">PARAMETERS</span></span>

### <span data-ttu-id="59976-115">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="59976-115">-AccountName</span></span>
<span data-ttu-id="59976-116">Указывает имя службы мультимедиа, которую получает этот командлет.</span><span class="sxs-lookup"><span data-stu-id="59976-116">Specifies the name of the media service that this cmdlet gets.</span></span>

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

### <span data-ttu-id="59976-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59976-117">-DefaultProfile</span></span>
<span data-ttu-id="59976-118">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="59976-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="59976-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59976-119">-ResourceGroupName</span></span>
<span data-ttu-id="59976-120">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="59976-120">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="59976-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59976-121">CommonParameters</span></span>
<span data-ttu-id="59976-122">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="59976-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59976-123">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59976-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59976-124">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="59976-124">INPUTS</span></span>

### <span data-ttu-id="59976-125">System. String</span><span class="sxs-lookup"><span data-stu-id="59976-125">System.String</span></span>

## <span data-ttu-id="59976-126">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="59976-126">OUTPUTS</span></span>

### <span data-ttu-id="59976-127">Microsoft. Azure. Commands. Media. Models. PSMediaService</span><span class="sxs-lookup"><span data-stu-id="59976-127">Microsoft.Azure.Commands.Media.Models.PSMediaService</span></span>

## <span data-ttu-id="59976-128">Пуск</span><span class="sxs-lookup"><span data-stu-id="59976-128">NOTES</span></span>

## <span data-ttu-id="59976-129">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="59976-129">RELATED LINKS</span></span>

[<span data-ttu-id="59976-130">New-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="59976-130">New-AzMediaService</span></span>](./New-AzMediaService.md)

[<span data-ttu-id="59976-131">Remove-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="59976-131">Remove-AzMediaService</span></span>](./Remove-AzMediaService.md)

[<span data-ttu-id="59976-132">Set-AzMediaService</span><span class="sxs-lookup"><span data-stu-id="59976-132">Set-AzMediaService</span></span>](./Set-AzMediaService.md)


