---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 3d0761ff05a0cdcd775a234b4da0a50d27c2ba08
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93558367"
---
# <span data-ttu-id="23f69-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="23f69-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="23f69-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="23f69-102">SYNOPSIS</span></span>
<span data-ttu-id="23f69-103">Задает контекст хранилища служб восстановления, который будет использоваться для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="23f69-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23f69-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="23f69-104">SYNTAX</span></span>

### <span data-ttu-id="23f69-105">AzureRecoveryServicesVault (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="23f69-105">AzureRecoveryServicesVault (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="23f69-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="23f69-106">ByResourceId</span></span>
```
Set-AzureRmRecoveryServicesAsrVaultContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23f69-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="23f69-107">DESCRIPTION</span></span>
<span data-ttu-id="23f69-108">Командлет **Set-AzureRmRecoveryServicesAsrVaultContext** задает контекст хранилища Azure Site Recovery для дальнейших операций.</span><span class="sxs-lookup"><span data-stu-id="23f69-108">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="23f69-109">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="23f69-109">EXAMPLES</span></span>

### <span data-ttu-id="23f69-110">Пример 1</span><span class="sxs-lookup"><span data-stu-id="23f69-110">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="23f69-111">Задает контексту хранилища указанное хранилище служб восстановления для последующих операций восстановления сайта Azure в текущем сеансе PowerShell.</span><span class="sxs-lookup"><span data-stu-id="23f69-111">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="23f69-112">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="23f69-112">PARAMETERS</span></span>

### <span data-ttu-id="23f69-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23f69-113">-DefaultProfile</span></span>
<span data-ttu-id="23f69-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="23f69-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23f69-115">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23f69-115">-ResourceId</span></span>
<span data-ttu-id="23f69-116">Указывает идентификатор ресурса хранилища recoveryservices, который нужно задать в качестве контекста хранилища.</span><span class="sxs-lookup"><span data-stu-id="23f69-116">Specifies the recoveryservices vault resource id to be set as Vault context.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23f69-117">-Хранилище</span><span class="sxs-lookup"><span data-stu-id="23f69-117">-Vault</span></span>
<span data-ttu-id="23f69-118">Объект хранилища служб восстановления, соответствующий хранилищу служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="23f69-118">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="23f69-119">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23f69-119">-Confirm</span></span>
<span data-ttu-id="23f69-120">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="23f69-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23f69-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23f69-121">-WhatIf</span></span>
<span data-ttu-id="23f69-122">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="23f69-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23f69-123">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="23f69-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23f69-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23f69-124">CommonParameters</span></span>
<span data-ttu-id="23f69-125">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="23f69-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23f69-126">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23f69-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23f69-127">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="23f69-127">INPUTS</span></span>

### <span data-ttu-id="23f69-128">Microsoft. Azure. Commands. RecoveryServices. ARSVault</span><span class="sxs-lookup"><span data-stu-id="23f69-128">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="23f69-129">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="23f69-129">OUTPUTS</span></span>

### <span data-ttu-id="23f69-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="23f69-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="23f69-131">Пуск</span><span class="sxs-lookup"><span data-stu-id="23f69-131">NOTES</span></span>

## <span data-ttu-id="23f69-132">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="23f69-132">RELATED LINKS</span></span>
