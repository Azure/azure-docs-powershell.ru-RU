---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 0a809f9ef3d3c89edc7571b9bb7b7cc2f03e043b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93734791"
---
# <span data-ttu-id="603e7-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="603e7-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="603e7-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="603e7-102">SYNOPSIS</span></span>
<span data-ttu-id="603e7-103">Возвращает сведения о параметрах хранилища ASR для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="603e7-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="603e7-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="603e7-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [<CommonParameters>]
```

## <span data-ttu-id="603e7-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="603e7-105">DESCRIPTION</span></span>
<span data-ttu-id="603e7-106">Командлет **Get-AzureRmRecoveryServicesAsrVaultContext** получает сведения о параметрах хранилища ASR, связанных с хранилищем служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="603e7-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="603e7-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="603e7-107">EXAMPLES</span></span>

### <span data-ttu-id="603e7-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="603e7-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="603e7-109">Получает параметры хранилища ASR для текущего активного сеанса (в сеансе PowerShell) в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="603e7-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="603e7-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="603e7-110">PARAMETERS</span></span>

### <span data-ttu-id="603e7-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="603e7-111">CommonParameters</span></span>
<span data-ttu-id="603e7-112">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="603e7-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="603e7-113">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="603e7-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="603e7-114">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="603e7-114">INPUTS</span></span>

### <span data-ttu-id="603e7-115">Ничего</span><span class="sxs-lookup"><span data-stu-id="603e7-115">None</span></span>

## <span data-ttu-id="603e7-116">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="603e7-116">OUTPUTS</span></span>

### <span data-ttu-id="603e7-117">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="603e7-117">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="603e7-118">Пуск</span><span class="sxs-lookup"><span data-stu-id="603e7-118">NOTES</span></span>

## <span data-ttu-id="603e7-119">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="603e7-119">RELATED LINKS</span></span>

