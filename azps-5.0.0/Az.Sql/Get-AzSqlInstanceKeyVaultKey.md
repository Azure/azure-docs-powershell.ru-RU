---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 61672d71c2b65ff3588f4a4d8827220695c2d8de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/27/2020
ms.locfileid: "94249365"
---
# <span data-ttu-id="7f0b2-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7f0b2-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="7f0b2-102">КРАТКИй обзор</span><span class="sxs-lookup"><span data-stu-id="7f0b2-102">SYNOPSIS</span></span>
<span data-ttu-id="7f0b2-103">Получает ключи хранилища ключей управляемого экземпляра SQL.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="7f0b2-104">Максимальное</span><span class="sxs-lookup"><span data-stu-id="7f0b2-104">SYNTAX</span></span>

### <span data-ttu-id="7f0b2-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7f0b2-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f0b2-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f0b2-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7f0b2-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7f0b2-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f0b2-108">NОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f0b2-108">DESCRIPTION</span></span>
<span data-ttu-id="7f0b2-109">Командлет Get-AzSqlInstanceKeyVaultKey получает сведения о ключах хранилища ключей в управляемом экземпляре SQL.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="7f0b2-110">Вы можете просмотреть все клавиши на управляемом экземпляре или просмотреть определенный ключ, предоставив KeyId.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="7f0b2-111">ИЛЛЮСТРИРУЮТ</span><span class="sxs-lookup"><span data-stu-id="7f0b2-111">EXAMPLES</span></span>

### <span data-ttu-id="7f0b2-112">Пример 1: получение всех ключей хранилища ключей</span><span class="sxs-lookup"><span data-stu-id="7f0b2-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="7f0b2-113">Эта команда получает все ключи хранилища ключей в управляемом экземпляре SQL.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="7f0b2-114">Пример 2: получение ключа хранилища с определенным ключом</span><span class="sxs-lookup"><span data-stu-id="7f0b2-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="7f0b2-115">Эта команда получает ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ".</span><span class="sxs-lookup"><span data-stu-id="7f0b2-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="7f0b2-116">Пример 3: использование объекта instance</span><span class="sxs-lookup"><span data-stu-id="7f0b2-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="7f0b2-117">Эта команда получает ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ".</span><span class="sxs-lookup"><span data-stu-id="7f0b2-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="7f0b2-118">Пример 4: использование идентификатора ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="7f0b2-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="7f0b2-119">Эта команда получает ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ".</span><span class="sxs-lookup"><span data-stu-id="7f0b2-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="7f0b2-120">Пример 5: использование трубопроводов</span><span class="sxs-lookup"><span data-stu-id="7f0b2-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="7f0b2-121">Эта команда получает ключ хранилища ключей с идентификатором " https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ".</span><span class="sxs-lookup"><span data-stu-id="7f0b2-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="7f0b2-122">ПАРАМЕТРЫ</span><span class="sxs-lookup"><span data-stu-id="7f0b2-122">PARAMETERS</span></span>

### <span data-ttu-id="7f0b2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f0b2-123">-DefaultProfile</span></span>
<span data-ttu-id="7f0b2-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7f0b2-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="7f0b2-125">-Instance</span></span>
<span data-ttu-id="7f0b2-126">Входной объект экземпляра</span><span class="sxs-lookup"><span data-stu-id="7f0b2-126">The instance input object</span></span>

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

### <span data-ttu-id="7f0b2-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7f0b2-127">-InstanceName</span></span>
<span data-ttu-id="7f0b2-128">Имя экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-128">The instance name</span></span>

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

### <span data-ttu-id="7f0b2-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="7f0b2-129">-InstanceResourceId</span></span>
<span data-ttu-id="7f0b2-130">Идентификатор ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="7f0b2-130">The instance resource id</span></span>

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

### <span data-ttu-id="7f0b2-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7f0b2-131">-KeyId</span></span>
<span data-ttu-id="7f0b2-132">ИД ключа AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="7f0b2-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f0b2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f0b2-133">-ResourceGroupName</span></span>
<span data-ttu-id="7f0b2-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7f0b2-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="7f0b2-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f0b2-135">-Confirm</span></span>
<span data-ttu-id="7f0b2-136">Запрашивает подтверждение перед запуском командлета.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f0b2-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f0b2-137">-WhatIf</span></span>
<span data-ttu-id="7f0b2-138">Показывает, что произойдет при запуске командлета.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f0b2-139">Командлет не выполняется.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f0b2-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f0b2-140">CommonParameters</span></span>
<span data-ttu-id="7f0b2-141">Этот командлет поддерживает общие параметры:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-of Variable,-out,-PipelineVariable,-Verbose, и-WarningAction.</span><span class="sxs-lookup"><span data-stu-id="7f0b2-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f0b2-142">Дополнительные сведения можно найти в разделе [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7f0b2-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f0b2-143">ВХОДНЫЕ данные</span><span class="sxs-lookup"><span data-stu-id="7f0b2-143">INPUTS</span></span>

### <span data-ttu-id="7f0b2-144">Microsoft. Azure. Commands. SQL. ManagedInstance. Model. AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7f0b2-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="7f0b2-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7f0b2-145">System.String</span></span>

## <span data-ttu-id="7f0b2-146">НАПРЯЖЕНИЕ</span><span class="sxs-lookup"><span data-stu-id="7f0b2-146">OUTPUTS</span></span>

### <span data-ttu-id="7f0b2-147">Microsoft. Azure. Commands. SQL. TransparentDataEncryption. Model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="7f0b2-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="7f0b2-148">Пуск</span><span class="sxs-lookup"><span data-stu-id="7f0b2-148">NOTES</span></span>

## <span data-ttu-id="7f0b2-149">ДОПОЛНИТЕЛЬНЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7f0b2-149">RELATED LINKS</span></span>