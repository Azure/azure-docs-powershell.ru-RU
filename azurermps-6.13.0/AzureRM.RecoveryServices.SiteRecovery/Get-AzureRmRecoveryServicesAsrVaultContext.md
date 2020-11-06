---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 52535af7a2e7e9282a94c07f62154e42fe807a82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93568165"
---
# <span data-ttu-id="e9348-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="e9348-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="e9348-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="e9348-102">SYNOPSIS</span></span>
<span data-ttu-id="e9348-103">Возвращает сведения о параметрах хранилища ASR для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e9348-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9348-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="e9348-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9348-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9348-105">DESCRIPTION</span></span>
<span data-ttu-id="e9348-106">Командлет **Get-AzureRmRecoveryServicesAsrVaultContext** получает сведения о параметрах хранилища ASR, связанных с хранилищем служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e9348-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="e9348-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="e9348-107">EXAMPLES</span></span>

### <span data-ttu-id="e9348-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e9348-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="e9348-109">Получает параметры хранилища ASR для текущего активного сеанса (в сеансе PowerShell) в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="e9348-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="e9348-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="e9348-110">PARAMETERS</span></span>

### <span data-ttu-id="e9348-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9348-111">-DefaultProfile</span></span>
<span data-ttu-id="e9348-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e9348-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9348-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9348-113">CommonParameters</span></span>
<span data-ttu-id="e9348-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="e9348-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9348-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9348-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9348-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="e9348-116">INPUTS</span></span>

### <span data-ttu-id="e9348-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="e9348-117">None</span></span>

## <span data-ttu-id="e9348-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="e9348-118">OUTPUTS</span></span>

### <span data-ttu-id="e9348-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="e9348-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="e9348-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="e9348-120">NOTES</span></span>

## <span data-ttu-id="e9348-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e9348-121">RELATED LINKS</span></span>
