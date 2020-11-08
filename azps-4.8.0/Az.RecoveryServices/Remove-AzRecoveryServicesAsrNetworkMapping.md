---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94077684"
---
# <span data-ttu-id="9f2db-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9f2db-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="9f2db-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="9f2db-102">SYNOPSIS</span></span>
<span data-ttu-id="9f2db-103">Удаляет указанное сетевое сопоставление ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="9f2db-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="9f2db-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="9f2db-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9f2db-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f2db-105">DESCRIPTION</span></span>
<span data-ttu-id="9f2db-106">Командлет **Remove-AzRecoveryServicesAsrNetworkMapping** удаляет указанное сетевое сопоставление ASR.</span><span class="sxs-lookup"><span data-stu-id="9f2db-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="9f2db-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="9f2db-107">EXAMPLES</span></span>

### <span data-ttu-id="9f2db-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="9f2db-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="9f2db-109">Запускает удаление указанного сопоставления сети ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="9f2db-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="9f2db-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="9f2db-110">PARAMETERS</span></span>

### <span data-ttu-id="9f2db-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f2db-111">-DefaultProfile</span></span>
<span data-ttu-id="9f2db-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9f2db-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9f2db-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9f2db-113">-InputObject</span></span>
<span data-ttu-id="9f2db-114">Входной объект для командлета: объект сопоставления ASR, соответствующий сетевому сопоставлению ASR для удаления.</span><span class="sxs-lookup"><span data-stu-id="9f2db-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: NetworkMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9f2db-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9f2db-115">-Confirm</span></span>
<span data-ttu-id="9f2db-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="9f2db-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9f2db-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9f2db-117">-WhatIf</span></span>
<span data-ttu-id="9f2db-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="9f2db-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9f2db-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="9f2db-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9f2db-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f2db-120">CommonParameters</span></span>
<span data-ttu-id="9f2db-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="9f2db-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f2db-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9f2db-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f2db-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="9f2db-123">INPUTS</span></span>

### <span data-ttu-id="9f2db-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9f2db-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="9f2db-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="9f2db-125">OUTPUTS</span></span>

### <span data-ttu-id="9f2db-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9f2db-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9f2db-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="9f2db-127">NOTES</span></span>

## <span data-ttu-id="9f2db-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9f2db-128">RELATED LINKS</span></span>

[<span data-ttu-id="9f2db-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9f2db-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="9f2db-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="9f2db-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
