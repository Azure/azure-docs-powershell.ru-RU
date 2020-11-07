---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 510e38e201c84ad6158c959d4d56fe9872ad83df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734797"
---
# <span data-ttu-id="b16ce-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b16ce-101">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="b16ce-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b16ce-102">SYNOPSIS</span></span>
<span data-ttu-id="b16ce-103">Получение сведений о сопоставлениях сети восстановления сайта для текущего хранилища.</span><span class="sxs-lookup"><span data-stu-id="b16ce-103">Gets information about Site Recovery network mappings for the current vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b16ce-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b16ce-104">SYNTAX</span></span>

### <span data-ttu-id="b16ce-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b16ce-105">ByObject (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Network <ASRNetwork> [<CommonParameters>]
```

### <span data-ttu-id="b16ce-106">ByObjectWithName</span><span class="sxs-lookup"><span data-stu-id="b16ce-106">ByObjectWithName</span></span>
```
Get-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -Network <ASRNetwork> [<CommonParameters>]
```

## <span data-ttu-id="b16ce-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b16ce-107">DESCRIPTION</span></span>
<span data-ttu-id="b16ce-108">Командлет **Get-AzureRmRecoveryServicesAsrNetworkMapping** получает сведения о сопоставлениях сети восстановления сайта Azure для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b16ce-108">The **Get-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet gets information about Azure Site Recovery network mappings for the Recovery Services vault.</span></span>

## <span data-ttu-id="b16ce-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b16ce-109">EXAMPLES</span></span>

### <span data-ttu-id="b16ce-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b16ce-110">Example 1</span></span>
```
PS C:\> $Networkmappings = Get-AzureRmRecoveryServicesAsrNetworkMapping -Network $Network
```

<span data-ttu-id="b16ce-111">Возвращает все сопоставления сетей для переданной сети.</span><span class="sxs-lookup"><span data-stu-id="b16ce-111">Gets all networks mappings for the passed Network.</span></span>

## <span data-ttu-id="b16ce-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b16ce-112">PARAMETERS</span></span>

### <span data-ttu-id="b16ce-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="b16ce-113">-Name</span></span>
<span data-ttu-id="b16ce-114">Имя получаемого объекта сетевого сопоставления ASR.</span><span class="sxs-lookup"><span data-stu-id="b16ce-114">The name of the ASR network mapping object to get.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectWithName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b16ce-115">-Network (сеть)</span><span class="sxs-lookup"><span data-stu-id="b16ce-115">-Network</span></span>
<span data-ttu-id="b16ce-116">Получение сетевых сопоставлений ASR, соответствующих указанному объекту сетевого ASR.</span><span class="sxs-lookup"><span data-stu-id="b16ce-116">Get the ASR network mappings corresponding to the specified network ASR object.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b16ce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b16ce-117">CommonParameters</span></span>
<span data-ttu-id="b16ce-118">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b16ce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b16ce-119">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b16ce-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b16ce-120">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b16ce-120">INPUTS</span></span>

### <span data-ttu-id="b16ce-121">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRFabric</span><span class="sxs-lookup"><span data-stu-id="b16ce-121">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="b16ce-122">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b16ce-122">OUTPUTS</span></span>

### <span data-ttu-id="b16ce-123">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = Neutral, PublicKeyToken = NULL]]</span><span class="sxs-lookup"><span data-stu-id="b16ce-123">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b16ce-124">Пуск</span><span class="sxs-lookup"><span data-stu-id="b16ce-124">NOTES</span></span>

## <span data-ttu-id="b16ce-125">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b16ce-125">RELATED LINKS</span></span>

[<span data-ttu-id="b16ce-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b16ce-126">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="b16ce-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b16ce-127">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
