---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 817BF177-519F-47BA-86CF-4591FB402E2Dl
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultKey.md
ms.openlocfilehash: bfdd237ecadadae181d9e9dd3a201580537097f0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/13/2020
ms.locfileid: "94236193"
---
# <span data-ttu-id="31797-101">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31797-101">Remove-AzKeyVaultKey</span></span>

## <span data-ttu-id="31797-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="31797-102">SYNOPSIS</span></span>
<span data-ttu-id="31797-103">Удаление ключа из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="31797-103">Deletes a key in a key vault.</span></span>

## <span data-ttu-id="31797-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="31797-104">SYNTAX</span></span>

### <span data-ttu-id="31797-105">ByVaultName (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="31797-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="31797-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="31797-106">ByInputObject</span></span>
```
Remove-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [-Force] [-PassThru] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31797-107">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="31797-107">DESCRIPTION</span></span>
<span data-ttu-id="31797-108">Командлет Remove-AzKeyVaultKey удаляет раздел из хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="31797-108">The Remove-AzKeyVaultKey cmdlet deletes a key in a key vault.</span></span>
<span data-ttu-id="31797-109">Если клавиша была случайно удалена, ключ может быть восстановлен с помощью Undo-AzKeyVaultKeyRemoval пользователем, у которого есть особые разрешения на восстановление.</span><span class="sxs-lookup"><span data-stu-id="31797-109">If the key was accidentally deleted the key can be recovered using Undo-AzKeyVaultKeyRemoval by a user with special 'recover' permissions.</span></span>
<span data-ttu-id="31797-110">Этот командлет имеет значение High для свойства **ConfirmImpact** .</span><span class="sxs-lookup"><span data-stu-id="31797-110">This cmdlet has a value of high for the **ConfirmImpact** property.</span></span>

## <span data-ttu-id="31797-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="31797-111">EXAMPLES</span></span>

### <span data-ttu-id="31797-112">Пример 1: Удаление ключа из хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="31797-112">Example 1: Remove a key from a key vault</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -PassThru

Vault Name           : contoso
Name                 : key2
Id                   : https://contoso.vault.azure.net:443/keys/itsoftware/fdad15793ba0437e960497908ef9eb32
Deleted Date         : 5/24/2018 11:28:25 PM
Scheduled Purge Date : 8/22/2018 11:28:25 PM
Enabled              : False
Expires              : 10/11/2018 11:32:49 PM
Not Before           : 4/11/2018 11:22:49 PM
Created              : 4/12/2018 10:16:38 PM
Updated              : 4/12/2018 10:16:38 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="31797-113">Эта команда удаляет ключ с именем ITSoftware из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="31797-113">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>

### <span data-ttu-id="31797-114">Пример 2: Удаление ключа без подтверждения пользователя</span><span class="sxs-lookup"><span data-stu-id="31797-114">Example 2: Remove a key without user confirmation</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Force
```

<span data-ttu-id="31797-115">Эта команда удаляет ключ с именем ITSoftware из хранилища ключей contoso.</span><span class="sxs-lookup"><span data-stu-id="31797-115">This command removes the key named ITSoftware from the key vault named Contoso.</span></span>
<span data-ttu-id="31797-116">Команда задает параметр *Force* и, следовательно, командлет не запрашивает подтверждение.</span><span class="sxs-lookup"><span data-stu-id="31797-116">The command specifies the *Force* parameter, and, therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="31797-117">Пример 3: Удаление удаленного ключа из хранилища ключей без возможности восстановления</span><span class="sxs-lookup"><span data-stu-id="31797-117">Example 3: Purge a deleted key from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -InRemovedState
```

<span data-ttu-id="31797-118">Эта команда удаляет ключ с именем ITSoftware из хранилища ключей Contoso без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="31797-118">This command removes the key named ITSoftware from the key vault named Contoso permanently.</span></span>
<span data-ttu-id="31797-119">Для выполнения этого командлета требуется разрешение на очистку, которое должно быть ранее и явно предоставлено пользователю для этого хранилища ключей.</span><span class="sxs-lookup"><span data-stu-id="31797-119">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user for this key vault.</span></span>

### <span data-ttu-id="31797-120">Пример 4: Удаление ключей с помощью оператора Pipeline</span><span class="sxs-lookup"><span data-stu-id="31797-120">Example 4: Remove keys by using the pipeline operator</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'Contoso' | Where-Object {$_.Attributes.Enabled -eq $False} | Remove-AzKeyVaultKey
```

