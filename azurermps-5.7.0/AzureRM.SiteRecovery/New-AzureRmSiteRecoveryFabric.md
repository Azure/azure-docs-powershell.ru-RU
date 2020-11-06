---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/new-azurermsiterecoveryfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 38a7f8ee32f02db10dc971d5be2016d5dea0b538
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93557159"
---
# <span data-ttu-id="22a19-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="22a19-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="22a19-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="22a19-102">SYNOPSIS</span></span>
<span data-ttu-id="22a19-103">Создает структуру восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="22a19-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22a19-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="22a19-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="22a19-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a19-105">DESCRIPTION</span></span>
<span data-ttu-id="22a19-106">Командлет **New-AzureRmSiteRecoveryFabric** создает структуру восстановления сайта Azure для указанного типа.</span><span class="sxs-lookup"><span data-stu-id="22a19-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="22a19-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="22a19-107">EXAMPLES</span></span>

## <span data-ttu-id="22a19-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="22a19-108">PARAMETERS</span></span>

### <span data-ttu-id="22a19-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22a19-109">-DefaultProfile</span></span>
<span data-ttu-id="22a19-110">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="22a19-110">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22a19-111">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="22a19-111">-Name</span></span>
<span data-ttu-id="22a19-112">Указывает имя структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="22a19-112">Specifies the name of the Azure Site Recovery Fabric</span></span>

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

### <span data-ttu-id="22a19-113">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="22a19-113">-Type</span></span>
<span data-ttu-id="22a19-114">Указывает тип структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="22a19-114">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22a19-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22a19-115">CommonParameters</span></span>
<span data-ttu-id="22a19-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="22a19-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22a19-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22a19-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22a19-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="22a19-118">INPUTS</span></span>

### <span data-ttu-id="22a19-119">Ничего</span><span class="sxs-lookup"><span data-stu-id="22a19-119">None</span></span>
<span data-ttu-id="22a19-120">Этот командлет не поддерживает никаких входных данных.</span><span class="sxs-lookup"><span data-stu-id="22a19-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22a19-121">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="22a19-121">OUTPUTS</span></span>

### <span data-ttu-id="22a19-122">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="22a19-122">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="22a19-123">Пуск</span><span class="sxs-lookup"><span data-stu-id="22a19-123">NOTES</span></span>

## <span data-ttu-id="22a19-124">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="22a19-124">RELATED LINKS</span></span>

[<span data-ttu-id="22a19-125">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="22a19-125">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="22a19-126">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="22a19-126">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
