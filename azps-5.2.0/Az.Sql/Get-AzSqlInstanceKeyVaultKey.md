---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 61672d71c2b65ff3588f4a4d8827220695c2d8de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98323445"
---
# <span data-ttu-id="7bbfb-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="7bbfb-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="7bbfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7bbfb-102">SYNOPSIS</span></span>
<span data-ttu-id="7bbfb-103">Возвращает SQL ключа экземпляра.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="7bbfb-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="7bbfb-104">SYNTAX</span></span>

### <span data-ttu-id="7bbfb-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="7bbfb-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bbfb-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bbfb-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7bbfb-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7bbfb-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7bbfb-108">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="7bbfb-108">DESCRIPTION</span></span>
<span data-ttu-id="7bbfb-109">Этот Get-AzSqlInstanceKeyVaultKey получает сведения о ключах сейфа в SQL управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="7bbfb-110">Вы можете просмотреть все ключи в управляемом экземпляре или только определенный ключ, задав keyId.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="7bbfb-111">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="7bbfb-111">EXAMPLES</span></span>

### <span data-ttu-id="7bbfb-112">Пример 1. Получить все клавиши key Vault</span><span class="sxs-lookup"><span data-stu-id="7bbfb-112">Example 1: Get all Key Vault keys</span></span>
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

<span data-ttu-id="7bbfb-113">Эта команда получает все клавиши key Vault в SQL управляемом экземпляре.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="7bbfb-114">Пример 2. Получить определенный ключ сейфа</span><span class="sxs-lookup"><span data-stu-id="7bbfb-114">Example 2: Get a specific Key Vault key</span></span>
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

<span data-ttu-id="7bbfb-115">Эта команда получает ключ ключа сейфа с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="7bbfb-116">Пример 3. Использование объекта экземпляра</span><span class="sxs-lookup"><span data-stu-id="7bbfb-116">Example 3: Using instance object</span></span>
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

<span data-ttu-id="7bbfb-117">Эта команда получает ключ ключа сейфа с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="7bbfb-118">Пример 4. Использование ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="7bbfb-118">Example 4: Using instance resource id</span></span>
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

<span data-ttu-id="7bbfb-119">Эта команда получает ключ ключа сейфа с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="7bbfb-120">Пример 5. Использование piping</span><span class="sxs-lookup"><span data-stu-id="7bbfb-120">Example 5: Using piping</span></span>
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

<span data-ttu-id="7bbfb-121">Эта команда получает ключ ключа сейфа с ИД https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 '.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="7bbfb-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7bbfb-122">PARAMETERS</span></span>

### <span data-ttu-id="7bbfb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7bbfb-123">-DefaultProfile</span></span>
<span data-ttu-id="7bbfb-124">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7bbfb-125">-Instance</span><span class="sxs-lookup"><span data-stu-id="7bbfb-125">-Instance</span></span>
<span data-ttu-id="7bbfb-126">Объект ввода экземпляра</span><span class="sxs-lookup"><span data-stu-id="7bbfb-126">The instance input object</span></span>

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

### <span data-ttu-id="7bbfb-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="7bbfb-127">-InstanceName</span></span>
<span data-ttu-id="7bbfb-128">Имя экземпляра</span><span class="sxs-lookup"><span data-stu-id="7bbfb-128">The instance name</span></span>

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

### <span data-ttu-id="7bbfb-129">-InstanceResourceId</span><span class="sxs-lookup"><span data-stu-id="7bbfb-129">-InstanceResourceId</span></span>
<span data-ttu-id="7bbfb-130">ИД ресурса экземпляра</span><span class="sxs-lookup"><span data-stu-id="7bbfb-130">The instance resource id</span></span>

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

### <span data-ttu-id="7bbfb-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="7bbfb-131">-KeyId</span></span>
<span data-ttu-id="7bbfb-132">Ключ AzureKeyVault</span><span class="sxs-lookup"><span data-stu-id="7bbfb-132">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="7bbfb-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7bbfb-133">-ResourceGroupName</span></span>
<span data-ttu-id="7bbfb-134">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="7bbfb-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="7bbfb-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7bbfb-135">-Confirm</span></span>
<span data-ttu-id="7bbfb-136">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7bbfb-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7bbfb-137">-WhatIf</span></span>
<span data-ttu-id="7bbfb-138">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7bbfb-139">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7bbfb-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7bbfb-140">CommonParameters</span></span>
<span data-ttu-id="7bbfb-141">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7bbfb-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7bbfb-142">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7bbfb-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7bbfb-143">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7bbfb-143">INPUTS</span></span>

### <span data-ttu-id="7bbfb-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span><span class="sxs-lookup"><span data-stu-id="7bbfb-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="7bbfb-145">System.String</span><span class="sxs-lookup"><span data-stu-id="7bbfb-145">System.String</span></span>

## <span data-ttu-id="7bbfb-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7bbfb-146">OUTPUTS</span></span>

### <span data-ttu-id="7bbfb-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="7bbfb-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="7bbfb-148">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="7bbfb-148">NOTES</span></span>

## <span data-ttu-id="7bbfb-149">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="7bbfb-149">RELATED LINKS</span></span>
