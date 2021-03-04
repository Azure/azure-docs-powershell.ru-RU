---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 5743d1d9288f0045755aab752274c24640b3c548
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953272"
---
# <span data-ttu-id="ef3cb-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ef3cb-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="ef3cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef3cb-102">SYNOPSIS</span></span>
<span data-ttu-id="ef3cb-103">Удаляет указанную политику репликации ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="ef3cb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="ef3cb-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef3cb-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ef3cb-105">DESCRIPTION</span></span>
<span data-ttu-id="ef3cb-106">Для удаления указанной политики репликации из хранилища служб восстановления был удален cmdlet **Remove-AzRecoveryServicesAsrPolicy.**</span><span class="sxs-lookup"><span data-stu-id="ef3cb-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="ef3cb-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="ef3cb-107">EXAMPLES</span></span>

### <span data-ttu-id="ef3cb-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ef3cb-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="ef3cb-109">Начало удаления указанной политики репликации и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="ef3cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef3cb-110">PARAMETERS</span></span>

### <span data-ttu-id="ef3cb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef3cb-111">-DefaultProfile</span></span>
<span data-ttu-id="ef3cb-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ef3cb-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ef3cb-113">-InputObject</span></span>
<span data-ttu-id="ef3cb-114">Входной объект для cmdlet: объект политики репликации ASR, соответствующий удаляемой политике репликации.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef3cb-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef3cb-115">-Confirm</span></span>
<span data-ttu-id="ef3cb-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef3cb-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef3cb-117">-WhatIf</span></span>
<span data-ttu-id="ef3cb-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef3cb-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef3cb-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef3cb-120">CommonParameters</span></span>
<span data-ttu-id="ef3cb-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef3cb-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef3cb-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ef3cb-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef3cb-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ef3cb-123">INPUTS</span></span>

### <span data-ttu-id="ef3cb-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="ef3cb-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="ef3cb-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ef3cb-125">OUTPUTS</span></span>

### <span data-ttu-id="ef3cb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ef3cb-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ef3cb-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="ef3cb-127">NOTES</span></span>

## <span data-ttu-id="ef3cb-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ef3cb-128">RELATED LINKS</span></span>

[<span data-ttu-id="ef3cb-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ef3cb-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="ef3cb-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="ef3cb-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
