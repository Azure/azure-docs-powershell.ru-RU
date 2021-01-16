---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrnetworkmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrNetworkMapping.md
ms.openlocfilehash: ef251bb9d1060e511658f9174cde2c04ab288ed7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506744"
---
# <span data-ttu-id="36aa7-101">Remove-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="36aa7-101">Remove-AzRecoveryServicesAsrNetworkMapping</span></span>

## <span data-ttu-id="36aa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="36aa7-102">SYNOPSIS</span></span>
<span data-ttu-id="36aa7-103">Удаляет указанное сетевое сопоставление ASR из хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="36aa7-103">Deletes the specified ASR network mapping from the Recovery Services vault.</span></span>

## <span data-ttu-id="36aa7-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="36aa7-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrNetworkMapping -InputObject <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36aa7-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="36aa7-105">DESCRIPTION</span></span>
<span data-ttu-id="36aa7-106">Командлет **Remove-AzRecoveryServicesAsrNetworkMapping** удаляет указанное сетевое сопоставление ASR.</span><span class="sxs-lookup"><span data-stu-id="36aa7-106">The **Remove-AzRecoveryServicesAsrNetworkMapping** cmdlet deletes the specified ASR network mapping.</span></span>

## <span data-ttu-id="36aa7-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="36aa7-107">EXAMPLES</span></span>

### <span data-ttu-id="36aa7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="36aa7-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrNetworkMapping -NetworkMapping $networkmapping
```

<span data-ttu-id="36aa7-109">Начало удаления указанного сопоставления сети ASR и возврат задания ASR, используемого для отслеживания операции.</span><span class="sxs-lookup"><span data-stu-id="36aa7-109">Starts the deletion of specified ASR network mapping and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="36aa7-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="36aa7-110">PARAMETERS</span></span>

### <span data-ttu-id="36aa7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36aa7-111">-DefaultProfile</span></span>
<span data-ttu-id="36aa7-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="36aa7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="36aa7-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="36aa7-113">-InputObject</span></span>
<span data-ttu-id="36aa7-114">Объект ввода для cmdlet: объект сетевого сопоставления ASR, соответствующий удаляемой схеме сети ASR.</span><span class="sxs-lookup"><span data-stu-id="36aa7-114">The input object to the cmdlet: The ASR network mapping object corresponding to the ASR network mapping to be deleted.</span></span>

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

### <span data-ttu-id="36aa7-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="36aa7-115">-Confirm</span></span>
<span data-ttu-id="36aa7-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36aa7-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36aa7-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36aa7-117">-WhatIf</span></span>
<span data-ttu-id="36aa7-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36aa7-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36aa7-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="36aa7-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36aa7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36aa7-120">CommonParameters</span></span>
<span data-ttu-id="36aa7-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36aa7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36aa7-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36aa7-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36aa7-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="36aa7-123">INPUTS</span></span>

### <span data-ttu-id="36aa7-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="36aa7-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRNetworkMapping</span></span>

## <span data-ttu-id="36aa7-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="36aa7-125">OUTPUTS</span></span>

### <span data-ttu-id="36aa7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="36aa7-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="36aa7-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="36aa7-127">NOTES</span></span>

## <span data-ttu-id="36aa7-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="36aa7-128">RELATED LINKS</span></span>

[<span data-ttu-id="36aa7-129">Get-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="36aa7-129">Get-AzRecoveryServicesAsrNetworkMapping</span></span>](./Get-AzRecoveryServicesAsrNetworkMapping.md)

[<span data-ttu-id="36aa7-130">New-AzRecoveryServicesAsrNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="36aa7-130">New-AzRecoveryServicesAsrNetworkMapping</span></span>](./New-AzRecoveryServicesAsrNetworkMapping.md)
