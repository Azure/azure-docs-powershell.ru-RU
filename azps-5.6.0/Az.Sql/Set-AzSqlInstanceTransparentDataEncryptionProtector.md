---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 4f3b0bccd8f352d6870899473440b690381bec10
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988795"
---
# <span data-ttu-id="c2d4b-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c2d4b-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="c2d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2d4b-102">SYNOPSIS</span></span>
<span data-ttu-id="c2d4b-103">Задает прозрачный защита шифрования данных (TDE) для SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="c2d4b-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="c2d4b-104">SYNTAX</span></span>

### <span data-ttu-id="c2d4b-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="c2d4b-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2d4b-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2d4b-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2d4b-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2d4b-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c2d4b-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="c2d4b-108">DESCRIPTION</span></span>
<span data-ttu-id="c2d4b-109">Этот Set-AzSqlInstanceTransparentDataEncryptionProtector задает защиту TDE для SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="c2d4b-110">При изменении типа защиты TDE он будет повернут.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="c2d4b-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="c2d4b-111">EXAMPLES</span></span>

### <span data-ttu-id="c2d4b-112">Пример 1. Задайте для типа защиты прозрачного шифрования данных (TDE) тип ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="c2d4b-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="c2d4b-113">Эта команда обновляет тип защиты TDE управляемого экземпляра на Service Managed.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="c2d4b-114">Пример 2. Выбор прозрачного типа защиты шифрования данных в хранилище ключей Azure</span><span class="sxs-lookup"><span data-stu-id="c2d4b-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2d4b-115">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ ключа управляемого экземпляра с ID ' в качестве защиты https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="c2d4b-116">Пример 3. Выбор типа прозрачного защищенного ключа шифрования данных в хранилище ключа Azure с помощью объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="c2d4b-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2d4b-117">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ ключа управляемого экземпляра с ID ' в качестве защиты https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="c2d4b-118">Пример 4. Выбор типа прозрачного защищенного ключа шифрования данных в хранилище ключа Azure с помощью ид ресурса</span><span class="sxs-lookup"><span data-stu-id="c2d4b-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2d4b-119">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ ключа управляемого экземпляра с ID ' в качестве защиты https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="c2d4b-120">Пример 5. Выбор прозрачного типа защиты шифрования данных в хранилище ключей Azure с помощью piping</span><span class="sxs-lookup"><span data-stu-id="c2d4b-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2d4b-121">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ ключа управляемого экземпляра с ID ' в качестве защиты https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="c2d4b-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2d4b-122">PARAMETERS</span></span>

### <span data-ttu-id="c2d4b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2d4b-123">-DefaultProfile</span></span>
<span data-ttu-id="c2d4b-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2d4b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c2d4b-125">-Force</span></span>
<span data-ttu-id="c2d4b-126">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="c2d4b-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="c2d4b-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="c2d4b-127">-Instance</span></span>
<span data-ttu-id="c2d4b-128">Объект ввода экземпляра</span><span class="sxs-lookup"><span data-stu-id="c2d4b-128">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d4b-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2d4b-129">-InstanceName</span></span>
<span data-ttu-id="c2d4b-130">Имя экземпляра</span><span class="sxs-lookup"><span data-stu-id="c2d4b-130">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2d4b-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="c2d4b-131">-InstanceResourceId</span></span>
<span data-ttu-id="c2d4b-132">ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="c2d4b-132">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2d4b-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c2d4b-133">-KeyId</span></span>
<span data-ttu-id="c2d4b-134">Ключ ключа Azure Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2d4b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2d4b-135">-ResourceGroupName</span></span>
<span data-ttu-id="c2d4b-136">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="c2d4b-136">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2d4b-137">-Type</span><span class="sxs-lookup"><span data-stu-id="c2d4b-137">-Type</span></span>
<span data-ttu-id="c2d4b-138">Прозрачный защита от шифрования данных в базе данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2d4b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2d4b-139">-Confirm</span></span>
<span data-ttu-id="c2d4b-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2d4b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2d4b-141">-WhatIf</span></span>
<span data-ttu-id="c2d4b-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2d4b-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2d4b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2d4b-144">CommonParameters</span></span>
<span data-ttu-id="c2d4b-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2d4b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2d4b-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2d4b-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2d4b-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="c2d4b-147">INPUTS</span></span>

### <span data-ttu-id="c2d4b-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="c2d4b-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="c2d4b-149">System.String</span><span class="sxs-lookup"><span data-stu-id="c2d4b-149">System.String</span></span>

## <span data-ttu-id="c2d4b-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c2d4b-150">OUTPUTS</span></span>

### <span data-ttu-id="c2d4b-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="c2d4b-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="c2d4b-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="c2d4b-152">NOTES</span></span>

## <span data-ttu-id="c2d4b-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="c2d4b-153">RELATED LINKS</span></span>
