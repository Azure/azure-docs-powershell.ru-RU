---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Media.dll-Help.xml
Module Name: Az.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/az.media/get-azmediaservicekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Media/Media/help/Get-AzMediaServiceKey.md
ms.openlocfilehash: a01aeaa5868ece4f376dd5be934ba1029379958b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506219"
---
# <span data-ttu-id="73535-101">Get-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="73535-101">Get-AzMediaServiceKey</span></span>

## <span data-ttu-id="73535-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73535-102">SYNOPSIS</span></span>
<span data-ttu-id="73535-103">Получает основные сведения о доступе к конечной точке REST, связанной со службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="73535-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

## <span data-ttu-id="73535-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="73535-104">SYNTAX</span></span>

```
Get-AzMediaServiceKey [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73535-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="73535-105">DESCRIPTION</span></span>
<span data-ttu-id="73535-106">Для доступа к конечной точке REST, связанной со службой мультимедиа Azure, с помощью cmdlet **Get-AzMediaServiceKey** вы получаете основные сведения.</span><span class="sxs-lookup"><span data-stu-id="73535-106">The **Get-AzMediaServiceKey** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="73535-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="73535-107">EXAMPLES</span></span>

### <span data-ttu-id="73535-108">Пример 1. Получите основные сведения о доступе к службе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="73535-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzMediaServiceKey -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="73535-109">Эта команда получает основные сведения о доступе к службе мультимедиа MediaService001, которая принадлежит к группе ресурсов ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="73535-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="73535-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73535-110">PARAMETERS</span></span>

### <span data-ttu-id="73535-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="73535-111">-AccountName</span></span>
<span data-ttu-id="73535-112">Указывает имя службы мультимедиа, из которую этот cmdlet получает ключи службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="73535-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="73535-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73535-113">-DefaultProfile</span></span>
<span data-ttu-id="73535-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="73535-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="73535-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73535-115">-ResourceGroupName</span></span>
<span data-ttu-id="73535-116">Имя группы ресурсов, которая содержит службу мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="73535-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="73535-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73535-117">CommonParameters</span></span>
<span data-ttu-id="73535-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73535-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73535-119">Дополнительные сведения см. в about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73535-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73535-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="73535-120">INPUTS</span></span>

### <span data-ttu-id="73535-121">System.String</span><span class="sxs-lookup"><span data-stu-id="73535-121">System.String</span></span>

## <span data-ttu-id="73535-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="73535-122">OUTPUTS</span></span>

### <span data-ttu-id="73535-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="73535-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="73535-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="73535-124">NOTES</span></span>

## <span data-ttu-id="73535-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="73535-125">RELATED LINKS</span></span>

[<span data-ttu-id="73535-126">Set-AzMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="73535-126">Set-AzMediaServiceKey</span></span>](./Set-AzMediaServiceKey.md)


