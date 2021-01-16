---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b93167e0e0a089595cb45710072c670c1cdb7af0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/08/2020
ms.locfileid: "98393292"
---
# <span data-ttu-id="b0d69-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="b0d69-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="b0d69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0d69-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d69-103">Задает прозрачный защита шифрования данных (TDE) для SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="b0d69-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="b0d69-104">СИНТАКСИС</span><span class="sxs-lookup"><span data-stu-id="b0d69-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0d69-105">ОПИСАНИЕ</span><span class="sxs-lookup"><span data-stu-id="b0d69-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d69-106">Этот Set-AzSqlServerTransparentDataEncryptionProtector задает защиту TDE для SQL сервера.</span><span class="sxs-lookup"><span data-stu-id="b0d69-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="b0d69-107">При изменении типа защиты TDE он будет повернут.</span><span class="sxs-lookup"><span data-stu-id="b0d69-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="b0d69-108">ПРИМЕРЫ</span><span class="sxs-lookup"><span data-stu-id="b0d69-108">EXAMPLES</span></span>

### <span data-ttu-id="b0d69-109">Пример 1. Задайте для типа защиты прозрачного шифрования данных (TDE) тип ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="b0d69-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="b0d69-110">Эта команда обновляет тип защищенного TDE на сервере в service Managed.</span><span class="sxs-lookup"><span data-stu-id="b0d69-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="b0d69-111">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="b0d69-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="b0d69-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span><span class="sxs-lookup"><span data-stu-id="b0d69-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="b0d69-113">Пример 2. Выбор прозрачного типа защиты шифрования данных в хранилище ключей Azure</span><span class="sxs-lookup"><span data-stu-id="b0d69-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="b0d69-114">Эта команда обновляет сервер, чтобы использовать ключ ключа сервера с ID ' в качестве защиты https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 TDE.</span><span class="sxs-lookup"><span data-stu-id="b0d69-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="b0d69-115">ResourceGroupName ServerName Type ServerKeyVaultKeyName</span><span class="sxs-lookup"><span data-stu-id="b0d69-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="b0d69-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="b0d69-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="b0d69-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0d69-117">PARAMETERS</span></span>

### <span data-ttu-id="b0d69-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b0d69-118">-AsJob</span></span>
<span data-ttu-id="b0d69-119">Запуск cmdlet в фоновом режиме</span><span class="sxs-lookup"><span data-stu-id="b0d69-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b0d69-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d69-120">-DefaultProfile</span></span>
<span data-ttu-id="b0d69-121">Учетные данные, учетная запись, клиент и подписка, используемые для связи с Azure</span><span class="sxs-lookup"><span data-stu-id="b0d69-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0d69-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b0d69-122">-Force</span></span>
<span data-ttu-id="b0d69-123">Пропустить сообщение с подтверждением выполнения действия</span><span class="sxs-lookup"><span data-stu-id="b0d69-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="b0d69-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="b0d69-124">-KeyId</span></span>
<span data-ttu-id="b0d69-125">Ключ ключа Azure Vault KeyId.</span><span class="sxs-lookup"><span data-stu-id="b0d69-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d69-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d69-126">-ResourceGroupName</span></span>
<span data-ttu-id="b0d69-127">Имя группы ресурсов</span><span class="sxs-lookup"><span data-stu-id="b0d69-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d69-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b0d69-128">-ServerName</span></span>
<span data-ttu-id="b0d69-129">Имя Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="b0d69-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d69-130">-Type</span><span class="sxs-lookup"><span data-stu-id="b0d69-130">-Type</span></span>
<span data-ttu-id="b0d69-131">Защита TDE базы данных Azure Sql.</span><span class="sxs-lookup"><span data-stu-id="b0d69-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d69-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0d69-132">-Confirm</span></span>
<span data-ttu-id="b0d69-133">Запрос на подтверждение перед запуском cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0d69-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0d69-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0d69-134">-WhatIf</span></span>
<span data-ttu-id="b0d69-135">Показывает, что произойдет при запуске cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0d69-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0d69-136">Этот cmdlet не будет выполниться.</span><span class="sxs-lookup"><span data-stu-id="b0d69-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0d69-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d69-137">CommonParameters</span></span>
<span data-ttu-id="b0d69-138">Этот cmdlet поддерживает общие параметры: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d69-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d69-139">Дополнительные сведения см. [в about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0d69-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d69-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="b0d69-140">INPUTS</span></span>

### <span data-ttu-id="b0d69-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span><span class="sxs-lookup"><span data-stu-id="b0d69-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="b0d69-142">System.String</span><span class="sxs-lookup"><span data-stu-id="b0d69-142">System.String</span></span>

## <span data-ttu-id="b0d69-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b0d69-143">OUTPUTS</span></span>

### <span data-ttu-id="b0d69-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="b0d69-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="b0d69-145">ПРИМЕЧАНИЯ</span><span class="sxs-lookup"><span data-stu-id="b0d69-145">NOTES</span></span>

## <span data-ttu-id="b0d69-146">СВЯЗАННЫЕ ССЫЛКИ</span><span class="sxs-lookup"><span data-stu-id="b0d69-146">RELATED LINKS</span></span>

[<span data-ttu-id="b0d69-147">SQL базы данных</span><span class="sxs-lookup"><span data-stu-id="b0d69-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
