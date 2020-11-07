---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b3bedc5c521736ff702f5e7378b4c401a42bce5f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732104"
---
# <span data-ttu-id="857c4-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="857c4-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="857c4-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="857c4-102">SYNOPSIS</span></span>
<span data-ttu-id="857c4-103">Удаляет указанный план восстановления ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="857c4-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="857c4-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="857c4-104">SYNTAX</span></span>

### <span data-ttu-id="857c4-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="857c4-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="857c4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="857c4-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="857c4-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="857c4-107">DESCRIPTION</span></span>
<span data-ttu-id="857c4-108">Командлет **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** удаляет указанный план восстановления из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="857c4-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="857c4-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="857c4-109">EXAMPLES</span></span>

### <span data-ttu-id="857c4-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="857c4-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="857c4-111">Запускает удаление указанного плана восстановления и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="857c4-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="857c4-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="857c4-112">PARAMETERS</span></span>

### <span data-ttu-id="857c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="857c4-113">-DefaultProfile</span></span>
<span data-ttu-id="857c4-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="857c4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="857c4-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="857c4-115">-InputObject</span></span>
<span data-ttu-id="857c4-116">Входной объект для командлета: объект плана восстановления ASR, соответствующий удаляемому плану восстановления.</span><span class="sxs-lookup"><span data-stu-id="857c4-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="857c4-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="857c4-117">-Name</span></span>
<span data-ttu-id="857c4-118">Указывает имя удаляемого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="857c4-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="857c4-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="857c4-119">-Confirm</span></span>
<span data-ttu-id="857c4-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="857c4-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="857c4-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="857c4-121">-WhatIf</span></span>
<span data-ttu-id="857c4-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="857c4-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="857c4-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="857c4-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="857c4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="857c4-124">CommonParameters</span></span>
<span data-ttu-id="857c4-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="857c4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="857c4-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="857c4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="857c4-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="857c4-127">INPUTS</span></span>

### <span data-ttu-id="857c4-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="857c4-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="857c4-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="857c4-129">OUTPUTS</span></span>

### <span data-ttu-id="857c4-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="857c4-130">System.Object</span></span>

## <span data-ttu-id="857c4-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="857c4-131">NOTES</span></span>

## <span data-ttu-id="857c4-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="857c4-132">RELATED LINKS</span></span>

[<span data-ttu-id="857c4-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="857c4-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="857c4-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="857c4-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="857c4-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="857c4-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


