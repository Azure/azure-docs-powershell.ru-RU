---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506013"
---
# <span data-ttu-id="a1ade-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="a1ade-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="a1ade-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1ade-102">SYNOPSIS</span></span>
<span data-ttu-id="a1ade-103">Получает свойства резервного копирования.</span><span class="sxs-lookup"><span data-stu-id="a1ade-103">Gets Backup properties.</span></span>

## <span data-ttu-id="a1ade-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="a1ade-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1ade-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="a1ade-105">DESCRIPTION</span></span>
<span data-ttu-id="a1ade-106">**Cmdlet Get-AzRecoveryServicesBackupProperty** получает свойства резервной копии хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="a1ade-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="a1ade-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="a1ade-107">EXAMPLES</span></span>

### <span data-ttu-id="a1ade-108">Пример 1</span><span class="sxs-lookup"><span data-stu-id="a1ade-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="a1ade-109">Получить свойство архива для хранилища.</span><span class="sxs-lookup"><span data-stu-id="a1ade-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="a1ade-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1ade-110">PARAMETERS</span></span>

### <span data-ttu-id="a1ade-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1ade-111">-DefaultProfile</span></span>
<span data-ttu-id="a1ade-112">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="a1ade-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1ade-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="a1ade-113">-Vault</span></span>
<span data-ttu-id="a1ade-114">Указывает имя сейфа.</span><span class="sxs-lookup"><span data-stu-id="a1ade-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="a1ade-115">Хранилище должно быть **объектом AzureRmRecoveryServicesVault.**</span><span class="sxs-lookup"><span data-stu-id="a1ade-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="a1ade-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1ade-116">CommonParameters</span></span>
<span data-ttu-id="a1ade-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1ade-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1ade-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1ade-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1ade-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a1ade-119">INPUTS</span></span>

### <span data-ttu-id="a1ade-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="a1ade-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a1ade-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="a1ade-121">OUTPUTS</span></span>

### <span data-ttu-id="a1ade-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="a1ade-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="a1ade-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="a1ade-123">NOTES</span></span>

## <span data-ttu-id="a1ade-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="a1ade-124">RELATED LINKS</span></span>
