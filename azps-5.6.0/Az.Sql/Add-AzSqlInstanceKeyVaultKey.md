---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 5a83d442f0b12731de3a00468283a8539b529fa7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101961523"
---
# <span data-ttu-id="e4693-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="e4693-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="e4693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4693-102">SYNOPSIS</span></span>
<span data-ttu-id="e4693-103">Добавляет ключ сейфа в предоставленный управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e4693-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="e4693-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="e4693-104">SYNTAX</span></span>

### <span data-ttu-id="e4693-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="e4693-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4693-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4693-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4693-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e4693-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4693-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="e4693-108">DESCRIPTION</span></span>
<span data-ttu-id="e4693-109">Этот Add-AzSqlInstanceKeyVaultKey добавляет ключ сейфа в предоставленный управляемый экземпляр.</span><span class="sxs-lookup"><span data-stu-id="e4693-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="e4693-110">У управляемого экземпляра должны быть разрешения на доступ к хранилищу с помощью следующего сценария.</span><span class="sxs-lookup"><span data-stu-id="e4693-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="e4693-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unw vaultKey</span><span class="sxs-lookup"><span data-stu-id="e4693-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="e4693-112">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="e4693-112">EXAMPLES</span></span>

### <span data-ttu-id="e4693-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="e4693-113">Example 1</span></span>
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

<span data-ttu-id="e4693-114">Эта команда добавляет ключ сейфа с ИД ' в управляемый экземпляр https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup. SQL</span><span class="sxs-lookup"><span data-stu-id="e4693-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="e4693-115">Пример 2. Использование объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="e4693-115">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="e4693-116">Эта команда добавляет ключ сейфа с ИД ' в управляемый экземпляр https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup. SQL</span><span class="sxs-lookup"><span data-stu-id="e4693-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="e4693-117">Пример 3. Использование ИД ресурса управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="e4693-117">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="e4693-118">Эта команда добавляет ключ сейфа с ИД ' в управляемый экземпляр https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup. SQL</span><span class="sxs-lookup"><span data-stu-id="e4693-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="e4693-119">Пример 4. Использование piping</span><span class="sxs-lookup"><span data-stu-id="e4693-119">Example 4: Using piping</span></span>
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

<span data-ttu-id="e4693-120">Эта команда добавляет ключ сейфа с ИД ' в управляемый экземпляр https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName в группе ресурсов ContosoResourceGroup. SQL</span><span class="sxs-lookup"><span data-stu-id="e4693-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="e4693-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e4693-121">PARAMETERS</span></span>

### <span data-ttu-id="e4693-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4693-122">-DefaultProfile</span></span>
<span data-ttu-id="e4693-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="e4693-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4693-124">-Instance</span><span class="sxs-lookup"><span data-stu-id="e4693-124">-Instance</span></span>
<span data-ttu-id="e4693-125">Объект ввода экземпляра</span><span class="sxs-lookup"><span data-stu-id="e4693-125">The instance input object</span></span>

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

### <span data-ttu-id="e4693-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="e4693-126">-InstanceName</span></span>
<span data-ttu-id="e4693-127">Имя экземпляра</span><span class="sxs-lookup"><span data-stu-id="e4693-127">The instance name</span></span>

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

### <span data-ttu-id="e4693-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="e4693-128">-InstanceResourceId</span></span>
<span data-ttu-id="e4693-129">ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="e4693-129">The instance resource id</span></span>

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

### <span data-ttu-id="e4693-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="e4693-130">-KeyId</span></span>
<span data-ttu-id="e4693-131">Ключ AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="e4693-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="e4693-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4693-132">-ResourceGroupName</span></span>
<span data-ttu-id="e4693-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="e4693-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="e4693-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e4693-134">-Confirm</span></span>
<span data-ttu-id="e4693-135">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4693-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4693-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4693-136">-WhatIf</span></span>
<span data-ttu-id="e4693-137">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4693-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4693-138">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="e4693-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4693-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4693-139">CommonParameters</span></span>
<span data-ttu-id="e4693-140">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4693-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4693-141">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4693-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4693-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="e4693-142">INPUTS</span></span>

### <span data-ttu-id="e4693-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="e4693-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="e4693-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e4693-144">System.String</span></span>

## <span data-ttu-id="e4693-145">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e4693-145">OUTPUTS</span></span>

### <span data-ttu-id="e4693-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="e4693-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="e4693-147">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="e4693-147">NOTES</span></span>

## <span data-ttu-id="e4693-148">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="e4693-148">RELATED LINKS</span></span>
