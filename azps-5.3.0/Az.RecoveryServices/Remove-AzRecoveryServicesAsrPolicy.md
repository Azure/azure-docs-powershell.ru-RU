---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506745"
---
# <span data-ttu-id="dc448-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="dc448-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="dc448-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc448-102">SYNOPSIS</span></span>
<span data-ttu-id="dc448-103">Удаляет указанную политику репликации ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="dc448-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="dc448-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="dc448-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc448-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="dc448-105">DESCRIPTION</span></span>
<span data-ttu-id="dc448-106">Для удаления указанной политики репликации из хранилища служб восстановления был удален cmdlet **Remove-AzRecoveryServicesAsrPolicy.**</span><span class="sxs-lookup"><span data-stu-id="dc448-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="dc448-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="dc448-107">EXAMPLES</span></span>

### <span data-ttu-id="dc448-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="dc448-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="dc448-109">Начало удаления указанной политики репликации и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="dc448-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="dc448-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc448-110">PARAMETERS</span></span>

### <span data-ttu-id="dc448-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc448-111">-DefaultProfile</span></span>
<span data-ttu-id="dc448-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="dc448-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="dc448-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc448-113">-InputObject</span></span>
<span data-ttu-id="dc448-114">Входной объект для cmdlet: объект политики репликации ASR, соответствующий удаляемой политике репликации.</span><span class="sxs-lookup"><span data-stu-id="dc448-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="dc448-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc448-115">-Confirm</span></span>
<span data-ttu-id="dc448-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc448-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc448-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc448-117">-WhatIf</span></span>
<span data-ttu-id="dc448-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dc448-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc448-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="dc448-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc448-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc448-120">CommonParameters</span></span>
<span data-ttu-id="dc448-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc448-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc448-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc448-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc448-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dc448-123">INPUTS</span></span>

### <span data-ttu-id="dc448-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="dc448-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="dc448-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dc448-125">OUTPUTS</span></span>

### <span data-ttu-id="dc448-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="dc448-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="dc448-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="dc448-127">NOTES</span></span>

## <span data-ttu-id="dc448-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="dc448-128">RELATED LINKS</span></span>

[<span data-ttu-id="dc448-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="dc448-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="dc448-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="dc448-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
