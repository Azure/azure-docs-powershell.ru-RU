---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 2be1ca7de1728d1aed7758cd170cb608c7645f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "93567957"
---
# <span data-ttu-id="ff873-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="ff873-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="ff873-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="ff873-102">SYNOPSIS</span></span>
<span data-ttu-id="ff873-103">Возвращает сведения о параметрах хранилища ASR для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="ff873-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ff873-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="ff873-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff873-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff873-105">DESCRIPTION</span></span>
<span data-ttu-id="ff873-106">Командлет **Get-AzureRmRecoveryServicesAsrVaultContext** получает сведения о параметрах хранилища ASR, связанных с хранилищем служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="ff873-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="ff873-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="ff873-107">EXAMPLES</span></span>

### <span data-ttu-id="ff873-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="ff873-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="ff873-109">Получает параметры хранилища ASR для текущего активного сеанса (в сеансе PowerShell) в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="ff873-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="ff873-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="ff873-110">PARAMETERS</span></span>

### <span data-ttu-id="ff873-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff873-111">-DefaultProfile</span></span>
<span data-ttu-id="ff873-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="ff873-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff873-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff873-113">CommonParameters</span></span>
<span data-ttu-id="ff873-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="ff873-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff873-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff873-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff873-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="ff873-116">INPUTS</span></span>

### <span data-ttu-id="ff873-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="ff873-117">None</span></span>

## <span data-ttu-id="ff873-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="ff873-118">OUTPUTS</span></span>

### <span data-ttu-id="ff873-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="ff873-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="ff873-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="ff873-120">NOTES</span></span>

## <span data-ttu-id="ff873-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="ff873-121">RELATED LINKS</span></span>
