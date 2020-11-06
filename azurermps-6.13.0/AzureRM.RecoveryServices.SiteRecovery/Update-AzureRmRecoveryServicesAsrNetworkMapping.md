---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/update-azurermrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Update-AzureRmRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: fb92ec38bcbe7addb23f274616cde0fd84ebbafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558339"
---
# <span data-ttu-id="b731e-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="b731e-101">Update-AzureRmRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="b731e-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="b731e-102">SYNOPSIS</span></span>
<span data-ttu-id="b731e-103">Обновляет указанное сетевое сопоставление для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="b731e-103">Updates the specified azure site recovery network mapping.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b731e-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="b731e-104">SYNTAX</span></span>

### <span data-ttu-id="b731e-105">ByNetworkObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="b731e-105">ByNetworkObject (Default)</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping> -RecoveryNetwork <ASRNetwork>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b731e-106">ById</span><span class="sxs-lookup"><span data-stu-id="b731e-106">ById</span></span>
```
Update-AzureRmRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 -RecoveryAzureNetworkId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b731e-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b731e-107">DESCRIPTION</span></span>
<span data-ttu-id="b731e-108">Командлет **Update-AzureRmRecoveryServicesAsrNetworkMapping** обновляет указанное сетевое сопоставление для восстановления сайта Azure.</span><span class="sxs-lookup"><span data-stu-id="b731e-108">The **Update-AzureRmRecoveryServicesAsrNetworkMapping** cmdlet updates the specified Azure Site Recovery network mapping.</span></span>

## <span data-ttu-id="b731e-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="b731e-109">EXAMPLES</span></span>

### <span data-ttu-id="b731e-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="b731e-110">Example 1</span></span>
```
PS C:\> $currentJob = Update-AzureRmRecoveryServicesAsrNetworkMapping -Mapping $NetworkMapping -RecoveryNetwork $RecoveryNetwork
```

<span data-ttu-id="b731e-111">Запускает операцию обновления сетевого сопоставления с указанными параметрами и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="b731e-111">Starts the update network mapping operation using the specified parameters and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="b731e-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="b731e-112">PARAMETERS</span></span>

### <span data-ttu-id="b731e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b731e-113">-DefaultProfile</span></span>
<span data-ttu-id="b731e-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="b731e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="b731e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b731e-115">-InputObject</span></span>
<span data-ttu-id="b731e-116">Объект input: определяет объект сетевого сопоставления ASR, соответствующий сетевому сопоставлению ASR для обновления.</span><span class="sxs-lookup"><span data-stu-id="b731e-116">Input Object: Specifies the ASR network mapping object corresponding to the ASR network mapping to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b731e-117">-RecoveryAzureNetworkId</span><span class="sxs-lookup"><span data-stu-id="b731e-117">-RecoveryAzureNetworkId</span></span>
<span data-ttu-id="b731e-118">Указывает идентификатор сети Azure Recovery Network для сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="b731e-118">Specifies the recovery azure network ID for the network mapping.</span></span>

```yaml
Type: System.String
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b731e-119">-RecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="b731e-119">-RecoveryNetwork</span></span>
<span data-ttu-id="b731e-120">Указывает сетевой объект для восстановления сетевого сопоставления.</span><span class="sxs-lookup"><span data-stu-id="b731e-120">Specifies the recovery network object for the network mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetwork
Parameter Sets: ByNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b731e-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b731e-121">-Confirm</span></span>
<span data-ttu-id="b731e-122">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="b731e-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b731e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b731e-123">-WhatIf</span></span>
<span data-ttu-id="b731e-124">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="b731e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b731e-125">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="b731e-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b731e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b731e-126">CommonParameters</span></span>
<span data-ttu-id="b731e-127">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="b731e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b731e-128">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b731e-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b731e-129">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="b731e-129">INPUTS</span></span>

### <span data-ttu-id="b731e-130">Ничего</span><span class="sxs-lookup"><span data-stu-id="b731e-130">None</span></span>

## <span data-ttu-id="b731e-131">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="b731e-131">OUTPUTS</span></span>

### <span data-ttu-id="b731e-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b731e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b731e-133">Пуск</span><span class="sxs-lookup"><span data-stu-id="b731e-133">NOTES</span></span>

## <span data-ttu-id="b731e-134">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b731e-134">RELATED LINKS</span></span>
