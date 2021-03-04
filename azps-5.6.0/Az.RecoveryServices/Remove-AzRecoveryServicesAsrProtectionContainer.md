---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: c1b5623e185c10471da674c21995917c169e5ffa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953256"
---
# <span data-ttu-id="1b23f-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1b23f-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="1b23f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b23f-102">SYNOPSIS</span></span>
<span data-ttu-id="1b23f-103">Удаляет указанный контейнер защиты из его ткань.</span><span class="sxs-lookup"><span data-stu-id="1b23f-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="1b23f-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="1b23f-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1b23f-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="1b23f-105">DESCRIPTION</span></span>
<span data-ttu-id="1b23f-106">С Remove-AzRecoveryServicesAsrProtectionContainer удаляется указанный контейнер Azure Site Recovery Protection.</span><span class="sxs-lookup"><span data-stu-id="1b23f-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="1b23f-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="1b23f-107">EXAMPLES</span></span>

### <span data-ttu-id="1b23f-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="1b23f-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="1b23f-109">Запускает удаление указанного контейнера защиты и возвращает задание ASR, используемую для отслеживания удаления.</span><span class="sxs-lookup"><span data-stu-id="1b23f-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="1b23f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b23f-110">PARAMETERS</span></span>

### <span data-ttu-id="1b23f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b23f-111">-DefaultProfile</span></span>
<span data-ttu-id="1b23f-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="1b23f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b23f-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1b23f-113">-InputObject</span></span>
<span data-ttu-id="1b23f-114">Определяет, что нужно удалить контейнер защиты.</span><span class="sxs-lookup"><span data-stu-id="1b23f-114">Specifies the protection container to be removed .</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer
Parameter Sets: (All)
Aliases: ProtectionContainer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b23f-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1b23f-115">-Confirm</span></span>
<span data-ttu-id="1b23f-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b23f-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b23f-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b23f-117">-WhatIf</span></span>
<span data-ttu-id="1b23f-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b23f-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b23f-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="1b23f-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b23f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b23f-120">CommonParameters</span></span>
<span data-ttu-id="1b23f-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b23f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b23f-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1b23f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b23f-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1b23f-123">INPUTS</span></span>

### <span data-ttu-id="1b23f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="1b23f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="1b23f-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1b23f-125">OUTPUTS</span></span>

### <span data-ttu-id="1b23f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1b23f-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1b23f-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="1b23f-127">NOTES</span></span>

## <span data-ttu-id="1b23f-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="1b23f-128">RELATED LINKS</span></span>
