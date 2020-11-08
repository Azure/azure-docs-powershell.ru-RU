---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 0ceaf3906860916c4740c3d06d1c9ee91be421cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/21/2020
ms.locfileid: "94065740"
---
# <span data-ttu-id="44828-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="44828-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="44828-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="44828-102">SYNOPSIS</span></span>
<span data-ttu-id="44828-103">Добавляет ключ хранилища ключей к указанному управляемому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="44828-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="44828-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="44828-104">SYNTAX</span></span>

### <span data-ttu-id="44828-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="44828-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44828-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="44828-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="44828-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="44828-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44828-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="44828-108">DESCRIPTION</span></span>
<span data-ttu-id="44828-109">Командлет Add-AzSqlInstanceKeyVaultKey добавляет ключ хранилища ключей к указанному управляемому экземпляру.</span><span class="sxs-lookup"><span data-stu-id="44828-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="44828-110">Управляемый экземпляр должен иметь разрешения "Get, wrapKey, unwrapKey" для хранилища, для предоставления разрешения на управляемый экземпляр с помощью следующего сценария.</span><span class="sxs-lookup"><span data-stu-id="44828-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="44828-111">$managedInstance = Get-AzSqlInstance-Name "ContosoManagedInstanceName"-ResourceGroupName "ContosoResourceGroup" Set-AzKeyVaultAccessPolicy-VaultName ContosoVault-ObjectId $managedInstance. Identity. PrincipalId-PermissionsToKeys Get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="44828-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="44828-112">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="44828-112">EXAMPLES</span></span>

### <span data-ttu-id="44828-113">Пример 1</span><span class="sxs-lookup"><span data-stu-id="44828-113">Example 1</span></span>
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

<span data-ttu-id="44828-114">Эта команда добавляет ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName" в управляемый экземпляр SQL Server "ContosoResourceGroup" в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44828-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="44828-115">Пример 2: использование объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="44828-115">Example 2: Using managed instance object</span></span>
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

<span data-ttu-id="44828-116">Эта команда добавляет ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName" в управляемый экземпляр SQL Server "ContosoResourceGroup" в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44828-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="44828-117">Пример 3: использование идентификатора ресурса управляемых экземпляров</span><span class="sxs-lookup"><span data-stu-id="44828-117">Example 3: Using managed instance resource id</span></span>
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

<span data-ttu-id="44828-118">Эта команда добавляет ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName" в управляемый экземпляр SQL Server "ContosoResourceGroup" в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44828-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="44828-119">Пример 4: использование трубопроводов</span><span class="sxs-lookup"><span data-stu-id="44828-119">Example 4: Using piping</span></span>
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

<span data-ttu-id="44828-120">Эта команда добавляет ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ContosoManagedInstanceName" в управляемый экземпляр SQL Server "ContosoResourceGroup" в группе ресурсов.</span><span class="sxs-lookup"><span data-stu-id="44828-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="44828-121">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="44828-121">PARAMETERS</span></span>

### <span data-ttu-id="44828-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44828-122">-DefaultProfile</span></span>
<span data-ttu-id="44828-123">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="44828-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44828-124">-Instance</span><span class="sxs-lookup"><span data-stu-id="44828-124">-Instance</span></span>
<span data-ttu-id="44828-125">Входной объект экземпляра</span><span class="sxs-lookup"><span data-stu-id="44828-125">The instance input object</span></span>

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

### <span data-ttu-id="44828-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="44828-126">-InstanceName</span></span>
<span data-ttu-id="44828-127">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="44828-127">The instance name</span></span>

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

### <span data-ttu-id="44828-128">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="44828-128">-InstanceResourceId</span></span>
<span data-ttu-id="44828-129">Идентификатор ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="44828-129">The instance resource id</span></span>

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

### <span data-ttu-id="44828-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="44828-130">-KeyId</span></span>
<span data-ttu-id="44828-131">ИД ключа AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="44828-131">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="44828-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44828-132">-ResourceGroupName</span></span>
<span data-ttu-id="44828-133">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="44828-133">The Resource Group Name</span></span>

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

### <span data-ttu-id="44828-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44828-134">-Confirm</span></span>
<span data-ttu-id="44828-135">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="44828-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44828-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44828-136">-WhatIf</span></span>
<span data-ttu-id="44828-137">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="44828-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44828-138">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="44828-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44828-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44828-139">CommonParameters</span></span>
<span data-ttu-id="44828-140">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="44828-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44828-141">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="44828-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44828-142">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="44828-142">INPUTS</span></span>

### <span data-ttu-id="44828-143">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="44828-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="44828-144">System. String</span><span class="sxs-lookup"><span data-stu-id="44828-144">System.String</span></span>

## <span data-ttu-id="44828-145">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="44828-145">OUTPUTS</span></span>

### <span data-ttu-id="44828-146">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="44828-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="44828-147">Пуск</span><span class="sxs-lookup"><span data-stu-id="44828-147">NOTES</span></span>

## <span data-ttu-id="44828-148">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="44828-148">RELATED LINKS</span></span>
