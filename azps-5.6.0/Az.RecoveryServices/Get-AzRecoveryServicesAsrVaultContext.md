---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 62f27b43158f8b01abc7be48cab93f4bb957258b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958083"
---
# <span data-ttu-id="25349-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="25349-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="25349-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25349-102">SYNOPSIS</span></span>
<span data-ttu-id="25349-103">Gets ASR vault settings information for the Recovery Services vault.</span><span class="sxs-lookup"><span data-stu-id="25349-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="25349-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="25349-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25349-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="25349-105">DESCRIPTION</span></span>
<span data-ttu-id="25349-106">**Cmdlet Get-AzRecoveryServicesAsrVaultContext** получает сведения о параметрах хранилища ASR, связанных с хранилищем служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="25349-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="25349-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="25349-107">EXAMPLES</span></span>

### <span data-ttu-id="25349-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="25349-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="25349-109">Получает параметры хранилища ASR для активного (в сеансе PowerShell) хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="25349-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="25349-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25349-110">PARAMETERS</span></span>

### <span data-ttu-id="25349-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25349-111">-DefaultProfile</span></span>
<span data-ttu-id="25349-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="25349-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25349-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25349-113">CommonParameters</span></span>
<span data-ttu-id="25349-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25349-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25349-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25349-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25349-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="25349-116">INPUTS</span></span>

### <span data-ttu-id="25349-117">Нет</span><span class="sxs-lookup"><span data-stu-id="25349-117">None</span></span>

## <span data-ttu-id="25349-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="25349-118">OUTPUTS</span></span>

### <span data-ttu-id="25349-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="25349-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="25349-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="25349-120">NOTES</span></span>

## <span data-ttu-id="25349-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="25349-121">RELATED LINKS</span></span>
