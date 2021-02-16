---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: da541e9f019dfb82efc496ce60ab300229e36ac0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/09/2021
ms.locfileid: "100226993"
---
# <span data-ttu-id="cba78-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="cba78-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="cba78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cba78-102">SYNOPSIS</span></span>
<span data-ttu-id="cba78-103">Возвращает свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cba78-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="cba78-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="cba78-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cba78-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="cba78-105">DESCRIPTION</span></span>
<span data-ttu-id="cba78-106">**Cmdlet Get-AzRecoveryServicesVaultProperty** возвращает свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cba78-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="cba78-107">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="cba78-107">EXAMPLES</span></span>

### <span data-ttu-id="cba78-108">Пример 1. Свойства сейфа</span><span class="sxs-lookup"><span data-stu-id="cba78-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="cba78-109">Первая команда получает объект Vault, а затем сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="cba78-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="cba78-110">Вторая команда получает свойства сейфа.</span><span class="sxs-lookup"><span data-stu-id="cba78-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="cba78-111">Теперь мы будем получать доступ к свойствам шифрования сейфа.</span><span class="sxs-lookup"><span data-stu-id="cba78-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="cba78-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cba78-112">PARAMETERS</span></span>

### <span data-ttu-id="cba78-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cba78-113">-DefaultProfile</span></span>
<span data-ttu-id="cba78-114">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="cba78-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cba78-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="cba78-115">-VaultId</span></span>
<span data-ttu-id="cba78-116">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="cba78-116">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="cba78-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cba78-117">CommonParameters</span></span>
<span data-ttu-id="cba78-118">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cba78-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cba78-119">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cba78-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cba78-120">INPUTS</span><span class="sxs-lookup"><span data-stu-id="cba78-120">INPUTS</span></span>

### <span data-ttu-id="cba78-121">System.String</span><span class="sxs-lookup"><span data-stu-id="cba78-121">System.String</span></span>

## <span data-ttu-id="cba78-122">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cba78-122">OUTPUTS</span></span>

### <span data-ttu-id="cba78-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="cba78-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="cba78-124">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="cba78-124">NOTES</span></span>

## <span data-ttu-id="cba78-125">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="cba78-125">RELATED LINKS</span></span>

[<span data-ttu-id="cba78-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="cba78-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="cba78-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="cba78-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
