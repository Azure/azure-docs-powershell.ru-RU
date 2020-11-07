---
external help file: Microsoft.Azure.Commands.Media.dll-Help.xml
Module Name: AzureRM.Media
ms.assetid: 2099938F-5325-416C-AE10-6813546A1055
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Media/Commands.Media/help/Get-AzureRmMediaServiceKeys.md
ms.openlocfilehash: 6cef357b636a48e433d545a56d2b5105556842da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734815"
---
# <span data-ttu-id="f45f7-101">Get-AzureRmMediaServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f45f7-101">Get-AzureRmMediaServiceKeys</span></span>

## <span data-ttu-id="f45f7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f45f7-102">SYNOPSIS</span></span>
<span data-ttu-id="f45f7-103">Получает сведения о ключах для доступа к конечной точке RESTFUL, связанной с службой мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f45f7-103">Gets key information for accessing the REST endpoint associated with the media service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f45f7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f45f7-104">SYNTAX</span></span>

```
Get-AzureRmMediaServiceKeys [-ResourceGroupName] <String> [-AccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f45f7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f45f7-105">DESCRIPTION</span></span>
<span data-ttu-id="f45f7-106">Командлет **Get-AzureRmMediaServiceKeys** получает сведения о ключах для доступа к конечной точке пересылки состояния (RESTful), связанной с службой мультимедиа Azure.</span><span class="sxs-lookup"><span data-stu-id="f45f7-106">The **Get-AzureRmMediaServiceKeys** cmdlet gets key information for accessing the Representational State Transfer (REST) endpoint associated with the Azure media service.</span></span>

## <span data-ttu-id="f45f7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f45f7-107">EXAMPLES</span></span>

### <span data-ttu-id="f45f7-108">Пример 1: получение сведений о ключе для доступа к службе мультимедиа</span><span class="sxs-lookup"><span data-stu-id="f45f7-108">Example 1: Get the key information for accessing the media service</span></span>
```
PS C:\>Get-AzureRmMediaServiceKeys -ResourceGroupName "ResourceGroup001" -AccountName "MediaService001"
```

<span data-ttu-id="f45f7-109">Эта команда получает сведения о ключе для доступа к службе мультимедиа с именем MediaService001, которая относится к группе ресурсов с именем ResourceGroup001.</span><span class="sxs-lookup"><span data-stu-id="f45f7-109">This command gets the key information for accessing the media service named MediaService001 that belongs to the resource group named ResourceGroup001.</span></span>

## <span data-ttu-id="f45f7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f45f7-110">PARAMETERS</span></span>

### <span data-ttu-id="f45f7-111">-Имя_учетной_записи</span><span class="sxs-lookup"><span data-stu-id="f45f7-111">-AccountName</span></span>
<span data-ttu-id="f45f7-112">Указывает имя службы мультимедиа, из которой этот командлет получает ключи службы мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f45f7-112">Specifies the name of the media service that this cmdlet gets the media service keys from.</span></span>

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

### <span data-ttu-id="f45f7-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45f7-113">-ResourceGroupName</span></span>
<span data-ttu-id="f45f7-114">Указывает имя группы ресурсов, в которой находится служба мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="f45f7-114">Specifies the name of the resource group that contains the media service.</span></span>

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

### <span data-ttu-id="f45f7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45f7-115">-DefaultProfile</span></span>
<span data-ttu-id="f45f7-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f45f7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f45f7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45f7-117">CommonParameters</span></span>
<span data-ttu-id="f45f7-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f45f7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45f7-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f45f7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45f7-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f45f7-120">INPUTS</span></span>

## <span data-ttu-id="f45f7-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f45f7-121">OUTPUTS</span></span>

### <span data-ttu-id="f45f7-122">Microsoft. Azure. Commands. Media. Models. PSServiceKeys</span><span class="sxs-lookup"><span data-stu-id="f45f7-122">Microsoft.Azure.Commands.Media.Models.PSServiceKeys</span></span>

## <span data-ttu-id="f45f7-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="f45f7-123">NOTES</span></span>

## <span data-ttu-id="f45f7-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f45f7-124">RELATED LINKS</span></span>

[<span data-ttu-id="f45f7-125">Set-AzureRmMediaServiceKey</span><span class="sxs-lookup"><span data-stu-id="f45f7-125">Set-AzureRmMediaServiceKey</span></span>](./Set-AzureRmMediaServiceKey.md)


