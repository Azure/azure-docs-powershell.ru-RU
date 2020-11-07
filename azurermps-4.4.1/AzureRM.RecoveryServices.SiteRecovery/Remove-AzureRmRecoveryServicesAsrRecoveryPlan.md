---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 2d172c440163d70ef388c7de190371492767b2e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734790"
---
# <span data-ttu-id="f9d5b-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f9d5b-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="f9d5b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f9d5b-102">SYNOPSIS</span></span>
<span data-ttu-id="f9d5b-103">Позволяет отменять указанный план восстановления ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f9d5b-103">Delets the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9d5b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f9d5b-104">SYNTAX</span></span>

### <span data-ttu-id="f9d5b-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="f9d5b-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f9d5b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="f9d5b-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9d5b-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9d5b-107">DESCRIPTION</span></span>
<span data-ttu-id="f9d5b-108">Командлет **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** удаляет указанный план восстановления из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f9d5b-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="f9d5b-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f9d5b-109">EXAMPLES</span></span>

### <span data-ttu-id="f9d5b-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f9d5b-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="f9d5b-111">Запускает удаление указанного плана восстановления и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="f9d5b-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f9d5b-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f9d5b-112">PARAMETERS</span></span>

### <span data-ttu-id="f9d5b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9d5b-113">-InputObject</span></span>
<span data-ttu-id="f9d5b-114">Входной объект для командлета: объект плана восстановления ASR, соответствующий удаляемому плану восстановления.</span><span class="sxs-lookup"><span data-stu-id="f9d5b-114">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5b-115">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="f9d5b-115">-Name</span></span>
<span data-ttu-id="f9d5b-116">Указывает имя удаляемого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="f9d5b-116">Specifies the name of the recovery plan to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9d5b-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f9d5b-117">-Confirm</span></span>
<span data-ttu-id="f9d5b-118">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f9d5b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9d5b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9d5b-119">-WhatIf</span></span>
<span data-ttu-id="f9d5b-120">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f9d5b-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9d5b-121">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9d5b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9d5b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9d5b-122">CommonParameters</span></span>
<span data-ttu-id="f9d5b-123">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f9d5b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9d5b-124">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9d5b-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9d5b-125">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f9d5b-125">INPUTS</span></span>

### <span data-ttu-id="f9d5b-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f9d5b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="f9d5b-127">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f9d5b-127">OUTPUTS</span></span>

### <span data-ttu-id="f9d5b-128">System. Object</span><span class="sxs-lookup"><span data-stu-id="f9d5b-128">System.Object</span></span>

## <span data-ttu-id="f9d5b-129">Пуск</span><span class="sxs-lookup"><span data-stu-id="f9d5b-129">NOTES</span></span>

## <span data-ttu-id="f9d5b-130">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f9d5b-130">RELATED LINKS</span></span>

[<span data-ttu-id="f9d5b-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f9d5b-131">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f9d5b-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f9d5b-132">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="f9d5b-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="f9d5b-133">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


