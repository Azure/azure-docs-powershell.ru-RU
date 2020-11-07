---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.media/get-azurermmediaservicekeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 7aab48c69dc1e10d35c49de2d1dff427d5df2c41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93733835"
---
# <span data-ttu-id="cd2d6-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="cd2d6-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="cd2d6-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="cd2d6-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2d6-103">Получает сведения о ключах для доступа к конечной точке RESTFUL, связанной с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd2d6-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="cd2d6-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd2d6-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd2d6-105">DESCRIPTION</span></span>
<span data-ttu-id="cd2d6-106">Командлет **Get-AzureRmMediaServiceKeys** получает сведения о ключах для доступа к конечной точке пересылки состояния (RESTful), связанной с службой мультимедиа Azure.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="cd2d6-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="cd2d6-107">EXAMPLES</span></span>

### <span data-ttu-id="cd2d6-108">Пример 1: получение сведений о ключе для доступа к службе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="cd2d6-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="cd2d6-109">Эта команда получает сведения о ключе для доступа к службе мультимедиа с именем MediaService001, которая относится к группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="cd2d6-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="cd2d6-110">PARAMETERS</span></span>

### <span data-ttu-id="cd2d6-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="cd2d6-111">-AccountName</span></span>
<span data-ttu-id="cd2d6-112">Указывает имя службы мультимедиа, из которой этот командлет получает ключи службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="cd2d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2d6-113">-DefaultProfile</span></span>
<span data-ttu-id="cd2d6-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="cd2d6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd2d6-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd2d6-115">-ResourceGroupName</span></span>
<span data-ttu-id="cd2d6-116">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-116">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="cd2d6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2d6-117">CommonParameters</span></span>
<span data-ttu-id="cd2d6-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="cd2d6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2d6-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd2d6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2d6-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="cd2d6-120">INPUTS</span></span>

### <span data-ttu-id="cd2d6-121">System. String</span><span class="sxs-lookup"><span data-stu-id="cd2d6-121">System.String</span></span>

## <span data-ttu-id="cd2d6-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="cd2d6-122">OUTPUTS</span></span>

### <span data-ttu-id="cd2d6-123">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="cd2d6-123">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="cd2d6-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="cd2d6-124">NOTES</span></span>

## <span data-ttu-id="cd2d6-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cd2d6-125">RELATED LINKS</span></span>

[<span data-ttu-id="cd2d6-126">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="cd2d6-126">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


