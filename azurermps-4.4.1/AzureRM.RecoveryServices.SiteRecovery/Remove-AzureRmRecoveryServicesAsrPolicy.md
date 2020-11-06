---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 7263601a3f719ce48a43e26ad76f9ba388a058ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562259"
---
# <span data-ttu-id="f2cbc-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f2cbc-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="f2cbc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f2cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="f2cbc-103">Удаляет указанную политику репликации ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f2cbc-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2cbc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f2cbc-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2cbc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2cbc-105">DESCRIPTION</span></span>
<span data-ttu-id="f2cbc-106">Командлет **Remove-AzureRmRecoveryServicesAsrPolicy** удалил указанную политику репликации из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f2cbc-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="f2cbc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f2cbc-107">EXAMPLES</span></span>

### <span data-ttu-id="f2cbc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f2cbc-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="f2cbc-109">Запускает удаление указанной политики репликации и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="f2cbc-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f2cbc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f2cbc-110">PARAMETERS</span></span>

### <span data-ttu-id="f2cbc-111">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2cbc-111">-InputObject</span></span>
<span data-ttu-id="f2cbc-112">Входной объект для командлета: объект политики репликации ASR, соответствующий политике репликации, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="f2cbc-112">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2cbc-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2cbc-113">-Confirm</span></span>
<span data-ttu-id="f2cbc-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f2cbc-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2cbc-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2cbc-115">-WhatIf</span></span>
<span data-ttu-id="f2cbc-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f2cbc-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2cbc-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f2cbc-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2cbc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2cbc-118">CommonParameters</span></span>
<span data-ttu-id="f2cbc-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f2cbc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2cbc-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2cbc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2cbc-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f2cbc-121">INPUTS</span></span>

### <span data-ttu-id="f2cbc-122">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="f2cbc-122">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="f2cbc-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f2cbc-123">OUTPUTS</span></span>

### <span data-ttu-id="f2cbc-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="f2cbc-124">System.Object</span></span>

## <span data-ttu-id="f2cbc-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="f2cbc-125">NOTES</span></span>

## <span data-ttu-id="f2cbc-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f2cbc-126">RELATED LINKS</span></span>

[<span data-ttu-id="f2cbc-127">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f2cbc-127">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="f2cbc-128">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="f2cbc-128">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
