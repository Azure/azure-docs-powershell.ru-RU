---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: 138fd84684fda149d66be85a0fabfbe4a2df0e52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408220"
---
# <span data-ttu-id="cff86-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cff86-101">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="cff86-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cff86-102">SYNOPSIS</span></span>
<span data-ttu-id="cff86-103">Удаляет указанный план восстановления ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cff86-103">Deletes the specified ASR recovery plan from Recovery Services vault.</span></span>

## <span data-ttu-id="cff86-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cff86-104">SYNTAX</span></span>

### <span data-ttu-id="cff86-105">ByObject (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="cff86-105">ByObject (Default)</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cff86-106">ByName</span><span class="sxs-lookup"><span data-stu-id="cff86-106">ByName</span></span>
```
Remove-AzRecoveryServicesAsrRecoveryPlan -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cff86-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cff86-107">DESCRIPTION</span></span>
<span data-ttu-id="cff86-108">С **его учетной записью будет** удален указанный план восстановления из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cff86-108">The **Remove-AzRecoveryServicesAsrRecoveryPlan** cmdlet deletes the specified recovery plan from the Recovery Services vault.</span></span>

## <span data-ttu-id="cff86-109">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cff86-109">EXAMPLES</span></span>

### <span data-ttu-id="cff86-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="cff86-110">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="cff86-111">Начало удаления указанного плана восстановления и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="cff86-111">Starts the deletion of specified recovery plan and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="cff86-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cff86-112">PARAMETERS</span></span>

### <span data-ttu-id="cff86-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cff86-113">-DefaultProfile</span></span>
<span data-ttu-id="cff86-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cff86-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="cff86-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cff86-115">-InputObject</span></span>
<span data-ttu-id="cff86-116">Входной объект для cmdlet: объект asR recovery plan, соответствующий удаляемой плану восстановления.</span><span class="sxs-lookup"><span data-stu-id="cff86-116">The input object to the cmdlet: The ASR recovery plan object corresponding to the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="cff86-117">-Name</span><span class="sxs-lookup"><span data-stu-id="cff86-117">-Name</span></span>
<span data-ttu-id="cff86-118">Имя плана восстановления, который нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="cff86-118">Specifies the name of the recovery plan to be deleted.</span></span>

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

### <span data-ttu-id="cff86-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cff86-119">-Confirm</span></span>
<span data-ttu-id="cff86-120">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cff86-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cff86-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cff86-121">-WhatIf</span></span>
<span data-ttu-id="cff86-122">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cff86-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cff86-123">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="cff86-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cff86-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cff86-124">CommonParameters</span></span>
<span data-ttu-id="cff86-125">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cff86-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cff86-126">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cff86-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cff86-127">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cff86-127">INPUTS</span></span>

### <span data-ttu-id="cff86-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cff86-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="cff86-129">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cff86-129">OUTPUTS</span></span>

### <span data-ttu-id="cff86-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="cff86-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="cff86-131">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cff86-131">NOTES</span></span>

## <span data-ttu-id="cff86-132">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cff86-132">RELATED LINKS</span></span>

[<span data-ttu-id="cff86-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cff86-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="cff86-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cff86-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="cff86-135">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="cff86-135">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Update-AzRecoveryServicesAsrRecoveryPlan.md)


