---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94244248"
---
# <span data-ttu-id="e64ab-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e64ab-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="e64ab-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e64ab-102">SYNOPSIS</span></span>
<span data-ttu-id="e64ab-103">Удаляет указанный план восстановления ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e64ab-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="e64ab-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e64ab-104">SYNTAX</span></span>

### <span data-ttu-id="e64ab-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e64ab-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e64ab-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e64ab-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e64ab-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e64ab-107">DESCRIPTION</span></span>
<span data-ttu-id="e64ab-108">Командлет **Remove-AzRecoveryServicesAsrRecoveryPlan** удаляет указанный план восстановления из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e64ab-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="e64ab-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e64ab-109">EXAMPLES</span></span>

### <span data-ttu-id="e64ab-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e64ab-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="e64ab-111">Запускает удаление указанного плана восстановления и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="e64ab-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="e64ab-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e64ab-112">PARAMETERS</span></span>

### <span data-ttu-id="e64ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e64ab-113">-DefaultProfile</span></span>
<span data-ttu-id="e64ab-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e64ab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e64ab-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e64ab-115">-InputObject</span></span>
<span data-ttu-id="e64ab-116">Входной объект для командлета: объект плана восстановления ASR, соответствующий удаляемому плану восстановления.</span><span class="sxs-lookup"><span data-stu-id="e64ab-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="e64ab-117">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="e64ab-117">-Name</span></span>
<span data-ttu-id="e64ab-118">Указывает имя удаляемого плана восстановления.</span><span class="sxs-lookup"><span data-stu-id="e64ab-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="e64ab-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e64ab-119">-Confirm</span></span>
<span data-ttu-id="e64ab-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="e64ab-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e64ab-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e64ab-121">-WhatIf</span></span>
<span data-ttu-id="e64ab-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="e64ab-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e64ab-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="e64ab-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e64ab-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e64ab-124">CommonParameters</span></span>
<span data-ttu-id="e64ab-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e64ab-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e64ab-126">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e64ab-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e64ab-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e64ab-127">INPUTS</span></span>

### <span data-ttu-id="e64ab-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e64ab-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="e64ab-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e64ab-129">OUTPUTS</span></span>

### <span data-ttu-id="e64ab-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e64ab-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e64ab-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="e64ab-131">NOTES</span></span>

## <span data-ttu-id="e64ab-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e64ab-132">RELATED LINKS</span></span>

[<span data-ttu-id="e64ab-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e64ab-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e64ab-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e64ab-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="e64ab-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="e64ab-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


