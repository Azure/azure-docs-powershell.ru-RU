---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: a358e38dcba9c0f7fb4bae0c1b1af28845a3851b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729642"
---
# <span data-ttu-id="bdc98-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bdc98-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="bdc98-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="bdc98-102">SYNOPSIS</span></span>
<span data-ttu-id="bdc98-103">Удаляет указанную политику репликации ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="bdc98-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="bdc98-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="bdc98-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdc98-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdc98-105">DESCRIPTION</span></span>
<span data-ttu-id="bdc98-106">Командлет **Remove-AzRecoveryServicesAsrPolicy** удалил указанную политику репликации из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="bdc98-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="bdc98-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="bdc98-107">EXAMPLES</span></span>

### <span data-ttu-id="bdc98-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="bdc98-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="bdc98-109">Запускает удаление указанной политики репликации и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="bdc98-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="bdc98-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="bdc98-110">PARAMETERS</span></span>

### <span data-ttu-id="bdc98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdc98-111">-DefaultProfile</span></span>
<span data-ttu-id="bdc98-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="bdc98-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="bdc98-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bdc98-113">-InputObject</span></span>
<span data-ttu-id="bdc98-114">Входной объект для командлета: объект политики репликации ASR, соответствующий политике репликации, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="bdc98-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="bdc98-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bdc98-115">-Confirm</span></span>
<span data-ttu-id="bdc98-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="bdc98-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdc98-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdc98-117">-WhatIf</span></span>
<span data-ttu-id="bdc98-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="bdc98-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bdc98-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="bdc98-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdc98-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdc98-120">CommonParameters</span></span>
<span data-ttu-id="bdc98-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="bdc98-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdc98-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdc98-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdc98-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="bdc98-123">INPUTS</span></span>

### <span data-ttu-id="bdc98-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="bdc98-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="bdc98-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="bdc98-125">OUTPUTS</span></span>

### <span data-ttu-id="bdc98-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="bdc98-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bdc98-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="bdc98-127">NOTES</span></span>

## <span data-ttu-id="bdc98-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="bdc98-128">RELATED LINKS</span></span>

[<span data-ttu-id="bdc98-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bdc98-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="bdc98-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="bdc98-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
