---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
ms.assetid: 0EB9F1C9-54CC-4794-9E37-108342341FE5
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/set-azcdnorigin
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Set-AzCdnOrigin.md
ms.openlocfilehash: 71f5732f7473a90af0509d2e3932ca5151ef870a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93727570"
---
# <span data-ttu-id="4a453-101">Set-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="4a453-101">Set-AzCdnOrigin</span></span>

## <span data-ttu-id="4a453-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4a453-102">SYNOPSIS</span></span>
<span data-ttu-id="4a453-103">Обновляет сервер источника CDN.</span><span class="sxs-lookup"><span data-stu-id="4a453-103">Updates a CDN origin server.</span></span>

## <span data-ttu-id="4a453-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4a453-104">SYNTAX</span></span>

```
Set-AzCdnOrigin -CdnOrigin <PSOrigin> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a453-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a453-105">DESCRIPTION</span></span>
<span data-ttu-id="4a453-106">Командлет **Set-AzCdnOrigin** обновляет сервер происхождения сети доставки содержимого (CDN) Azure.</span><span class="sxs-lookup"><span data-stu-id="4a453-106">The **Set-AzCdnOrigin** cmdlet updates an Azure Content Delivery Network (CDN) origin server.</span></span>

## <span data-ttu-id="4a453-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4a453-107">EXAMPLES</span></span>

## <span data-ttu-id="4a453-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4a453-108">PARAMETERS</span></span>

### <span data-ttu-id="4a453-109">-CdnOrigin</span><span class="sxs-lookup"><span data-stu-id="4a453-109">-CdnOrigin</span></span>
<span data-ttu-id="4a453-110">Указывает исходный сервер, который обновляется этим командлетом.</span><span class="sxs-lookup"><span data-stu-id="4a453-110">Specifies the origin server that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a453-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a453-111">-DefaultProfile</span></span>
<span data-ttu-id="4a453-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="4a453-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4a453-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a453-113">CommonParameters</span></span>
<span data-ttu-id="4a453-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4a453-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a453-115">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4a453-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a453-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4a453-116">INPUTS</span></span>

### <span data-ttu-id="4a453-117">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="4a453-117">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="4a453-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4a453-118">OUTPUTS</span></span>

### <span data-ttu-id="4a453-119">Microsoft. Azure. Commands. CDN. Models. Origin. PSOrigin</span><span class="sxs-lookup"><span data-stu-id="4a453-119">Microsoft.Azure.Commands.Cdn.Models.Origin.PSOrigin</span></span>

## <span data-ttu-id="4a453-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="4a453-120">NOTES</span></span>

## <span data-ttu-id="4a453-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4a453-121">RELATED LINKS</span></span>

[<span data-ttu-id="4a453-122">Get-AzCdnOrigin</span><span class="sxs-lookup"><span data-stu-id="4a453-122">Get-AzCdnOrigin</span></span>](./Get-AzCdnOrigin.md)


