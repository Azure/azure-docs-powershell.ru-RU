---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/05/2021
ms.locfileid: "98505861"
---
# <span data-ttu-id="263c1-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="263c1-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="263c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="263c1-102">SYNOPSIS</span></span>
<span data-ttu-id="263c1-103">Удаление ключа сейфа из SQL экземпляра</span><span class="sxs-lookup"><span data-stu-id="263c1-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="263c1-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="263c1-104">SYNTAX</span></span>

### <span data-ttu-id="263c1-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="263c1-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="263c1-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="263c1-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="263c1-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="263c1-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="263c1-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="263c1-108">DESCRIPTION</span></span>
<span data-ttu-id="263c1-109">Этот Remove-AzSqlInstanceKeyVaultKey удаляет ключ сейфа из указанного управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="263c1-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="263c1-110">Обратите внимание SQL что разрешения управляемого экземпляра для хранилища ключа не меняются.</span><span class="sxs-lookup"><span data-stu-id="263c1-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="263c1-111">Чтобы изменить разрешения, используйте Set-AzKeyVaultAccessPolicy.</span><span class="sxs-lookup"><span data-stu-id="263c1-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="263c1-112">Обратите внимание, что этот cmdlet не изменяет хранилище ключей.</span><span class="sxs-lookup"><span data-stu-id="263c1-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="263c1-113">Чтобы удалить ключ из key Vault, используйте Remove-AzureKeyVaultKey.</span><span class="sxs-lookup"><span data-stu-id="263c1-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="263c1-114">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="263c1-114">EXAMPLES</span></span>

### <span data-ttu-id="263c1-115">Пример 1</span><span class="sxs-lookup"><span data-stu-id="263c1-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="263c1-116">Эта команда удаляет ключ хранилища ключей с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' из указанного управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="263c1-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="263c1-117">Пример 2. Использование объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="263c1-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="263c1-118">Эта команда удаляет ключ хранилища ключей с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' из указанного управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="263c1-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="263c1-119">Пример 3. Использование ИД ресурса управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="263c1-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="263c1-120">Эта команда удаляет ключ хранилища ключей с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' из указанного управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="263c1-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="263c1-121">Пример 4. Использование piping</span><span class="sxs-lookup"><span data-stu-id="263c1-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="263c1-122">Эта команда удаляет ключ хранилища ключей с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' из указанного управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="263c1-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="263c1-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="263c1-123">PARAMETERS</span></span>

### <span data-ttu-id="263c1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="263c1-124">-DefaultProfile</span></span>
<span data-ttu-id="263c1-125">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="263c1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="263c1-126">-Instance</span><span class="sxs-lookup"><span data-stu-id="263c1-126">-Instance</span></span>
<span data-ttu-id="263c1-127">Объект ввода экземпляра</span><span class="sxs-lookup"><span data-stu-id="263c1-127">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="263c1-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="263c1-128">-InstanceName</span></span>
<span data-ttu-id="263c1-129">Имя экземпляра</span><span class="sxs-lookup"><span data-stu-id="263c1-129">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263c1-130">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="263c1-130">-InstanceResourceId</span></span>
<span data-ttu-id="263c1-131">ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="263c1-131">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="263c1-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="263c1-132">-KeyId</span></span>
<span data-ttu-id="263c1-133">Ключ AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="263c1-133">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263c1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="263c1-134">-ResourceGroupName</span></span>
<span data-ttu-id="263c1-135">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="263c1-135">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="263c1-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="263c1-136">-Confirm</span></span>
<span data-ttu-id="263c1-137">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="263c1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="263c1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="263c1-138">-WhatIf</span></span>
<span data-ttu-id="263c1-139">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="263c1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="263c1-140">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="263c1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="263c1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="263c1-141">CommonParameters</span></span>
<span data-ttu-id="263c1-142">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="263c1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="263c1-143">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="263c1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="263c1-144">INPUTS</span><span class="sxs-lookup"><span data-stu-id="263c1-144">INPUTS</span></span>

### <span data-ttu-id="263c1-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="263c1-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="263c1-146">System.String</span><span class="sxs-lookup"><span data-stu-id="263c1-146">System.String</span></span>

## <span data-ttu-id="263c1-147">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="263c1-147">OUTPUTS</span></span>

### <span data-ttu-id="263c1-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="263c1-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="263c1-149">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="263c1-149">NOTES</span></span>

## <span data-ttu-id="263c1-150">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="263c1-150">RELATED LINKS</span></span>
