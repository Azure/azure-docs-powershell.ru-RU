---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: c85d372ccd17b23fec46655245d050b668a32dc6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93563387"
---
# <span data-ttu-id="948fc-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="948fc-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="948fc-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="948fc-102">SYNOPSIS</span></span>
<span data-ttu-id="948fc-103">Задает контекст хранилища служб восстановления, который будет использоваться для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="948fc-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="948fc-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="948fc-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="948fc-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="948fc-105">DESCRIPTION</span></span>
<span data-ttu-id="948fc-106">Командлет **Set-AzureRmRecoveryServicesAsrVaultContext** задает контекст хранилища Azure Site Recovery для дальнейших операций.</span><span class="sxs-lookup"><span data-stu-id="948fc-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="948fc-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="948fc-107">EXAMPLES</span></span>

### <span data-ttu-id="948fc-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="948fc-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="948fc-109">Задает контексту хранилища указанное хранилище служб восстановления для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="948fc-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="948fc-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="948fc-110">PARAMETERS</span></span>

### <span data-ttu-id="948fc-111">-Confirm</span><span class="sxs-lookup"><span data-stu-id="948fc-111">-Confirm</span></span>
<span data-ttu-id="948fc-112">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="948fc-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="948fc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948fc-113">-DefaultProfile</span></span>
<span data-ttu-id="948fc-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="948fc-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="948fc-115">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="948fc-115">-Vault</span></span>
<span data-ttu-id="948fc-116">Объект хранилища служб восстановления, соответствующий хранилищу служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="948fc-116">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="948fc-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948fc-117">-WhatIf</span></span>
<span data-ttu-id="948fc-118">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="948fc-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="948fc-119">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="948fc-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="948fc-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948fc-120">CommonParameters</span></span>
<span data-ttu-id="948fc-121">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="948fc-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948fc-122">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948fc-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948fc-123">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="948fc-123">INPUTS</span></span>

### <span data-ttu-id="948fc-124">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="948fc-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="948fc-125">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="948fc-125">OUTPUTS</span></span>

### <span data-ttu-id="948fc-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="948fc-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="948fc-127">Пуск</span><span class="sxs-lookup"><span data-stu-id="948fc-127">NOTES</span></span>

## <span data-ttu-id="948fc-128">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="948fc-128">RELATED LINKS</span></span>
