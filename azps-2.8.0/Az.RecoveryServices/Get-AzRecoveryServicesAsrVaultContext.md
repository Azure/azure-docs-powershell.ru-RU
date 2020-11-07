---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: e5bb8a19cb616c9696ec224d8f1d9d25678d9e47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93904950"
---
# <span data-ttu-id="0bc9b-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="0bc9b-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="0bc9b-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="0bc9b-102">SYNOPSIS</span></span>
<span data-ttu-id="0bc9b-103">Возвращает сведения о параметрах хранилища ASR для хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="0bc9b-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="0bc9b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0bc9b-105">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bc9b-105">DESCRIPTION</span></span>
<span data-ttu-id="0bc9b-106">Командлет **Get-AzRecoveryServicesAsrVaultContext** получает сведения о параметрах хранилища ASR, связанных с хранилищем служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="0bc9b-107">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="0bc9b-107">EXAMPLES</span></span>

### <span data-ttu-id="0bc9b-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="0bc9b-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="0bc9b-109">Получает параметры хранилища ASR для текущего активного сеанса (в сеансе PowerShell) в хранилище служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="0bc9b-110">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="0bc9b-110">PARAMETERS</span></span>

### <span data-ttu-id="0bc9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bc9b-111">-DefaultProfile</span></span>
<span data-ttu-id="0bc9b-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bc9b-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bc9b-113">CommonParameters</span></span>
<span data-ttu-id="0bc9b-114">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="0bc9b-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bc9b-115">Дополнительные сведения можно найти в разделе about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0bc9b-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bc9b-116">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="0bc9b-116">INPUTS</span></span>

### <span data-ttu-id="0bc9b-117">Ничего</span><span class="sxs-lookup"><span data-stu-id="0bc9b-117">None</span></span>

## <span data-ttu-id="0bc9b-118">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="0bc9b-118">OUTPUTS</span></span>

### <span data-ttu-id="0bc9b-119">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="0bc9b-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="0bc9b-120">Пуск</span><span class="sxs-lookup"><span data-stu-id="0bc9b-120">NOTES</span></span>

## <span data-ttu-id="0bc9b-121">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="0bc9b-121">RELATED LINKS</span></span>
