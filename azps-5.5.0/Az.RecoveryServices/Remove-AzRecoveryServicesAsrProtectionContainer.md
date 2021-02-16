---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100217961"
---
# <span data-ttu-id="d4a98-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d4a98-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="d4a98-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4a98-102">SYNOPSIS</span></span>
<span data-ttu-id="d4a98-103">Удаляет указанный контейнер защиты из его ткань.</span><span class="sxs-lookup"><span data-stu-id="d4a98-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="d4a98-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="d4a98-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4a98-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="d4a98-105">DESCRIPTION</span></span>
<span data-ttu-id="d4a98-106">С Remove-AzRecoveryServicesAsrProtectionContainer удаляется указанный контейнер Azure Site Recovery Protection.</span><span class="sxs-lookup"><span data-stu-id="d4a98-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="d4a98-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="d4a98-107">EXAMPLES</span></span>

### <span data-ttu-id="d4a98-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="d4a98-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="d4a98-109">Запускает удаление указанного контейнера защиты и возвращает задание asR, используемую для отслеживания удаления.</span><span class="sxs-lookup"><span data-stu-id="d4a98-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="d4a98-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4a98-110">PARAMETERS</span></span>

### <span data-ttu-id="d4a98-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4a98-111">-DefaultProfile</span></span>
<span data-ttu-id="d4a98-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="d4a98-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4a98-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d4a98-113">-InputObject</span></span>
<span data-ttu-id="d4a98-114">Определяет, что нужно удалить контейнер защиты.</span><span class="sxs-lookup"><span data-stu-id="d4a98-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="d4a98-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4a98-115">-Confirm</span></span>
<span data-ttu-id="d4a98-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="d4a98-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4a98-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4a98-117">-WhatIf</span></span>
<span data-ttu-id="d4a98-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d4a98-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4a98-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="d4a98-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4a98-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4a98-120">CommonParameters</span></span>
<span data-ttu-id="d4a98-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4a98-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4a98-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4a98-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4a98-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d4a98-123">INPUTS</span></span>

### <span data-ttu-id="d4a98-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="d4a98-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="d4a98-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d4a98-125">OUTPUTS</span></span>

### <span data-ttu-id="d4a98-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d4a98-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d4a98-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="d4a98-127">NOTES</span></span>

## <span data-ttu-id="d4a98-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="d4a98-128">RELATED LINKS</span></span>
