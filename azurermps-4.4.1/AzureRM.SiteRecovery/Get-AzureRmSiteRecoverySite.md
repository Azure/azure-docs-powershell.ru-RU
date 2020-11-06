---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: F9A652D0-26D9-4F3F-A365-285B05AA7C0B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Get-AzureRmSiteRecoverySite.md
ms.openlocfilehash: e41b491611ebc5dda1da56ac26827c5fa547dd4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562092"
---
# <span data-ttu-id="0d24a-101">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0d24a-101">Get-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="0d24a-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0d24a-102">SYNOPSIS</span></span>
<span data-ttu-id="0d24a-103">Получает сайты Hyper-V из хранилища сайтов для восстановления.</span><span class="sxs-lookup"><span data-stu-id="0d24a-103">Gets the Hyper-V sites from the Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d24a-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0d24a-104">SYNTAX</span></span>

### <span data-ttu-id="0d24a-105">По умолчанию (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="0d24a-105">Default (Default)</span></span>
```
Get-AzureRmSiteRecoverySite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d24a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="0d24a-106">ByName</span></span>
```
Get-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0d24a-107">ByFriendlyName</span><span class="sxs-lookup"><span data-stu-id="0d24a-107">ByFriendlyName</span></span>
```
Get-AzureRmSiteRecoverySite -FriendlyName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0d24a-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d24a-108">DESCRIPTION</span></span>
<span data-ttu-id="0d24a-109">Командлет **Get-AzureRmSiteRecoverySite** получает сайты Hyper-V в хранилище Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="0d24a-109">The **Get-AzureRmSiteRecoverySite** cmdlet gets the Hyper-V sites in the Azure Site Recovery vault.</span></span>

## <span data-ttu-id="0d24a-110">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0d24a-110">EXAMPLES</span></span>

## <span data-ttu-id="0d24a-111">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0d24a-111">PARAMETERS</span></span>

### <span data-ttu-id="0d24a-112">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="0d24a-112">-FriendlyName</span></span>
<span data-ttu-id="0d24a-113">Указывает понятное имя сайта.</span><span class="sxs-lookup"><span data-stu-id="0d24a-113">Specifies the friendly name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFriendlyName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d24a-114">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="0d24a-114">-Name</span></span>
<span data-ttu-id="0d24a-115">Указывает имя сайта.</span><span class="sxs-lookup"><span data-stu-id="0d24a-115">Specifies the name of the site.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0d24a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d24a-116">-DefaultProfile</span></span>
<span data-ttu-id="0d24a-117">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0d24a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d24a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d24a-118">CommonParameters</span></span>
<span data-ttu-id="0d24a-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0d24a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d24a-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d24a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d24a-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0d24a-121">INPUTS</span></span>

## <span data-ttu-id="0d24a-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0d24a-122">OUTPUTS</span></span>

### <span data-ttu-id="0d24a-123">System. Collections. Generic. List ' 1 [Microsoft. Azure. SiteRecovery. ASRSite]</span><span class="sxs-lookup"><span data-stu-id="0d24a-123">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.SiteRecovery.ASRSite]</span></span>

## <span data-ttu-id="0d24a-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="0d24a-124">NOTES</span></span>

## <span data-ttu-id="0d24a-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0d24a-125">RELATED LINKS</span></span>

[<span data-ttu-id="0d24a-126">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0d24a-126">New-AzureRmSiteRecoverySite</span></span>](./New-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="0d24a-127">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="0d24a-127">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
