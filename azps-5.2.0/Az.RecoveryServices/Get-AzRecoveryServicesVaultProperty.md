---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98396295"
---
# <span data-ttu-id="091f2-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="091f2-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="091f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="091f2-102">SYNOPSIS</span></span>
<span data-ttu-id="091f2-103">Возвращает свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="091f2-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="091f2-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="091f2-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="091f2-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="091f2-105">DESCRIPTION</span></span>
<span data-ttu-id="091f2-106">**Cmdlet Get-AzRecoveryServicesVaultProperty** возвращает свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="091f2-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="091f2-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="091f2-107">EXAMPLES</span></span>

### <span data-ttu-id="091f2-108">Пример 1. Свойства сейфа</span><span class="sxs-lookup"><span data-stu-id="091f2-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="091f2-109">Первая команда получает объект Vault, а затем сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="091f2-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="091f2-110">Вторая команда получает свойства сейфа.</span><span class="sxs-lookup"><span data-stu-id="091f2-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="091f2-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="091f2-111">PARAMETERS</span></span>

### <span data-ttu-id="091f2-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="091f2-112">-DefaultProfile</span></span>
<span data-ttu-id="091f2-113">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="091f2-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="091f2-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="091f2-114">-VaultId</span></span>
<span data-ttu-id="091f2-115">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="091f2-115">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="091f2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="091f2-116">CommonParameters</span></span>
<span data-ttu-id="091f2-117">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="091f2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="091f2-118">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="091f2-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="091f2-119">INPUTS</span><span class="sxs-lookup"><span data-stu-id="091f2-119">INPUTS</span></span>

### <span data-ttu-id="091f2-120">System.String</span><span class="sxs-lookup"><span data-stu-id="091f2-120">System.String</span></span>

## <span data-ttu-id="091f2-121">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="091f2-121">OUTPUTS</span></span>

### <span data-ttu-id="091f2-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="091f2-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="091f2-123">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="091f2-123">NOTES</span></span>

## <span data-ttu-id="091f2-124">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="091f2-124">RELATED LINKS</span></span>

[<span data-ttu-id="091f2-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="091f2-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="091f2-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="091f2-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
