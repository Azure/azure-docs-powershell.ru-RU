---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100225361"
---
# <span data-ttu-id="3ee1a-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="3ee1a-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="3ee1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3ee1a-102">SYNOPSIS</span></span>

<span data-ttu-id="3ee1a-103">Задает контекст сейфа.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-103">Sets vault context.</span></span>

## <span data-ttu-id="3ee1a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3ee1a-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3ee1a-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3ee1a-105">DESCRIPTION</span></span>

<span data-ttu-id="3ee1a-106">**Cmdlet Set-AzRecoveryServicesVaultContext** задает контекст хранилища для служб восстановления сайтов Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="3ee1a-107">Предупреждение. Этот cmdlet не является готовым к выпуску изменений в будущем.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="3ee1a-108">Заменять его не нужно.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-108">There will be no replacement for it.</span></span> <span data-ttu-id="3ee1a-109">Используйте параметр -VaultId во всех командах служб восстановления в будущем.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="3ee1a-110">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3ee1a-110">EXAMPLES</span></span>

### <span data-ttu-id="3ee1a-111">Пример 1</span><span class="sxs-lookup"><span data-stu-id="3ee1a-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="3ee1a-112">Задает контекст сейфа.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-112">Sets vault context.</span></span>

## <span data-ttu-id="3ee1a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3ee1a-113">PARAMETERS</span></span>

### <span data-ttu-id="3ee1a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3ee1a-114">-DefaultProfile</span></span>

<span data-ttu-id="3ee1a-115">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3ee1a-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="3ee1a-116">-Vault</span></span>

<span data-ttu-id="3ee1a-117">Указывает имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="3ee1a-118">Хранилище должно быть **объектом AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="3ee1a-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="3ee1a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ee1a-119">CommonParameters</span></span>
<span data-ttu-id="3ee1a-120">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ee1a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ee1a-121">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3ee1a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ee1a-122">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3ee1a-122">INPUTS</span></span>

### <span data-ttu-id="3ee1a-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="3ee1a-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="3ee1a-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3ee1a-124">OUTPUTS</span></span>

### <span data-ttu-id="3ee1a-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="3ee1a-125">System.Void</span></span>

## <span data-ttu-id="3ee1a-126">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3ee1a-126">NOTES</span></span>

## <span data-ttu-id="3ee1a-127">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3ee1a-127">RELATED LINKS</span></span>
