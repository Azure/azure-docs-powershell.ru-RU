---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ab2cca2fc0b517d8923d117978887c6dd0196ce5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567544"
---
# <span data-ttu-id="6e987-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6e987-101">New-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="6e987-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6e987-102">SYNOPSIS</span></span>
<span data-ttu-id="6e987-103">Создание сетевого сопоставления ASR между двумя сетями.</span><span class="sxs-lookup"><span data-stu-id="6e987-103">Creates an ASR network mapping between two networks.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e987-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6e987-104">SYNTAX</span></span>

### <span data-ttu-id="6e987-105">EnterpriseToEnterprise (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="6e987-105">EnterpriseToEnterprise (Default)</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryNetwork <ASRNetwork> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6e987-106">EnterpriseToAzure</span><span class="sxs-lookup"><span data-stu-id="6e987-106">EnterpriseToAzure</span></span>
```
New-AzureRmRecoveryServicesAsrNetworkMapping -Name <String> -PrimaryNetwork <ASRNetwork>
 -RecoveryAzureNetworkId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6e987-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e987-107">DESCRIPTION</span></span>
<span data-ttu-id="6e987-108">Командлет **New-AzureRmRecoveryServicesAsrNetworkMapping** запускает операцию создания сетевого сопоставления ASR из двух сетей и возвращает объект задания ASR для задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="6e987-108">The **New-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet starts the operation of creating an ASR network mapping between two networks and returns the ASR job object for the ASR job used to track the operation.</span></span>

## <span data-ttu-id="6e987-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6e987-109">EXAMPLES</span></span>

### <span data-ttu-id="6e987-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6e987-110">Example 1</span></span>
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrNetworkMapping -Name $NetworkMapName -PrimaryNetwork $PrimaryNetwork -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="6e987-111">Запускает операцию создания сетевого сопоставления, используя указанные имя, основную сеть и сети восстановления, и возвращает задание ASR, чтобы отслеживать операцию.</span><span class="sxs-lookup"><span data-stu-id="6e987-111">Starts the network mapping creation operation using the specified name, primary and recovery networks, and returns an ASR job to track the operation.</span></span>

## <span data-ttu-id="6e987-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6e987-112">PARAMETERS</span></span>

### <span data-ttu-id="6e987-113">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="6e987-113">-Name</span></span>
<span data-ttu-id="6e987-114">Имя сопоставления сети ASR для создания.</span><span class="sxs-lookup"><span data-stu-id="6e987-114">Name of the ASR network mapping to create.</span></span>

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

### <span data-ttu-id="6e987-115">-PrimaryNetwork</span><span class="sxs-lookup"><span data-stu-id="6e987-115">-PrimaryNetwork</span></span>
<span data-ttu-id="6e987-116">Указывает основной объект сети для сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="6e987-116">Specifies the primary network object for the network mapping.</span></span>

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

### <span data-ttu-id="6e987-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="6e987-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="6e987-118">Указывает идентификатор сети Azure Recovery Network для сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="6e987-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: String
Parameter Sets: EnterpriseToAzure
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e987-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="6e987-119">-RecoveryNetwork</span></span>
<span data-ttu-id="6e987-120">Указывает сетевой объект для восстановления сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="6e987-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: EnterpriseToEnterprise
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e987-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6e987-121">-Confirm</span></span>
<span data-ttu-id="6e987-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6e987-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6e987-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6e987-123">-WhatIf</span></span>
<span data-ttu-id="6e987-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6e987-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6e987-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6e987-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6e987-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e987-126">CommonParameters</span></span>
<span data-ttu-id="6e987-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6e987-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e987-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e987-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e987-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6e987-129">INPUTS</span></span>

### <span data-ttu-id="6e987-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetwork</span><span class="sxs-lookup"><span data-stu-id="6e987-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork</span></span>

## <span data-ttu-id="6e987-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6e987-131">OUTPUTS</span></span>

### <span data-ttu-id="6e987-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="6e987-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6e987-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="6e987-133">NOTES</span></span>

## <span data-ttu-id="6e987-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6e987-134">RELATED LINKS</span></span>

[<span data-ttu-id="6e987-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6e987-135">Get-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzureRmRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="6e987-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="6e987-136">Remove-AzureRmRecoveryServicesAsrNetworkMapping</span></span>](./Remove-AzureRmRecoveryServicesAsrNetworkMapping.md)
