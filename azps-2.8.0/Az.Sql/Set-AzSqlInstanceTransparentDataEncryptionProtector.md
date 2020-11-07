---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 0321fc68c22e3bea973c25f9bbb27e0c5736e944
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/29/2020
ms.locfileid: "93906302"
---
# <span data-ttu-id="34147-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="34147-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="34147-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="34147-102">SYNOPSIS</span></span>
<span data-ttu-id="34147-103">Задает предохранитель прозрачного шифрования данных (TDE) для экземпляра, управляемого SQL.</span><span class="sxs-lookup"><span data-stu-id="34147-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="34147-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="34147-104">SYNTAX</span></span>

### <span data-ttu-id="34147-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="34147-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34147-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="34147-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34147-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="34147-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="34147-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="34147-108">DESCRIPTION</span></span>
<span data-ttu-id="34147-109">Командлет Set-AzSqlInstanceTransparentDataEncryptionProtector задает предохранитель TDE для управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="34147-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="34147-110">Изменение типа предохранителя TDE приводит к повернутию предохранителя.</span><span class="sxs-lookup"><span data-stu-id="34147-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="34147-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="34147-111">EXAMPLES</span></span>

### <span data-ttu-id="34147-112">Пример 1: Настройка типа предохранителя прозрачного шифрования данных (TDE) на ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="34147-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="34147-113">Эта команда обновляет Тип предохранителя TDE управляемого экземпляра для управления службами.</span><span class="sxs-lookup"><span data-stu-id="34147-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="34147-114">Пример 2: Установка прозрачного типа предохранителя для шифрования данных Azure Key Vault</span><span class="sxs-lookup"><span data-stu-id="34147-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="34147-115">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ хранилища ключей управляемых экземпляров с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " в качестве предохранителя TDE.</span><span class="sxs-lookup"><span data-stu-id="34147-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="34147-116">Пример 3: Установка прозрачного типа предохранителя шифрования данных Azure Key Vault с помощью объекта управляемого экземпляра</span><span class="sxs-lookup"><span data-stu-id="34147-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="34147-117">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ хранилища ключей управляемых экземпляров с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " в качестве предохранителя TDE.</span><span class="sxs-lookup"><span data-stu-id="34147-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="34147-118">Пример 4: Установка прозрачного типа предохранителя шифрования данных Azure Key Vault с помощью идентификатора ресурса</span><span class="sxs-lookup"><span data-stu-id="34147-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="34147-119">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ хранилища ключей управляемых экземпляров с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " в качестве предохранителя TDE.</span><span class="sxs-lookup"><span data-stu-id="34147-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="34147-120">Пример 5: Настройка прозрачного типа предохранителя шифрования данных для Azure Key Vault с помощью конвейера</span><span class="sxs-lookup"><span data-stu-id="34147-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="34147-121">Эта команда обновляет указанный управляемый экземпляр, чтобы использовать ключ хранилища ключей управляемых экземпляров с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 " в качестве предохранителя TDE.</span><span class="sxs-lookup"><span data-stu-id="34147-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="34147-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="34147-122">PARAMETERS</span></span>

### <span data-ttu-id="34147-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34147-123">-DefaultProfile</span></span>
<span data-ttu-id="34147-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="34147-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34147-125">-Force</span><span class="sxs-lookup"><span data-stu-id="34147-125">-Force</span></span>
<span data-ttu-id="34147-126">Пропустить предупреждающее сообщение для выполнения действия</span><span class="sxs-lookup"><span data-stu-id="34147-126">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="34147-127">-Instance</span><span class="sxs-lookup"><span data-stu-id="34147-127">-Instance</span></span>
<span data-ttu-id="34147-128">Входной объект экземпляра</span><span class="sxs-lookup"><span data-stu-id="34147-128">The instance input object</span></span>

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

### <span data-ttu-id="34147-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="34147-129">-InstanceName</span></span>
<span data-ttu-id="34147-130">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="34147-130">The instance name</span></span>

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

### <span data-ttu-id="34147-131">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="34147-131">-InstanceResourceId</span></span>
<span data-ttu-id="34147-132">Идентификатор ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="34147-132">The instance resource id</span></span>

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

### <span data-ttu-id="34147-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="34147-133">-KeyId</span></span>
<span data-ttu-id="34147-134">Azure Key Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="34147-134">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="34147-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="34147-135">-ResourceGroupName</span></span>
<span data-ttu-id="34147-136">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="34147-136">The Resource Group Name</span></span>

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

### <span data-ttu-id="34147-137">-Type (тип)</span><span class="sxs-lookup"><span data-stu-id="34147-137">-Type</span></span>
<span data-ttu-id="34147-138">Тип предохранителя прозрачного шифрования для базы данных SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="34147-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

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

### <span data-ttu-id="34147-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34147-139">-Confirm</span></span>
<span data-ttu-id="34147-140">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="34147-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34147-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34147-141">-WhatIf</span></span>
<span data-ttu-id="34147-142">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="34147-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34147-143">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="34147-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34147-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34147-144">CommonParameters</span></span>
<span data-ttu-id="34147-145">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="34147-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34147-146">Дополнительные сведения можно найти в разделе [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="34147-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34147-147">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="34147-147">INPUTS</span></span>

### <span data-ttu-id="34147-148">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="34147-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="34147-149">System. String</span><span class="sxs-lookup"><span data-stu-id="34147-149">System.String</span></span>

## <span data-ttu-id="34147-150">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="34147-150">OUTPUTS</span></span>

### <span data-ttu-id="34147-151">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="34147-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="34147-152">Пуск</span><span class="sxs-lookup"><span data-stu-id="34147-152">NOTES</span></span>

## <span data-ttu-id="34147-153">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="34147-153">RELATED LINKS</span></span>
