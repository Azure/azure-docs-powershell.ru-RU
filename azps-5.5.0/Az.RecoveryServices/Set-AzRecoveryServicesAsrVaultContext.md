---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225372"
---
# <span data-ttu-id="043c9-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="043c9-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="043c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="043c9-102">SYNOPSIS</span></span>
<span data-ttu-id="043c9-103">Задает контекст хранилища служб восстановления, который будет использоваться для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="043c9-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="043c9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="043c9-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="043c9-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="043c9-105">DESCRIPTION</span></span>
<span data-ttu-id="043c9-106">**Cmdlet Set-AzRecoveryServicesAsrVaultContext** задает контекст хранилища восстановления сайта Azure для дальнейших операций.</span><span class="sxs-lookup"><span data-stu-id="043c9-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="043c9-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="043c9-107">EXAMPLES</span></span>

### <span data-ttu-id="043c9-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="043c9-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="043c9-109">Задает контекст хранилища для указанного хранилища служб восстановления для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="043c9-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="043c9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="043c9-110">PARAMETERS</span></span>

### <span data-ttu-id="043c9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="043c9-111">-DefaultProfile</span></span>
<span data-ttu-id="043c9-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="043c9-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="043c9-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="043c9-113">-Vault</span></span>
<span data-ttu-id="043c9-114">Объект хранилища служб восстановления, соответствующий сейфу служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="043c9-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="043c9-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="043c9-115">-Confirm</span></span>
<span data-ttu-id="043c9-116">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="043c9-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="043c9-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="043c9-117">-WhatIf</span></span>
<span data-ttu-id="043c9-118">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="043c9-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="043c9-119">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="043c9-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="043c9-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="043c9-120">CommonParameters</span></span>
<span data-ttu-id="043c9-121">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="043c9-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="043c9-122">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="043c9-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="043c9-123">INPUTS</span><span class="sxs-lookup"><span data-stu-id="043c9-123">INPUTS</span></span>

### <span data-ttu-id="043c9-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="043c9-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="043c9-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="043c9-125">OUTPUTS</span></span>

### <span data-ttu-id="043c9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="043c9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="043c9-127">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="043c9-127">NOTES</span></span>

## <span data-ttu-id="043c9-128">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="043c9-128">RELATED LINKS</span></span>
