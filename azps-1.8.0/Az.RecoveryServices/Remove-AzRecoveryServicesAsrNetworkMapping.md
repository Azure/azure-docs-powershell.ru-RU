---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: e4e6579c330f8ac4189db2ddfc5d3a0578fd07f2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93729643"
---
# <span data-ttu-id="f8b13-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f8b13-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="f8b13-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="f8b13-102">SYNOPSIS</span></span>
<span data-ttu-id="f8b13-103">Удаляет указанное сетевое сопоставление ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="f8b13-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="f8b13-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="f8b13-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8b13-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8b13-105">DESCRIPTION</span></span>
<span data-ttu-id="f8b13-106">Командлет **Remove-AzRecoveryServicesAsrNetworkMapping** удаляет указанное сетевое сопоставление ASR.</span><span class="sxs-lookup"><span data-stu-id="f8b13-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="f8b13-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="f8b13-107">EXAMPLES</span></span>

### <span data-ttu-id="f8b13-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="f8b13-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="f8b13-109">Запускает удаление указанного сопоставления сети ASR и возвращает задание ASR, используемое для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="f8b13-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="f8b13-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="f8b13-110">PARAMETERS</span></span>

### <span data-ttu-id="f8b13-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8b13-111">-DefaultProfile</span></span>
<span data-ttu-id="f8b13-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="f8b13-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="f8b13-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8b13-113">-InputObject</span></span>
<span data-ttu-id="f8b13-114">Входной объект для командлета: объект сопоставления ASR, соответствующий сетевому сопоставлению ASR для удаления.</span><span class="sxs-lookup"><span data-stu-id="f8b13-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="f8b13-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8b13-115">-Confirm</span></span>
<span data-ttu-id="f8b13-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="f8b13-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8b13-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8b13-117">-WhatIf</span></span>
<span data-ttu-id="f8b13-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="f8b13-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8b13-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f8b13-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8b13-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8b13-120">CommonParameters</span></span>
<span data-ttu-id="f8b13-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="f8b13-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8b13-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8b13-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8b13-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="f8b13-123">INPUTS</span></span>

### <span data-ttu-id="f8b13-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f8b13-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="f8b13-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="f8b13-125">OUTPUTS</span></span>

### <span data-ttu-id="f8b13-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="f8b13-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="f8b13-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="f8b13-127">NOTES</span></span>

## <span data-ttu-id="f8b13-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="f8b13-128">RELATED LINKS</span></span>

[<span data-ttu-id="f8b13-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f8b13-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="f8b13-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="f8b13-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
