---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: dd17eef73ab07d662a10177ffb68776aa4ec6016
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567538"
---
# <span data-ttu-id="4b9d5-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="4b9d5-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="4b9d5-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="4b9d5-102">SYNOPSIS</span></span>
<span data-ttu-id="4b9d5-103">Обновляет указанное сопоставление сети ASR.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-103">Updates the specified ASR network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b9d5-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="4b9d5-104">SYNTAX</span></span>

### <span data-ttu-id="4b9d5-105">ByNetworkObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="4b9d5-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4b9d5-106">ById</span><span class="sxs-lookup"><span data-stu-id="4b9d5-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b9d5-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b9d5-107">DESCRIPTION</span></span>
<span data-ttu-id="4b9d5-108">Командлет **Update-AzureRmRecoveryServicesAsrNetworkMapping** обновляет указанное сетевое сопоставление для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="4b9d5-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="4b9d5-109">EXAMPLES</span></span>

### <span data-ttu-id="4b9d5-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="4b9d5-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="4b9d5-111">Запускает операцию обновления сетевого сопоставления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="4b9d5-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="4b9d5-112">PARAMETERS</span></span>

### <span data-ttu-id="4b9d5-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4b9d5-113">-InputObject</span></span>
<span data-ttu-id="4b9d5-114">Объект input: определяет объект сетевого сопоставления ASR, соответствующий сетевому сопоставлению ASR для обновления.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-114">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated</span></span> 

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

### <span data-ttu-id="4b9d5-115">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="4b9d5-115">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="4b9d5-116">Указывает идентификатор сети Azure Recovery Network для сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-116">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9d5-117">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="4b9d5-117">-RecoveryNetwork</span></span>
<span data-ttu-id="4b9d5-118">Указывает сетевой объект для восстановления сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-118">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByNetworkObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b9d5-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4b9d5-119">-Confirm</span></span>
<span data-ttu-id="4b9d5-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b9d5-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b9d5-121">-WhatIf</span></span>
<span data-ttu-id="4b9d5-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b9d5-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b9d5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b9d5-124">CommonParameters</span></span>
<span data-ttu-id="4b9d5-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="4b9d5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b9d5-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b9d5-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b9d5-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="4b9d5-127">INPUTS</span></span>

### <span data-ttu-id="4b9d5-128">Ничего</span><span class="sxs-lookup"><span data-stu-id="4b9d5-128">None</span></span>

## <span data-ttu-id="4b9d5-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="4b9d5-129">OUTPUTS</span></span>

### <span data-ttu-id="4b9d5-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="4b9d5-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="4b9d5-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="4b9d5-131">NOTES</span></span>

## <span data-ttu-id="4b9d5-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="4b9d5-132">RELATED LINKS</span></span>

