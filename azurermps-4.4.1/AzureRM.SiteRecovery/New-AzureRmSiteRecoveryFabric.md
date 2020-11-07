---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: B087194B-DA3F-4E45-BD2D-788F9E6F03EA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryFabric.md
ms.openlocfilehash: 9601a3a9a64e52938ebad2024bbc9fd1301b920a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734511"
---
# <span data-ttu-id="075d2-101">New-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="075d2-101">New-AzureRmSiteRecoveryFabric</span></span>

## <span data-ttu-id="075d2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="075d2-102">SYNOPSIS</span></span>
<span data-ttu-id="075d2-103">Создает структуру восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="075d2-103">Creates an Azure Site Recovery Fabric.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="075d2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="075d2-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryFabric -Name <String> [-Type <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="075d2-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="075d2-105">DESCRIPTION</span></span>
<span data-ttu-id="075d2-106">Командлет **New-AzureRmSiteRecoveryFabric** создает структуру восстановления сайта Azure для указанного типа.</span><span class="sxs-lookup"><span data-stu-id="075d2-106">The **New-AzureRmSiteRecoveryFabric** cmdlet creates an Azure Site Recovery Fabric of the specified type.</span></span>

## <span data-ttu-id="075d2-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="075d2-107">EXAMPLES</span></span>

## <span data-ttu-id="075d2-108">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="075d2-108">PARAMETERS</span></span>

### <span data-ttu-id="075d2-109">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="075d2-109">-Name</span></span>
<span data-ttu-id="075d2-110">Указывает имя структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="075d2-110">Specifies the name of the Azure Site Recovery Fabric</span></span>

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

### <span data-ttu-id="075d2-111">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="075d2-111">-Type</span></span>
<span data-ttu-id="075d2-112">Указывает тип структуры восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="075d2-112">Specifies the Azure Site Recovery Fabric Type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: HyperVSite

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="075d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="075d2-113">-DefaultProfile</span></span>
<span data-ttu-id="075d2-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="075d2-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="075d2-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="075d2-115">CommonParameters</span></span>
<span data-ttu-id="075d2-116">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="075d2-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="075d2-117">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="075d2-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="075d2-118">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="075d2-118">INPUTS</span></span>

## <span data-ttu-id="075d2-119">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="075d2-119">OUTPUTS</span></span>

### <span data-ttu-id="075d2-120">Microsoft. Azure. Commands. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="075d2-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="075d2-121">Пуск</span><span class="sxs-lookup"><span data-stu-id="075d2-121">NOTES</span></span>

## <span data-ttu-id="075d2-122">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="075d2-122">RELATED LINKS</span></span>

[<span data-ttu-id="075d2-123">Get-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="075d2-123">Get-AzureRmSiteRecoveryFabric</span></span>](./Get-AzureRmSiteRecoveryFabric.md)

[<span data-ttu-id="075d2-124">Remove-AzureRmSiteRecoveryFabric</span><span class="sxs-lookup"><span data-stu-id="075d2-124">Remove-AzureRmSiteRecoveryFabric</span></span>](./Remove-AzureRmSiteRecoveryFabric.md)