<span data-ttu-id="31797-121">Эта команда получает все ключи из хранилища ключей Contoso и передает их в командлет **Where-Object** с помощью оператора конвейера.</span><span class="sxs-lookup"><span data-stu-id="31797-121">This command gets all the keys in the key vault named Contoso, and passes them to the **Where-Object** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="31797-122">Этот командлет передает ключи со значением $False для атрибута **Enabled** для текущего командлета.</span><span class="sxs-lookup"><span data-stu-id="31797-122">That cmdlet passes the keys that have a value of $False for the **Enabled** attribute to the current cmdlet.</span></span>
<span data-ttu-id="31797-123">Этот командлет удаляет эти ключи.</span><span class="sxs-lookup"><span data-stu-id="31797-123">That cmdlet removes those keys.</span></span>

## <span data-ttu-id="31797-124">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="31797-124">PARAMETERS</span></span>

### <span data-ttu-id="31797-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31797-125">-DefaultProfile</span></span>
<span data-ttu-id="31797-126">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="31797-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="31797-127">-Force</span><span class="sxs-lookup"><span data-stu-id="31797-127">-Force</span></span>
<span data-ttu-id="31797-128">Принудительное выполнение команды без запроса подтверждения пользователя.</span><span class="sxs-lookup"><span data-stu-id="31797-128">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31797-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="31797-129">-InputObject</span></span>
<span data-ttu-id="31797-130">Объект KeyBundle</span><span class="sxs-lookup"><span data-stu-id="31797-130">KeyBundle Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31797-131">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="31797-131">-InRemovedState</span></span>
<span data-ttu-id="31797-132">Удаление ранее удаленного ключа без возможности восстановления.</span><span class="sxs-lookup"><span data-stu-id="31797-132">Remove the previously deleted key permanently.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31797-133">-Name (имя)</span><span class="sxs-lookup"><span data-stu-id="31797-133">-Name</span></span>
<span data-ttu-id="31797-134">Задает имя удаляемого ключа.</span><span class="sxs-lookup"><span data-stu-id="31797-134">Specifies the name of the key to remove.</span></span>
<span data-ttu-id="31797-135">Этот командлет создает полное доменное имя (FQDN) ключа на основе имени, которое указывает этот параметр, имя хранилища ключей и текущую среду.</span><span class="sxs-lookup"><span data-stu-id="31797-135">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31797-136">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31797-136">-PassThru</span></span>
<span data-ttu-id="31797-137">Указывает на то, что этот командлет возвращает объект **Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKey** .</span><span class="sxs-lookup"><span data-stu-id="31797-137">Indicates that this cmdlet returns a **Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey** object.</span></span>
<span data-ttu-id="31797-138">По умолчанию этот командлет не создает никаких выходных данных.</span><span class="sxs-lookup"><span data-stu-id="31797-138">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31797-139">-VaultName</span><span class="sxs-lookup"><span data-stu-id="31797-139">-VaultName</span></span>
<span data-ttu-id="31797-140">Указывает имя хранилища ключей, из которого нужно удалить ключ.</span><span class="sxs-lookup"><span data-stu-id="31797-140">Specifies the name of the key vault from which to remove the key.</span></span>
<span data-ttu-id="31797-141">Этот командлет создает полное доменное имя хранилища ключей, основываясь на имени, указанном этим параметром, и текущей среде.</span><span class="sxs-lookup"><span data-stu-id="31797-141">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31797-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="31797-142">-Confirm</span></span>
<span data-ttu-id="31797-143">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="31797-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31797-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31797-144">-WhatIf</span></span>
<span data-ttu-id="31797-145">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31797-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31797-146">Командлет не выполняется. Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="31797-146">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31797-147">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="31797-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31797-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31797-148">CommonParameters</span></span>
<span data-ttu-id="31797-149">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="31797-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31797-150">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="31797-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31797-151">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="31797-151">INPUTS</span></span>

### <span data-ttu-id="31797-152">Microsoft. Azure. Commands. KeyVault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="31797-152">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="31797-153">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="31797-153">OUTPUTS</span></span>

### <span data-ttu-id="31797-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31797-154">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="31797-155">Пуск</span><span class="sxs-lookup"><span data-stu-id="31797-155">NOTES</span></span>

## <span data-ttu-id="31797-156">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="31797-156">RELATED LINKS</span></span>

[<span data-ttu-id="31797-157">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31797-157">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="31797-158">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="31797-158">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="31797-159">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="31797-159">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

[<span data-ttu-id="31797-160">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="31797-160">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

