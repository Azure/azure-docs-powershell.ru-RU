---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: e6bd0284d9ce5b5cb6973fce6aae5e16a4c06883
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98506792"
---
# <span data-ttu-id="3199a-101">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="3199a-101">Set-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="3199a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3199a-102">SYNOPSIS</span></span>
<span data-ttu-id="3199a-103">Обновляет свойства сейфа.</span><span class="sxs-lookup"><span data-stu-id="3199a-103">Updates properties of a Vault.</span></span>

## <span data-ttu-id="3199a-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="3199a-104">SYNTAX</span></span>

### <span data-ttu-id="3199a-105">AzureRSVaultSoftDelteParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="3199a-105">AzureRSVaultSoftDelteParameterSet (Default)</span></span>
```
Set-AzRecoveryServicesVaultProperty -SoftDeleteFeatureState <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3199a-106">AzureRSVaultCMKParameterSet</span><span class="sxs-lookup"><span data-stu-id="3199a-106">AzureRSVaultCMKParameterSet</span></span>
```
Set-AzRecoveryServicesVaultProperty -EncryptionKeyId <string> -KeyVaultSubscriptionId <string> [-InfrastructureEncryption] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3199a-107">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="3199a-107">DESCRIPTION</span></span>
<span data-ttu-id="3199a-108">**Cmdlet Set-AzRecoveryServicesVaultProperty** обновляет свойства хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="3199a-108">The **Set-AzRecoveryServicesVaultProperty** cmdlet updates properties of a Recovery services vault.</span></span> <span data-ttu-id="3199a-109">С помощью этого cmdlet можно включить или отключить soft delete или настроить шифрование CMK для хранилища с двумя различными наборами параметров.</span><span class="sxs-lookup"><span data-stu-id="3199a-109">This cmdlet can be used to enable/disable soft delete or set CMK encryption for a vault with two different parameter sets.</span></span> 
<span data-ttu-id="3199a-110">**Свойство SoftDeleteFeatureState** хранилища можно отключить только в том случае, если в сейфе нет зарегистрированных контейнеров.</span><span class="sxs-lookup"><span data-stu-id="3199a-110">**SoftDeleteFeatureState** property of a vault can be disabled only if there are no registered containers in the vault.</span></span> <span data-ttu-id="3199a-111">InfrastructurEncryption можно настроить только при первом обновлении пользователем хранилища CMK.</span><span class="sxs-lookup"><span data-stu-id="3199a-111">InfrastructurEncryption can only be set the first time a user updates the CMK vault.</span></span>

## <span data-ttu-id="3199a-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="3199a-112">EXAMPLES</span></span>

