---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/remove-azurermrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrPolicy.md
ms.openlocfilehash: c8ef77367c66cc479bcbab25aba427c50a38447e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93732848"
---
# <span data-ttu-id="450bf-101">Remove-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="450bf-101">Remove-AzureRmRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="450bf-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="450bf-102">SYNOPSIS</span></span>
<span data-ttu-id="450bf-103">Удаляет указанную политику репликации ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="450bf-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="450bf-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="450bf-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="450bf-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="450bf-105">DESCRIPTION</span></span>
<span data-ttu-id="450bf-106">Командлет **Remove-AzureRmRecoveryServicesAsrPolicy** удалил указанную политику репликации из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="450bf-106">The **Remove-AzureRmRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="450bf-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="450bf-107">EXAMPLES</span></span>

### <span data-ttu-id="450bf-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="450bf-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="450bf-109">Запускает удаление указанной политики репликации и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="450bf-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="450bf-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="450bf-110">PARAMETERS</span></span>

### <span data-ttu-id="450bf-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="450bf-111">-Confirm</span></span>
<span data-ttu-id="450bf-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="450bf-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="450bf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="450bf-113">-DefaultProfile</span></span>
<span data-ttu-id="450bf-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="450bf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="450bf-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="450bf-115">-InputObject</span></span>
<span data-ttu-id="450bf-116">Входной объект для командлета: объект политики репликации ASR, соответствующий политике репликации, которую нужно удалить.</span><span class="sxs-lookup"><span data-stu-id="450bf-116">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

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

### <span data-ttu-id="450bf-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="450bf-117">-WhatIf</span></span>
<span data-ttu-id="450bf-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="450bf-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="450bf-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="450bf-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="450bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="450bf-120">CommonParameters</span></span>
<span data-ttu-id="450bf-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="450bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="450bf-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="450bf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="450bf-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="450bf-123">INPUTS</span></span>

### <span data-ttu-id="450bf-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="450bf-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="450bf-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="450bf-125">OUTPUTS</span></span>

### <span data-ttu-id="450bf-126">System. Object</span><span class="sxs-lookup"><span data-stu-id="450bf-126">System.Object</span></span>

## <span data-ttu-id="450bf-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="450bf-127">NOTES</span></span>

## <span data-ttu-id="450bf-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="450bf-128">RELATED LINKS</span></span>

[<span data-ttu-id="450bf-129">Get-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="450bf-129">Get-AzureRmRecoveryServicesAsrPolicy</span></span>](./Get-AzureRmRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="450bf-130">New-AzureRmRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="450bf-130">New-AzureRmRecoveryServicesAsrPolicy</span></span>](./New-AzureRmRecoveryServicesAsrPolicy.md)
