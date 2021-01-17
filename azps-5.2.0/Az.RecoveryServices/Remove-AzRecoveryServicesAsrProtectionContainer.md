---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrProtectionContainer.md
ms.openlocfilehash: 36b13334c032304ddb61db04c360a1e310ef0876
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98408228"
---
# <span data-ttu-id="6d706-101">Remove-AzRecoveryServicesAsrProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6d706-101">Remove-AzRecoveryServicesAsrProtectionContainer</span></span>

## <span data-ttu-id="6d706-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d706-102">SYNOPSIS</span></span>
<span data-ttu-id="6d706-103">Удаляет указанный контейнер защиты из его ткань.</span><span class="sxs-lookup"><span data-stu-id="6d706-103">Deletes the specified Protection Container from its Fabric.</span></span>

## <span data-ttu-id="6d706-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="6d706-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrProtectionContainer -InputObject <ASRProtectionContainer>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d706-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d706-105">DESCRIPTION</span></span>
<span data-ttu-id="6d706-106">С Remove-AzRecoveryServicesAsrProtectionContainer удаляется указанный контейнер Azure Site Recovery Protection.</span><span class="sxs-lookup"><span data-stu-id="6d706-106">The Remove-AzRecoveryServicesAsrProtectionContainer cmdlet deletes the specified Azure Site Recovery Protection Container.</span></span>

## <span data-ttu-id="6d706-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="6d706-107">EXAMPLES</span></span>

### <span data-ttu-id="6d706-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d706-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesAsrProtectionContainer -Name xxxxx  -Fabric $fabric
PS C:\> Remove-AzRecoveryServicesAsrProtectionContainer -InputObject $protectionContainer
```

<span data-ttu-id="6d706-109">Запускает удаление указанного контейнера защиты и возвращает задание asR, используемую для отслеживания удаления.</span><span class="sxs-lookup"><span data-stu-id="6d706-109">Starts the deletion of specified protection container and returns the ASR job used to track the remove operation.</span></span>

## <span data-ttu-id="6d706-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d706-110">PARAMETERS</span></span>

### <span data-ttu-id="6d706-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d706-111">-DefaultProfile</span></span>
<span data-ttu-id="6d706-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d706-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6d706-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6d706-113">-InputObject</span></span>
<span data-ttu-id="6d706-114">Определяет, что нужно удалить контейнер защиты.</span><span class="sxs-lookup"><span data-stu-id="6d706-114">Specifies the protection container to be removed .</span></span>

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

### <span data-ttu-id="6d706-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d706-115">-Confirm</span></span>
<span data-ttu-id="6d706-116">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d706-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d706-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d706-117">-WhatIf</span></span>
<span data-ttu-id="6d706-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6d706-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d706-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="6d706-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d706-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d706-120">CommonParameters</span></span>
<span data-ttu-id="6d706-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d706-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d706-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6d706-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d706-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6d706-123">INPUTS</span></span>

### <span data-ttu-id="6d706-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="6d706-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRProtectionContainer</span></span>

## <span data-ttu-id="6d706-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6d706-125">OUTPUTS</span></span>

### <span data-ttu-id="6d706-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="6d706-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="6d706-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="6d706-127">NOTES</span></span>

## <span data-ttu-id="6d706-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d706-128">RELATED LINKS</span></span>
