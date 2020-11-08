---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94245703"
---
# <span data-ttu-id="6d54d-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="6d54d-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="6d54d-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="6d54d-102">SYNOPSIS</span></span>
<span data-ttu-id="6d54d-103">Задает контекст хранилища служб восстановления, который будет использоваться для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6d54d-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="6d54d-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="6d54d-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d54d-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d54d-105">DESCRIPTION</span></span>
<span data-ttu-id="6d54d-106">Командлет **Set-AzRecoveryServicesAsrVaultContext** задает контекст хранилища Azure Site Recovery для дальнейших операций.</span><span class="sxs-lookup"><span data-stu-id="6d54d-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="6d54d-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="6d54d-107">EXAMPLES</span></span>

### <span data-ttu-id="6d54d-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="6d54d-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="6d54d-109">Задает контексту хранилища указанное хранилище служб восстановления для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="6d54d-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="6d54d-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="6d54d-110">PARAMETERS</span></span>

### <span data-ttu-id="6d54d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d54d-111">-DefaultProfile</span></span>
<span data-ttu-id="6d54d-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="6d54d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d54d-113">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="6d54d-113">-Vault</span></span>
<span data-ttu-id="6d54d-114">Объект хранилища служб восстановления, соответствующий хранилищу служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="6d54d-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="6d54d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6d54d-115">-Confirm</span></span>
<span data-ttu-id="6d54d-116">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="6d54d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d54d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d54d-117">-WhatIf</span></span>
<span data-ttu-id="6d54d-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="6d54d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d54d-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="6d54d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d54d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d54d-120">CommonParameters</span></span>
<span data-ttu-id="6d54d-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="6d54d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d54d-122">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6d54d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d54d-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="6d54d-123">INPUTS</span></span>

### <span data-ttu-id="6d54d-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="6d54d-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="6d54d-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="6d54d-125">OUTPUTS</span></span>

### <span data-ttu-id="6d54d-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="6d54d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="6d54d-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="6d54d-127">NOTES</span></span>

## <span data-ttu-id="6d54d-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="6d54d-128">RELATED LINKS</span></span>