### <span data-ttu-id="3199a-113">Пример 1. Обновление статуса softDeleteFeature для сейфа</span><span class="sxs-lookup"><span data-stu-id="3199a-113">Example 1: Update SoftDeleteFeatureState of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $props = Set-AzRecoveryServicesVaultProperty -VaultId $vault.Id -SoftDeleteFeatureState Enable
```

<span data-ttu-id="3199a-114">Первая команда получает объект Vault, а затем сохраняет его в $vault переменной.</span><span class="sxs-lookup"><span data-stu-id="3199a-114">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="3199a-115">Вторая команда обновляет свойство SoftDeleteFeatureState хранилища до состояния Enabled.</span><span class="sxs-lookup"><span data-stu-id="3199a-115">The second command Updates the SoftDeleteFeatureState property of the vault to "Enabled" state.</span></span>

### <span data-ttu-id="3199a-116">Пример 2. Обновление шифрования CMK в хранилище</span><span class="sxs-lookup"><span data-stu-id="3199a-116">Example 2: Update CMK encryption of a vault</span></span>

```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "rgName" -Name "vaultName"
PS C:\> $keyVault = Get-AzKeyVault -VaultName "keyVaultName" -ResourceGroupName "RGName" 
PS C:\> $key = Get-AzKeyVaultKey -VaultName "keyVaultName" -Name "keyName" 
PS C:\> Set-AzRecoveryServicesVaultProperty -EncryptionKeyId $key.ID -KeyVaultSubscriptionId "f870818k-5h28-4t48-8961-37458592348r" -InfrastructureEncryption -VaultId $vault.ID
```

<span data-ttu-id="3199a-117">Первый cmdlet получает RSVault для обновления свойств шифрования.</span><span class="sxs-lookup"><span data-stu-id="3199a-117">First cmdlet gets the RSVault to update encryption properties.</span></span> <span data-ttu-id="3199a-118">Второй cmdlet получает хранилище ключей Azure.</span><span class="sxs-lookup"><span data-stu-id="3199a-118">Second cmdlet gets the azure key vault.</span></span> <span data-ttu-id="3199a-119">Третий cmdlet get the key from the key vault.</span><span class="sxs-lookup"><span data-stu-id="3199a-119">Third cmdlet get the key from the key vault.</span></span>
<span data-ttu-id="3199a-120">Четвертый cmdlet обновляет ключ шифрования, управляемый клиентом, в RSVault.</span><span class="sxs-lookup"><span data-stu-id="3199a-120">Fourth cmdlet updates the customer managed encryption key within the RSVault.</span></span> <span data-ttu-id="3199a-121">Используйте параметр "-InfrastructureEncryption param", чтобы включить шифрование инфраструктуры при первом обновлении.</span><span class="sxs-lookup"><span data-stu-id="3199a-121">Use -InfrastructureEncryption param to enable infrastructure encryption for the first time update.</span></span> 

## <span data-ttu-id="3199a-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3199a-122">PARAMETERS</span></span>

### <span data-ttu-id="3199a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3199a-123">-DefaultProfile</span></span>
<span data-ttu-id="3199a-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="3199a-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3199a-125">-SoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="3199a-125">-SoftDeleteFeatureState</span></span>
<span data-ttu-id="3199a-126">SoftDeleteFeatureState хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="3199a-126">SoftDeleteFeatureState of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3199a-127">-EncryptionKeyId</span><span class="sxs-lookup"><span data-stu-id="3199a-127">-EncryptionKeyId</span></span>
<span data-ttu-id="3199a-128">KeyId ключа шифрования, который будет использоваться для CMK.</span><span class="sxs-lookup"><span data-stu-id="3199a-128">KeyId of the encryption key to be used for CMK.</span></span>

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

### <span data-ttu-id="3199a-129">-KeyVaultSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3199a-129">-KeyVaultSubscriptionId</span></span>
<span data-ttu-id="3199a-130">ИД подписки на хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="3199a-130">Subscription Id of the Key Vault.</span></span>

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

### <span data-ttu-id="3199a-131">-InfrastructureEncryption</span><span class="sxs-lookup"><span data-stu-id="3199a-131">-InfrastructureEncryption</span></span>
<span data-ttu-id="3199a-132">Включает шифрование инфраструктуры в этом хранилище.</span><span class="sxs-lookup"><span data-stu-id="3199a-132">Enables infrastructure encryption on this vault.</span></span> <span data-ttu-id="3199a-133">При настройке шифрования необходимо включить шифрование инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="3199a-133">Infrastructure encryption must be enabled when configuring encryption.</span></span>

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

### <span data-ttu-id="3199a-134">-VaultId</span><span class="sxs-lookup"><span data-stu-id="3199a-134">-VaultId</span></span>
<span data-ttu-id="3199a-135">ARM ИД хранилища служб восстановления.</span><span class="sxs-lookup"><span data-stu-id="3199a-135">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="3199a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3199a-136">-Confirm</span></span>
<span data-ttu-id="3199a-137">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3199a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3199a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3199a-138">-WhatIf</span></span>
<span data-ttu-id="3199a-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3199a-139">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="3199a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3199a-140">CommonParameters</span></span>
<span data-ttu-id="3199a-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3199a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3199a-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3199a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3199a-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="3199a-143">INPUTS</span></span>

### <span data-ttu-id="3199a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="3199a-144">System.String</span></span>

### <span data-ttu-id="3199a-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span><span class="sxs-lookup"><span data-stu-id="3199a-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.VaultSoftDeleteFeatureState</span></span>

## <span data-ttu-id="3199a-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="3199a-146">OUTPUTS</span></span>

### <span data-ttu-id="3199a-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="3199a-147">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="3199a-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="3199a-148">NOTES</span></span>

## <span data-ttu-id="3199a-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="3199a-149">RELATED LINKS</span></span>

[<span data-ttu-id="3199a-150">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="3199a-150">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="3199a-151">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="3199a-151">Get-AzRecoveryServicesVaultProperty</span></span>](./Get-AzRecoveryServicesVaultProperty.md)
