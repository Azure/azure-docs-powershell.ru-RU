---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: 13c2f20f6d8ef7823244c62cfbe97e4b3a25eb73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562256"
---
# <span data-ttu-id="b30dd-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b30dd-101">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="b30dd-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b30dd-102">SYNOPSIS</span></span>
<span data-ttu-id="b30dd-103">Удаляет указанное сетевое сопоставление ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="b30dd-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b30dd-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b30dd-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b30dd-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b30dd-105">DESCRIPTION</span></span>
<span data-ttu-id="b30dd-106">Командлет **Remove-AzureRmRecoveryServicesAsrNetworkMapping** удаляет указанное сетевое сопоставление ASR.</span><span class="sxs-lookup"><span data-stu-id="b30dd-106">The **Remove-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="b30dd-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b30dd-107">EXAMPLES</span></span>

### <span data-ttu-id="b30dd-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b30dd-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="b30dd-109">Запускает удаление указанного сопоставления сети ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="b30dd-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b30dd-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b30dd-110">PARAMETERS</span></span>

### <span data-ttu-id="b30dd-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b30dd-111">-InputObject</span></span>
<span data-ttu-id="b30dd-112">Входной объект для командлета: объект сопоставления ASR, соответствующий сетевому сопоставлению ASR для удаления.</span><span class="sxs-lookup"><span data-stu-id="b30dd-112">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b30dd-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b30dd-113">-Confirm</span></span>
<span data-ttu-id="b30dd-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b30dd-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30dd-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b30dd-115">-WhatIf</span></span>
<span data-ttu-id="b30dd-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b30dd-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b30dd-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b30dd-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b30dd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b30dd-118">CommonParameters</span></span>
<span data-ttu-id="b30dd-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b30dd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b30dd-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b30dd-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b30dd-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b30dd-121">INPUTS</span></span>

### <span data-ttu-id="b30dd-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b30dd-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="b30dd-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b30dd-123">OUTPUTS</span></span>

### <span data-ttu-id="b30dd-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b30dd-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b30dd-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="b30dd-125">NOTES</span></span>

## <span data-ttu-id="b30dd-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b30dd-126">RELATED LINKS</span></span>

[<span data-ttu-id="b30dd-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b30dd-127">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="b30dd-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b30dd-128">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./New-AzureRmRecoveryServicesAsrNetworkMapping.md)
