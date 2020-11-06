---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: D0336AB5-019F-4EFD-88D2-63E12BA1ED95
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoverysite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoverySite.md
ms.openlocfilehash: 053cd7695768be44cf3cecc5964e037f12f0b84e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93566095"
---
# <span data-ttu-id="20807-101">New-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="20807-101">New-AzureRmSiteRecoverySite</span></span>

## <span data-ttu-id="20807-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="20807-102">SYNOPSIS</span></span>
<span data-ttu-id="20807-103">Создает сайт восстановления сайта.</span><span class="sxs-lookup"><span data-stu-id="20807-103">Creates a Site Recovery site.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20807-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="20807-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoverySite -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20807-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="20807-105">DESCRIPTION</span></span>
<span data-ttu-id="20807-106">Командлет **New-AzureRmSiteRecoverySite** создает сайт Azure Site Recovery в текущем хранилище.</span><span class="sxs-lookup"><span data-stu-id="20807-106">The **New-AzureRmSiteRecoverySite** cmdlet creates an Azure Site Recovery site in the current vault.</span></span>

## <span data-ttu-id="20807-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="20807-107">EXAMPLES</span></span>

## <span data-ttu-id="20807-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="20807-108">PARAMETERS</span></span>

### <span data-ttu-id="20807-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20807-109">-DefaultProfile</span></span>
<span data-ttu-id="20807-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="20807-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20807-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="20807-111">-Name</span></span>
<span data-ttu-id="20807-112">Указывает имя сайта.</span><span class="sxs-lookup"><span data-stu-id="20807-112">Specifies the name of the site.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20807-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20807-113">CommonParameters</span></span>
<span data-ttu-id="20807-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="20807-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20807-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20807-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20807-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="20807-116">INPUTS</span></span>

### <span data-ttu-id="20807-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="20807-117">None</span></span>
<span data-ttu-id="20807-118">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="20807-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20807-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="20807-119">OUTPUTS</span></span>

## <span data-ttu-id="20807-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="20807-120">NOTES</span></span>

## <span data-ttu-id="20807-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="20807-121">RELATED LINKS</span></span>

[<span data-ttu-id="20807-122">Get-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="20807-122">Get-AzureRmSiteRecoverySite</span></span>](./Get-AzureRmSiteRecoverySite.md)

[<span data-ttu-id="20807-123">Remove-AzureRmSiteRecoverySite</span><span class="sxs-lookup"><span data-stu-id="20807-123">Remove-AzureRmSiteRecoverySite</span></span>](./Remove-AzureRmSiteRecoverySite.md)
