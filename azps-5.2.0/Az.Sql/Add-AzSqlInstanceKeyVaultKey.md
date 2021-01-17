---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98392735"
---
# <span data-ttu-id="40eb9-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="40eb9-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="40eb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40eb9-102">SYNOPSIS</span></span>
<span data-ttu-id="40eb9-103">Добавляет ключ сейфа в предоставленный управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="40eb9-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="40eb9-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="40eb9-104">SYNTAX</span></span>

### <span data-ttu-id="40eb9-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="40eb9-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40eb9-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="40eb9-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40eb9-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40eb9-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40eb9-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="40eb9-108">DESCRIPTION</span></span>
<span data-ttu-id="40eb9-109">Этот Add-AzSqlInstanceKeyVaultKey добавляет ключ сейфа в предоставленный управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="40eb9-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="40eb9-110">У управляемого экземпляра должны быть разрешения на доступ к хранилищу "get, wrapKey, unw переупоситьKey", а для его предоставления используйте следующий сценарий:</span><span class="sxs-lookup"><span data-stu-id="40eb9-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="40eb9-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unw vaultKey</span><span class="sxs-lookup"><span data-stu-id="40eb9-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="40eb9-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="40eb9-112">EXAMPLES</span></span>

### <span data-ttu-id="40eb9-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="40eb9-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="40eb9-114">Эта команда добавляет ключ сейфа с ИД SQL ' в управляемый экземпляр https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="40eb9-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="40eb9-115">Пример 2. Использование объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="40eb9-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="40eb9-116">Эта команда добавляет ключ сейфа с ИД SQL ' в управляемый экземпляр https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="40eb9-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="40eb9-117">Пример 3. Использование ИД ресурса управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="40eb9-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="40eb9-118">Эта команда добавляет ключ сейфа с ИД SQL ' в управляемый экземпляр https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="40eb9-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="40eb9-119">Пример 4. Использование piping</span><span class="sxs-lookup"><span data-stu-id="40eb9-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="40eb9-120">Эта команда добавляет ключ сейфа с ИД SQL ' в управляемый экземпляр https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="40eb9-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="40eb9-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40eb9-121">PARAMETERS</span></span>

### <span data-ttu-id="40eb9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40eb9-122">-DefaultProfile</span></span>
<span data-ttu-id="40eb9-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="40eb9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40eb9-124">-Instance</span><span class="sxs-lookup"><span data-stu-id="40eb9-124">-Instance</span></span>
<span data-ttu-id="40eb9-125">Объект ввода экземпляра</span><span class="sxs-lookup"><span data-stu-id="40eb9-125">The instance input object</span></span>

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

### <span data-ttu-id="40eb9-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="40eb9-126">-InstanceName</span></span>
<span data-ttu-id="40eb9-127">Имя экземпляра</span><span class="sxs-lookup"><span data-stu-id="40eb9-127">The instance name</span></span>

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

### <span data-ttu-id="40eb9-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="40eb9-128">-InstanceResourceId</span></span>
<span data-ttu-id="40eb9-129">ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="40eb9-129">The instance resource id</span></span>

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

### <span data-ttu-id="40eb9-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="40eb9-130">-KeyId</span></span>
<span data-ttu-id="40eb9-131">Ключ AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="40eb9-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="40eb9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40eb9-132">-ResourceGroupName</span></span>
<span data-ttu-id="40eb9-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="40eb9-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="40eb9-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="40eb9-134">-Confirm</span></span>
<span data-ttu-id="40eb9-135">Перед запуском cmdlet вам будет предложено подтвердить его.</span><span class="sxs-lookup"><span data-stu-id="40eb9-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40eb9-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40eb9-136">-WhatIf</span></span>
<span data-ttu-id="40eb9-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40eb9-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40eb9-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="40eb9-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40eb9-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40eb9-139">CommonParameters</span></span>
<span data-ttu-id="40eb9-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40eb9-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40eb9-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40eb9-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40eb9-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="40eb9-142">INPUTS</span></span>

### <span data-ttu-id="40eb9-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="40eb9-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="40eb9-144">System.String</span><span class="sxs-lookup"><span data-stu-id="40eb9-144">System.String</span></span>

## <span data-ttu-id="40eb9-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="40eb9-145">OUTPUTS</span></span>

### <span data-ttu-id="40eb9-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="40eb9-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="40eb9-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="40eb9-147">NOTES</span></span>

## <span data-ttu-id="40eb9-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="40eb9-148">RELATED LINKS</span></span>
