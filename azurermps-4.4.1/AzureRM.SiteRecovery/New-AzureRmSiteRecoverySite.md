---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 7f8dfed861abd9d426a72c5d66f7c41b4efc947e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93559500"
---
# <span data-ttu-id="f3572-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="f3572-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="f3572-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f3572-102">SYNOPSIS</span></span>
<span data-ttu-id="f3572-103">Создает сайт восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="f3572-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3572-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f3572-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3572-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3572-105">DESCRIPTION</span></span>
<span data-ttu-id="f3572-106">Командлет **New-AzureRmSiteRecoverySite** создает сайт Azure Site Recovery в текущем хранилище.</span><span class="sxs-lookup"><span data-stu-id="f3572-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="f3572-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f3572-107">EXAMPLES</span></span>

## <span data-ttu-id="f3572-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f3572-108">PARAMETERS</span></span>

### <span data-ttu-id="f3572-109">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f3572-109">-Name</span></span>
<span data-ttu-id="f3572-110">Указывает имя сайта.</span><span class="sxs-lookup"><span data-stu-id="f3572-110">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3572-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3572-111">-DefaultProfile</span></span>
<span data-ttu-id="f3572-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f3572-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3572-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3572-113">CommonParameters</span></span>
<span data-ttu-id="f3572-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f3572-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3572-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3572-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3572-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f3572-116">INPUTS</span></span>

## <span data-ttu-id="f3572-117">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f3572-117">OUTPUTS</span></span>

## <span data-ttu-id="f3572-118">Пуск</span><span class="sxs-lookup"><span data-stu-id="f3572-118">NOTES</span></span>

## <span data-ttu-id="f3572-119">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f3572-119">RELATED LINKS</span></span>

[<span data-ttu-id="f3572-120">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="f3572-120">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="f3572-121">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="f3572-121">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
