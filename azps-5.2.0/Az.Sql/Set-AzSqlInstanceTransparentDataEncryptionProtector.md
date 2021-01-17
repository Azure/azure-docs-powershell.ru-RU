---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98403519"
---
# <span data-ttu-id="9d582-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="9d582-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="9d582-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d582-102">SYNOPSIS</span></span>
<span data-ttu-id="9d582-103">Задает прозрачный защита шифрования данных (TDE) для SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9d582-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="9d582-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="9d582-104">SYNTAX</span></span>

### <span data-ttu-id="9d582-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="9d582-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d582-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d582-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d582-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9d582-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9d582-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="9d582-108">DESCRIPTION</span></span>
<span data-ttu-id="9d582-109">Этот Set-AzSqlInstanceTransparentDataEncryptionProtector задает защиту TDE для SQL управляемого экземпляра.</span><span class="sxs-lookup"><span data-stu-id="9d582-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="9d582-110">При изменении типа защиты TDE он будет повернут.</span><span class="sxs-lookup"><span data-stu-id="9d582-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="9d582-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="9d582-111">EXAMPLES</span></span>

### <span data-ttu-id="9d582-112">Пример 1. Задайте для типа защиты прозрачного шифрования данных (TDE) тип ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="9d582-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="9d582-113">Эта команда обновляет тип защиты TDE управляемого экземпляра на Service Managed.</span><span class="sxs-lookup"><span data-stu-id="9d582-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="9d582-114">Пример 2. Выбор прозрачного типа защиты шифрования данных в хранилище ключей Azure</span><span class="sxs-lookup"><span data-stu-id="9d582-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="9d582-115">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ ключа управляемого экземпляра с ID ' в качестве защиты https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE.</span><span class="sxs-lookup"><span data-stu-id="9d582-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="9d582-116">Пример 3. Выбор типа прозрачного защищенного ключа шифрования данных в хранилище ключа Azure с помощью объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="9d582-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="9d582-117">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ ключа управляемого экземпляра с ID ' в качестве защиты https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE.</span><span class="sxs-lookup"><span data-stu-id="9d582-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="9d582-118">Пример 4. Выбор прозрачного типа защиты шифрования данных в хранилище ключа Azure с помощью ид ресурса</span><span class="sxs-lookup"><span data-stu-id="9d582-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="9d582-119">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ ключа управляемого экземпляра с ID ' в качестве защиты https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE.</span><span class="sxs-lookup"><span data-stu-id="9d582-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="9d582-120">Пример 5. Выбор прозрачного типа защиты шифрования данных в хранилище ключей Azure с помощью piping</span><span class="sxs-lookup"><span data-stu-id="9d582-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="9d582-121">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ ключа управляемого экземпляра с ID ' в качестве защиты https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE.</span><span class="sxs-lookup"><span data-stu-id="9d582-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="9d582-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d582-122">PARAMETERS</span></span>

### <span data-ttu-id="9d582-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d582-123">-DefaultProfile</span></span>
<span data-ttu-id="9d582-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="9d582-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d582-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9d582-125">-Force</span></span>
<span data-ttu-id="9d582-126">Пропустить сообщение подтверждения для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="9d582-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="9d582-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="9d582-127">-Instance</span></span>
<span data-ttu-id="9d582-128">Объект ввода экземпляра</span><span class="sxs-lookup"><span data-stu-id="9d582-128">The instance input object</span></span>

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

### <span data-ttu-id="9d582-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="9d582-129">-InstanceName</span></span>
<span data-ttu-id="9d582-130">Имя экземпляра</span><span class="sxs-lookup"><span data-stu-id="9d582-130">The instance name</span></span>

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

### <span data-ttu-id="9d582-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="9d582-131">-InstanceResourceId</span></span>
<span data-ttu-id="9d582-132">ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="9d582-132">The instance resource id</span></span>

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

### <span data-ttu-id="9d582-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="9d582-133">-KeyId</span></span>
<span data-ttu-id="9d582-134">Ключ ключа Azure Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="9d582-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="9d582-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d582-135">-ResourceGroupName</span></span>
<span data-ttu-id="9d582-136">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="9d582-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="9d582-137">-Type</span><span class="sxs-lookup"><span data-stu-id="9d582-137">-Type</span></span>
<span data-ttu-id="9d582-138">Прозрачный защита от шифрования данных в базе данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="9d582-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="9d582-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d582-139">-Confirm</span></span>
<span data-ttu-id="9d582-140">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d582-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d582-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d582-141">-WhatIf</span></span>
<span data-ttu-id="9d582-142">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d582-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d582-143">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="9d582-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d582-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d582-144">CommonParameters</span></span>
<span data-ttu-id="9d582-145">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d582-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d582-146">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d582-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d582-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9d582-147">INPUTS</span></span>

### <span data-ttu-id="9d582-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="9d582-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="9d582-149">System.String</span><span class="sxs-lookup"><span data-stu-id="9d582-149">System.String</span></span>

## <span data-ttu-id="9d582-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="9d582-150">OUTPUTS</span></span>

### <span data-ttu-id="9d582-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="9d582-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="9d582-152">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="9d582-152">NOTES</span></span>

## <span data-ttu-id="9d582-153">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="9d582-153">RELATED LINKS</span></span>
