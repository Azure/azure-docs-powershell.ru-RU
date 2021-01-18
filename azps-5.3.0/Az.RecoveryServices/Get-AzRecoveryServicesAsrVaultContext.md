---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98508102"
---
# <span data-ttu-id="200b0-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="200b0-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="200b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="200b0-102">SYNOPSIS</span></span>
<span data-ttu-id="200b0-103">Gets ASR vault settings information for the Recovery Services vault.</span><span class="sxs-lookup"><span data-stu-id="200b0-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="200b0-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="200b0-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="200b0-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="200b0-105">DESCRIPTION</span></span>
<span data-ttu-id="200b0-106">**Cmdlet Get-AzRecoveryServicesAsrVaultContext** получает сведения о параметрах хранилища ASR, связанные с хранилищем служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="200b0-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="200b0-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="200b0-107">EXAMPLES</span></span>

### <span data-ttu-id="200b0-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="200b0-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="200b0-109">Получает параметры хранилища ASR для активного (в сеансе PowerShell) хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="200b0-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="200b0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="200b0-110">PARAMETERS</span></span>

### <span data-ttu-id="200b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="200b0-111">-DefaultProfile</span></span>
<span data-ttu-id="200b0-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="200b0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="200b0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="200b0-113">CommonParameters</span></span>
<span data-ttu-id="200b0-114">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="200b0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="200b0-115">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="200b0-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="200b0-116">INPUTS</span><span class="sxs-lookup"><span data-stu-id="200b0-116">INPUTS</span></span>

### <span data-ttu-id="200b0-117">Нет</span><span class="sxs-lookup"><span data-stu-id="200b0-117">None</span></span>

## <span data-ttu-id="200b0-118">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="200b0-118">OUTPUTS</span></span>

### <span data-ttu-id="200b0-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="200b0-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="200b0-120">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="200b0-120">NOTES</span></span>

## <span data-ttu-id="200b0-121">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="200b0-121">RELATED LINKS</span></span>
