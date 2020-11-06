---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 5f4298c2a4bfdc081447e6a8b15bac565b20b2db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563423"
---
# <span data-ttu-id="49787-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49787-101">Remove-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="49787-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="49787-102">SYNOPSIS</span></span>
<span data-ttu-id="49787-103">Удаляет указанный план восстановления ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="49787-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="49787-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="49787-104">SYNTAX</span></span>

### <span data-ttu-id="49787-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="49787-105">ByObject (Default)</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="49787-106">ByName</span><span class="sxs-lookup"><span data-stu-id="49787-106">ByName</span></span>
```
Remove-AzureRmRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49787-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="49787-107">DESCRIPTION</span></span>
<span data-ttu-id="49787-108">Командлет **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** удаляет указанный план восстановления из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="49787-108">The **Remove-AzureRmRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="49787-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="49787-109">EXAMPLES</span></span>

### <span data-ttu-id="49787-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="49787-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="49787-111">Запускает удаление указанного плана восстановления и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="49787-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="49787-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="49787-112">PARAMETERS</span></span>

### <span data-ttu-id="49787-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49787-113">-Confirm</span></span>
<span data-ttu-id="49787-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="49787-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49787-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49787-115">-DefaultProfile</span></span>
<span data-ttu-id="49787-116">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="49787-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="49787-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="49787-117">-InputObject</span></span>
<span data-ttu-id="49787-118">Входной объект для командлета: объект плана восстановления ASR, соответствующий удаляемому плану восстановления.</span><span class="sxs-lookup"><span data-stu-id="49787-118">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="49787-119">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="49787-119">-Name</span></span>
<span data-ttu-id="49787-120">Указывает имя удаляемого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="49787-120">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="49787-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49787-121">-WhatIf</span></span>
<span data-ttu-id="49787-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="49787-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49787-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="49787-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49787-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49787-124">CommonParameters</span></span>
<span data-ttu-id="49787-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="49787-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49787-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49787-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49787-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="49787-127">INPUTS</span></span>

### <span data-ttu-id="49787-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49787-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="49787-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="49787-129">OUTPUTS</span></span>

### <span data-ttu-id="49787-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="49787-130">System.Object</span></span>

## <span data-ttu-id="49787-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="49787-131">NOTES</span></span>

## <span data-ttu-id="49787-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="49787-132">RELATED LINKS</span></span>

[<span data-ttu-id="49787-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49787-133">Get-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="49787-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49787-134">New-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzureRmRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="49787-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="49787-135">Update-AzureRmRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzureRmRecoveryServicesAsrRecoveryPlan.md)


