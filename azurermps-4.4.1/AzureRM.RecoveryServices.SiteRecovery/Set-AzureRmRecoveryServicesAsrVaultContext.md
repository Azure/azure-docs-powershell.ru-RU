---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: f8d55ec80c6120f2159969ae6a58a531bea50b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93562251"
---
# <span data-ttu-id="c7acc-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="c7acc-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="c7acc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="c7acc-102">SYNOPSIS</span></span>
<span data-ttu-id="c7acc-103">Задает контекст хранилища служб восстановления, который будет использоваться для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c7acc-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7acc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="c7acc-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7acc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7acc-105">DESCRIPTION</span></span>
<span data-ttu-id="c7acc-106">Командлет **Set-AzureRmRecoveryServicesAsrVaultContext** задает контекст хранилища Azure Site Recovery для дальнейших операций.</span><span class="sxs-lookup"><span data-stu-id="c7acc-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="c7acc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="c7acc-107">EXAMPLES</span></span>

### <span data-ttu-id="c7acc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="c7acc-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="c7acc-109">Задает контексту хранилища указанное хранилище служб восстановления для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c7acc-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="c7acc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="c7acc-110">PARAMETERS</span></span>

### <span data-ttu-id="c7acc-111">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="c7acc-111">-Vault</span></span>
<span data-ttu-id="c7acc-112">Объект хранилища служб восстановления, соответствующий хранилищу служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="c7acc-112">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c7acc-113">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c7acc-113">-Confirm</span></span>
<span data-ttu-id="c7acc-114">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="c7acc-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7acc-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7acc-115">-WhatIf</span></span>
<span data-ttu-id="c7acc-116">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="c7acc-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7acc-117">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="c7acc-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7acc-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7acc-118">CommonParameters</span></span>
<span data-ttu-id="c7acc-119">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="c7acc-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7acc-120">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7acc-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7acc-121">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="c7acc-121">INPUTS</span></span>

### <span data-ttu-id="c7acc-122">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="c7acc-122">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="c7acc-123">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="c7acc-123">OUTPUTS</span></span>

### <span data-ttu-id="c7acc-124">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="c7acc-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="c7acc-125">Пуск</span><span class="sxs-lookup"><span data-stu-id="c7acc-125">NOTES</span></span>

## <span data-ttu-id="c7acc-126">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c7acc-126">RELATED LINKS</span></span>

