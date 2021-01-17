---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 6ff0031c5bb8571c69287968f984565daf58b530
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408236"
---
# <span data-ttu-id="02a0b-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="02a0b-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="02a0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="02a0b-103">Удаляет указанную политику репликации ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="02a0b-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="02a0b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="02a0b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a0b-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="02a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="02a0b-106">Для удаления указанной политики репликации из хранилища служб восстановления был удален cmdlet **Remove-AzRecoveryServicesAsrPolicy.**</span><span class="sxs-lookup"><span data-stu-id="02a0b-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="02a0b-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="02a0b-107">EXAMPLES</span></span>

### <span data-ttu-id="02a0b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="02a0b-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="02a0b-109">Начало удаления указанной политики репликации и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="02a0b-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="02a0b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02a0b-110">PARAMETERS</span></span>

### <span data-ttu-id="02a0b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a0b-111">-DefaultProfile</span></span>
<span data-ttu-id="02a0b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="02a0b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="02a0b-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02a0b-113">-InputObject</span></span>
<span data-ttu-id="02a0b-114">Входной объект для cmdlet: объект политики репликации ASR, соответствующий удаляемой политике репликации.</span><span class="sxs-lookup"><span data-stu-id="02a0b-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="02a0b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02a0b-115">-Confirm</span></span>
<span data-ttu-id="02a0b-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="02a0b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a0b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a0b-117">-WhatIf</span></span>
<span data-ttu-id="02a0b-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02a0b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02a0b-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="02a0b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a0b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a0b-120">CommonParameters</span></span>
<span data-ttu-id="02a0b-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02a0b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a0b-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="02a0b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a0b-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="02a0b-123">INPUTS</span></span>

### <span data-ttu-id="02a0b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="02a0b-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="02a0b-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="02a0b-125">OUTPUTS</span></span>

### <span data-ttu-id="02a0b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="02a0b-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="02a0b-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="02a0b-127">NOTES</span></span>

## <span data-ttu-id="02a0b-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="02a0b-128">RELATED LINKS</span></span>

[<span data-ttu-id="02a0b-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="02a0b-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="02a0b-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="02a0b-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
