---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: a88b137b5735984ce6b5f19389d9035b85b1dfe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997380"
---
# <span data-ttu-id="3b40e-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="3b40e-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="3b40e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b40e-102">SYNOPSIS</span></span>
<span data-ttu-id="3b40e-103">Обновляет свойства сейфа.</span><span class="sxs-lookup"><span data-stu-id="3b40e-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="3b40e-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3b40e-104">SYNTAX</span></span>

### <span data-ttu-id="3b40e-105">AzureRSVaultSoftDelteParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3b40e-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b40e-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b40e-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b40e-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3b40e-107">DESCRIPTION</span></span>
<span data-ttu-id="3b40e-108">**Cmdlet Set-AzRecoveryServicesVaultProperty** обновляет свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="3b40e-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="3b40e-109">С помощью этого cmdlet можно включить или отключить soft delete или настроить шифрование CMK для хранилища с двумя различными наборами параметров.</span><span class="sxs-lookup"><span data-stu-id="3b40e-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="3b40e-110">**Свойство SoftDeleteFeatureState** хранилища можно отключить только в том случае, если в сейфе нет зарегистрированных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="3b40e-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="3b40e-111">InfrastructurEncryption можно настроить только при первом обновлении пользователем хранилища CMK.</span><span class="sxs-lookup"><span data-stu-id="3b40e-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="3b40e-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3b40e-112">EXAMPLES</span></span>

### <span data-ttu-id="3b40e-113">Пример 1. Обновление статуса softDeleteFeature для сейфа</span><span class="sxs-lookup"><span data-stu-id="3b40e-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="3b40e-114">Первая команда получает объект Vault, а затем сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="3b40e-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="3b40e-115">Вторая команда обновляет свойство SoftDeleteFeatureState сейфа до состояния Enabled.</span><span class="sxs-lookup"><span data-stu-id="3b40e-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="3b40e-116">Пример 2. Обновление шифрования CMK в хранилище</span><span class="sxs-lookup"><span data-stu-id="3b40e-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="3b40e-117">Первый cmdlet получает RSVault для обновления свойств шифрования.</span><span class="sxs-lookup"><span data-stu-id="3b40e-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="3b40e-118">Второй cmdlet получает хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="3b40e-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="3b40e-119">Третий cmdlet get the key from the key vault.</span><span class="sxs-lookup"><span data-stu-id="3b40e-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="3b40e-120">Четвертый cmdlet обновляет ключ шифрования, управляемый клиентом, в RSVault.</span><span class="sxs-lookup"><span data-stu-id="3b40e-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="3b40e-121">Используйте параметр "-InfrastructureEncryption param", чтобы включить шифрование инфраструктуры при первом обновлении.</span><span class="sxs-lookup"><span data-stu-id="3b40e-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="3b40e-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3b40e-122">PARAMETERS</span></span>

### <span data-ttu-id="3b40e-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b40e-123">-DefaultProfile</span></span>
<span data-ttu-id="3b40e-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3b40e-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b40e-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="3b40e-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="3b40e-126">SoftDeleteFeatureState хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="3b40e-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enable, Disable

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b40e-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="3b40e-127">-EncryptionKeyId</span></span>
<span data-ttu-id="3b40e-128">KeyId ключа шифрования, который будет использоваться для CMK.</span><span class="sxs-lookup"><span data-stu-id="3b40e-128">KeyId of the encryption key to be used for CMK.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: KeyID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b40e-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3b40e-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="3b40e-130">ИД подписки на хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3b40e-130">Subscription Id of the Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: SubscriptionID

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b40e-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="3b40e-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="3b40e-132">Включает шифрование инфраструктуры в этом хранилище.</span><span class="sxs-lookup"><span data-stu-id="3b40e-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="3b40e-133">При настройке шифрования необходимо включить шифрование инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="3b40e-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b40e-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3b40e-134">-VaultId</span></span>
<span data-ttu-id="3b40e-135">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="3b40e-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3b40e-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3b40e-136">-Confirm</span></span>
<span data-ttu-id="3b40e-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b40e-137">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b40e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b40e-138">-WhatIf</span></span>
<span data-ttu-id="3b40e-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b40e-139">Shows what would happen if the cmdlet runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b40e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b40e-140">CommonParameters</span></span>
<span data-ttu-id="3b40e-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b40e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b40e-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3b40e-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b40e-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3b40e-143">INPUTS</span></span>

### <span data-ttu-id="3b40e-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3b40e-144">System.String</span></span>

### <span data-ttu-id="3b40e-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="3b40e-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="3b40e-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3b40e-146">OUTPUTS</span></span>

### <span data-ttu-id="3b40e-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="3b40e-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="3b40e-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3b40e-148">NOTES</span></span>

## <span data-ttu-id="3b40e-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3b40e-149">RELATED LINKS</span></span>

[<span data-ttu-id="3b40e-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3b40e-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="3b40e-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="3b40e-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
